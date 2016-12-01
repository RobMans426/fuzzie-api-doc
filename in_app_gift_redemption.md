Gift Redemption - In App
------------------------

Request

```
[POST] /gifts/gift-id/redeem
params: {pin: '4 digit store pin'}
````

Response

- Upon successful redemption, Gift object will be sent with status code 200
- 422: Gift used for expired - cannot be redeemed.
- 404: Invaid gift id
- 401: if the gift sender (user) has been blocked by the admin.
