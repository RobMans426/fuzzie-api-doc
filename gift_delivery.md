By Email
========

Request
-------

```
 [POST] /api/gifts/:gift_id/notify
 
 params: {email: 'unni.tallman@gmail.com'}
 
 Optional params:
 
 {copy_to_self: "true"}
 
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
