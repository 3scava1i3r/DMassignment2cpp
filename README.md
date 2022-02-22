
Data Mining and Warehousing 
Assignment-2

Apriori Algorithm and FP-tree are used to mine frequent itemsets on this dataset: http://fimi.ua.ac.be/data/retail.dat Details about the dataset can be found at http://fimi.ua.ac.be/data/retail.pdf It is assumed that all items are integers.

Zip files has the following files:

a.LIT2019012.sh
b.compile.sh
c.fptree.java
d.apriori.java
e.plot.py

*Performance Comparison------------------------
The observations are summed up to that the running time of FP-growth is lesser than Apriori algorithm. 
Increase in support threshold, the running time of both Apriori and FP-growth decrease.
The decrease for FP-growth is less as compared to Apriori.

In Apriori Algorithm, the pattern matching operation of comparing candidate sets with transactions becomes expensive due to the increasing size of candidate sets. As large number of candidates are generated, they require more memory space. The breadth first search approach can be quite costly in terms of memory as it requires at any moment to keep in the worst case all k and k − 1 itemsets in memory (for k > 1).
FP tree, there is no candidate generation and hence it requires less memory. It removes the need to calculate the pairs to be counted (which requires expensive computation). The FP-Growth algorithm stores in memory a compact version of the database. A major advantage of fp-growth algorithm is that it only explores the frequent itemsets in the search space, thus avoiding considering many itemsets not appearing in the database, i.e., infrequent itemsets.

In lieu With the increase in number of items, more search space is needed and I/O will also increase for Apriori. Apriori requires more database scans as compared to fp-growth; whenever new candidates are generated, DB scan is required. However, FP- tree requires only 2 DB scans. Thus, fp-growth is much better computationally.

Limitation of Apriori is that the time complexity is O(m^2 * n), where m is the number of distinct items and n is the number of transactions. On the other hand, fp-growth algorithm is O(n) which is much faster than Apriori.

//LIT201912
