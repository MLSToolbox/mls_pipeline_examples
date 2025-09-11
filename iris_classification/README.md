# Diabetes prediction -- TO BE CHANGEd
--- I added an image to the media folder, without file I was not able to create the repository
--- this figure should be replaced with the correct one

This pipeline is implemented to illustrate the use of MSLToolbox Code Generator, you can find details on the [MLSToolbox Code Generator Wiki](https://github.com/MLSToolbox/mls_code_generator/wiki). We encourage to read that article to understand the problem that the pipeline is trying to solve.

The pipeline is composed of 4 stages:
- *Data collection*, which will load de data from a `.csv` file
- *Split*, where features data will be split into features_train and features_test data and truth data into truth_train and truth_test data
- *Model Training*, where two different models will be trained
- *Model Evaluation*, where using the test part of the dataset we'll assesss the accuracy of both models

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/iris_classification/media/0_main.png" alt="Main editor" width="75%">
</p>

## Stages
### Data Collection
A simple stage with one only task that loads the data from the `.csv` file and generate two outputs: iris_data and iris_target

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/iris_classification/media/1_data_collection.png" alt="Data collection" width="50%">
</p>

### Split

The data of both outputs obtained in the previous step are split in train and test datasets.

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/iris_classification/media/2_split.png" alt="Split" width="75%">
</p>


### Model Training
The training data obtained in the previous step is used to train a Random Regressor model and a SVC model.

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/iris_classification/media/3.1_model_training.png" alt="Model training with Linear Regressor" width="75%">
</p>

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/iris_classification/media/3.2_model_training.png" alt="Model training with SVC" width="75%">
</p>

### Model evaluation
Finally, with both model trained and the test data obtained in the Split step, both model are evaluated for their accuracy.

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/iris_classification/media/4.1_model_evaluation.png" alt="Model evaluation for Linear Regressor" width="75%">
</p>

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/iris_classification/media/4.2_model_evaluation.png" alt="Model evaluation for SVC" width="75%">
</p>

