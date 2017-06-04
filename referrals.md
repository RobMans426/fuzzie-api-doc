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
      "status": "signed_up",
      "id": "afb24ef7-328f-44b0-b861-723170aa75a8",
      "email": "hello@mail.com",
      "avatar": "https://d3mytoddva16m1.cloudfront.net/users/profile_pictures/afb/24e/f7-/standard/b646035d-ed5b-46b8-b57c-617235df6065.jpeg?1495739011",
      "birthdate": null,
      "gender": null,
      "first_name": "Tester45",
      "last_name": "Hello",
      "name": "Tester45 Hello"
    }
  ]
}

status can be either 'signed_up' or 'purchased'
```

