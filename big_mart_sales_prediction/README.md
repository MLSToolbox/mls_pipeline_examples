# Big Mart Sales Predicition

This pipeline is the one implemented for the demo at the [MLS Toolbox Wiki](https://github.com/MLS-Toobox/.github/wiki/4.1-MLS-Code-Generator-Demo's#real-case-scenario-example). We encourage to read that article to understand the problem that the pipeline is trying to solve.

The pipeline is composed of 7 stages:
- *Data Collection*, where data for training, testing and then preparing the submission for the hackthon is loaded. 
- *Data Cleaning*, where the columns thata may have null values are replaced following different strategies. This stage is performed both for the train/test data and the valid/submission data.
- *Feature Engineering*, where transformations on the data are performed to simplify the data and ensure the model only receives numeric data as inputs, as it can't process categoric data.
- *Reuse Feature Engineering*, where we perform the same processes of *Feature Engineering* to the data that is going to be submitted by also using the encoders and scalers trained.
- *Model Train*, where the data is split in train and test datasets and the model is trained
- *Model Evaluation*, where the accuracy of the model is assessed using the test dataset.
- *Deployment*, where the model is used to perform a prediction with the submission dataset and the result is stored into a CSV.

## Stages
### Data Collection
### Data Cleaning
### Feature Engieering
### Reuse Feature Engineering
### Model training
### Model Evaluation
### Deployment

