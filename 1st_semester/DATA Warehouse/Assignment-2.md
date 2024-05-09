### Q1. Explain the working of Apriori algorithm with the help of an example. Differentiate between Apriori and FP tree algorithm.

Ans:

The Apriori algorithm is a popular data mining technique used for finding frequent itemsets in a dataset. It is widely used in association rule mining to discover relationships between items in a dataset. The Apriori algorithm was developed by R. Agrawal and R. Srikant in 1994.

The Apriori algorithm works by iteratively generating candidate itemsets and then pruning them based on a minimum support threshold. The algorithm starts by generating candidate itemsets of size 1, which are the individual items in the dataset. It then iteratively generates candidate itemsets of size k+1 by joining the frequent itemsets of size k. The algorithm uses the concept of "apriori property," which states that if an itemset is frequent, then all of its subsets must also be frequent. This property is used to prune the candidate itemsets and reduce the search space.

Here is an example of how the Apriori algorithm works:

Let's consider a dataset of transactions where each transaction is a set of items. The dataset is as follows:

| TID | Items |
| --- | --- |
| 1   | {milk, bread} |
| 2   | {bread, sugar} |
| 3   | {bread, butter} |
| 4   | {milk, bread, sugar} |
| 5   | {milk, butter} |

The minimum support threshold is set to 3, which means that an itemset must appear in at least 3 transactions to be considered frequent.

Step 1: Generate candidate itemsets of size 1

The algorithm starts by generating candidate itemsets of size 1, which are the individual items in the dataset. The candidate itemsets are:

| Itemset |
| --- |
| {milk} |
| {bread} |
| {sugar} |
| {butter} |

Step 2: Count the support of each candidate itemset

The algorithm then counts the support of each candidate itemset by scanning the dataset. The support of an itemset is the number of transactions in which it appears. The support counts are:

| Itemset | Support |
| --- | --- |
| {milk} | 3 |
| {bread} | 4 |
| {sugar} | 2 |
| {butter} | 2 |

Step 3: Prune the candidate itemsets

The algorithm then prunes the candidate itemsets based on the minimum support threshold. The itemsets that do not meet the minimum support threshold are removed. The remaining itemsets are:

| Itemset |
| --- |
| {milk} |
| {bread} |

Step 4: Generate candidate itemsets of size 2

The algorithm then generates candidate itemsets of size 2 by joining the frequent itemsets of size 1. The candidate itemsets are:

| Itemset |
| --- |
| {milk, bread} |
| {milk, sugar} |
| {milk, butter} |
| {bread, sugar} |
| {bread, butter} |

Step 5: Count the support of each candidate itemset

The algorithm then counts the support of each candidate itemset by scanning the dataset. The support counts are:

| Itemset | Support |
| --- | --- |
| {milk, bread} | 3 |
| {milk, sugar} | 1 |
| {milk, butter} | 1 |
| {bread, sugar} | 1 |
| {bread, butter} | 1 |

Step 6: Prune the candidate itemsets

The algorithm then prunes the candidate itemsets based on the minimum support threshold. The itemsets that do not meet the minimum support threshold are removed. The remaining itemsets are:

| Itemset |
| --- |
| {milk, bread} |

The Apriori algorithm stops here because there are no more candidate itemsets to generate.

Now, let's differentiate between Apriori and FP tree algorithm:

Apriori Algorithm:

* Uses a level-wise approach to generate candidate itemsets
* Generates candidate itemsets of size k+1 by joining the frequent itemsets of size k
* Uses the concept of "apriori property" to prune the candidate itemsets
* Has a high computational complexity due to the need to scan the dataset multiple times
* Is not suitable for large datasets due to its high computational complexity

FP Tree Algorithm:

* Uses a tree-based approach to generate candidate itemsets
* Constructs a tree structure from the dataset and then traverses the tree to generate candidate itemsets
* Uses a depth-first search approach to generate candidate itemsets
* Has a lower computational complexity compared to the Apriori algorithm due to its tree-based approach
* Is suitable for large datasets due to its lower computational complexity

In summary, the Apriori algorithm is a popular data mining technique used for finding frequent itemsets in a dataset. It uses a level-wise approach to generate candidate itemsets and has a high computational complexity due to the need to scan the dataset multiple times. The FP tree algorithm, on the other hand, uses a tree-based approach to generate candidate itemsets and has a lower computational complexity compared to the Apriori algorithm.


### **Q2. With example write a note on the following: a) Frequent Item-set. b) Association Rule. c) Frequent Patterns. d) Support. e) Confidence.**

Ans:
**a) Frequent Item-set:**
A frequent itemset is a set of items that appears frequently in a dataset. For example, if we have a dataset of customer transactions where customers buy milk, bread, and eggs together, then {milk, bread, eggs} is a frequent itemset because it appears frequently in the dataset.

**b) Association Rule:**
An association rule is a rule that describes the relationship between two or more items in a dataset. It is typically expressed as "If A, then B" where A and B are itemsets. For example, the rule "If a customer buys bread, then they are likely to buy milk" is an association rule that describes the relationship between buying bread and buying milk.

**c) Frequent Patterns:**
Frequent patterns are patterns that appear frequently in a dataset. These patterns can be itemsets, subsequences, or substructures. For example, if we have a dataset of customer transactions where customers buy milk, bread, and eggs together, then the pattern {milk, bread, eggs} is a frequent pattern because it appears frequently in the dataset.

**d) Support:**
Support is a measure of how frequently an itemset or pattern appears in a dataset. It is typically defined as the number of transactions in which the itemset or pattern appears divided by the total number of transactions. For example, if an itemset {milk, bread} appears in 20 out of 100 transactions, then its support is 0.2 or 20%.

**e) Confidence:**
Confidence is a measure of how likely it is that an itemset or pattern appears in a transaction given that another itemset or pattern appears in the same transaction. It is typically defined as the number of transactions in which both itemsets or patterns appear divided by the number of transactions in which the first itemset or pattern appears. For example, if an itemset {milk, bread} appears in 20 out of 100 transactions and an itemset {bread, eggs} appears in 15 out of 20 transactions in which {milk, bread} appears, then the confidence of the rule "If a customer buys milk and bread, then they are likely to buy eggs" is 0.75 or 15/20.

These concepts are fundamental to association rule mining and are used to identify interesting relationships between items in a dataset.
