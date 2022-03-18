# Earn V1

## Introduction

Welcome to Alta Finance Earn V1.

Earn is an Alta Finance feature that lets you loan your crypto via ALTA and earn up to 19.75% APR in USDC.

Earn makes it easy to have exposure to the underlying real world asset revenue streams wrapped in a smart contract.

You can learn more about AltaFin Earn in:

* [Understanding AltaFin Earn](../getting-started/understanding-altafin-earn.md)
* [How to open an Earn contract](../tutorials/how-to-open-an-earn-contract.md)
* [How to put an Earn contract up for bidding](../tutorials/how-to-put-an-earn-contract-up-for-bidding.md)

**Contract Address:** `0x88549Ed1c99ADC0B33B4517B7F70485Ea107a30f`

**Deployed Networks:** Ethereum, Polygon

**Test Networks:** Ropsten, Goerli,  Rinkeby, Kovan, Mumbai,

**Note:** The contract address is the same on all deployed networks.

### Contract ABI

```
[
    {
      "inputs": [
        {
          "internalType": "contract IERC20",
          "name": "_USDC",
          "type": "address"
        },
        {
          "internalType": "contract IERC20",
          "name": "_AFN",
          "type": "address"
        },
        {
          "internalType": "address",
          "name": "_loanAddress",
          "type": "address"
        },
        {
          "internalType": "address",
          "name": "_feeAddress",
          "type": "address"
        }
      ],
      "stateMutability": "nonpayable",
      "type": "constructor"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "address",
          "name": "owner",
          "type": "address"
        },
        {
          "indexed": false,
          "internalType": "uint256",
          "name": "earnContractId",
          "type": "uint256"
        }
      ],
      "name": "ContractClosed",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "address",
          "name": "owner",
          "type": "address"
        },
        {
          "indexed": false,
          "internalType": "uint256",
          "name": "earnContractId",
          "type": "uint256"
        }
      ],
      "name": "ContractOpened",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "address",
          "name": "previousOwner",
          "type": "address"
        },
        {
          "indexed": true,
          "internalType": "address",
          "name": "newOwner",
          "type": "address"
        },
        {
          "indexed": false,
          "internalType": "uint256",
          "name": "earnContractId",
          "type": "uint256"
        }
      ],
      "name": "EarnContractOwnershipTransferred",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "address",
          "name": "previousOwner",
          "type": "address"
        },
        {
          "indexed": true,
          "internalType": "address",
          "name": "newOwner",
          "type": "address"
        }
      ],
      "name": "OwnershipTransferred",
      "type": "event"
    },
    {
      "inputs": [],
      "name": "AFN",
      "outputs": [
        {
          "internalType": "contract IERC20",
          "name": "",
          "type": "address"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "USDC",
      "outputs": [
        {
          "internalType": "contract IERC20",
          "name": "",
          "type": "address"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_bidId",
          "type": "uint256"
        }
      ],
      "name": "acceptBid",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_time",
          "type": "uint256"
        },
        {
          "internalType": "uint16",
          "name": "_usdcRate",
          "type": "uint16"
        },
        {
          "internalType": "uint64",
          "name": "_afnHighAmount",
          "type": "uint64"
        },
        {
          "internalType": "uint64",
          "name": "_afnMedAmount",
          "type": "uint64"
        },
        {
          "internalType": "uint64",
          "name": "_afnLowAmount",
          "type": "uint64"
        },
        {
          "internalType": "bool",
          "name": "_otherTokens",
          "type": "bool"
        },
        {
          "internalType": "bool",
          "name": "_whitelist",
          "type": "bool"
        },
        {
          "internalType": "address[]",
          "name": "_tokensAccepted",
          "type": "address[]"
        }
      ],
      "name": "addTerm",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "afnBonusMultiplier",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "baseBonusMultiplier",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "name": "bids",
      "outputs": [
        {
          "internalType": "address",
          "name": "bidder",
          "type": "address"
        },
        {
          "internalType": "address",
          "name": "to",
          "type": "address"
        },
        {
          "internalType": "uint256",
          "name": "earnContractId",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "amount",
          "type": "uint256"
        },
        {
          "internalType": "bool",
          "name": "accepted",
          "type": "bool"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "_token",
          "type": "address"
        },
        {
          "internalType": "uint256",
          "name": "_earnTermsId",
          "type": "uint256"
        }
      ],
      "name": "checkTokenWhitelist",
      "outputs": [
        {
          "internalType": "bool",
          "name": "",
          "type": "bool"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_earnContractId",
          "type": "uint256"
        }
      ],
      "name": "closeContract",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "name": "earnContractBidCount",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "name": "earnContractToOwner",
      "outputs": [
        {
          "internalType": "address",
          "name": "",
          "type": "address"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "name": "earnContracts",
      "outputs": [
        {
          "internalType": "address",
          "name": "owner",
          "type": "address"
        },
        {
          "internalType": "uint256",
          "name": "startTime",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "contractLength",
          "type": "uint256"
        },
        {
          "internalType": "address",
          "name": "tokenAddress",
          "type": "address"
        },
        {
          "internalType": "uint256",
          "name": "tokenAmount",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "usdcPrincipal",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "usdcRate",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "afnAmount",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "usdcBonusRate",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "afnBonusAmount",
          "type": "uint256"
        },
        {
          "internalType": "enum Earn.ContractStatus",
          "name": "status",
          "type": "uint8"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "name": "earnTerms",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "time",
          "type": "uint256"
        },
        {
          "internalType": "uint16",
          "name": "usdcRate",
          "type": "uint16"
        },
        {
          "internalType": "uint64",
          "name": "afnHighAmount",
          "type": "uint64"
        },
        {
          "internalType": "uint64",
          "name": "afnMedAmount",
          "type": "uint64"
        },
        {
          "internalType": "uint64",
          "name": "afnLowAmount",
          "type": "uint64"
        },
        {
          "internalType": "bool",
          "name": "otherTokens",
          "type": "bool"
        },
        {
          "internalType": "bool",
          "name": "whitelist",
          "type": "bool"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "getAllBids",
      "outputs": [
        {
          "components": [
            {
              "internalType": "address",
              "name": "bidder",
              "type": "address"
            },
            {
              "internalType": "address",
              "name": "to",
              "type": "address"
            },
            {
              "internalType": "uint256",
              "name": "earnContractId",
              "type": "uint256"
            },
            {
              "internalType": "uint256",
              "name": "amount",
              "type": "uint256"
            },
            {
              "internalType": "bool",
              "name": "accepted",
              "type": "bool"
            }
          ],
          "internalType": "struct Earn.Bid[]",
          "name": "",
          "type": "tuple[]"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "getAllEarnContracts",
      "outputs": [
        {
          "components": [
            {
              "internalType": "address",
              "name": "owner",
              "type": "address"
            },
            {
              "internalType": "uint256",
              "name": "startTime",
              "type": "uint256"
            },
            {
              "internalType": "uint256",
              "name": "contractLength",
              "type": "uint256"
            },
            {
              "internalType": "address",
              "name": "tokenAddress",
              "type": "address"
            },
            {
              "internalType": "uint256",
              "name": "tokenAmount",
              "type": "uint256"
            },
            {
              "internalType": "uint256",
              "name": "usdcPrincipal",
              "type": "uint256"
            },
            {
              "internalType": "uint256",
              "name": "usdcRate",
              "type": "uint256"
            },
            {
              "internalType": "uint256",
              "name": "afnAmount",
              "type": "uint256"
            },
            {
              "internalType": "uint256",
              "name": "usdcBonusRate",
              "type": "uint256"
            },
            {
              "internalType": "uint256",
              "name": "afnBonusAmount",
              "type": "uint256"
            },
            {
              "internalType": "enum Earn.ContractStatus",
              "name": "status",
              "type": "uint8"
            }
          ],
          "internalType": "struct Earn.EarnContract[]",
          "name": "",
          "type": "tuple[]"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "getAllEarnTerms",
      "outputs": [
        {
          "components": [
            {
              "internalType": "uint256",
              "name": "time",
              "type": "uint256"
            },
            {
              "internalType": "uint16",
              "name": "usdcRate",
              "type": "uint16"
            },
            {
              "internalType": "uint64",
              "name": "afnHighAmount",
              "type": "uint64"
            },
            {
              "internalType": "uint64",
              "name": "afnMedAmount",
              "type": "uint64"
            },
            {
              "internalType": "uint64",
              "name": "afnLowAmount",
              "type": "uint64"
            },
            {
              "internalType": "bool",
              "name": "otherTokens",
              "type": "bool"
            },
            {
              "internalType": "bool",
              "name": "whitelist",
              "type": "bool"
            },
            {
              "internalType": "address[]",
              "name": "tokensAccepted",
              "type": "address[]"
            }
          ],
          "internalType": "struct Earn.EarnTerm[]",
          "name": "",
          "type": "tuple[]"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_earnContractId",
          "type": "uint256"
        }
      ],
      "name": "getBidsByContract",
      "outputs": [
        {
          "internalType": "uint256[]",
          "name": "",
          "type": "uint256[]"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "_owner",
          "type": "address"
        }
      ],
      "name": "getContractsByOwner",
      "outputs": [
        {
          "internalType": "uint256[]",
          "name": "",
          "type": "uint256[]"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "_owner",
          "type": "address"
        }
      ],
      "name": "getCurrentUsdcValueByOwner",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "_owner",
          "type": "address"
        }
      ],
      "name": "getRedemptionUsdcValueByOwner",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "highTier",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "isOwner",
      "outputs": [
        {
          "internalType": "bool",
          "name": "",
          "type": "bool"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "lowTier",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_earnContractId",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "_amount",
          "type": "uint256"
        }
      ],
      "name": "makeBid",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "medTier",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_earnTermsId",
          "type": "uint256"
        },
        {
          "internalType": "address",
          "name": "_tokenAddress",
          "type": "address"
        },
        {
          "internalType": "uint256",
          "name": "_amount",
          "type": "uint256"
        },
        {
          "internalType": "address",
          "name": "_swapTarget",
          "type": "address"
        },
        {
          "internalType": "bytes",
          "name": "_swapCallData",
          "type": "bytes"
        }
      ],
      "name": "openContractTokenSwapToUSDC",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_earnTermsId",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "_amount",
          "type": "uint256"
        }
      ],
      "name": "openContractUsdc",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "owner",
      "outputs": [
        {
          "internalType": "address",
          "name": "",
          "type": "address"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "",
          "type": "address"
        }
      ],
      "name": "ownerEarnContractCount",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_earnContractId",
          "type": "uint256"
        }
      ],
      "name": "putSale",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_bidId",
          "type": "uint256"
        }
      ],
      "name": "removeBid",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_earnContractId",
          "type": "uint256"
        }
      ],
      "name": "removeContractFromMarket",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_earnTermsId",
          "type": "uint256"
        }
      ],
      "name": "removeTerm",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "renounceOwnership",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_afnBonusMultiplier",
          "type": "uint256"
        }
      ],
      "name": "setAfnBonusMultiplier",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_highTier",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "_medTier",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "_lowTier",
          "type": "uint256"
        }
      ],
      "name": "setAfnContractTiers",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_baseBonusMultiplier",
          "type": "uint256"
        }
      ],
      "name": "setBaseBonusMultiplier",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "_feeAddress",
          "type": "address"
        }
      ],
      "name": "setFeeAddress",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "_loanAddress",
          "type": "address"
        }
      ],
      "name": "setLoanAddress",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_transferFee",
          "type": "uint256"
        }
      ],
      "name": "setTransferFee",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address payable",
          "name": "_to",
          "type": "address"
        },
        {
          "internalType": "uint256",
          "name": "_amount",
          "type": "uint256"
        }
      ],
      "name": "transfer",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "transferFee",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "newOwner",
          "type": "address"
        }
      ],
      "name": "transferOwnership",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_earnTermsId",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "_time",
          "type": "uint256"
        },
        {
          "internalType": "uint16",
          "name": "_usdcRate",
          "type": "uint16"
        },
        {
          "internalType": "uint64",
          "name": "_afnHighAmount",
          "type": "uint64"
        },
        {
          "internalType": "uint64",
          "name": "_afnMedAmount",
          "type": "uint64"
        },
        {
          "internalType": "uint64",
          "name": "_afnLowAmount",
          "type": "uint64"
        },
        {
          "internalType": "bool",
          "name": "_otherTokens",
          "type": "bool"
        },
        {
          "internalType": "bool",
          "name": "_whitelist",
          "type": "bool"
        },
        {
          "internalType": "address[]",
          "name": "_tokensAccepted",
          "type": "address[]"
        }
      ],
      "name": "updateTerm",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address payable",
          "name": "_addr",
          "type": "address"
        }
      ],
      "name": "withdraw",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address payable",
          "name": "_addr",
          "type": "address"
        }
      ],
      "name": "withdrawUSDC",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    }
  ]
```

### Contract Source Code

Follow this link to find the Contract Source Code&#x20;
