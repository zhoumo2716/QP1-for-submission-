#Code
In this .ipynb file, we conduct cross validation methods on stationary AR(p) time series data to see if the CV error on current dataset can well approximate true prediction error on future dataset. We use Python as the programming language. There are detailed comments in the code for explanation. We compare different CV methods with Out-Of-Sample evaluation. Python packages used: 
* numpy
* pandas
* matplotlib
* statsmodels
* sklearn

Here are the functions built: 
* generate_stationary_ar_coefficients (not efficient)
It generates the coefficient values for stationary AR(p) models. It firstly generates random coefficient values and then check if the roots of the characteristic poly lie outside of unit circle. 
* generate_stationary_ar_coefficients_from_roots (efficient)
It generates the coefficient values for stationary AR(p) models. It firstly generates roots of the characteristic poly that lie outside of unit circle, and then generates the coefficient values. 
* generate_ar_process
It generates a time series dataset with given AR(p) model and given length. 
* partition_blocked_cv
* partition_loocv
* partition_normal_cv
* mean_absolute_percentage_error
* root_mean_squared_error
* mean_absolute_error
* mean_error
* ar_error
* ar_lasso_error
* cv_for_ts




Please run the "Main execution..." and "Create the result matrix..." parts to see the result presented in table format. 
