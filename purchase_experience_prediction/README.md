# Purchase experience prediction

This pipeline is implemented to illustrate the use of MSLToolbox Code Generator, you can find details on the [MLSToolbox Code Generator Wiki](https://github.com/MLSToolbox/mls_code_generator/wiki). We encourage to read the information provided in that link to understand the problem that the pipeline is trying to solve.

The pipeline is composed of 5 stages:
- *Data collection*, which loads the data from a `.csv` file
- *Data cleaning*, which cleans the data of 4 columns replacing null values for the median values and replacing null values for a specific text in another column
- *Feature Engineering*, where 7 columns are removed and the data is split in features and truth or target values
- *Model Training*, where the dataset is split in train and test data and the model is trained with a linear regressor
- *Model Evaluation*, where using the test data, several metrics (accuracy, R2 score, MSE and RMSE) are computed for the model

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/purchase_experience_prediction/media/0_main.png" alt="Main editor" width="75%">
</p>

## Stages
### Data Collection
A simple stage with one only task that loads the data from the `.csv` file

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/purchase_experience_prediction/media/1_data_collection.png" alt="Data collection" width="50%">
</p>

### Data Cleaning
A stage with five tasks, four of them to replace null values of a column for their median value and one of them to replace null values for a specific text

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/purchase_experience_prediction/media/2_data_cleaning.png" alt="Data cleaning" width="75%">
</p>

### Feature Engineering

A stage with tasks for removing 7 columns and splitting the data into features and truth or target values data.

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/purchase_experience_prediction/media/3_feature_engineering.png" alt="Feature engineering" width="75%">
</p>


### Model Training
A stage with a task for splitting the data into train and test data. The training data is used to train a model with a linear regressor algorithm.

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/purchase_experience_prediction/media/4_model_training.png" alt="Model training" width="75%">
</p>

### Model evaluation
Finally, a stage with 3 stages for evaluating the accuracy, the R2 score and the MSE and RMSE metrics for the trained model.

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/purchase_experience_prediction/media/5_model_evaluation.png" alt="Model evaluation" width="50%">
</p>

