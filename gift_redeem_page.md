To get all the details needed on the gift redeem page, the below end point cam be used: 

```
[GET] /gifts/:id/details
with X-Fuzzie-Token

Response will be a gift object.
```

The Gift object will have a boolean called `online`. This will indicate if the gift is to be redeemed at a Fuzzie store or a third party store.
If its a fuzzie store, then we have to show the interface for entering a store pin. If its a online (third party) store, then we just need to 
display the `third_party_code` to the the user. Also a button to go the third party website from where the user can redeem it. Link to this site will
be available at `external_redeem_page`. 

There will also be `logo` and `redeem_instructions`.
