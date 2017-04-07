Home
----

```
/api/home
```

This API endpoint provides the client app with almost all of the data that it needs. It includes

- brands
- banners
- upcoming_birthdays
- friends
- categories
- sub_categories
- recommended_brands
- popular_brands
- near_brands
- hottest_brands
- most_wish_listed_brands
- most_cash_back_brands
- stories
- mini_banners
- min_banner_positions
- top_brands
- new_brands

```
[GET] /home

X-Fuzzie-Token - optional. If called without it, it won't contain the user specific data like `friends`. 
```
