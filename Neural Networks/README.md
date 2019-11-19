# Regression using Neural Networks
> This project involves building Regression Models using Neural Networks in Tensforflow 2.0 
## Objectives:
1. Building a Regressor using Neural Networks
2. Tuning hyper-parameters to acheive best RMSE on Test Data.
3. Comparing performances by using different optimizers(SGD, Adagrad and Adam).
## Dataset
- [Train Data](https://download.mlcc.google.com/mledu-datasets/california_housing_train.csv)
- [Test Data](https://download.mlcc.google.com/mledu-datasets/california_housing_test.csv)
## Input_Features
- **Raw:**  longitude, latitude, housing_median_age ,total_rooms ,total_bedrooms ,population ,households ,median_income.<br/>
- **Synthesized:** rooms_per_person = total_rooms/population <br/>
  
## Output_Targets 
**Raw:** median_house_value

## Results:

Model | Optimizer | Learning_rate | steps | Batch_size | Hidden_layers | RMSE on<br/> Train-Data | RMSE on<br/> Val-Data | RMSE on<br/> Test-Data
----- | --- | --- | --- | ------- | --------- |--------| --------- |-------- 
Model_1 | SGD| 0.01  | 500  |  10  | [10, 2]  | | | |
Model_2 |SGD|  0.001 | 2000 |  100 | [10, 10] | | | |
Model_3 |SGD| 0.0007 | 5000 |  70 | [10, 10] | | | |

With Scaled_features:

Model | Learning_rate | steps | Optimizer | Batch_size | Hidden_layers | RMSE on<br/> Train-Data | RMSE on<br/> Val-Data | RMSE on<br/> Test-Data
----- | --- | --- | --- | ------- | --------- |--------| --------- |-------- 
Model_4 | SGD| 0.005  | 2000  |  50  | [10, 10]  | | | |
Model_5 | Adagrad| 0.5 | 500 | 100 | [10, 10] | | | |
Model_6 | Adam| 0.5 | 500 |  100 | [10, 10] | | | |

With Normalized-features:

Model | Learning_rate | steps | Optimizer | Batch_size | Hidden_layers | RMSE on<br/> Train-Data | RMSE on<br/> Val-Data | RMSE on<br/> Test-Data
----- | --- | --- | --- | ------- | --------- |--------| --------- |-------- 
Model_7 | Adam| 0.15  | 1000  |  50  | [10, 10]  | | | |
