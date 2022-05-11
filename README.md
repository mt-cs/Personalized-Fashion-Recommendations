# H&M Personalized Fashion Recommendations
H&amp;M Personalized Fashion Recommendations

Source: Kaggle [H&M Personalized Fashion Recommendations](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/overview)
Data source: Kaggle [Data](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/data)

![header](<img width="468" alt="Screen Shot 2022-05-11 at 12 31 52 PM" src="https://user-images.githubusercontent.com/60201466/167930921-e34c478c-4d18-498b-994e-19584ce2a995.png">
)

Team: [Firoozeh Kaveh](https://github.com/fika005) | [Marisa Tania](https://github.com/mt-cs) | [Ryan Tjakrakartadinata](https://github.com/tjakrak) 


## 📂 Files

👗 articles_EDA.ipynb: EDA for articles dataset

👥 customers.ipynb: EDA for customers dataset

🧾 transaction_train_EDA.ipynb: EDA for transactions dataset

⚙️ feature_engineering.ipynb: Feature engineering, model, result

## ✨ Project Overview

Given the purchase history of customers over time, along with supporting metadata, we want to predict what products each customer will purchase in the 7-day period immediately after the training data ends.

## 🌻 Motivation

Online stores offer shoppers an extensive selection of products to browse through, which is often overwhelming. To enhance the shopping experience, product recommendations are key. Not merely to drive sales, but also to reduce returns, and thereby minimizes emissions from transportation.

## 🗂 Dataset

### articles.csv
Unique indentifier of an article:
- article_id (int64) - an unique 9-digit identifier of the article, 105 542 unique values (as the length of the database)

5 product related columns:
- product_code (int64) - 6-digit product code (the first 6 digits of article_id, 47 224 unique values
- prod_name (object) - name of a product, 45 875 unique values
- product_type_no (int64) - product type number, 131 unique values
- product_type_name (object) - name of a product type, equivalent of product_type_no
- product_group_name (object) - name of a product group, in total 19 groups

2 columns related to the pattern:
- graphical_appearance_no (int64) - code of a pattern, 30 unique values
- graphical_appearance_name (object) - name of a pattern, 30 unique values

2 columns related to the color:
- colour_group_code (int64) - code of a color, 50 unique values
- colour_group_name (object) - name of a color, 50 unique values

4 columns related to perceived colour (general tone):
- perceived_colour_value_id - perceived color id, 8 unique values
- perceived_colour_value_name - perceived color name, 8 unique values
- perceived_colour_master_id - perceived master color id, 20 unique values
- perceived_colour_master_name - perceived master color name, 20 unique values

2 columns related to the department:
- department_no - department number, 299 unique values
- department_name - department name, 299 unique values

4 columns related to the index, which is actually a top-level category:
- index_code - index code, 10 unique values
- index_name - index name, 10 unique values
- index_group_no - index group code, 5 unique values
- index_group_name - index group code, 5 unique values

2 columns related to the section:
- section_no - section number, 56 unique values
- section_name - section name, 56 unique values

2 columns related to the garment group:
- garment_group_n - section number, 56 unique values
- garment_group_name - section name, 56 unique values

1 column with a detailed description of the article:
- detail_desc - 43 404 unique values

### customers.csv
Unique indentifier of a customer:
- customer_id - an unique identifier of the customer

5 product related columns:
- FN - binary feature (1 or NaN)
- Active - binary feature (1 or NaN)
- club_member_status - status in a club, 3 unique values
- fashion_news_frequency - frequency of sending communication to the customer, 4 unique values
- age - age of the customer
- postal_code - postal code (anonimized), 352 899 unique values
 
### transactions_train.csv
The transaction dataset is the largest database containing everyday transactions in two years period. It contains 31788324 rows × 5 columns:
- t_dat : Date of a transaction in format YYYY-MM-DD but provided as a string.
- customer_id : A unique identifier of every customer (mapped to the customer_id in customers table)
- article_id : A unique identifier of every article (mapped to the article_id in articles table)
- price : Price of purchase
- sales_channel_id : sales channel 1 or 2

