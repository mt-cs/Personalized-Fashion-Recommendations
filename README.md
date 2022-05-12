# H&M Personalized Fashion Recommendations Machine Learning Project

![header](https://user-images.githubusercontent.com/60201466/167953233-53ce9848-5da5-481b-a14d-270c794255d1.jpg)

Source: Kaggle [H&M Personalized Fashion Recommendations](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/overview)

Data source: Kaggle [Data](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/data)

Null Team: [Firoozeh Kaveh](https://github.com/fika005) | [Marisa Tania](https://github.com/mt-cs) | [Ryan Tjakrakartadinata](https://github.com/tjakrak) 

## 📂 Files

👗 articles_EDA.ipynb: EDA for articles dataset

👥 customers.ipynb: EDA for customers dataset

🧾 transaction_train_EDA.ipynb: EDA for transactions dataset

⚙️ feature_engineering.ipynb: Feature engineering, model, result

---

<a href="https://youtu.be/-VX6G6C-xPk" title="H&M Personalized Fashion Recommendations"><img src="https://user-images.githubusercontent.com/60201466/167955862-9c911516-c1cb-46fa-8c51-7d807c3fae26.jpg" width="650"></a>

### ✨ Project Overview

Given the purchase history of customers over time, along with supporting metadata, we want to predict what products each customer will purchase in the 7-day period immediately after the training data ends.

## 🌻 Motivation

Online stores offer shoppers an extensive selection of products to browse through, which is often overwhelming. To enhance the shopping experience, product recommendations are key. Not merely to drive sales, but also to reduce returns, and thereby minimizes emissions from transportation.

## 🧠 Model & Result

#### Bagging Classifier
- Accuracy score = 78 %
- Execution time = 2.06 s per test datapoint

#### Light GBM
- Accuracy score = 80 %
- Execution time = 670 ms per test datapoint

#### Neural Network
- Accuracy score = 77 %
- Execution time = 5.5 ms per test datapoint

## ✅ Submission
The final submission is consisted of 12 articles recommendations for each customer in the dataset.

_5 first row of submission:_
| customer_id | articles_id|
| --- | --- |
|00000dbacae5abe5e238 <br/> 85899a1fa44253a17956 <br/> c6d1c3d25f88aa139f <br/> dfc657| 0637847001 0786925004 0607884001 0681002002 <br/> 0719628001 0732017002 0579541004 0579541001 <br/> 0579541036 0841565001 0732017001 0920448002|
|0000423b00ade91418cc <br/> eaf3b26c6af3dd342b51 <br/> fd051eec9c12fb3698 <br/> 4420fa| 0719628001 0607884001 0841565001 0732017001 <br/> 0732017002 0637847001 0681002002 0920448001 <br/> 0920448002 0579541001 0579541004 0579541036|
|000058a12d5b43e67d22 <br/> 5668fa1f8d618c13dc23 <br/> 2df0cad8ffe7ad4a10 <br/> 91e318| 0902802001 0815434001 0852584001 0906576001 <br/> 0503095001 0926564001 0920610002 0906125001 <br/> 0661735001 0793443002 0793443004 0747854001|
|00005ca1c9ed5f5146b5 <br/> 2ac8639a40ca9d57aeff <br/> 4d1bd2c5feb1ca5dff0 <br/> 7c43e| 0902802001 0906576001 0815434001 0852584001 <br/> 0804992017 0927131002 0849886001 0865086003 <br/> 0757303014 0757303013 0678687013 0849886002|
|00006413d8573cd20ed7 <br/> 128e53b7b13819fe5cfc2 <br/> d801fe7fc0f26dd8d6 <br/> 5a85a| 0815434001 0852584001 0906576001 0902802001 <br/> 0804992017 0927131002 0592098003 0741409003 <br/> 0817554001 0730685001 0561066001 0735583001|

## 🗂 Dataset
We use three datasets in this project:

#### 1. transactions_train.csv
The transaction dataset is the largest database containing everyday transactions in two years period. It contains 31788324 rows × 5 columns:
- t_dat - Date of a transaction in format YYYY-MM-DD but provided as a string.
- customer_id - A unique identifier of every customer (mapped to the customer_id in customers table)
- article_id - A unique identifier of every article (mapped to the article_id in articles table)
- price - Price of purchase
- sales_channel_id - sales channel 1 or 2

#### 2. customers.csv
Unique indentifier of a customer:
- customer_id - an unique identifier of the customer

5 product related columns:
- FN - binary feature (1 or NaN)
- Active - binary feature (1 or NaN)
- club_member_status - status in a club, 3 unique values
- fashion_news_frequency - frequency of sending communication to the customer, 4 unique values
- age - age of the customer
- postal_code - postal code (anonimized), 352 899 unique values
 
#### 3. articles.csv
Unique indentifier of an article:
- article_id (int64) - an unique 9-digit identifier of the article, 105542 unique values (as the length of the database)

Columns related to the pattern, color, perceived colour (general tone), department, index, section, garment group, and detailed description:
- product_code (int64) - 6-digit product code (the first 6 digits of article_id, 47224 unique values)
- prod_name (object) - name of a product, 45875 unique values
- product_type_no (int64) - product type number, 131 unique values
- product_type_name (object) - name of a product type, equivalent of product_type_no
- product_group_name (object) - name of a product group, in total 19 groups
- graphical_appearance_no (int64) - code of a pattern, 30 unique values
- graphical_appearance_name (object) - name of a pattern, 30 unique values
- colour_group_code (int64) - code of a color, 50 unique values
- colour_group_name (object) - name of a color, 50 unique values
- perceived_colour_value_id - perceived color id, 8 unique values
- perceived_colour_value_name - perceived color name, 8 unique values
- perceived_colour_master_id - perceived master color id, 20 unique values
- perceived_colour_master_name - perceived master color name, 20 unique values
- department_no - department number, 299 unique values
- department_name - department name, 299 unique values
- index_code - index code, 10 unique values
- index_name - index name, 10 unique values
- index_group_no - index group code, 5 unique values
- index_group_name - index group code, 5 unique values
- section_no - section number, 56 unique values
- section_name - section name, 56 unique values
- garment_group_n - section number, 56 unique values
- garment_group_name - section name, 56 unique values
- detail_desc - 43404 unique values

