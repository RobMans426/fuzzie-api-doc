Activation
=============================


Request
-------

```
[POST] /api/codes/:merchant_code/activate

Params: {store_id: 'store-identifier'}

Example: [POST] http://fuzzie.com.sg/api/codes/FUZZIEUIBC3KX/activate
          Params: {'store-id' : fee8bc53-e3a0-48bc-a26c-95ac0d6a3e21}

```

Response
--------

1. Success

```
Status: 200
{
  "activation_code":
    {
      "expiration_date":"2016-08-07",
      "activated_at":"2016-05-09T07:24:48.817Z",
      "merchant_code":"dsfdsfdsfgesrgt"
    }
}

```


2. Failure

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