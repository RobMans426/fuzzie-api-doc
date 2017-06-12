Updating an logged in user's password
=====================================

Request
-------

```
[PUT] /user/update_password

{"current_password"=>"bear6578", "new_password"=>"bear1234"}
```

Success
-------

`200 with {message: 'Password updated'}`

Failure
-------

`401 with {message: 'Current password is wrong'}`
