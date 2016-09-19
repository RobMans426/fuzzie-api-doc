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

FB login/signup

```
[POST] /user
X-Facebook-Token: <facebook token>
```

OTP (this won’t send any SMS verification as of now)
```
[POST] '/phone/9008298574/verify'

Response: {otp: '4569'}
```
