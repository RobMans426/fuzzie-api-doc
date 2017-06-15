Request
-------

`[GET] /api/banks`

Response
--------

Response will be an array of `Bank` objects. A `Bank` object will be of the form: 

```
  {
    "id": 2,
    "name": "HSBC",
    "banner": "http://d3mytoddva16m1.cloudfront.net/banks/banners/000/000/002/original/hsbc-bank-logo.jpg?1497507001",
    "credit_cards": [
      {
        "id": 2,
        "title": "HSBC Premier",
        "banner": "http://d3mytoddva16m1.cloudfront.net/credit_cards/banners/000/000/002/original/hsbc_premier.png?1497507267",
        "banner_details_page": "http://d3mytoddva16m1.cloudfront.net/credit_cards/banner_details_pages/000/000/002/original/hsbc_premier_2.jpg?1497507267",
        "bank_name": "HSBC",
        "preview_copy": "test",
        "details": [
          "one",
          "two",
          "three"
        ],
        "enable_signup": true,
        "signup_body": "this is test again",
        "signup_url": "http://google.com/"
      }
    ]
  }
```
