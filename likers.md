Likers (Heart icon)
------

We are going to have 2 separate lists of every user:

1. Wish List
2. Liked brands list.

API 
---

Add/remove brands and list the liked list

```
[PUT]    /liked_list/41976500-f380-4ead-8f7b-a70651ac820b
[DELETE] /liked_list/41976500-f380-4ead-8f7b-a70651ac820b
[GET]    /liked_list
```

Home API

- `likers_count` added in Brand object

Likers for a brand
------------------

```
/api/brands/:brand_id/likers
```

Response: Will be an array of liker objects. 

```
[
  {
    "id": "6441b74b-94d4-48eb-86b7-365b9427a75c",
    "avatar": "http://graph.facebook.com/10154432774204156/picture?width=400&height=400",
    "email": "rahulmax@gmail.com",
    "birthdate": "1983-12-18",
    "gender": "m",
    "first_name": "Rahul",
    "last_name": "Hareendran",
    "name": "Rahul Hareendran",
    "app_version": null,
    "app_platform": null,
    "bonus_awarded_for_referer": false,
    "power_up_code_gifted": false,
    "friend": true
  },
  {
    "id": "d2a89be8-bf07-465e-8438-a7dff93c9106",
    "avatar": "http://graph.facebook.com/10207679198764247/picture?width=400&height=400",
    "email": "dipu.kherudkar@gmail.com",
    "birthdate": "1982-03-26",
    "gender": "f",
    "first_name": "Deepali",
    "last_name": "Kherudkar",
    "name": "Deepali Kherudkar",
    "app_version": null,
    "app_platform": null,
    "bonus_awarded_for_referer": false,
    "power_up_code_gifted": false,
    "friend": true
  }
```

