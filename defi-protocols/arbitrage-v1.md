# Arbitrage V1

## Introduction

Welcome to the AltaFin Arbitrage (called Divergence) docs.

Divergence is an arbitrage smart contract built on Uniswap Flash Swaps. It lets you borrow up to millions of dollars of capital, execute swaps on 2 decentralized exchanges, pay back your loan + fees, and collect your profit—all in a single transaction.

### Supported Exchanges

| Exchanges      | Router Address                               |
| -------------- | -------------------------------------------- |
| Uniswap V3     | `0xE592427A0AEce92De3Edee1F18E0157C05861564` |
| Uniswap V2     | `0xf164fC0Ec4E93095b804a4795bBe1e041497b92a` |
| SushiSwap      | `0xd9e1cE17f2641f24aE83637ab66a2cca9C378B9F` |
| Kyber Network  | `0x818E6FECD516Ecc3849DAf6845e3EC868087B755` |
| Dodo V2        | `0xa356867fDCEa8e71AEaF87805808803806231FdC` |
| Bancor Network | `0x52Ae12ABe5D8BD778BD5397F99cA900624CfADD4` |
| Curve Finance  | `0x0000000022D53366457F9d5E68Ec105046FC4383` |

### Contract Address

| Network | Address                                      |
| ------- | -------------------------------------------- |
| Mainnet | `0xa8e88d68e8b114b18ce01cfa4566778d020789bb` |

### Contract ABI

```
"abi": [
    {
      "inputs": [],
      "stateMutability": "nonpayable",
      "type": "constructor"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "internalType": "address",
          "name": "",
          "type": "address"
        },
        {
          "indexed": false,
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "name": "Received",
      "type": "event"
    },
    {
      "inputs": [],
      "name": "WETH9",
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
      "inputs": [],
      "name": "factory",
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
          "components": [
            {
              "internalType": "address",
              "name": "inputToken",
              "type": "address"
            },
            {
              "internalType": "address",
              "name": "outputToken",
              "type": "address"
            },
            {
              "internalType": "address",
              "name": "loanPairToken",
              "type": "address"
            },
            {
              "internalType": "uint24",
              "name": "flashLoanFee",
              "type": "uint24"
            },
            {
              "internalType": "uint24",
              "name": "uniPoolFee",
              "type": "uint24"
            },
            {
              "internalType": "uint256",
              "name": "amount0",
              "type": "uint256"
            },
            {
              "internalType": "address",
              "name": "exchange0",
              "type": "address"
            },
            {
              "internalType": "address",
              "name": "exchange1",
              "type": "address"
            },
            {
              "internalType": "uint256",
              "name": "slippage",
              "type": "uint256"
            }
          ],
          "internalType": "struct Divergence0_1.FlashParams",
          "name": "params",
          "type": "tuple"
        }
      ],
      "name": "initFlash",
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
      "inputs": [],
      "name": "refundETH",
      "outputs": [],
      "stateMutability": "payable",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "swapRouter",
      "outputs": [
        {
          "internalType": "contract ISwapRouter",
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
          "name": "token",
          "type": "address"
        },
        {
          "internalType": "uint256",
          "name": "amountMinimum",
          "type": "uint256"
        },
        {
          "internalType": "address",
          "name": "recipient",
          "type": "address"
        }
      ],
      "name": "sweepToken",
      "outputs": [],
      "stateMutability": "payable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "fee0",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "fee1",
          "type": "uint256"
        },
        {
          "internalType": "bytes",
          "name": "data",
          "type": "bytes"
        }
      ],
      "name": "uniswapV3FlashCallback",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "amountMinimum",
          "type": "uint256"
        },
        {
          "internalType": "address",
          "name": "recipient",
          "type": "address"
        }
      ],
      "name": "unwrapWETH9",
      "outputs": [],
      "stateMutability": "payable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "token",
          "type": "address"
        },
        {
          "internalType": "address",
          "name": "recipient",
          "type": "address"
        },
        {
          "internalType": "uint256",
          "name": "value",
          "type": "uint256"
        }
      ],
      "name": "withdrawToken",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "stateMutability": "payable",
      "type": "receive"
    }
  ]
```

### Flash Swap

Uniswap Flash Swaps allow you to withdraw up to the full reserves of any ERC20 token on Uniswap and execute arbitrary logic at no upfront cost, provided that by the end of the transaction you either:

* pay for the withdrawn ERC20 tokens with the corresponding pair tokens
* return the withdrawn ERC20 tokens along with a small fee

Flash swaps are incredibly useful because they obviate upfront capital requirements and unnecessary order-of-operations constraints for multi-step transactions involving Uniswap.

Learn more about Flash Swaps [here](https://docs.uniswap.org/protocol/V2/concepts/core-concepts/flash-swaps).

#### initFlash

This method executes the following steps in a single transaction:

1. Borrows an ERC20 token "token0" from a Uniswap Liquidity Pool via Flash Loan
2. Swaps token0 for another ERC20 token "token1" on a DEX "exchange0"
3. Swaps token1 back to token0 on a second DEX "exchange1"
4. Repays the Flash Loan + all fees
5. Deposits profit into your wallet

_Note: Transaction will revert if Flash Loan and fees are unable to be paid only costing a very small gas fee._

#### Parameters

Call `initFlash` with a single struct containing the following parameters:

| Query Param   | Type    | Description                                             |
| ------------- | ------- | ------------------------------------------------------- |
| token0        | Address | Contract Address for token0                             |
| token1        | Address | Contract Address of token1                              |
| loanPairToken | Address | Contract Address of Loan Pair Token                     |
| flashLoanFee  | Number  | Fee for Uniswap Flash Loan (10000, 3000, or 500)        |
| poolFee       | Number  | Fee for Liquidity Pool (10000, 3000, or 500)            |
| amount0       | Number  | Amount of Base Token to be swapped (including decimals) |
| exchange0     | Address | Contract Address for First Exchange                     |
| exchange1     | Address | Contract Address for Second Exchange                    |
| slippage      | Number  | Percent slippage allowed                                |

### Gas Cost

For successful transactions, the gas used by transactions is approximately 680,000.

| Gas Price | Transaction Fee |
| --------- | --------------- |
| 50        | 0.034 Ether     |
| 100       | 0.068 Ether     |
| 200       | 0.136 Ether     |
| 300       | 0.204 Ether     |

### Examples

#### Hardhat + Javascript

```
const hre = require('hardhat');

const divergenceContract = new hre.ethers.Contract(CONTRACT_ADDRESS, abi, signer);
```

```
const contractParams = { 
    token0: "0x6B175474E89094C44Da98b954EedeAC495271d0F", // DAI Contract Address
    token1: "0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48", //USDT Contract Address
    loanPairToken: "0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48", // USDC Contract Address
    flashLoanFee: 3000, // 0.3% Uniswap Flash Loan Fee
    poolFee: 3000, // 0.3% Liquidity Pool Fee
    amount0: 100000000000000000000, // 100 DAI w/ 18 Decimals
    exchange0: "0xE592427A0AEce92De3Edee1F18E0157C05861564", // Uniswap V3 Router Address
    exchange1: "0xd9e1cE17f2641f24aE83637ab66a2cca9C378B9F", // SushiSwap Router Address
    slippage: 1 // 1% slippage allowance 
}
```

```
await divergenceContract.initFlash(contractParams);
```
