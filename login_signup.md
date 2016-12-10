Email Login

```
[POST] `/user/email_login`
{email: 'mangotan.13@gmail.com', password:'mango'}

On success 

{
  id: "ffe7776b-280c-4834-81a3-eb115bcc8659",
  email: "mangotan.13@gmail.com",
  birthdate: "1985-09-07",
  fuzzie_token: "BAhJIilmZmU3Nzc2Yi0yODBjLTQ4MzQtODFhMy1lYjExNWJjYzg2NTkGOgZFVA==--74e80501f40e36164a6784a851ae5a96d768c776"
}
```

Email Signup

```
[POST] `/user/email_register`

{
  first_name: 'Optimus', 
  last_name, 'Prime',
  email: 'optimus@autobots.com' 
  birthdate: '03/05/1985' 
  profile_picture: <image data like in usual file uploads>,
  password: 'kmcdka09',
  password_confirmation: 'kmcdka09',
  phone: '9008298574'
}
```

`birthdate` should be in `mm/dd/yyyy` format.

FB login

```
[POST] /user
X-Facebook-Token: <facebook token>

Response can have 3 different status codes:

1. 200

This indicates successful login and the User object is returned.

2. 226

This indicates that the user is already present in the database, but phone number is absent (old existing users)
User object will be returned with this as well. Show the user a page similar to email signup with details prefilled (without the password) and empty phone number field. Submit this page using the FB register API given below.

3. 202

This indicates that the user is a new one. The user data obtained from Facebook will be returned. Show the user a page similar to email signup with details prefilled (without the password) and empty phone number field. Submit this page using the FB register API given below.
```

FB Signup
```
[POST] /user/facebook_register
Similar to the Email signup API. OTP will be send to the user. 
```

OTP Verification
```
[POST] '/api/phone/6326/verify'

Response: if success then status code of `200` else `404`
```

Forgot Password

```
[POST] '/password/forgot'
params: {email_or_phone: 'pearlychan341@yahoo.com.sg'}

Response: 200 if the email/phone exists in Users database. Else 404. 
```

Update password

```
[PUT] /user/update_password
{
  current_password: 'abcdefg',
  new_password: 'newpassword'
}
