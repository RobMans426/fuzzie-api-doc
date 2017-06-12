There are 2 API calls that deal with payment: 

1. Express checkout (buying of a single gift)

```
[POST] /gifts
{
  "friend_name":"Kumara",
  "friend_id": '234'
  "gift_card_type":"aeb10188",
  "message":"Happy Birthday!",
  "payment_receipt":{"payment_method_nonce":"7fd993d1-55f6-441c-83e9-3135b5059f21"},
  "wallet":"10.0"
}

- if the gift it is being bought for self (Buy It), `friend_id` and `friend_name` should be omitted.
- `gift_card_type` - this specifies the gift card being bought. it comes from the `type` field on a GiftCard or Service(package) object.
- payment_receipt - it should contain either a `payment_method_nonce` (from from Braintree using BrainTree's client SDK) OR a `payment_method_token` (in the case of a saved card. Refer to https://github.com/fuzziegang/fuzzie-api-doc/blob/master/payment_methods.md)
- wallet: how much of the total amount is to be taken from user's wallet. (optional)
```

2. Shopping bag checkout (buying of one or more gifts in the user's shopping bag, in one go).

```
[POST] /api/shopping_bag/checkout
params - same as the Express Checkout. Omit the `gift_card_type` parameter.
```

Errors

- Invalid Payment 

Code: 422

- Gift card sold out

Code: 406
The response JSON will have a `error` key. Its value needs to be displayed to the user. 

---------------------------------

Notes for iOS app developers
----------------------------

- Payment bug- HSBC webview cookies error. Solution given below by Braintree. Add this to the docs for future reference.

```
Regarding the iOS case, I've performed a number of tests myself and confirmed that 
setting the cookieAcceptPolicy on NSHTTPCookieStorage sharedHTTPCookieStorageto 
NSHTTPCookieAcceptPolicyAlways works, as long as the cookieAcceptPolicy isn't being 
overridden elsewhere, and displays the HSBC authentication page instead of the error page.
```
Notes for Android app developers
--------------------------------

- [The fix for the bug with HSBC](https://github.com/braintree/braintree_android/releases/tag/2.5.4.)



