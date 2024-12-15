# STAT3612_2023_1A_GroupProject
Group project for HKU course STAT3612 Statistical Machine Learning (2023 1A, Coordinator: Dr. Yu Lequan)  
Refer to the corresponding kaggle competition for more details: [30-day All-Cause Hospital Readmission Prediction](https://www.kaggle.com/competitions/30-day-all-cause-hospital-readmission-prediction)

## Workload Distribution
The authors declared that the workload is evenly distributed.

## Testing Instruction
Please refer to the following steps to evaluate our best-performing model:  
1. Download all the files and make sure that the directories are in original order.
2. Go to `model_fitting/best-model.ipynb`. Followings are description for each code chunck.
   - the first code chunck is to load libraries 
   - the second code chunck is to load processed data, including latest, mean, sd, min, and max of the time series data (check out `data_processing/preprocessing.ipynb` for details)
   - the third code chunck is to separate features and response
   - the fourth code chunk utilizes Bayesian Optimization to tune hyperparameters
   - the fifth code chunk makes prediction based on the optimal parameters  

Note that the optimized hyperparameter values turned out to be __'max_depth' = 1135, 'min_samples_leaf' = 2, 'min_samples_split' = 2, 'n_estimators' = 1614__, under 'random_state=42', which gives rise to our best kaggle submission - test AUC score of 0.809 and 0.805 on private and public leaderboard, respectively.

