Code Redemption or Activation
=============================

```
[POST] /api/codes/FCXQD39E9/redeem

```

* Success

Depending on the type of code redeemed, response will be one of the below:

```
Status: 200

{
  type: 'PowerUpCode', 
  time_to_expire: 24, 
  brands: [1,2,3,4]  
}

OR

{
  type: 'WalletCode', 
  credits: 25
}

OR

{
  type: 'ActivationCode',
  brand_name: 'Lazada',
  cash_back: 0,
  gift_type: 'GiftCard',
  gift_title: '25$ Lazada E-GiftCard'
}

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