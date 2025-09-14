This pipeline is implemented to illustrate the use of MSLToolbox Code Generator, you can find details on the [MLSToolbox Code Generator Wiki](https://github.com/MLSToolbox/mls_code_generator/wiki). We encourage to read the information provided in that link to understand the problem that the pipeline is trying to solve.

The pipeline is composed of 4 stages:
- *Data collection*, which loads the colour images of the CIFAR-10 dataset and their labels.
- *Feature Engineering*, where the data is normalized (scaling pixel values to range [0,1]), a smaller subset for faster training is selected and the columns are selected
- *Model Training*, where the dataset obtained in the previous stage is split in train and test data and the model is trained with a SVM algoritm
- *Model Evaluation*, where using the test data, predictions are performed and a classification report is generated with the predictions, the confusion matrix and metrics such as precision, recall, f1-score and support
 
<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/svm_image_classification/media/0_main.png" alt="Main editor" width="75%">
</p>

## Stages
### Data Collection
A stage with two tasks that load the images of the CIFAR-10 dataset and the labels file

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/svm_image_classification/media/1_data_collection.png" alt="Data collection" width="50%">
</p>

### Feature Engineering
A stage with four tasks, one for selecting a smaller subset of data for faster training, another for normalizing the data and the other two for selecting the columns for training
<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/svm_image_classification/media/2_feature_engineering.png" alt="Feature engineering" width="75%">
</p>

### Model Training
A stage with a task for splitting the data into train and test data. The training data is used to train a model with a SVM algorithm.

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/svm_image_classification/media/3_model_training.png" alt="Model training" width="75%">
</p>

### Model evaluation
Finally, a stage with 2 tasks for making predictions and evaluating the trained model providing the confusion matrix and metrics such as precision, recall, f1-score and support

<p align="center" width="100%">
   <img src="https://github.com/MLSToolbox/mls_pipeline_examples/blob/main/svm_image_classification/media/4_model_evaluation.png" alt="Model evaluation" width="50%">
</p>


