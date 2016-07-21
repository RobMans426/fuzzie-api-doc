Loyalty Programmes
------------------

1. Get the list of loyalty programmes

Request

`[GET] /api/loyalty_programmes`

Response

```
[
  {
    name: 'Capistar'
    points_per_dollar: 3
  },

  {
    name: 'Passion'
    points_per_dollar: 1
  }
]

```


2. Link a user account to one or more loyalty programmes

Request

`[POST] /api/loyalty_programmes/link`

Params

```
{
  number: '827DB2N71',
  loyalty_programme_ids: [1,2,3]
}
```

Response: 200

