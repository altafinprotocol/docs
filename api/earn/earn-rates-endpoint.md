# Earn Rates Endpoint

## **Endpoint**

Alta Finance has an Earn Rates API endpoint that will return details about the individual max USDC rates calculated in **APY** and **APR**, separated by network.

**apy** and **apr** are returned in `percentage` units.

> GET https://alta.finance/api/earn/rates

## The Earn Rates object

### Attributes

––

**data**

This is the lending rates offered by Alta Finance Earn Protocol broken down by asset and network.

### **Response**

**––**

```
// Earn Rates API Endpoint Response
{
  "data": [
    {
      "ethereum": {
        "lendRates": [
          { "tokenSymbol": "USDC", "apy": 0.10695129284612537, "apr": 0.10335 },
          { "tokenSymbol": "USDT", "apy": 0.10695129284612537, "apr": 0.10335 },
          { "tokenSymbol": "DAI", "apy": 0.10695129284612537, "apr": 0.10335 },
          { "tokenSymbol": "FRAX", "apy": 0.10695129284612537, "apr": 0.10335 },
          { "tokenSymbol": "ALTA", "apy": 0.10695129284612537, "apr": 0.10335 }
        ],
        "borrowRates": []
      }
    },
    {
      "polygon": {
        "lendRates": [
          { "tokenSymbol": "USDC", "apy": 0.10695129284612537, "apr": 0.10335 },
          { "tokenSymbol": "USDT", "apy": 0.10695129284612537, "apr": 0.10335 },
          { "tokenSymbol": "DAI", "apy": 0.10695129284612537, "apr": 0.10335 },
          { "tokenSymbol": "FRAX", "apy": 0.10695129284612537, "apr": 0.10335 },
          { "tokenSymbol": "ALTA", "apy": 0.10695129284612537, "apr": 0.10335 }
        ],
        "borrowRates": []
      }
    }
  ]
}
```

