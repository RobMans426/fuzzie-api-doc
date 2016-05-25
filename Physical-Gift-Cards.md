A Fuzzie gift card will have 2 unique codes associated with it.

1. Merchant Code: This code will be either visible on the gift card or embedded within a barcode or QR code. This code is used by the merchant, at the POS for activating the card.

2. Gift Code: This won't be visible directly on the card. The user who buys the gift card will need to scratch the card to access this code. This code needs to be entered into the Fuzzie App to add the gift card to a user's gift box. The user can then redeem the gift by showing this gift card within the Fuzzie app at a store. 


Gift Card Activation at POS
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
