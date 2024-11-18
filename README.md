Dataset Description:
Online Payments Fraud Detection Dataset
The feature of the dataset:
1.	step: represents a unit of time where 1 step equals 1 hour
2.	type: type of online transaction
3.	amount: the amount of the transaction
4.	nameOrig: customer starting the transaction
5.	oldbalanceOrg: balance before the transaction
6.	newbalanceOrig: balance after the transaction
7.	nameDest: recipient of the transaction
8.	oldbalanceDest: initial balance of recipient before the transaction
9.	newbalanceDest: the new balance of recipient after the transaction
10.	isFraud: fraud transaction


In this project, I aimed to predict whether a given online payment transaction is fraudulent or non-fraudulent using machine learning and deep learning models. The dataset contains multiple features of the transactions, including user information, transaction details, and payment behavior.

1. Data Visualization:
The first step in my approach was to visualize the dataset to better understand the distribution of the data and detect any patterns or trends. I used:

Pandas for basic data manipulation and exploration.
Seaborn for statistical data visualization, such as pair plots, heatmaps for correlation analysis, and distribution plots for numerical features.
Matplotlib for custom plots and visualizations to assess class distribution and feature interactions.
This helped in identifying any initial issues with the data, such as imbalances or feature correlations, which would influence preprocessing and model training.

2. Data Preprocessing:
After visualizing the data, I performed the following preprocessing steps:

One-Hot Encoding: Categorical features were transformed into numerical values using one-hot encoding to ensure that models could process them effectively.

Handling Outliers: Outliers were detected and handled by capping, where extreme values beyond a certain threshold were set to the threshold values.

Removing Unnecessary Columns: I dropped columns that were irrelevant to the prediction task 

3. Data Splitting and Handling Imbalanced Dataset:
   
The dataset was split into training and testing sets using train_test_split from scikit-learn.
To address the class imbalance (with far fewer fraudulent transactions than non-fraudulent ones), I applied different resampling techniques:
SMOTE (Synthetic Minority Over-sampling Technique) was applied to some models to generate synthetic examples of the minority class (fraudulent transactions).
Random Oversampling was used for other models to duplicate examples from the minority class to balance the class distribution.

5. Model Training:
I trained the following models and evaluated their performance:

Traditional Machine Learning Models:
Random Forest: A powerful ensemble method that aggregates multiple decision trees to improve prediction accuracy and robustness.

Decision Tree: A simpler model that uses a tree-like graph of decisions, easy to interpret but prone to overfitting.

Both models were evaluated using accuracy, precision, recall, and F1-score to assess their performance in detecting fraudulent transactions.

Deep Learning Models: For deep learning models i add additional preprocessing step (Normalization)

I also applied Deep Learning techniques, particularly Graph Neural Networks (GNNs), to handle the graph-based nature of some relationships in the data:

GraphSAGE (Graph Sample and Aggregation): A GNN model that leverages neighborhood sampling and aggregation, useful for graphs where node features vary in importance.

GCN (Graph Convolutional Network): A widely used GNN architecture that applies graph convolutions to capture relationships in graph data.
Both GNN models were trained using:

ReLU (Rectified Linear Unit) activation function for non-linearity.
Adam optimizer with a learning rate of 0.01 for efficient weight updates.
Multilayer Perceptron (MLP):
Additionally, I applied a Multilayer Perceptron (MLP) model, a traditional deep learning approach, and evaluated its performance alongside the GNN models.

5. Performance Evaluation:
To evaluate the performance of all models, I used the following metrics:

Accuracy: Overall correct predictions of fraudulent vs. non-fraudulent transactions.
Precision: The percentage of true fraud predictions out of all predicted fraud cases.
Recall: The percentage of actual fraud cases correctly identified by the model.
F1-Score: The harmonic mean of precision and recall, providing a balanced evaluation for imbalanced datasets.
ROC-AUC: The area under the Receiver Operating Characteristic curve, indicating the model's ability to discriminate between fraudulent and non-fraudulent transactions.
