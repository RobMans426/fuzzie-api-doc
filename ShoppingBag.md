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
  [POST]    /api/shopping_bag/add    {ids: gift-card or service IDs, separated by comma}
  [DELETE]  /api/shopping_bag/remove {ids: gift-card or service IDs, separated by comma}
  [GET]     /api/shopping_bag/items
  
  Example: 
  
  [POST]   /api/shopping_bag/add?ids=7b061eca,f6cce788
  [DELETE] /api/shopping_bag/remove?ids=7b061eca,f6cce788
```
