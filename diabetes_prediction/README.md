# Diabetes prediction

This pipeline is the one implemented to illustrate the use of MSLToolbox Code Generator, you can find details on the [MLSToolbox Code Generator Wiki](https://github.com/MLSToolbox/mls_code_generator/wiki/Generating-pipeline-code). We encourage to read that article to understand the problem that the pipeline is trying to solve.

The pipeline is composed of 4 stages:
- *Data collection*, which will load de data from a `.csv` file
- *Feature Engineering*, where some of the values will be scaled for faster and more accurate training
- *Model Training*, where our dataset will be split in train an test and the model will be trained
- *Model Evaluation*, where using the test part of the dataset we'll assesss the accuracy of the model

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/diabetes_prediction/media/00_main.png" alt="Main editor" width="75%">
</p>

## Stages
### Data Collection
A simple stage with one only task that loads the data from the `.csv` file

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/diabetes_prediction/media/01_data_collection.png" alt="Data collection" width="50%">
</p>

### Feature Engineering

Here we separate the data into the features and the labels/truth. Afterwards, different scaling is done for the columns.

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/diabetes_prediction/media/02_feature_engineering.png" alt="Feature engineering" width="75%">
</p>


### Model Training
We get the data and split it in train and test datasets. The training part is used to train an SVM and the test part is outputed for the *Model Evaluation* stage to use.

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/diabetes_prediction/media/03_model_training.png" alt="Model training" width="75%">
</p>

### Model evaluation
Finally, with the model trained and the test data, the model can be evaluated for its accuracy.

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/diabetes_prediction/media/05_model_evaluation.png" alt="Model evaluation" width="50%">
</p>


## Results
With this configuration, the SVM can predict the columns with an accuracy of almost 60%.
