Checkout
--------

```
[POST] /api/shopping_bag
```

Success

```
{ 
  type: 'ShoppingBag', 
  cash_back: 25, 
  number_of_gifts: 3,
  bought_for_self: true
}
```

Failure (all the below responses will have a `message` field)

```
401: Blocked user
422: Payment Failure
406: Sold out OR Daily/Weekly limit reached
```

Add/Remove/List
---------------

```
  [POST]    /api/shopping_bag/add    {id: gift-card or service ID}
  [DELETE]  /api/shopping_bag/remove {id: gift-card or service ID}
  [GET]     /api/shopping_bag/items
```
