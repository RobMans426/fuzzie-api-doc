Mini Banners
============

A `mini_banners`key is present in the Home API (`/api/home`). It is an array of MiniBanner objects. 

MiniBanner Object
-----------------

```
{
  "id": 6,
  "banner_type": "Referral Page",
  "header": "",
  "sub_header": "",
  "image": "URL",
  "link": "",
  "story_id": null,
  "brand_id": "a5dcabac-f4d9-432e-bd23-03e425849fcc",
  "power_up_campaign_id": null,
  "brand_ids": [],
  "sequence": 0,
  "general_page": null,
  "position": 6,
  "locations": [
    "home_page",
    "brand_page"
  ],
  "container_brand_id": null
}
```
Refer to the main Banner implementation on the app for the different types of banners and where each of them should be linked. 
Mini banner follows the same format as of Banner in this respect. 

Placement of mini banner
------------------------

Check the `locations` key.

1. `home_page`: Place the mini banner on the Home page. Also check the `position` key to determine where on the home page
the mini banner should be placed. If 2 or more mini banners have the same value for `position`, thn their order of placement
should be determined using the `sequence` key.

2. `brand_page`: Place the mini banner on all the brand pages. Check for `container_brand_id` key. If it is not null
and contains a brand ID, then place this mini banner only on this specific brand's page. 

3. `payment_page`: Pick all mini banners that have `payment_page` in `locations` and place them in a slider 

```
"mini_banner_locations": [
  "home_page",
  "brand_page",
  "payment_page"
]

"mini_banner_positions": {
    "0": "Above recommended brands",
    "1": "Above trending brands",
    "2": "Above new brands",
    "3": "Above top brands",
    "4": "Above categories"
  }
```
