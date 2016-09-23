Gift Card Redemption on the Fuzzie App
======================================

Gift Activation Code
--------------------

```
[GET] /api/codes/:merchant_code/check

Params: {store_id: 'store-identifier'}

Headers: HTTP_API_TOKEN

Example: [GET] http://fuzzie.com.sg/api/codes/FUZZIEUIBC3KX/check
          Params: {'store-id' : fee8bc53-e3a0-48bc-a26c-95ac0d6a3e21}
          Headers: {HTTP_API_TOKEN=abcdef123*$%}

```

* Success

```
Status: 200
{
  "activatable": "true"
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
  "message": "Already activated"
}
```


___________________________________________________________

Wallet Code
-----------


```
[POST] /api/codes/:merchant_code/activate

Params: {store_id: 'store-identifier'}

Headers: HTTP_API_TOKEN

Example: [POST] http://fuzzie.com.sg/api/codes/FUZZIEUIBC3KX/activate
          Params: {'store-id' : fee8bc53-e3a0-48bc-a26c-95ac0d6a3e21}
          Headers: {HTTP_API_TOKEN=abcdef123*$%}

```

Response
--------

* Success

```
Status: 200
{
  "activation_code":
    {
      "expiration_date":"2016-08-07",
      "activated_at":"2016-05-09T07:24:48.817Z",
      "merchant_code":"FUZZIEUIBC3KX"
    }
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
  "message": "Already activated"
}

```
___________________________________________________________
