Likers
------

We are going to have 2 separate lists of every user:

1. Wish List
2. Liked brands list.

API 
---

1. Add/remove brands and list the liked list

```
[PUT]    http://localhost:3000/liked_list/41976500-f380-4ead-8f7b-a70651ac820b
[DELETE] http://localhost:3000/liked_list/41976500-f380-4ead-8f7b-a70651ac820b
[GET]    http://localhost:3000/liked_list
```

2. Changes in the Home API

- `liked_list_ids` added in User object, similar to `wish_list_ids`
- `likers` have been added in the Brand object, similar to `wish_listers` (array of User objects)

Note: Once these changes are deployed, the present wish-list will be converted to the liked list and the wishlist for all users will go empty.
