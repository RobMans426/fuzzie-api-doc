Bank Accounts Management
------------------------

All requests are authenticated. Send `Fuzzie-Token`

- Get the list of all Bank accounts of a user

```
GET /api/bank_accounts
```

- Create a new Bank Account

```
POST /api/bank_accounts
{
  bank_name: 'ICICI'
  account_name: 'Ravindra'
  account_number: '32423432432'
}
```

- Edit a Bank Account

```
[PUT] /api/bank_accounts/4
{
  bank_name: 'HDFC'
  account_name: 'Ravindra'
  account_number: '32423432432'
}

```

_________________________________________________________________________________

CashOut Requests
----------------

- Get the list of active cash out requests of a user.

```
GET /api/cash_out_requests
```
- Create a new CashOutRequest
```
POST /api/cash_out_requests
{
  amount: 350,
  bank_account_id: 10
}
```

- Cancel a CashOutRequest
```
DELETE /api/cash_out_requests/12
```

