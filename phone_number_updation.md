Phone number Updation
---------------------

Send X-Fuzzie-Token with the request.

```
POST '/api/phone/:new_number/update'
```

This will send an OTP to the new number.


New Phone number verification
-----------------------------

```
POST '/api/phone/:otp/verify_new_number'
```

If the OTP is verified successfully, then user's phone number will be updated with the new one.
