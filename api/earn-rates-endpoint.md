# Earn Rates Endpoint

### **Project Data**

Alta Finance has an Earn API endpoint that will return details about the Earn protocol by network in addition to **tvl** across all networks in aggregate**.**

**tvl** is returned in `usdc` units.

**aprBase** and **aprBonus** are returned in `percentage` units.

`GET https://alta.finance/api/earn`

**Response**

```
// Earn API Endpoint Response
{
    "tvl": 2550.973029221971,
    "data": [
        {
            "contractAddress": "0x88549Ed1c99ADC0B33B4517B7F70485Ea107a30f",
            "aprBase": 0.1975,
            "aprBonus": 0.07479466666666668,
            "symbolBase": "USDC",
            "symbolBonus": "AFN",
            "tvl": 1680.3586932462013,
            "network": "ethereum",
            "link": "https://app.alta.finance/earn"
        },
        {
            "contractAddress": "0x88549Ed1c99ADC0B33B4517B7F70485Ea107a30f",
            "aprBase": 0.1975,
            "aprBonus": 0.07479466666666668,
            "symbolBase": "USDC",
            "symbolBonus": "AFN",
            "tvl": 870.61433597577,
            "network": "polygon",
            "link": "https://app.alta.finance/earn"
        }
    ]
}
```

