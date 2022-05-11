# H&M Personalized Fashion Recommendations
H&amp;M Personalized Fashion Recommendations

Source: Kaggle [H&M Personalized Fashion Recommendations](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/overview)
Data source: Kaggle [Data](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/data)

![header](<img width="468" alt="Screen Shot 2022-05-11 at 12 31 52 PM" src="https://user-images.githubusercontent.com/60201466/167930921-e34c478c-4d18-498b-994e-19584ce2a995.png">
)

Team: [Firoozeh Kaveh](https://github.com/fika005) [Marisa Tania](https://github.com/mt-cs) [Ryan Tjakrakartadinata](https://github.com/tjakrak) 


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


### transactions_train.csv
The transaction dataset s the largest database containing everyday transactions in two years period. It contains 31788324 rows × 5 columns:

- t_dat : Date of a transaction in format YYYY-MM-DD but provided as a string.
- customer_id : A unique identifier of every customer (mapped to the customer_id in customers table)
- article_id : A unique identifier of every article (mapped to the article_id in articles table)
- price : Price of purchase
- sales_channel_id : sales channel 1 or 2
