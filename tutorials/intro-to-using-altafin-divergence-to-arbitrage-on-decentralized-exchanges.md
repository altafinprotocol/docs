# Intro to using AltaFin Divergence to arbitrage on decentralized exchanges

Learn how to execute an arbitrage opportunity between two decentralized exchanges using the AltaFin Divergence smart contract.

![](../.gitbook/assets/altafin\_defi\_divergence\_1800x800.png)

![](https://images.ctfassets.net/dj2ij87ekk1y/27Su0yjuJ7VXavjTbA2z0f/daa0a0fced000edbf730f87fab23a2db/altafin\_defi\_divergence\_exchanges\_03.png?h=250)

### How does the AltaFin Divergence smart contract work?

Simplified a little bit, you call a function called `initFlash` and include the following parameters:

* Token0: Token you wish to borrow and then trade for Token1 on Exchange0
* Token1: Token you wish to trade for
* Amount: Amount of Token0 you wish to borrow and trade
* Exchange0: Exchange where you wish to trade Token0 for Token1
* Exchange1: Exchange where you wish to trade Token1 back for Token0

Here is a simplified example of how the `initFlash` would be called:

```
// Example Trade

function initFlash({
    token0: 'LINK',
    token1: 'AAVE',
    amount: 100,
    exchange0: 'uniswapV2',
    exchange1: 'sushiswap'
})
```

Let's say you called this function using `LINK` and `AAVE` as your trade-able pair, here is how it would work:

1. Borrow `100 LINK` from Uniswap Flash Swaps
2. Swap `100 LINK` for `10.83 AAVE` on Uniswap V2 Exchange
3. Swap `10.83 AAVE` for  `118.2 LINK` on SushiSwap
4. Pay pack original Uniswap Flash Swap `100 LINK` + 0.3% fee of `0.3` for borrowing `100 LINK` from Uniswap Flash Swap in Step 1
5. Calculate Gross Profit in `LINK` of `18.2 - 0.3 = 17.9 LINK`
6. Calculate 3% smart contract fee of `0.537 LINK` from gross profit of `17.9 LINK` in Step 5
7. Calculate Net Profit in `LINK` of `17.9 - 0.537 = 17.363 LINK`&#x20;
8. Return `17.363 LINK`

|                                    Uniswap V2 |                       Balance |                     SushiSwap |
| --------------------------------------------: | ----------------------------: | ----------------------------: |
|                               Borrow 100 LINK |                      100 LINK |                               |
|                   Swap 100 LINK <> 10.83 AAVE |                    10.83 AAVE |                               |
|                                               |                    118.2 LINK | Swap 10.83 AAVE <> 118.2 LINK |
| Payback Borrow 100 LINK + 0.3 LINK (0.3% fee) |                     17.9 LINK |                               |
|                                               |  Subtract 0.537 LINK (3% fee) |                               |
|                                               |                   17.363 LINK |                               |

In the example above, this transaction earned a profit of `17.363 LINK` without having to own any of the original `100 LINK`. This is how the smart contract does not require any capital.

These calculations do not include gas fees. You will want to make sure that your potential profit exceeds the gas fees of the smart contract.

### How do I use the AltaFin smart contract?

Until the AltaFin Web3 UI launches, you will need to connect to the smart contract via API.

### Which exchanges are supported?

The Divergence V1 smart contract supports the following exchanges:

* UniswapV2
* UniswapV3
* SushiSwap
* DodoEX
* Kyber Network
* Curve
* Bancor

### I'm ready to start trading, how do I learn more?

View the Divergence DeFi Protocol API documents [here](../defi-protocols/arbitrage-v1.md).

