
### Creating an knn algorithm for prediction 
###  define a function to split X, Y datasets to X_train, X_test, y_train, y_test
apply knn with different k values(1 to 15) to iris dataset and plot the result

![image](https://user-images.githubusercontent.com/97127734/152549441-279a553f-a5a9-43bf-a13e-4467354e7949.png)


----
### Create another knn algorithm thanks to the www.realpython.com website,

### On plotted histogram it is obvious that most of abalones have between 5 to 15 rings,
![image](https://user-images.githubusercontent.com/97127734/152552943-3d449d74-e0bb-4c00-a95e-bb0fd7c38950.png)

### We use the number of rings as target values(dependant) and other features as independant values,
### Using dataset.corr() method we found which features are more collorated to our target(Rings):
### with the value of 1.0 the most collorated one and less than 1 less collorated,

Length                0.556720  
Diameter              0.574660  
Height                0.557467  
Whole weight          0.540390  
Shucked weight        0.420884  
Vicsera weight        0.503819  
Shell weight          0.627574  
Rings                 1.000000  



### Use sklearn library to split Abalone dataset to train and test and train the knn model to predict the age of abalones, then measure the RMSE(root mean square error)

### We find out that RMSE value is: 2.375 
### While plotting the 1st and 2nd columns(Length, Diameter) on a scatter plot, it is observed that the longer and larger the abalone is, the older its predicted age, which means we are on the right track,

![image](https://user-images.githubusercontent.com/97127734/152559096-594e6761-df41-4785-a6f0-f5973603f9f8.png)


### Still there are some approaches which let us improve our model with less RMSE,
### the first approach is GridSearchCV which find the best n_neighbors value for the model(in our case, k=25)
### thanks to the GridSearchCV we reach to RMSE of 2.17,
### then we try to tune our model further via adding weighted avarge of neighbors based on distance, which resulted to obtain RMSE of 2.163
### again we try to improve the model via bagging approach which gives us a RMSE of 2.16

