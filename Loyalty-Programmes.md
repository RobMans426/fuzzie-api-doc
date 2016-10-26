Loyalty Programmes
==================

Note: All the calls are authenticaed. Send `X-Fuzzie-Token`


Add/Edit Citizen Number of a user
---------------------------------

Request

`[PUT] /api/loyalty_programmes/user`

Params


{
  number: 1232432
}


Response: 200

____________________________

Get the list of loyalty programmes
----------------------------------

Request

`[GET] /api/loyalty_programmes`

Response


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



____________________________

Get the list of loyalty programmes for the current user
-------------------------------------------------------

Request

`[GET] /api/loyalty_programmes/user`

____________________________


Link a user account to a loyalty programme
------------------------------------------
Request

`[POST] /api/loyalty_programmes/link`

Params


{
  id: 12
}


Response: 200

____________________________

Unlink a user from a  loyalty programme
---------------------------------------
Request

`[DELETE] /api/loyalty_programmes/unlink`

Params


{
  id: 12
}


Response: 200
