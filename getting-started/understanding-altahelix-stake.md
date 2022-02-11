# Understanding AltaHelix Stake

AltaHelix is a smart contract deployed with solidity or in other words, the coolest club in town. Here, you can come in with some AFN, and leave with more! The longer you stay, the more AFN you get.

To learn specifically how to stake, go to [How to Stake AFN for xAFN](../tutorials/how-to-stake-afn-for-xafn.md).

The smart contract has mainly two functions, "enter" and "leave". "enter" lets you enter the amount of AFN that you want to stake, and "leave" lets you claim back your AFN with its increased value.

Those two functions are defined in the following way:

```
    // Enter the helix. Pay some AFN. Earn some shares
    // Locks AFN and mints xAFN
    function enter(uint256 _amount) public {
        // Gets the amount of AFN locked in the contract
        uint256 totalAFN = AFN.balanceOf(address(this));
        // Gets the amount of xAFN in existence
        uint256 totalShares = totalSupply();
        // If no xAFN exists, mint it 1:1 to the amount put in
        if (totalShares == 0 || totalAFN == 0) {
            _mint(msg.sender, _amount);
        } 
        // Calculate and mint the amount of xAFN the AFN is worth. The ratio will change overtime, as xAFN is burned/minted and AFN deposited + gained from fees / withdrawn.
        else {
            uint256 what = _amount * totalShares / totalAFN;
            _mint(msg.sender, what);
        }
        // Lock the AFN in the contract
        AFN.transferFrom(msg.sender, address(this), _amount);
    }

    // Leave the helix. Claim back your AFN
    // Unlocks the staked + gained AFN and burns xAFN
    function leave(uint256 _share) public {
        // Gets the amount of xAFN in existence
        uint256 totalShares = totalSupply();
        // Calculates the amount of AFN the xAFN is worth
        uint256 what = _share * AFN.balanceOf(address(this)) / totalShares;
        _burn(msg.sender, _share);
        AFN.transfer(msg.sender, what);
    }
```
