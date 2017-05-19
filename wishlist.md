WishList
========

*Pass X-Fuzzie-Token with all the Wishlist API calls.*

Get a user's wish list
----------------------

```
[GET] /api/v2/wish_listed_brands/:user_id
```

Get the current user's wish list
--------------------------------

```
[GET] /api/v2/wish_listed_brands/me
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


Add an item to the current user's wish list
-------------------------------------------

```
[PUT] /api/wish_list/:brand_id
```

Remove an item from the current user's wish list
------------------------------------------------

```
[DELETE] /api/wish_list/:brand_id
```

Home API

`wish_listers_count` added to Brand object.
