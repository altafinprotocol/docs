# AFN Token Supply Endpoints

### **Project Data**

AltaFin has an AFN token project API endpoint that will return details about the AFN token project in addition to **totalSupply** and **totalCirculating** values.

**totalSupply** and **totalCirculating** values are returned in `ether` units.

`GET https://altafin.co/api/project`

**Response**

```
// Project API Endpoint Response
{
  "project": {
    "name": "AltaFin",
    "asset": "AFN",
    "url": "https://altafin.co",
    "logo": "https://images.ctfassets.net/dj2ij87ekk1y/6QLADorHyGFcr804X0spbG/a11f3a582c9f6b40bc7b010d481c9242/AltaFin-Logo-Square-700x.png"
  },
  "protocol": [
    {
      "name": "Ethereum",
      "type": "ERC-20",
      "contractId": "0xe46f290cd59195a83e757891430d8d517d16b334",
      "explorerLink": "https://etherscan.io/token/0xe46f290cd59195a83e757891430d8d517d16b334"
    },
    {
      "name": "Polygon",
      "type": "ERC-20",
      "contractId": "0xb4a055786ee8b9c9a09156bb185eba7b91540ee5",
      "explorerLink": "https://polygonscan.com/token/0xb4a055786ee8b9c9a09156bb185eba7b91540ee5"
    },
    {
      "name": "Solana",
      "type": "SPL",
      "contractId": "BCTqtHLmYTFyqXTVPtggwoJ2fkV17AVyZXZCTbKXoaeX",
      "explorerLink": "https://solscan.io/token/BCTqtHLmYTFyqXTVPtggwoJ2fkV17AVyZXZCTbKXoaeX"
    }
  ],
  "totalCirculating": "1645404455.617882",
  "totalSupply": "10000000000"
}

```

### Circulating Supply

API endpoint that will return the **totalCirculating** value.

`GET https://altafin.co/api/project/supply/circulating`

**Response**

```
{ 
  "circulatingSupply": "1645404455.617881" 
}
```

### Total Supply

API endpoint that will return the **totalSupply** value.

`GET https://altafin.co/api/project/supply/total`

**Response**

```
{ 
  "totalSupply": "10000000000" 
}
```

