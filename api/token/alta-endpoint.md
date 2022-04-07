# ALTA Endpoint

### **Endpoint**

Alta Finance has an ALTA token API endpoint that will return details about the ALTA token in addition to **totalSupply** and **totalCirculating** values.

**totalSupply** and **totalCirculating** values are returned in `ether` units.

`GET https://alta.finance/api/project`

### ALTA object



**Response**

```
// Project API Endpoint Response
{
  "project": {
    "name": "Alta Finance",
    "asset": "ALTA",
    "url": "https://alta.finance",
    "logo": "https://images.ctfassets.net/dj2ij87ekk1y/6QLADorHyGFcr804X0spbG/a11f3a582c9f6b40bc7b010d481c9242/AltaFin-Logo-Square-700x.png"
  },
  "protocol": [
    {
      "name": "Ethereum",
      "type": "ERC-20",
      "contractId": "0xe0cCa86B254005889aC3a81e737f56a14f4A38F5",
      "explorerLink": "https://etherscan.io/token/0xe0cCa86B254005889aC3a81e737f56a14f4A38F5"
    },
    {
      "name": "Polygon",
      "type": "ERC-20",
      "contractId": "0xe0cCa86B254005889aC3a81e737f56a14f4A38F5",
      "explorerLink": "https://polygonscan.com/token/0xe0cCa86B254005889aC3a81e737f56a14f4A38F5"
    }
  ],
  "totalCirculating": "1645404455.617882",
  "totalSupply": "10000000000"
}
```

### Circulating Supply

API endpoint that will return the **totalCirculating** value.

`GET https://alta.finance/api/project/supply/circulating`

**Response**

```
{ 
  "circulatingSupply": "1645404455.617881" 
}
```

### Total Supply

API endpoint that will return the **totalSupply** value.

`GET https://alta.finance/api/project/supply/total`

**Response**

```
{ 
  "totalSupply": "10000000000" 
}
```

