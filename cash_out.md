Bank Accounts Management
------------------------

All requests are authenticated. Send `Fuzzie-Token`

1. Get the list of all Bank accounts of a user

```
GET /api/bank_accounts
```

2. Create a new Bank Account

```
POST /api/bank_accounts
{
  bank_name: 'ICICI'
  account_name: 'Ravindra'
  account_number: '32423432432'
}
```

3. Edit a Bank Account

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

1. Get the list of active cash out requests of a user.

```
GET /api/cash_out_requests
```

2. Create a new CashOutRequest
```
POST /api/cash_out_requests
{
  amount: 350,
  bank_account_id: 10
}
```

3. Cancel a CashOutRequest
```
DELETE /api/cash_out_requests/12
```

