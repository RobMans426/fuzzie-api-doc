Gift It
-------

Use the same [API call that is used to buy a single gift](https://github.com/fuzziegang/fuzzie-api-doc/blob/master/payment.md). 

Additional Parameters
---------------------

1. `gifted` - set this as `true`
2. `friend_name` - Name of the person to whom the gift is sent.
3. `friend_id` (optional) - Facebook ID of the friend. 
4. `message` - Message to be sent to the person along with the gift. 

Notes
-----

- The API response now has a `gift` key which contains the Gift object. 
- The Gift object contains as `gift_url` key
