All the requests need authentication. Send `X-Fuzzie-Token`

Create a new Payment Method
---------------------------

```
POST /api/payment_methods
params: {payment_method_nonce=aa9c4061-2c57-4d08-9f03-3d171af5587e}
```

Get the list of saved Payment Methods
-------------------------------------

```
GET /api/payment_methods 
```

Delete a saved Payment Method
-----------------------------

```
DELETE /api/payment_methods/:token
```
