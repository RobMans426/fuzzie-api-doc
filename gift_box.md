Request
-------

`http://beta.fuzzie.com.sg/api/my_gifts/active`

and 

`http://beta.fuzzie.com.sg/api/my_gifts/used`

Response
--------

An array of `Gift` objects. 

A Sample Gift Object
--------------------
```
{
    "id": "a5a962e7-cb14-42ae-8ba4-c1cb65adb460",
    "code": "87996622",
    "used": true,
    "opened": true,
    "message": "",
    "expiration_date": "2018-04-05T23:59:59.999+08:00",
    "order_number": "386281",
    "redeemed_time": "2017-05-19T16:56:04.115+08:00",
    "expired": false,
    "cash_back": 0,
    "online": true,
    "image": "http://d3mytoddva16m1.cloudfront.net/photos/images/000/000/810/original/BookDepository_4.jpg?1485579870",
    "logo": "http://d3mytoddva16m1.cloudfront.net/brands/online_brand_redeem_page_logos/dc5/dfb/69-/original/Book-Depository-logo.png?1485579870",
    "third_party_code": "fuzzie128",
    "external_redeem_page": "",
    "redeem_timer_started_at": "2017-05-19T15:46:42.300+08:00",
    "brand_id": "dc5dfb69-f9af-4229-baae-8692e8bd47c4",
    "sent_time": "2017-04-05T13:51:28.877+08:00",
    "redeemed_store": null,
    "gift_card": null,
    "service": {
      "type": "5592c16d",
      "price": {
        "value": "10",
        "currency_code": "SGD",
        "currency_symbol": "S$"
      },
      "name": "25% Discount Card",
      "discounted_price": 10,
      "kind": "Service",
      "valid_with_in_store_promo": false,
      "promotional_price": null,
      "start_date": null,
      "end_date": null,
      "terms": "1. You will instantly receive your Book Depository E-Discount Card on your Fuzzie Gift Box upon purchase\r\n\r\n2. Redeemable only on Book Depository via this link www.bookdepository.com/fuzzie\r\n\r\n3. Valid WITH in-store promotions and cashback referral programmes (unless otherwise stated)- yay!\r\n\r\n5. Expires 12 months from date of purchase\r\n\r\n6. Valid for new and existing customers\r\n\r\n7. Not exchangeable for cash\r\n\r\n8. Valid for one-time use only\r\n\r\n9. Only one E-Discount Card can be used per checkout\r\n\r\n10. Eligible for free shipping worldwide, no minimum spending required\r\n\r\nHOW TO REDEEM YOUR BOOK DEPOSITORY E-DISCOUNT CARD\r\n\r\n1. Press the Redeem button on your E-Discount Card to obtain your unique coupon code\r\n\r\n2. Go to www.bookdepository.com/fuzzie\r\n\r\n3. Click the Redeem Coupon button and select as many books as you like\r\n\r\n4. When you reach Your Basket, enter your unique coupon code received from Fuzzie in the Coupon code box",
      "on_promotion": false,
      "description": "this is a test description",
      "cash_back": {
        "percentage": 10,
        "cash_back_percentage": 10,
        "power_up_percentage": 0,
        "value": 1
      },
      "sold_out": true,
      "display_name": "Book Depository- 25% Discount Card",
      "service_category_ids": []
    }
  }

```
