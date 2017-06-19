Gift It
-------

Use the same [API call that is used to buy a single gift](https://github.com/fuzziegang/fuzzie-api-doc/blob/master/payment.md). 

Additional Parameters
---------------------

1. `gifted` - set this as `true`
2. `friend_name` - Name of the person to whom the gift is sent.
3. `friend_id` (optional) - Facebook ID of the friend. 
4. `message` - Message to be sent to the person along with the gift. 

Sample Response
---------------

```
{
    "type": "Gift",
    "cash_back": 120,
    "number_of_gifts": 1,
    "bought_for_self": false,
    "online_brand": false,
    "third_party_code": null,
    "gift": {
        "id": "a8a03bba-93e6-4685-bd3e-dbe9de5ec327",
        "code": "77817676",
        "used": false,
        "opened": false,
        "message": "Happy Holocaust !",
        "expiration_date": "2017-09-17T23:59:59.999+08:00",
        "order_number": "358187",
        "redeemed_time": null,
        "expired": false,
        "cash_back": 0,
        "online": false,
        "image": "http://d3mytoddva16m1.cloudfront.net/photos/images/000/000/718/original/appGraphic_Septiemie.png?1456975243",
        "logo": "http://fuzzie-assets.s3.amazonaws.com/pictures/images/3e6/1e6/78-/original/fuzzie_logo.png",
        "third_party_code": null,
        "external_redeem_page": "",
        "redeem_timer_started_at": null,
        "brand_id": "34cb9194-d3f9-4b2b-b2fa-e8796759e0c8",
        "gift_url": "http://beta.fuzzie.com.sg/gifts/E9TdKX14Ou",
        "gifted": true,
        "sent_time": "2017-06-19T17:23:12.932+08:00",
        "redeemed_store": null,
        "gift_card": {
            "type": "f6cce788",
            "price": {
                "value": "800",
                "currency_code": "SGD",
                "currency_symbol": "S$"
            },
            "name": "S$800 Gift Card",
            "discounted_price": 800,
            "kind": "GiftCard",
            "valid_with_in_store_promo": false,
            "promotional_price": null,
            "start_date": null,
            "end_date": null,
            "terms": "Redeemable only at Septieme Largeur’s store at Pickering Street<br>Expires 90 days from date of purchase<br>Not valid for online purchases<br>Not exchangeable for cash<br>Valid for one time use only. Balance credit will not be stored<br>Multiple gift cards can be used in a single bill<br>",
            "on_promotion": false,
            "description": null,
            "cash_back": {
                "percentage": 0,
                "cash_back_percentage": 0,
                "power_up_percentage": 0,
                "value": 0
            },
            "sold_out": false,
            "display_name": "Septième Larguer E-Gift Card"
        },
        "service": null
    }
}
```

Notes
-----

- The API response now has a `gift` key which contains the Gift object. 
- The Gift object contains as `gift_url` key
