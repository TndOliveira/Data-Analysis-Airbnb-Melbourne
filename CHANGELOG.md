# Changelog
This file contains the notable changes to the project



# Versão 1.0.0 (10-12-2023)

## New
    - Created data_v2 DataFrame backcup
    - Created a new dataset called "bedrooms_info" to extract values from the column "name" to fill missing values in the "bedroom" column
    - Created two lists to extract specific values from the second and third column in "bedrooms_info" DataFrame
    - Created two variables containing the extracted bedrooms information from the second and third column in bedrooms_info
    - Created a DataFrame called "bedrooms_info_complete" to join the information from the two variables containing the extracted bedrooms information
    - Created data_v3 DataFrame backcup
    - Created data_v4 DataFrame backcup
    
    
## Changes
    - Deleted of  "id", "scrape_id", "last_scraped", "source", 
                  "description", "neighborhood_overview", "picture_url", 
                  "host_id", "host_url", "host_since", "host_location", "host_about",
                  "host_response_time", "host_response_rate", "host_acceptance_rate",
                  "host_is_superhost", "host_thumbnail_url", "host_picture_url", "host_neighbourhood", 
                  "host_listings_count", "host_total_listings_count", "host_verifications",
                  "host_has_profile_pic", "host_identity_verified", "neighbourhood",
                  "neighbourhood_group_cleansed", "property_type", "bathrooms", "maximum_nights", 
                  "minimum_minimum_nights", "maximum_minimum_nights", "minimum_maximum_nights",
                  "maximum_maximum_nights", "minimum_nights_avg_ntm", "maximum_nights_avg_ntm", "calendar_updated", "has_availability", "availability_30", "availability_60", "availability_90", "availability_365", "calendar_last_scraped", "number_of_reviews_ltm", "number_of_reviews_l30d", "first_review", "last_review", "review_scores_accuracy", "review_scores_cleanliness", "review_scores_checkin",
                  "review_scores_communication", "review_scores_location", "review_scores_value", 
                  "license", "instant_bookable", "calculated_host_listings_count",      "calculated_host_listings_count_entire_homes", "calculated_host_listings_count_private_rooms",
                  "calculated_host_listings_count_shared_rooms", "reviews_per_month"
    - Replaced 11 missing values from "bathrooms_text" column with '0 baths'
    - Sorted index from "bedrooms_info_complete"
    - Replaced categorical values in "bedrooms_info_complete" to numeric values
    - Replaced NaN values in "bedrooms" using values from "bedrooms_info_complete"
    - Replaced the rest 22 NaN values in "bedrooms" with 0.0 (Studio)
    - Replaced NaN values in "beds" with the mode, which is 1, where listings are either 1 bedroom or studio and accommodate no more than 2 guests
    - Replaced NaN values in "beds" with specific values
    - Converted "price" column data type to continous data
    - Converted "bedrooms" and "beds" to discrete data
    - Replaced 'Moreland' values in "neighbourhood_cleansed" to 'Merri-bek'
    - Replaced values below $30 in "price" column with the median
    - Replaced one value equals 999 to 2 in the 'minimum_nights' column


## Fixes
    - Removal of 5 missing values in "beds" column
    - Removal of outlier in "beds" column
    - Removal of values above $2000 in "price" column
    - Removal of values above 365 in 'minimum_nights' column

    