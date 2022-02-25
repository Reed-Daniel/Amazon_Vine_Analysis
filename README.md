# Amazon_Vine_Analysis
## Project Overview
In this project we were tasked with analyzing Amazon reviews for a specific category of products (Video Games) written by members of the paid Amazon Vine program which allows manufacturers and publishers to receive reviews for their products. We used PySpark, AWS, and pgAdmin to perform the ETL process on our dataset in an effort to determine if there is any bias toward favorable reviews from Vine members.

## Resources
- Data Source: [Amazon Review datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt), [Video Games Review dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz)
- Software: Google Colab Notebook, PostgreSQL, pgAdmin 4, AWS

## Results
### Deliverable 1: Perform ETL on Amazon Product Reviews
**Extracted a review dataset and transformed it into 4 DataFrames**
- Customers Table DataFrame 
<img width="271" alt="customers_table" src="https://user-images.githubusercontent.com/93271297/155754651-dd9f1420-b489-4b97-9595-92a7f70cfe25.png">

- Products Table DataFrame
<img width="486" alt="products_table" src="https://user-images.githubusercontent.com/93271297/155754996-b274c3b4-c6ae-4ca8-8374-6629672da44d.png">

- Review ID Table DataFrame
<img width="595" alt="review_id_table" src="https://user-images.githubusercontent.com/93271297/155755639-3518f35b-61f0-4a28-a656-7d9d55e5c0fb.png">

- Vine Table DataFrame

<img width="595" alt="vine_table" src="https://user-images.githubusercontent.com/93271297/155755651-1006b87f-ce9b-4e39-8229-684fa46daf05.png">

### Deliverable 2: Determine Bias of Vine Reviews
#### Total Reviews
- Vine Reviews
<img width="353" alt="vine_total" src="https://user-images.githubusercontent.com/93271297/155760747-86b576a4-6099-4ec9-aa3f-fb1ad25d1450.png">

- Non-Vine Reviews
<img width="382" alt="NonVine_total" src="https://user-images.githubusercontent.com/93271297/155760769-6d4b4880-6f20-4291-94e6-3df295f3ef69.png">

#### Total number of 5-star reviews
- Vine Reviews 
<img width="657" alt="Vine_Review" src="https://user-images.githubusercontent.com/93271297/155759013-b3e27caa-c20c-41e6-a242-9683906282d1.png">


- Non-Vine Reviews 
<img width="711" alt="Non-Vine_Review" src="https://user-images.githubusercontent.com/93271297/155759143-5ed0ed30-54a4-499b-a8f9-b7ae4a4f74eb.png">

### Percentage of 5-star reviews
- Vine Reviews
<img width="691" alt="Vine_percentage" src="https://user-images.githubusercontent.com/93271297/155759671-939ff0ee-e1bd-4d64-bf0f-80527562d0aa.png">


- Non-Vine Reviews
<img width="739" alt="Non-Vine_percentage" src="https://user-images.githubusercontent.com/93271297/155759693-7a3db64e-fc71-494c-b18d-169ec9efc6a5.png">

## Summary
Out of the total quantity of video game reviews from the Vine program, a little more than half (**51%**) were 5-star reviews. Out of the total of Non-Vine reviews, a little more than a third (**39%**) were 5-star reviews. This stark contrast between the Non-Vine and Vine 5-star ratings alludes to a positive bias for reviews in the Vine program. An additional analysis on the dataset that could further our understanding of this bias would be to determine the statistical distribution (mean, median and mode) of all star ratings for the Vine and Nonn-Vine reviews.
