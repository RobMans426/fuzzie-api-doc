CashBack Summary
================

1. Single Gift
--------------

[GET] /api/cashback_summary/:gift_card_type

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
  [GET] /api/cashback_summary/shopping_bag
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
      gift_card_type: 'asbc123',
      price: 50,
      cash_back: {
        percentage: 10,
        value: 5
      }
    },

    {
      gift_card_type: 'xyz123',
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
  
  campaigns: [
    {
      title: "DCB Diners Choice", 
      cash_back: {
        percentage: 3,
        value: 7
      } 
    },
    
    {
      title: "Visa Card CashBack", 
      cash_back: {
        percentage: 5,
        value: 12
      } 
    }
  ]
}
```
