Friends
=======

Fuzzie Friends
--------------

`[GET] /api/friends/fuzzie`  with `X-FUZZIE-TOKEN`

Response will be an array, with each element of the format: 

```
{
    "id": "372c7293-0382-4dc5-8f13-171023ef4440",
    "email": "ershad92@gmail.com",
    "avatar": "https://graph.facebook.com/10201186540182627/picture?width=400&height=400",
    "birthdate": "1992-03-18",
    "gender": "m",
    "first_name": "Ershad",
    "last_name": "Kunnakkadan",
    "name": "Ershad Kunnakkadan"
  }
```

Facebook Friends
----------------

`[GET] /api/friends/facebook`  with `X-FUZZIE-TOKEN`

Response will be an array, with each element of the format: 

```
{
  "name": "Charles Josh",
  "avatar": "https://scontent.xx.fbcdn.net/v/t1.0-1/1912447_10152268817301974_653943558_n.jpg?oh=417bf82e5d8bef9f2097567dd49a34f7&oe=59D70B33"
}
```
