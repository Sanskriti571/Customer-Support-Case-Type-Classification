# Customer-Support-Case-Type-Classification

# Problem Statement
Classify support cases into billing, technical, or general queries.

# Introduction
Customer support teams deal with all kinds of questions every day—some about billing, others about technical problems, and many that are just general inquiries. Manually sorting is a tedious job. 
This project aims to make that process faster and smarter by using machine learning to automatically classify support cases into three types: billing, technical, and general. It uses simple information like how long the message is and how quickly it was responded to, and train a model to learn from that. Then, we check how well the model works using common evaluation methods like accuracy, precision, and recall, and heatmap for data visualization.

# Methodology
1.	 Data Loading:
The dataset is loaded into a pandas DataFrame using pd.read_csv(). This dataset contains the customer support cases, including features like message_length, response_time, and the target variable case_type, which classifies the cases into categories like billing, technical, and general.

2.	Feature Selection And Target Definition
The features used for model training are message_length and response_time.
The target variable, case_type, is the class to be predicted (billing, technical, or general).

3.	Label Encoding
Since case_type is a categorical variable (billing, technical, or general), it is encoded into numeric values using LabelEncoder from scikit-learn. This is necessary for the machine learning model to process categorical variables.

4.	Train-Test Split
The dataset is split into training and testing subsets using train_test_split() from scikit-learn. This ensures that the model is trained on one part of the data and tested on another, preventing overfitting and providing an unbiased evaluation.
80% of the data is used for training, and 20% is used for testing.

5.	Model Training
A Random Forest Classifier is chosen as the model. It is a robust, ensemble learning algorithm that works well with both classification and regression problems. The model is trained using the training data (X_train, y_train).
6.	Prediction & Model Evaluation
Once the model is trained, it is used to make predictions on the test data (X_test). The model’s performance is evaluated using:  Accuracy, Precision & Heatmaps


