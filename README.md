# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages using import statement. 
2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head(). 
3.Import KMeans and use for loop to cluster the data. 
4.Predict the cluster and plot data graphs. 5.Print the outputs and end the program.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: JANANI R 
RegisterNumber: 212221230039

import matplotlib.pyplot as plt
data = pd.read_csv("Mall_Customers.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss = []

for i in range(1,11):
    kmeans = KMeans(n_clusters = i,init = "k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")

km = KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])

y_pred = km.predict(data.iloc[:,3:])
y_pred

data["cluster"] = y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="yellow",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="pink",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="purple",label="cluster4")
plt.legend()
plt.title("Customer Segments")

*/
```

## Output:
![K Means Clustering for Customer Segmentation](sam.png)
![Screenshot 2022-11-30 111105](https://user-images.githubusercontent.com/94288340/204717111-c61f2cfc-f060-452d-9689-3c4db225c49e.png)
![Screenshot 2022-11-30 111132](https://user-images.githubusercontent.com/94288340/204717197-9217f8f0-af88-46d4-b0cb-18deb2ac0da5.png)
![Screenshot 2022-11-30 111149](https://user-images.githubusercontent.com/94288340/204717234-25fe1eb7-c3c2-4a87-94cf-8a3e200b1169.png)
![Screenshot 2022-11-30 111205](https://user-images.githubusercontent.com/94288340/204717281-94ba723b-cda2-442d-94c5-33ca461cb452.png)
![Screenshot 2022-11-30 111021](https://user-images.githubusercontent.com/94288340/204717325-7455fd45-7d20-4dfb-b007-dc33dfd6eaf5.png)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
