# Supply API Endpoints

### **Project Data**

AltaFin has a token project API endpoint that will return details about the project in addition to **totalSupply** and **totalCirculating** values.

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
  "protocol": {
    "name": "Ethereum",
    "asset": "ETH",
    "type": "ERC-20",
    "contractId": "0xe46f290cd59195a83e757891430d8d517d16b334"
  },
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

