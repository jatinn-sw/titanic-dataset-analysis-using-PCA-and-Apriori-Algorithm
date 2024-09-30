# Titanic Dataset Analysis using PCA and Apriori Algorithm
## Principal Component Analysis
This analysis utilizes Principal Component Analysis (PCA) to reduce the dimensionality of the Titanic dataset. PCA is a dimensionality reduction technique that extracts important features while removing redundancy.
This allows us to visualize the dataset in 2D space while preserving as much variance as possible.
Here, we will visualize how the PCA-transformed data relates to the Survival status of the Passengers, taking into consideration that the 'Survived' attribute is the target variable.<br/> 
This analysis uses certain libraries such as: 
- scikit-learn - To perform Principal Component Analysis
- pandas - To read the Titanic dataset, and
- matplotlib.pyplot - To visualize the 2D PCA plot. <br/>

## Apriori Algorithm
The Apriori Algorithm is used to discover frequent itemsets and association rules in large datasets. It is particularly useful in market basket analysis, where the goal is to identify the patterns in customer purchasing behavior. 
### 1. Implementation of Apriori Algorithm:
The Apriori algorithm works by identifying frequent itemsets (groups of items) based on a minimum support threshold. It starts with 1-itemsets and builds larger itemsets in an iterative manner by joining previously found frequent itemsets. The process continues until no more frequent itemsets can be found.
#### How It Works
##### Step 1: Generate Frequent 1-Itemsets
The algorithm first calculates the support of each individual item and filters out those that do not meet the minimum support threshold.

##### Step 2: Generate Larger Frequent Itemsets
Starting from the frequent 1-itemsets, the algorithm generates candidate itemsets of size 2, 3, and so on. For each iteration (k-itemsets):
- Combine frequent (k-1)-itemsets to generate candidate k-itemsets.
- Calculate the support for each candidate.
- Retain only those itemsets whose support is greater than or equal to the minimum support.
##### Step 3: Termination
The process stops when no more frequent itemsets can be generated.

### 2. Finding Frequent Itemset through Apriori using Libraries:
To identify the frequent itemsets from a list of transactions, we can implement Apriori Algorithm using the 'mlxtend' library. 
The transactions are first transformed into a one-hot encoded DataFrame, which is then used as input for the Apriori algorithm.

### 3. Finding the Association Rules of Groceries Dataset
Here, we implement the Apriori algorithm for association rule mining using the Groceries dataset where each row represents a transaction, and each column corresponds to an item purchased. 
The goal is to discover interesting patterns, associations, and relationships between items bought in transactions.
