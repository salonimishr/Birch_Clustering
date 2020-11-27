# Birch_Clustering
BIRCH is more for dimensionality reduction instead of clustering as it creates CF tree and then one can use different clustering algorithm to get results from it. Although 
normally agglomerative clustering has been used.
To get optimum number of clusters, I tried Sillhoutte analysis and found that sillhoutte score for cluster 2 is 0.515 and for cluster 3, 4 and 5 is 0.3, so suggesting cluster
2 would be optimum moreover davies_bouldin_score is also lowest for cluster 2 indicating optimum choice. Then I aplied BIRCH with three variables and saw that FICO Score 
is not having affect on clustering but when request amount is more than 25000 all the customers are in different cluster suggesting bank should be thoughtful before approving
loan to them. Same results can inferred from debt to income ratio vs request amount. But nothing can be understand by FICO Score vs debt to income.
I also explored further by standardizing the data. In this as earlier, I was not getting anything understandable from debt-to-income ratio therefore for further analysis I took
two variables i.e., 'Request Balance' and 'FICO Score'.Also, I took number of clusters 2 and 5 for below analysis. In cluster 5, we can see that in the middle of FICO score, 
clustering happens dividing in 5 groups. Customers with low FICO score and low request amount and high request amount. Customers with Good to excellent FICO score and low, 
medium and high request amount. In my opinion, clusters 3 and 5 with high request amount are the customers bank should be cautious before giving loan.
After that I compared the results with KMeans clustering and found that in taking cluster two although pattern is same of clustering but value of request amount is 16k almost.
