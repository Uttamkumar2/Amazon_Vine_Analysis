# Amazon_Vine_Analysis
## Overview of the analysis

The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. 

I have used Amazon video games review data set, to determine if there is a bias toward favorable reviews from Vine member.

The analysis uses Amazons video games review data stored in S3 Bucket, Using PySpark to read and perform ETL to Extract dataset, transform and loaded data in Amazons RDS Postgres Relational Database using PgAdmin and calculated different statics of data.

## Resource 

* Data Source [Amazon Customer Review](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt), [Video Games Review dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz)
* Software Google Colab Notebook, PostgreSQL 12.9, PGAdmin 4, AWS.

## Process
   
* Below are sample data which was read and transfomed before loading to Relational Database...
*   Customer Dataframe 

     ![customer_df_output](https://user-images.githubusercontent.com/91766890/152720600-82f732ce-2699-4511-bc65-1a390c221490.PNG)
*   Product Dataframe

     ![product_df_output](https://user-images.githubusercontent.com/91766890/152720634-1b2eed3e-c966-4360-ac7a-2204f834053a.PNG)
*   Review Dataframe

     ![review_df_output](https://user-images.githubusercontent.com/91766890/152720668-eff1a73c-6c9b-4f91-957e-5ac4dbd5d1c9.PNG)

* After readhing and transforming csv file data was loaded to All 4 table data coount after load into AWS RDS Postgres   
  *   CUSTOMERS_TABLE
  *   PRODUCTS_TABLE
  *   VINE_TABLE
  *   REVIEW_ID_TABLE
    
    ![Loaded_tablesCount](https://user-images.githubusercontent.com/91766890/152720228-750381fd-6ff3-43c3-9224-b42fc220792a.PNG)
## Results
  * As it required to determine the total number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews for the two types of review (paid vs unpaid), here are the results say's stastics of the given requirement.
    ![deliverable2_output](https://user-images.githubusercontent.com/91766890/152721686-1c54b9b9-c10e-40c8-b808-ca9793f98457.PNG)
## Summary
  51.06% of review in Vine Program were 5 Star review where as it was 38.97% of non-paid review was 5 star.  This describes a positivity bias for reviews in the Vine program.

