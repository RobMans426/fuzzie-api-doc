Fuzzie Gift Card
================

A gift card is sold offline to a user at a store. At this point, the POS needs to activate the gift card by making an HTTP API call to the Fuzzie servers. Only an activated gift card can later be redeemed.

A Fuzzie gift card will have 2 unique codes associated with it. Both these codes will be unique to a particular gift card.

1. *Merchant Code*: This code will be either visible on the gift card or embedded within a barcode or QR code. This code is used by the merchant, at the POS for activating the card.

2. *Gift Code*: This won't be visible directly on the card. The user who buys the gift card will need to scratch the card to access this code. This code needs to be entered into the Fuzzie App to add the gift card to a user's gift box. The user can then redeem the gift by showing this gift card within the Fuzzie app at a store. 


Gift Card Activation at POS
=============================

To activate a gift card, the POS will need to make an API call to the Fuzzie server. This request has to include the following:

1. Secret API token.

This needs to be included as an HTTP Header `HTTP_API_TOKEN`

2. Merchant code of the gift card.

The merchant (cashier) needs to enter this on the POS either by reading the merchant code on a gift card or by scanning a bar code.

3. Store identifier. 

Every store should have a unique identifier. This is needed so that Fuzzie can track the store from where a particular gift card has been sold/activated.


API Request
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
