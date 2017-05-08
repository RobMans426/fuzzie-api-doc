CashBack Summary
================

1. Single Gift
--------------

[GET] /api/gifts/:gift_template_id/cashback_summary

Pass X-FUZZIE-TOKEN

optional params: 
```
{
  payment_method_token: 'abcdef',
  promo_code: 'MYPROMOCODE'  
}
```
2. Shopping Bag
---------------

```
  [GET] /api/shopping_bag/cashback_summary
```

Pass X-FUZZIE-TOKEN

optional params: 
```
{
  payment_method_token: 'abcdef',
  promo_code: 'MYPROMOCODE'  
}
```

Response
--------

```
{
  gifts: [
    {
      gift_template_id: 'asbc123',
      price: 50,
      cash_back: {
        percentage: 10,
        value: 5
      }
    },

    {
      gift_template_id: 'xyz123',
      price: 200
      cash_back: {
        percentage: 20,
        value: 40
      }
    },

  ],

  promo_code: {
    code: 'MYPROMOCODE',
    cash_back: {
      percentage: 10,
      value: 25
    }
  },

  campaigns: {
    title: 'DBC Camapign',
    cash_back: {
      percentage: 5,
      value: 12
    }
  },

  total: {
    price: 250,
    cashback: 82
  }
}
```
