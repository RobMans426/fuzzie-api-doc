Request
-------

```
  [GET] /api/credit_cards
```

Response
--------

Will be an array of `CreditCard` objects. A CreditCard object will be of the form:

```
  {
    "id": 1,
    "title": "HDFC Platina",
    "banner": "http://fuzzie-assets.s3.amazonaws.com/credit_cards/banners/000/000/001/original/icici.jpg?1493884994",
    "banner_details_page": "http://fuzzie-assets.s3.amazonaws.com/credit_cards/banners/000/000/001/original/hdfc.jpg?1493884994",
    "bank_name": "ICICI",
    "preview_copy": "test preview",
    "details": [
      "point 1",
      "point 2",
      "point 3"
    ],
    "enable_signup": true,
    "signup_body": "test signup copy",
    "signup_url": "http://google.com/signup"
  }
```
