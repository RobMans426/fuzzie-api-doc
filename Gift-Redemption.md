# Gift Redemption Process

It is a two step process:

1. Looking up the gift using the gift-code provided by the user on their physical or virtual gift card. 
2. If the lookup is a success, and the gift is found to be redeemable, go ahead with the second step of actually redeeming the gift.

## Lookup

### Request

    [GET] `/api/gifts/:code`

### Response

If the lookup is a success:

```
{
  gift: {
    code: "EANCMOPH",
    value: "15",
    redeemable: true,
    expired: false,
    expiration_date: "2016-03-09T11:12:34.452Z",
    used: false,
    redeemed_at: null,
    redeemed_store: null,
    sender: {
      name: "Unnikrishnan Kp",
      email: "unni.tallman@gmail.com",
      sent_at: "2015-03-13T10:44:11.024+08:00"
    }
  }
}

```
 
In case of failure:

- Invalid Gift code: `Status code 404`
- Store authentication failed: `Status Code 401`


## Redeem

### Request

    [PUT] `/api/gifts/:gift-code/redeem`

### Response

if the gift has been redeemed successfully:

```
{
  gift: {
    code: "EANCMOPH",
    value: "15",
    redeemable: false,
    expired: false,
    expiration_date: "2016-03-09T11:12:34.452Z",
    used: true,
    redeemed_at: "2016-02-08T19:12:36.744+08:00",
    redeemed_store: "Aramsa ~ The Garden Spa",
    sender: {
      name: "Unnikrishnan Kp",
      email: "unni.tallman@gmail.com",
      sent_at: "2015-03-13T10:44:11.024+08:00"
    }
  }
}
```

In case of failure: 

- Invalid Gift code: `Status code 404`
- Gift expired: `Status Code 410`
- Gift used: `Status Code 412`
- Store authentication failed: `Status Code 401`

## Authentication

All stores will be provided a unique secret token. This needs to be sent in `X-StoreToken` header with the above API calls in order to authenticate the store. 