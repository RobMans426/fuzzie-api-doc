Mark a received gift as opened
==============================

`[PUT] /api/gifts/:gift-id/mark_received_gift_as_opened`

Response
--------

200 with 

```
{
    "message": "Gift marked as opened"
}
```

Mark a received gift as unredeemed
==================================

`[PUT] /api/gifts/:gift-id/mark_as_unredeemed`

Response
--------

200 with 

```
{
    "message": "Gift marked as opened"
}
```

or 

401 with 

```
{message: 'Only online gifts can be marked as unredeemed'}
```

Get unopened gifts count for a User
===================================

`[GET] /api/gifts/upopened_gifts_count`

Pass the header `X-FUZZIE-TOKEN`

Response
--------

```
{
    "upopened_gifts_count": 1
}
```
