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
