Promo Code Validation
=====================

```
[GET] /api/promo_codes/MYPROMOCODE/validate
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
1. 406 {error: 'Invlaid Promo Code'}
2. 407 {error: 'Expired or already been used'}
```
