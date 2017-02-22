## スキーマ・バージョニング

![スキーマベース・コントラクト・バージョニング](img/8-2.png)

図8-2. スキーマベース・コントラクト・バージョニング

```javascript
{
    "$schema": "http://json-schema.org/draft-04/schema#",
    "properties": {
      "version": {"type": "integer"},
      "acct": {"type": "number"},
      "cusip": {"type": "string"},
      "sedol": {"type": "string"},
      "shares": {"type": "number", "minimum": 100}
    },
     "required": ["version", "acct", "shares"]
}
```

```javascript
POST /trade/buy
Accept: application/json
{ "version": "2",
  "acct": "12345",
  "sedol": "2046251",
  "shares": "1000" }
```
```javascript
String msg = createJSON(
  "version","2",
  "acct","12345",
  "sedol","2046251",
  "shares","1000")};
jmsContext.createProducer().send(queue, msg);   
```