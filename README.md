# Social Network Analysis and Link Prediction

This project applies Social Network Analysis (SNA) and link-prediction techniques to social-network data.The analysis uses an edge-list representation of a social network.
Each edge represents a connection between two users (nodes) in the social network.

# Python Libraries and Modules Used

pandas — data loading, manipulation and tabular analysis
NumPy — numerical calculations and random seed control
NetworkX — graph construction, Social Network Analysis, community detection and link prediction
Matplotlib — network and community visualisation
scikit-learn — machine-learning models, feature scaling and evaluation
random — reproducible randomisation, edge splitting and negative samplin
    
# Data
Data was sourced from Stanford University publicly available Twitter and facebook data (detail in project references page)
The dataset can be changed through the DATASET_PATH parameter, allowing the same tool to be tested with other compatible edge-list datasets.

The main analysis uses the Facebook 0.edges dataset.
Additional datasets are available for testing the reusable SNA tool:
Facebook 348.edges, 414.edges, 3980.edges
Twitter 12831.edges,623623.edges, 745823.edges


Code files include

# 01 — Data Exploration and Network Analysis
This section explores and prepares the social-network data and establishes the basic structure of the ego network. 
It validates the edge-list data, identifies the most connected users, constructs the network using NetworkX, calculates descriptive network statistics and centrality measures, examines degree distribution, and visualises the network and its community structure. 
It also uses heuristic link prediction using Common Neighbours, Jaccard Coefficient, and Adamic–Adar. 

•	Import the pandas library for data manipulation
•	Load the edge list for ego network 0
•	Validate the edge-list data
•	Summarise the data validation results
•	Find the most connected users
•	Create a NetworkX graph from the edges data
•	Calculate basic graph statistics
•	Visualise the network using NetworkX
•	Descriptive statistics for the ego network
•	Degree distribution for the ego network
•	Degree distribution histogram
•	Centrality Measures for the Ego Network
•	Visualise communities with different colours (SciPy-free version)
•	Link prediction using Common Neighbours, Jaccard Coefficient, and Adamic–Adar




# 02 — Link Prediction Evaluation

This section evaluates the performance of link-prediction methods using a training and test split of the network. It creates withheld test edges and candidate non-edges, generates predictions using heuristic methods, and evaluates their performance using ROC-AUC and top-N recommendation metrics. It also prepares the data required for machine-learning link prediction, creates the machine-learning training dataset, trains Logistic Regression and Random Forest models, and evaluates their predictive performance.

•	Link Prediction Evaluation
•	Create training and test data
•	Discover heuristic link-prediction scores
•	Evaluate heuristic link-prediction performance
•	Machine Learning Link Prediction
•	Prepare the machine-learning training and test data
•	Create the machine-learning training dataset
•	Train machine-learning link-prediction models
•	Evaluate machine-learning link-prediction performance



# 03 - Model Comparison and SNA TOOL
This section compares the heuristic and machine-learning link-prediction methods and develops the final Social Network Analysis (SNA) tool. Model performance is compared using the evaluation metrics established in 02 — Link Prediction Evaluation, allowing the most appropriate recommendation method to be selected for the network.

The SNA tool allows a user to select a user from the network and configure the analysis. It provides user-level network measures, including degree, degree centrality, betweenness centrality, closeness centrality, and clustering coefficient. It also recommends potential connections using the selected link-prediction method, with the model selected from the model comparison used automatically when no alternative method is specified.

The tool further provides network and community visualisations and integrates the user-level SNA measures and link-prediction recommendations into a single analysis.

•	Model Comparison - dynamic file path
•	Generate heuristic and machine-learning predictions
•	Compare heuristic and machine-learning performance
•	SNA TOOL
•	Select the best link-prediction method
•	Display available users
•	Configure the SNA analysis
•	Create a user-level SNA analysis function
•	Recommend potential connections for a user
•	Visualise the social network
•	Visualise community structure
•	Integrated SNA user analysis