Signup with referral code
=========================

Use the regular [Signup API calls](https://github.com/fuzziegang/fuzzie-api-doc/blob/master/login_signup.md) with an addition `referred_by_code` parameter. Everything else remain the same.


Get details of the Referrals made by the current user
=====================================================

Request
-------

```
[GET] http://beta.fuzzie.com.sg/api/referrals
Pass X-FUZZIE-TOKEN header with the request
```

Response
--------
```
{
  "credits": 0,
  "referred_users": [
    {
      "name": "Hari Damodaran",
      "status": "signed_up"
    }
  ]
}

status can be either 'signed_up' or 'purchased'
```