# Intro to using AltaFin Divergence to arbitrage on decentralized exchanges

![](https://images.ctfassets.net/dj2ij87ekk1y/27Su0yjuJ7VXavjTbA2z0f/daa0a0fced000edbf730f87fab23a2db/altafin\_defi\_divergence\_exchanges\_03.png?h=250)

Learn how to execute an arbitrage opportunity between two decentralized exchanges using the AltaFin Divergence smart contract.

### What is arbitrage?

Arbitrage is the act of buying a token in one decentralized exchange and instantly selling it in another decentralized exchange at a higher price, thus earning a profit.

Arbitrage takes advantage of the inevitable inefficiencies in markets. The effect of arbitrage is to converge the prices of similar tokens across different exchanges.

### Why did AltaFin create this smart contract?

We created this smart contract as we were experimenting in our lab with finding arbitrage opportunities. We found that it was easy to find the opportunities, but difficult to execute the trades.

So we built this smart contract for any trader to use at a very low fee.

### How does the AltaFin Divergence smart contract work?

Simplified a little bit, you call a function called `initFlash` and include the following parameters:

* Token0: Token you wish to borrow and then trade for Token1 on Exchange0
* Token1: Token you wish to trade for
* Amount: Amount of Token0 you wish to borrow and trade
* Exchange0: Exchange where you wish to trade Token0 for Token1
* Exchange1: Exchange where you with to trade Token1 back for Token0

Here is an simplified example of how the `initFlash` would be called:

```
// Example Trade

function initFlash[
    token0: 'LINK',
    token1: 'AAVE',
    amount: 100,
    exchange0: 'uniswapV2',
    exchange1: 'sushiswap'
]
```

Let's say you called this function using `LINK` and `AAVE` as your trade-able pair, here is how it would work:

1. Borrow `100 LINK` from Uniswap Flash Swaps
2. Swap `100 LINK` for `10.83 AAVE` on Uniswap V2 Exchange
3. Swap `10.83 AAVE` for  `118.2 LINK` on SushiSwap
4. Pay 0.3% fee of `0.3` for borrowing `100 LINK` from Uniswap Flash Swap in Step 1
5. Calculate Gross Profit in `LINK` of `118.2 - 0.3 = 117.9 LINK`
6. Calculate 3% smart contract fee of `3.537 LINK` from gross profit of `117.9 LINK` in Step 5
7. Calculate Net Profit in `LINK` of `117.9 - 3.537 = 114.363 LINK`&#x20;
8. Return `114.363 LINK`

In the example above, this transaction earned a profit of `14.363 LINK` without having to own any of the original `100 LINK`. This is how the smart contract does not require any capital.

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

View the Divergence DeFi Protocol API documents [here](../defi-protocols/divergence.md).

