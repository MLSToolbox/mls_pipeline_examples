# Diabetes prediction

This pipeline is the one implemented for the demo at the [MLS Toolbox Wiki](https://github.com/MLS-Toobox/.github/wiki/4.1-MLS-Code-Generator-Demo's#simple-pipeline-example). We encourage to read that article to understand the problem that the pipeline is trying to solve.

The pipeline is composed of 4 stages:
- *Data collection*, which will load de data from a `.csv` file
- *Feature Engineering*, where some of the values will be scaled for faster and more accurate training
- *Model Training*, where our dataset will be split in train an test and the model will be trained
- *Model Evaluation*, where using the test part of the dataset we'll assesss the accuracy of the model

![main editor](https://raw.githubusercontent.com/MLS-Toobox/pipeline_examples/main/diabetes_prediction/media/00_main.png)

## Stages
### Data Collection
![data collection](https://raw.githubusercontent.com/MLS-Toobox/pipeline_examples/main/diabetes_prediction/media/01_data_collection.png)


A simple stage with one only task that loads the data from the `.csv` file

### Feature Engineering
![feature engineering](https://raw.githubusercontent.com/MLS-Toobox/pipeline_examples/main/diabetes_prediction/media/02_feature_engineering.png)

Here we separate the data into the features and the labels/truth. Afterwards, different scaling is done for the columns.

### Model Training
![model training](https://raw.githubusercontent.com/MLS-Toobox/pipeline_examples/main/diabetes_prediction/media/03_model_training.png)

We get the data and split it in train and test datasets. The training part is used to train an SVM and the test part is outputed for the *Model Evaluation* stage to use.

### Model evaluation
![model evaluation](https://raw.githubusercontent.com/MLS-Toobox/pipeline_examples/main/diabetes_prediction/media/05_model_evaluation.png)

Finally, with the model trained and the test data, the model can be evaluated for its accuracy.

## Results
With this configuration, the SVM can predict the columns with an accuracy of almost 60%.
