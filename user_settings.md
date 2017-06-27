User Settings
=============

Updating user settings
----------------------

```
[POST] /api/user_settings

settings: {
  shares_likes_and_wish_list: false,
  activate_push_notifications: true,
  enable_credit_reminders: false,    
  enable_announcements: true,
  display_birthdays_row: true
}
```

The User object (which is returned after a successful login into the app) will contain the saved settings for that user - 

```
"settings": {
  "shares_likes_and_wish_list": false,
  "activate_push_notifications": true,
  "enable_credit_reminders": false,
  "enable_announcements": true,
  "display_birthdays_row": true
}
```

User object can also be fetched using `[GET] /user` passing the `X-FUZZIE-TOKEN` header.
