Referral code/url of the current user
=====================================

[GET] http://fuzzie.com.sg/user with X-FUZZIE-TOKEN header.

Response will have a `referral_code` as well as `referral_url` key.


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

------------------------------------------------------

Manual Referral Code Redemption
===============================

This is for a user to apply a referral code manually on the app, after he has completed sign up and has logged in.

Request
-------

```
  [POST] /api/referrals 
  {"referred_by_code":"sweeling1023"}
```

Success
-------
```
{message: "Referral Code has been redeemed"}, status: 200
```

Error
-----

```
{error: "This code is invalid"}, status: 404
{error: "You have already used this code"}, status: 406
{error: "This code is for first time customers only"}, status: 405
```
