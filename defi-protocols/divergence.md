# Divergence

## Introduction

The Divergence smart contract is an arbitrage + flash loan function rolled into one transaction. It lets you ... Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam pellentesque, quam volutpat porta tincidunt, leo est pharetra ligula, et pulvinar justo sapien vel augue.

#### Supported Exchanges

| Exchanges  | Address                                      |
| ---------- | -------------------------------------------- |
| Uniswap V3 | `0xE592427A0AEce92De3Edee1F18E0157C05861564` |
| Uniswap V2 | `0xf164fC0Ec4E93095b804a4795bBe1e041497b92a` |
| Sushiswap  | `0xd9e1cE17f2641f24aE83637ab66a2cca9C378B9F` |
| Kyber      | `0x818E6FECD516Ecc3849DAf6845e3EC868087B755` |
| Dodo V2    | `0xa356867fDCEa8e71AEaF87805808803806231FdC` |
| Bancor     | `0x52Ae12ABe5D8BD778BD5397F99cA900624CfADD4` |
| Curve      | `0x0000000022D53366457F9d5E68Ec105046FC4383` |

### Versioning

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam pellentesque, quam volutpat porta tincidunt, leo est pharetra ligula, et pulvinar justo sapien vel augue.

### Arbitrage

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam pellentesque, quam volutpat porta tincidunt, leo est pharetra ligula, et pulvinar justo sapien vel augue.

#### Flash Loan

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam pellentesque, quam volutpat porta tincidunt, leo est pharetra ligula, et pulvinar justo sapien vel augue.

#### initFlash

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam pellentesque, quam volutpat porta tincidunt, leo est pharetra ligula, et pulvinar justo sapien vel augue.

#### Request

Call `initFlash` with the following parameters:

| Query Param | Description |
| ----------- | ----------- |
|             |             |
|             |             |
|             |             |

#### Response

| Field | Description |
| ----- | ----------- |
|       |             |
|       |             |
|       |             |

#### Examples

```
// Some code
{ 
    inputToken: tokenPair.token0,
    amount0: inputAmount,
    slippage: 1,
    loanPairToken: '0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48',
    outputToken: tokenPair.token1,
    flashLoanFee: 3000,
    uniPoolFee: 3000,
    exchange0: exchange0,
    exchange1: exchange1
}
```
