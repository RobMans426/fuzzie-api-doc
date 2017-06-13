Linking an existing Fuzzie Account to a Facebook Account
========================================================

Request
-------

```
[POST] /api/accounts/link

X-FUZZIE-TOKEN: 'fuzzie-token'
X-FACEBOOK-TOKEN: 'facebook-token'

```

Response
--------

An array of `friends` sorted by their birthdays

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
