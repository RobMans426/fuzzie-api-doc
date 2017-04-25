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
  "message": "You have entered an invalid code."
}
```

```
Status Code: 410
{
  "message": "You have already used this code or it has expired."
}
```

```
Status Code: 409
{
  "message": "This code has not been activated."
}
```

