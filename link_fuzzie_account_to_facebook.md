Linking an existing Fuzzie Account to a Facebook Account
========================================================

```
[POST] /api/accounts/link

X-FUZZIE-TOKEN: 'fuzzie-token'
X-FACEBOOK-TOKEN: 'facebook-token'

```

Response
--------

An array of `fuzzie friends` sorted by their birthdays

```
[
  {
    "birthdate": "1985-01-07",
    "id": "687ac36b-74ce-491c-a592-5fcc0bc3bb0a",
    "email": "bastion53@yahoo.com.sg",
    "avatar": "https://graph.facebook.com/100007614606520/picture?width=400&height=400",
    "gender": "m",
    "first_name": "Johnny",
    "last_name": "Good",
    "name": "Johnny Good"
  },
  {
    "birthdate": "1985-01-10",
    "id": "dd5843ab-a393-49d4-aa7a-3e65c1cf197c",
    "email": "bastion53@yahoo.com.sg",
    "avatar": "https://graph.facebook.com/100001771043148/picture?width=400&height=400",
    "gender": "m",
    "first_name": "Farhan",
    "last_name": "Noor",
    "name": "Farhan Noor"
  }
]
```

OR

```
[POST] /api/accounts/connect

X-FUZZIE-TOKEN: 'fuzzie-token'
X-FACEBOOK-TOKEN: 'facebook-token'

```

Response
--------

An array of `facebook friends`

```
[
  {
      "name": "Karel Vacek",
      "avatar": "https://scontent.xx.fbcdn.net/v/t1.0-1/p200x200/17554315_423197204696260_515488409821016044_n.jpg?oh=8149e32d79a22bd49e20022c9c0a5517&oe=599B9170"
  },
  {
      "name": "Julian Bruneau",
      "avatar": "https://scontent.xx.fbcdn.net/v/t1.0-1/p200x200/17342619_10155929763521982_9221143969814060905_n.jpg?oh=500eaa4609ea20588bf430582c4313b7&oe=59E402BF"
  }
]
```
