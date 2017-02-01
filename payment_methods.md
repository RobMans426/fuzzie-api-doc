Payment Methods
---------------

Pass X-Fuzzie-Token header for all requests

- Create a new payment method for a user

```
  [POST] /api/payment_methods
  params: {payment_method_nonce: 'abcedfghij'}
```  

- Delete a payment method

```
  [DELETE] /api/payment_methods/:token
````

- List all payment methods for a user

```
  [GET] /api/payment_methods
  
  Response will be an array, each element in the following format: 
    {
			token: '3fdg34', 
			bin: '23213', 
			card_type: 'VISA', 
			cardholder_name: 'Unni', 
			created_at: , 
			expiration_month: '06', 
			expiration_year: '2017', 
			last_4: '4444',
			country_of_issuance: 'Singapore', 
			issuing_bank: 'ICICI', 
			image_url: '',
			default: true
		}
    
`default` will be set to true, if this payment method has been set as the default payment method by the user.     
```

- Set a payment method as default

```
[PUT] /api/payment_methods/set_default
{token: '32df3'}
```

- Fetch a Nonce for a given Token

```
[GET] /api/payment_methods/jjzp3t
Response will a payment method object in the same format as `/api/payment_methods`
```
