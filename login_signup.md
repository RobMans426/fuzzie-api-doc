1. Email Login

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

2. Email Signup

```
[POST] `/user/email_register`

{
  first_name: 'Optimus', 
  last_name, 'Prime',
  email: 'optimus@autobots.com' 
  birthdate: '05-03-1985' 
  profile_picture: <image data like in usual file uploads>
}
```

3. OTP (this won’t send any SMS verification as of now)
```
[POST] '/phone/9008298574/verify'

Response: {otp: '4569'}
```
