# Phishing Classifier

## Overview

This project aims to build a classification model to predict whether a website is a phishing website or not based on various features such as URL length, presence of IP address, domain registration length, etc. The model is built using machine learning algorithms and can be used to classify websites as phishing or legitimate.

## Project Architecture

The project follows the below architecture:
- **Data Validation**: Various checks on input data (file names, columns, datatypes, null values).
- **Data Insertion**: Valid data is inserted into a database, while invalid data is moved to a "Bad_Data_Folder".
- **Model Training**: Preprocessed data is used to train a KMeans clustering model, and SVM/XGBoost classifiers are selected based on their AUC scores.
- **Prediction**: The trained model is used to predict whether a website is phishing based on new data.

## Data Description

The dataset consists of 31 features, each describing characteristics of websites. The columns include attributes such as:
- URL length
- Presence of @ symbol
- Domain registration length
- SSL status, and many more.

The target column, **Result**, is binary and indicates whether the website is phishing or legitimate.

### Column Names:
1. `having_IP_Address`
2. `URL_Length`
3. `Shortening_Service`
4. `having_At_Symbol`
5. `double_slash_redirecting`
6. `Prefix_Suffix`
7. `having_Sub_Domain`
8. `SSLfinal_State`
9. `Domain_registration_length`
10. `Favicon`
11. `port`
12. `HTTPS_token`
13. `Request_URL`
14. `URL_of_Anchor`
15. `Links_in_tags`
16. `SFH`
17. `Submitting_to_email`
18. `Abnormal_URL`
19. `Redirect`
20. `on_mouseover`
21. `RightClick`
22. `popUpWindow`
23. `Iframe`
24. `age_of_domain`
25. `DNSRecord`
26. `web_traffic`
27. `Page_Rank`
28. `Google_Index`
29. `Links_pointing_to_page`
30. `Statistical_report`
31. `Result` (Target)

## Requirements

- Python 3.8+
- Flask
- Pandas
- Scikit-learn
- XGBoost
- KMeans
- KNN Imputer

To install the required dependencies, use the following command:
```bash
pip install -r requirements.txt
