## 契約の変更

契約をバージョン管理しないことによる問題を説明するために、Appleの普通株式（AAPL）の一定数の株式を購入する例を使用します。
このリクエストのスキーマは次のようになります

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

この場合、株式を購入するには、acct：仲介アカウント、cusip：CUSIPコード（有価証券識別コード[Committee on Uniform Securities Identification Procedures]）、
および最後に100より大きいshares：株式数、を指定しなければなりません。
RESTを使用して仲介アカウント12345に対してApple株式1000株（CUSIPコード 037833100）を購入するように要求するコードは次のようになります

```javascript
POST /trade/buy
Accept: application/json
{ "acct": "12345",
"cusip": "037833100",
"shares": "1000" }
```

さて、このサービスにCUSIPコードではなくSEDOLコード（有価証券識別コード[Stock Exchange Daily Official List]）を受け入れる契約を変更するとしましょう。
これは、取引される特定の商品を識別する別の業界標準の方法です。そうすると、契約は以下のようになります。

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

これは、主要なクライアントコードがまだCUSIPを使用しているためにエラーになるという点で、破壊的変更と見なされます。
取引されている株式を識別するのにバージョン1はCUSIPを使用し、バージョン2はSEDOLを使用するようバージョン管理する必要があります。
