## 契約の変更

```javascript
{
    "$schema": "http://json-schema.org/draft-04/schema#",
    "properties": {
      "acct": {"type": "number"},
      "cusip": {"type": "string"},
      "shares": {"type": "number", "minimum": 100}
    },
     "required": ["acct", "cusip", "shares"]
}
```

```javascript
POST /trade/buy
Accept: application/json
{ "acct": "12345",
"cusip": "037833100",
"shares": "1000" }
```


```javascript
{
    "$schema": "http://json-schema.org/draft-04/schema#",
    "properties": {
      "acct": {"type": "number"},
      "sedol": {"type": "string"},
      "shares": {"type": "number", "minimum": 100}
    },
     "required": ["acct", "sedol", "shares"]
}
```