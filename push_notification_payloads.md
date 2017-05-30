Push Notification Payload (both iOS and Android)
------------------------------------------------

Payload will contain a dictionary called `data`. 

A sample:
```
{
  redirect_to: 'wishlist',
  user_id: '12123'
}
```

`redirect_to` is the page in the app, to which the notification has to be linked to. `user_id` is the data required for this linking. 

Given below are the various `redirect_to` values used in the pushes so far. 

```
1. 
{
  redirect_to: 'wishlist',
  user_id: '12123'
}

2. {redirect_to: 'home'}
3. {redirect_to: 'giftbox'}
4. {redirect_to: 'referrals'}
```
