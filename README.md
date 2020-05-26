# Rating-Prediction
COMP4332 Project3
> Wide & Deep Learning for Rating Prediction (Recommendation System)

### Feature Engineering:
1. continuous featues: 
> tr_continuous_features.shape: (60080, 23)

* "user_average_stars", "user_cool", "user_fans", "user_review_count", "user_useful", "user_funny",
"item_is_open", "item_latitude", "item_longitude", "item_review_count", "item_stars",
'user_compliment_hot', 'user_compliment_more', 'user_compliment_profile', 'user_compliment_cute','user_compliment_list',
'user_compliment_note', 'user_compliment_plain', 'user_compliment_cool', 'user_compliment_funny',
'user_compliment_writer', 'user_compliment_photos',
'user_year' (new feature from *user_yelping_since*)
                     

2. item categorical features: 
> tr_deep_categorical_features.shape: (60080, 15)

* "item_city", "item_postal_code", "item_state", 'business_id', 'item_RestaurantsAttire', 'item_WiFi', 'item_Ambience', 'item_NoiseLevel', 'item_BusinessAcceptsCreditCards',  'item_RestaurantsPriceRange2', 'item_GoodForMeal', 'item_BusinessParking', 'item_RestaurantsGoodForGroups' (new featuers from *item_attributes*)

3. user categorical features: 
> tr_deep_categorical_features.shape: (60080, 15)

* "user_id", "user_elite"

4. wide features (item_categories):
> tr_wide_features.shape: (60080, 806)
* all 605 categories
* top 100 2-categories combinantions
* top 60 3-categories combinantions
* top 40 4-categories combinantions

<br>

### Parameters:
* Embedding Size: 32, **50**, 64, 100
* Dropout = **0.0**, 0.1, 0.2, 0.3
* deep components layers: (256, 128, 64), (512, 256, 128), **(128, 64)**, (64, 32)

<br>

### Ensemble
* TRAIN RMSE:  0.9728837378504239; VALID RMSE:  1.0226843085225688

* TRAIN RMSE:  0.977544920488189; VALID RMSE:  1.0252415830075328

* TRAIN RMSE:  0.976045028585581; VALID RMSE:  1.0266512934518501

* TRAIN RMSE:  0.9787179092755424; VALID RMSE:  1.0245971891429382

* TRAIN RMSE:  0.9763686275005208; VALID RMSE:  1.0253317879018073

* Take Mean Value - **VALIDATION RMSE: 1.0210420495271597**
