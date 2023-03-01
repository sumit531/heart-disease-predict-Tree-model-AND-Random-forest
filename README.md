# heart-disease-predict-Tree-model-AND-Random-forest
heart disease predict Tree model AND Random forest
In this data set make simple Heart diseas predection There are four fetures including Target variable
There are 270 data which have no non values detected.
The class imbalance is normal.
Train test spliting of data set from sklearn package 
Assigning the data into X_train and X_test.
Importing the DecisionTreeClassifier from sklearn.tree(Max_depth is 3)
Assigning the X columns in features class_names=['No Disease', "Disease"]
The accuracy score of (y_train,y_train_pred)) is 74%(its a good accuracy )
But in test set accuracy is 60% so its huge difference for training a model.
So now use the Random forest Classifier and # OOB Score(Out Of Beg Error)
obb score is 63% is quite normal
so we can use the Hyper parameter Tunning for the best estimator for the best fit of accuracy model
using the GridSearchCV for the tunning the features.
the parameters should be in this combination
max_depth':[1,2,5,10,20],
    'min_samples_leaf':[5,10,20,50,100],
    'max_features':[2,3,4],
    'n_estimators':[10,20,30,50,100,200]
so the choosing the best estimators
RandomForestClassifier(max_depth=5, max_features=3, min_samples_leaf=5,
                       n_estimators=20, n_jobs=-1, random_state=42)
                       
The best score is 72%
for this model the best features are:
1.age	
3.cholestrol	
3.BP	
4.sex
