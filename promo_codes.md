Promo Code Validation
=====================

Request
-------

```
[GET] /api/promo_codes/MYPROMOCODE/validate
```

Optional params

```
{
  payment_method_token: 'abcdef',
}
```

Response
--------

Success:

```
{
  code: MYPROMOCODE
  cash_back_percentage: 10
}
```

Failure:

```
1. 411 {error: 'Invlaid Promo Code'}
2. 412 {error: 'Expired or already been used'}
```
