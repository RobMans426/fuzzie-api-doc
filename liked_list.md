LikedList
========

*Pass X-Fuzzie-Token with all the Likedlist API calls.*

Get a user's Liked List
----------------------

```
[GET] /api/v2/liked_brands/:user_id
```

Get the current user's liked list
--------------------------------

```
[GET] /api/v2/liked_brands/me
```

Response
--------

```
[
  "brand_id_1",
  "brand_id_2",
  "brand_id_3"
]
```


Add an item to the current user's liked list
-------------------------------------------

```
[PUT] /api/wish_list/:brand_id
```

Remove an item from the current user's liked list
------------------------------------------------

```
[DELETE] /api/wish_list/:brand_id
```

Home API

`likers_count` added to Brand object.
