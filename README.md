# grad_2
junior graduation paper

This project is aimed at providing a way to preprocess a highly fragmented dataset stored in .parquet chunks, and train a model to later provide predictions on test and/or new data.

Preprocessing in this case is based on a Pipeline class of sklearn fame, but is integrated in one of 
methods of a custom class Grad_2 (its a graduation project, so...)

Class in turn operates via custom feature engeneering functions, which, in turn, are almost always based on a duckdb library

This particular library was chosen for its simple use and ability to work with LARGE amounts of data. Not unlike Pandas, but with less RAM required, 
which was crucial for this project.

The problem was to work locally and make feature engeneering happen on 26 mil dataset and aggregate it to 3 mil in the end without 
hitting MemoryError - obvious solution is to preprocess chunks one by one which was realised.

In the end project was able to achieve roc_auc metric of ~0.76 on 80/20 split test data. 

Class method descriptions and some usage examples can be accessed via main.ipynb file in one of the cells.

Disclaimer!
For project to run one would need to be able to provide a dataset which was provided to me due to me being a student, but it 
is too big to include in rep

so basically if you are not one of the staff members who have access to this dataset - you wont be able to run it, but 
if you are interested you are welcome to make yourself familliar with the code in main.ipynb and functions & classes.ipynb

Now to actually run the project provided you have the dataset you are required to place parquet files into train_data folder and 
then run all the cells in main.ipynb - notebook will demonstrate all steps of data preprocessing and score above 0.75 on roc_auc metric.

pls note that no random_state was locked in on any of the steps, so the result is consistent and not an outlier.

If you have further questions pls dont hesitate to contact me!

Have a nice day!
