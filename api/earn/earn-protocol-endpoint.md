# Earn Protocol Endpoint

## **Endpoint**

Alta Finance has an Earn API endpoint that will return details about the Earn protocol by network in addition to **tvl** across all networks in aggregate.

**tvl** is returned in `usdc` units.

**maxAPR** is returned in `percentage` units.

**aprBase** and **aprBonus** are returned in `percentage` units.

> GET https://alta.finance/api/earn

## The Earn Procotol object

### Attributes

––

**tvl**

The total value of Earn contracts that have been opened.

**maxAPR**

The current max USDC apr rate.

**data**

The individual rates and tvl broken down by network.

### **Response**

––

```
// Earn API Endpoint Response
{
  "tvl": 9246931.603002686,
  "maxAPR": 0.10335,
  "data": [
    {
      "contractAddress": "0xaaaaaa7a1cff5a1e91d57f4a2c8f8dfc9c60116c",
      "aprBase": 0.10335,
      "aprBonus": 0,
      "symbolBase": ["USDC", "USDT", "DAI", "FRAX", "ALTA"],
      "symbolBonus": "",
      "tvl": 9019625.126175,
      "network": "ethereum",
      "link": "https://app.alta.finance/earn"
    },
    {
      "contractAddress": "0xaaaaaa7a1cff5a1e91d57f4a2c8f8dfc9c60116c",
      "aprBase": 0.10335,
      "aprBonus": 0,
      "symbolBase": ["USDC", "USDT", "DAI", "FRAX", "ALTA"],
      "symbolBonus": "",
      "tvl": 227306.47682768747,
      "network": "polygon",
      "link": "https://app.alta.finance/earn"
    }
  ]
}

```

