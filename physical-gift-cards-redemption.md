Gift Card Redemption on the Fuzzie App
======================================

Gift Activation Code
--------------------

```
[POST] /api/codes/FCXQD39E9/redeem

```

* Success

```
Status: 200
{
  gift: <Gift Object>
}

Gift Object will also contain a `cash_back` key that contains the amount of cash back received while redeeming this code.

```

* Failure

```
Status Code: 404
{
  "message": "Invalid code"
}
```

```
Status Code: 410
{
  "message": "Used code"
}
```

```
Status Code: 409
{
  "message": "Code not activated"
}
```


___________________________________________________________

Wallet Code
-----------


```
[POST] /api/codes/FCEE9UABE/redeem

```

Response
--------

* Success

```
Status: 200
{
  cash_back: 100
}

```

___________________________________________________________
