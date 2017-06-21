To link a gift to a Fuzzie User's GiftBox
=========================================

Request
-------

```
[POST] /api/gifts/:gift_id/add_to_gift_box

Pass X-FUZZIE-TOKEN header.
```

Response
--------

Success

```
{message: 'Gift added to GiftBox'} with 200
```

Failure

```
{message: 'This gift has already been claimed'} with 401
```
