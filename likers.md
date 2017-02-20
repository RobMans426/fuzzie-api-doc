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

2. Home API

- `likers_count` added in User object
