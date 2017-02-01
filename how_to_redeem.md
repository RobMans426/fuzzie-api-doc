How to Redeem
=============

The `/home` API has two new keys - `how_to_redeem_online_brands` and `how_to_redeem_offline_brands`. 
Depending on the type of the brand choose one of these. But before picking from these, check for a `how_to_redeem` key within 
the brand object. If it is present, pick it from there, else from the keys mentioned above. This is to allow admin to override 
the default redeem steps for a few brands on a case to case basis.

Format of the How To Redeem object
----------------------------------

It will be an array of objects of the format

[
  {
    title: 'Step 1',
    body: 'A paragraph usually',
    image: 'this is optional - can be an image url or null'
  }
]
