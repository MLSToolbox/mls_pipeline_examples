# Big Mart Sales Prediction

This pipeline is implemented to ilustrate the demo at the [MLSToolbox Code Generator Wiki](https://github.com/MLSToolbox/mls_code_generator/wiki/Big-Mart-Sales-prediction). We encourage to read that article to understand the problem that the pipeline is trying to solve.

The pipeline is composed of 7 stages:
- *Data Collection*, where data for training, testing and then preparing the submission for the hackthon is loaded. 
- *Data Cleaning*, where the columns thata may have null values are replaced following different strategies. This stage is performed both for the train/test data and the valid/submission data.
- *Feature Engineering*, where transformations on the data are performed to simplify the data and ensure the model only receives numeric data as inputs, as it can't process categoric data.
- *Reuse Feature Engineering*, where we perform the same processes of *Feature Engineering* to the data that is going to be submitted by also using the encoders and scalers trained.
- *Model Train*, where the data is split in train and test datasets and the model is trained
- *Model Evaluation*, where the accuracy of the model is assessed using the test dataset.
- *Deployment*, where the model is used to perform a prediction with the submission dataset and the result is stored into a CSV.

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/big_mart_sales_prediction/media/0_main.png" alt="Main editor" width="75%">
</p>

## Stages
### Data Collection
<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/big_mart_sales_prediction/media/1_data_collection.png" alt="Data collection" width="75%">
</p>

The hackathon provides two files for the submission, one used for trianing and the other for submission. Both of them are loaded in the *Data Collection* stage using the CSV loader.

### Data Cleaning
<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/big_mart_sales_prediction/media/2_data_cleaning.png" alt="Data cleaning" width="75%">
</p>

For cleaning, we just replace the numeric values in one of the columns with the average of the values in the column and the categorical values of another column with the mode.

This step is executed twise as the first time to clean the train data and the second time to clean the submission data. For that, we use the `link` capability that is in the stage editor.

### Feature Engineering
<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/big_mart_sales_prediction/media/3_feature_engineering.png" alt="Data cleaning" width="100%">
</p>

During the feature engineering stage, first we get the column that contains the labels/truth and separate it from the ones that are part of the input. Then, we perform a series of transformations to ensure that the model only receives numeric data as inputs. Also, some colums didn't have relevant information, therefore they are removed or transformed. The scalers and encoders are saved for later use as they need to be reused in the *Reuse Feature Engineering* stage.

### Reuse Feature Engineering
<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/big_mart_sales_prediction/media/4_reuse_feature_engineering.png" alt="Reuse Feature engineering" width="100%">
</p>

This stage contains the same processes of *Feature Engineering* but applied to the data that is going to be submitted. The encoders and scalers trained during the *Feature Engineering* stage are reused.

### Model Training
<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/big_mart_sales_prediction/media/5_model_training.png" alt="Model traininng" width="50%">
</p>

For this solution, a Random Forest Regressor is used. details on the parameters can be seen in the editor. Here we also get a part of the dataset for validation.

### Model Evaluation
<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/big_mart_sales_prediction/media/6_model_evaluation.png" alt="Model evaluation" width="50%">
</p>

A simple accuracy of the model is calculated using the test dataset created in the *Model Training* stage.

### Deployment
<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/big_mart_sales_prediction/media/7_deployment.png" alt="Model deployment" width="50%">
</p>

In this final stage we use the model to make a prediction with the submission dataset and store the result into a CSV file with the columns indicated in the hackathon.

## Results
Files used to create the model are: **test.csv** and **train.csv** that can be found in this repository. The submitted file is **out.csv**, produced by our pipeline, that can also be found in  this repository.

During the evaluation the model showed up a 61% accuracy. Once submited our results to the [hackathon](https://www.analyticsvidhya.com/datahack/contest/practice-problem-big-mart-sales-iii) and got a score of **1152.2938**, placing our submission in the 1189 place of the total 52384 participants by the time of the submission (February 18th, 2025).

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/big_mart_sales_prediction/media/8_submission_results.png" alt="Submission results" width="100%">
</p>

