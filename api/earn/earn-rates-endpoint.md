# Earn Rates Endpoint

### **Endpoint**

Alta Finance has an Earn Rates API endpoint that will return details about the individual max USDC rates calculated in **APY** and **APR**, separated by network.

**apy** and **apr** are returned in `percentage` units.

`GET https://alta.finance/api/earn/rates`

**Response**

```
{
    "data": [
        {
            "ethereum": {
                "lendRates": [
                    {
                        "tokenSymbol": "USDC",
                        "apy": 0.2107874068287039,
                        "apr": 0.1975
                    },
                    {
                        "tokenSymbol": "ALTA",
                        "apr": 0,
                        "apy": 0
                    }
                ],
                "borrowRates": []
            }
        },
        {
            "polygon": {
                "lendRates": [
                    {
                        "tokenSymbol": "USDC",
                        "apy": 0.2107874068287039,
                        "apr": 0.1975
                    },
                    {
                        "tokenSymbol": "ALTA",
                        "apr": 0,
                        "apy": 0
                    }
                ],
                "borrowRates": []
            }
        }
    ]
}
```

