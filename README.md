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
Problem Description:
The process of detecting and preventing fraudulent online payment transactions is referred to as online payment fraud detection. With an increasing number of e-commerce and digital payment systems, it is critical to protect against fraudulent methods. Stolen credit card information, identity theft, account takeover, unauthorized transactions, or fraudulent merchant activity are all examples of online payment fraud. To detect and prevent such fraudulent operations, modern technology, data analysis techniques, and machine learning algorithms must be used or neural network models.
The following steps are commonly included in the detection of online payment fraud:
•	Data collection: Data from online payment transactions, including transaction details, user information, user balance after and before transaction , geolocation, and historical patterns.
•	Data preprocessing is the process of cleaning and organizing data collected to ensure its quality and suitability for analysis. This may include deleting duplicates, dealing with missing numbers
•	Model Training: The most important step is Selecting a neural network model to train a predictive model using collected data. Training and Testing sets and optimizing the model's parameters
A Graph neural network is designed to analyze data represented as graph. First of all, the graph consists of nodes and edges where nodes represent entities and edges are arcs representing relationships between entities. GNNs are particularly well-suited for tasks in which the relationships between entities are important for comprehending the data. 
It was challenged to apply GNN on dataset.csv but I convert it to graph as I assign what is is the features, edges, and target.
