By Email
========

Request
-------

```
 [POST] /api/gifts/:gift_id/notify
 
 params: {email: 'unni.tallman@gmail.com'}
 
 also pass the X-FUZZIE-TOKEN header
```

Response
--------

```
200 with 

{
  "message": "Email sent"
}
```
