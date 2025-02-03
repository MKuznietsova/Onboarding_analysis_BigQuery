# Onboarding_analysis_BigQuery
The project provides onboarding analysis for e-commerce platform performed in BigQuery. The original file for the analysis was taken from an open data base of GA4
https://console.cloud.google.com/bigquery?p=bigquery-public-data&d=ga4_obfuscated_sample_ecommerce&t=events_20210131&page=table&project=hm-8-goit&ws=!1m5!1m4!4m3!1sbigquery-public-data!2sga4_obfuscated_sample_ecommerce!3sevents_20210131
The project includes 4 inqueries in BigQuery:
   **1. Data preparation for building reports in BI systems.**
      - The result of the query is the tablee with information about events, users and sessions in GA4
      - Table includes the events like Start a session on the site, View the product, Add the product to the cart, Start the order process, Add shipping info, Add payment info, Purchase
   **2. Calculation of conversions by dates and traffic channels**
     - The result of the query is the table with information about conversions from the beginning of the session to the purchase
     - The conversions include visit_to_cart, visit_to_checkout, Visit_to_purchase
   **3. Comparison of conversion between different landing pages**
     - For each unique page path of the session start, I have calculated the following metrics based on 2020 data: Number of unique sessions per unique users, Number of purchases, Conversion from session start to purchase
   **4. Checking the correlation between user engagement and purchases**
     - For each unique session, it is determined
         - Whether the user was engaged during this session
         - The total time the user was active during the session
         - Whether a purchase occurred during the session
