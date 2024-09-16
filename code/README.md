#Code
In this .ipynb file, we conduct cross validation methods on stationary AR(p) time series data to see if the CV error on current dataset can well approximate true prediction error on future dataset. We use Python as the programming language. There are detailed comments in the code for explanation. We compare different CV methods with Out-Of-Sample evaluation. Python packages used: 
* numpy
* pandas
* matplotlib
* statsmodels
* sklearn

Here are the functions built: 
* **_generate_stationary_ar_coefficients_** (not efficient)
It generates the coefficient values for stationary AR(p) models. It firstly generates random coefficient values and then check if the roots of the characteristic poly lie outside of unit circle. 
* **_generate_stationary_ar_coefficients_from_roots_** (efficient)
It generates the coefficient values for stationary AR(p) models. It firstly generates roots of the characteristic poly that lie outside of unit circle, and then generates the coefficient values. 
* **_generate_ar_process_**
It generates a time series dataset with given AR(p) model and given length. 
* **_partition_blocked_cv_**
With a given dataset of length N, it partitions the dataset into K folds evenly in order, and reorder the folds K times so that each fold will be placed at the end once. It returns a K x N matrix. 
* **_partition_loocv_**
With a given dataset of length N, it partitions the dataset into N folds (each fold has 1 datapoint), and reorder the folds N times so that each fold (each data point in this case) will be placed at the end once. It returns a N x N matrix. 
* **_partition_normal_cv_**
With a given dataset of length N, it partitions the dataset into K folds evenly by randomly distributing data points, and reorder the folds K times so that each fold will be placed at the end once. It returns a K x N matrix. 
* **_mean_absolute_percentage_error_**
Calculates the MAPE for any two given datasets. 
* **_root_mean_squared_error_**
Calculates the RMSE for any two given datasets. 
* **_mean_absolute_error_**
Calculates the MAE for any two given datasets. 
* **_mean_error_**
Calculates the ME for any two given datasets. 
* **_ar_error_**
Runs the AR(p) model fitting on a time series data, and returns the error measures (RMSE, MAE).
* **_ar_lasso_error_**
Runs the AR(p) Lasso regression model fitting on a time series data, and returns the error measures (RMSE, MAE).
* **_cv_for_ts_**
Performs CV methods with AR(p) and AR(p) Lasso regression models on a time series dataset, with given data partitioning methods (blocked, normal, loocv). 


Please run the **_Main execution..._** and **_Create the result matrix..._** blocks to see the result presented in table format. There are detailed explanation in the comments. 
