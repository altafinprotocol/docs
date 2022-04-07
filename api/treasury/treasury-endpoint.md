# Treasury Endpoint

### **Endpoint**

Alta Finance has a Treasury API endpoint that will return details about the Alta Finance Treasury.

> GET https://alta.finance/api/earn/rates

### The Treasury object

#### Attributes

––

**balance**

This represents the USDC value of the Treasury balance. This value is calculated using the following formula:

`wallet.balance + exchanges.balance + funds.balance + earn.balance`

**address**

This represents the blockchain addresses used to calculate the Alta Finance Treasury.

**wallet**

This represents the liquid token holdings of Alta Finance.

**vault**

This represents the Alta Finance ALTA tokens held in reserve for strategic use according the ALTA Token Model.

**exchanges**

This represents the protocol owned liquidity pool values that ALTA holds.

**funds**

This represents the real world asset funds. The values of these are created following the burning/minting rules set for raALTA and rdALTA.

**networks**

This represents the combined value of ALTA across the different blockchain networks, (note: this is the only attribute that includes vault value).

#### **Response**

**––**

```
{
    "address": [
        "0x087183a411770a645a96cf2e31fa69ab89e22f5e",
        "0xBDfFBAbFC682f4a800EBFBA3eD147fd629FC8572",
        "0x92fc4338ad16d07be1d79098015cb2957d21fdc0",
        "0x5706d4Cc27b5f5B59d026c6E03DEDED995455071"
    ],
    "wallet": {
        "response": {
            "balance": 229.18809173237716,
            "data": [
                {
                    "asset": "ETH",
                    "value": "0.06736811202756947",
                    "usdValue": 214.36735351508688,
                    "usdPrice": 3182.03,
                    "network": "ethereum",
                    "rawContract": {
                        "address": null,
                        "decimal": 18
                    },
                    "metadata": {
                        "logo": "https://storage.googleapis.com/zapper-fi-assets/tokens/ethereum/0x0000000000000000000000000000000000000000.png"
                    }
                },
                {
                    "asset": "WETH",
                    "value": "0.003089530486684978",
                    "usdValue": 9.831534810033803,
                    "usdPrice": 3182.21,
                    "network": "ethereum",
                    "rawContract": {
                        "address": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
                        "decimal": 18
                    },
                    "metadata": {
                        "decimals": 18,
                        "logo": "https://static.alchemyapi.io/images/assets/2396.png",
                        "name": "WETH",
                        "symbol": "WETH"
                    }
                },
                {
                    "asset": "MATIC",
                    "value": "3.045666182603816",
                    "usdValue": 4.4771292884276095,
                    "usdPrice": 1.47,
                    "network": "ethereum",
                    "rawContract": {
                        "address": "0x7d1afa7b718fb893db30a3abc0cfc608aacfebb0",
                        "decimal": 18
                    },
                    "metadata": {
                        "decimals": 18,
                        "logo": "https://static.alchemyapi.io/images/assets/3890.png",
                        "name": "Polygon",
                        "symbol": "MATIC"
                    }
                },
                {
                    "asset": "MATIC",
                    "value": "0.34834974069989645",
                    "usdValue": 0.5120741188288478,
                    "usdPrice": 1.47,
                    "network": "polygon",
                    "rawContract": {
                        "address": "0x0000000000000000000000000000000000001010",
                        "decimal": 18
                    },
                    "metadata": {
                        "decimals": 18,
                        "logo": "https://static.alchemyapi.io/images/assets/3890.png",
                        "name": "Polygon",
                        "symbol": "MATIC"
                    }
                }
            ]
        }
    },
    "vault": {
        "response": {
            "balance": 79.55075000000001,
            "data": [
                {
                    "asset": "ETH",
                    "value": "0.025",
                    "usdValue": 79.55075000000001,
                    "usdPrice": 3182.03,
                    "network": "ethereum",
                    "rawContract": {
                        "address": null,
                        "decimal": 18
                    },
                    "metadata": {
                        "logo": "https://storage.googleapis.com/zapper-fi-assets/tokens/ethereum/0x0000000000000000000000000000000000000000.png"
                    }
                }
            ]
        }
    },
    "exchanges": {
        "success": true,
        "statusCode": 200,
        "response": {
            "balance": 0,
            "balanceEthereum": 0,
            "balancePolygon": 0,
            "data": []
        }
    },
    "funds": {
        "success": true,
        "statusCode": 200,
        "response": {
            "balance": 4850000,
            "balancePolygon": 4850000,
            "balanceEthereum": 0,
            "data": [
                {
                    "balance": 4850000,
                    "title": "Short-Term Fund",
                    "data": [
                        {
                            "asset": "raALTA",
                            "value": 59950000,
                            "usdValue": 59950000,
                            "usdPrice": 1,
                            "network": "polygon",
                            "rawContract": {
                                "address": "0x336f20Ddf1325092E1de4203B09Ae1df9e277Ded",
                                "decimal": 18
                            },
                            "metadata": {
                                "decimals": 18,
                                "name": "Alta Asset",
                                "symbol": "raALTA",
                                "logo": "https://images.ctfassets.net/dj2ij87ekk1y/7f11nN6RuNJ5KNaBPqFTcw/3e698f1737cba01aa9cd4daf2362561b/AltaFin-Logo-Square-700x.png?h=250"
                            }
                        },
                        {
                            "asset": "rdALTA",
                            "value": 55100000,
                            "usdValue": 55100000,
                            "usdPrice": 1,
                            "network": "polygon",
                            "rawContract": {
                                "address": "0x935e49Fc1389Cb5358dBa426Dc64a0Fa27071abB",
                                "decimal": 18
                            },
                            "metadata": {
                                "decimals": 18,
                                "name": "Alta Debt",
                                "symbol": "rdALTA",
                                "logo": "https://images.ctfassets.net/dj2ij87ekk1y/7f11nN6RuNJ5KNaBPqFTcw/3e698f1737cba01aa9cd4daf2362561b/AltaFin-Logo-Square-700x.png?h=250"
                            }
                        }
                    ]
                },
                {
                    "balance": 0,
                    "title": "Dream Fund",
                    "data": [
                        {
                            "asset": "raALTA",
                            "value": 0,
                            "usdValue": 0,
                            "usdPrice": 1,
                            "network": "polygon",
                            "rawContract": {
                                "address": "0x336f20Ddf1325092E1de4203B09Ae1df9e277Ded",
                                "decimal": 18
                            },
                            "metadata": {
                                "decimals": 18,
                                "name": "Alta Asset",
                                "symbol": "raALTA",
                                "logo": "https://images.ctfassets.net/dj2ij87ekk1y/7f11nN6RuNJ5KNaBPqFTcw/3e698f1737cba01aa9cd4daf2362561b/AltaFin-Logo-Square-700x.png?h=250"
                            }
                        },
                        {
                            "asset": "rdALTA",
                            "value": 0,
                            "usdValue": 0,
                            "usdPrice": 1,
                            "network": "polygon",
                            "rawContract": {
                                "address": "0x935e49Fc1389Cb5358dBa426Dc64a0Fa27071abB",
                                "decimal": 18
                            },
                            "metadata": {
                                "decimals": 18,
                                "name": "Alta Debt",
                                "symbol": "rdALTA",
                                "logo": "https://images.ctfassets.net/dj2ij87ekk1y/7f11nN6RuNJ5KNaBPqFTcw/3e698f1737cba01aa9cd4daf2362561b/AltaFin-Logo-Square-700x.png?h=250"
                            }
                        }
                    ]
                },
                {
                    "balance": 0,
                    "title": "Long-Term Fund",
                    "data": [
                        {
                            "asset": "raALTA",
                            "value": 0,
                            "usdValue": 0,
                            "usdPrice": 1,
                            "network": "polygon",
                            "rawContract": {
                                "address": "0x336f20Ddf1325092E1de4203B09Ae1df9e277Ded",
                                "decimal": 18
                            },
                            "metadata": {
                                "decimals": 18,
                                "name": "Alta Asset",
                                "symbol": "raALTA",
                                "logo": "https://images.ctfassets.net/dj2ij87ekk1y/7f11nN6RuNJ5KNaBPqFTcw/3e698f1737cba01aa9cd4daf2362561b/AltaFin-Logo-Square-700x.png?h=250"
                            }
                        },
                        {
                            "asset": "rdALTA",
                            "value": 0,
                            "usdValue": 0,
                            "usdPrice": 1,
                            "network": "polygon",
                            "rawContract": {
                                "address": "0x935e49Fc1389Cb5358dBa426Dc64a0Fa27071abB",
                                "decimal": 18
                            },
                            "metadata": {
                                "decimals": 18,
                                "name": "Alta Debt",
                                "symbol": "rdALTA",
                                "logo": "https://images.ctfassets.net/dj2ij87ekk1y/7f11nN6RuNJ5KNaBPqFTcw/3e698f1737cba01aa9cd4daf2362561b/AltaFin-Logo-Square-700x.png?h=250"
                            }
                        }
                    ]
                }
            ]
        }
    },
    "earn": {
        "success": true,
        "statusCode": 200,
        "response": {
            "balance": -10674.896156035584,
            "data": [
                {
                    "asset": "USDC",
                    "value": 0,
                    "usdValue": 0,
                    "usdPrice": 1,
                    "network": "ethereum",
                    "rawContract": {
                        "address": "0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
                        "decimal": 6
                    },
                    "metadata": {
                        "decimals": 6,
                        "name": "USD Coin",
                        "symbol": "USDC",
                        "logo": "https://static.alchemyapi.io/images/assets/3408.png"
                    }
                },
                {
                    "asset": "USDC",
                    "value": 10674.896156035584,
                    "usdValue": -10674.896156035584,
                    "usdPrice": 1,
                    "network": "polygon",
                    "rawContract": {
                        "address": "0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
                        "decimal": 6
                    },
                    "metadata": {
                        "decimals": 6,
                        "name": "USD Coin",
                        "symbol": "USDC",
                        "logo": "https://static.alchemyapi.io/images/assets/3408.png"
                    }
                }
            ]
        }
    },
    "balance": 4839554.291935697,
    "networks": {
        "balance": 4850308.738841732,
        "ethereum": 308.2267676135483,
        "polygon": 4850000.5120741185
    }
}
```

