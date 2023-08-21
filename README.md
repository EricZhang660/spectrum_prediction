# spectrum_prediction
The colab jupyter notebook used in SDIC individual project

It is highly recommended to view in Google Colab platform, you can directly visit it by clicking the blue buttom "open in colab" on the top of 'spectrum_prediction.ipynb' file. There are some viewing problem in Github page.


There are in total 8 parts in the 'spectrum_prediction.ipynb': 'package import', and 'part 0' to 'part 7'. While part 0 to part 7 can all be executed independently, you have to run 'package import' section everytime, since it install and import essential packages to be used in rest of notebook.

The 'spectrum_prediction.ipynb' is now accessible to everyone as visitors on Google Colab, that is, you can view the code on it. If you wish to execute some of these codes, and load the trained machine learning models which is stored in my Google Drive, feel free to send me email and provide your Gmail account, so that I can add you to be editor.

## Introduction of each parts' functionality

### Part 0: pre-process raw dataset

Do the explotary data analysis on the raw dataset. Decide the format of ground-truth spectrum data, convert molecule name to SMILES encoding notations, as well as retrieve ECFP of each molecules using SMILES.

### Part 1: Base Model

train the base model on the training dataset usinng 5-fold cross validation technique, and then test on the test set.

### Part 2: Random Forest

train the random forest model on the dataset. Test how the different n_estimators affect its performance on validation set. Finally select random forest with 300 tree-like estimators as the candidate model, and test its performance on test set.

### Part 3: vanilla MLP model

train the vanilla MLP model on the training dataset usinng 5-fold cross validation technique, and then test on the test set.

### Part 4: cnn MLP model

train the cnn MLP model on the dataset. Test how the different amount of CNN layer affect its performance on validation set. Finally select 3-layer cnn MLP as the candidate model, and test its performance on test set.

### Part 5: Feature Importance Evaluation

For each feature, use itself alone to fit the random forest with 300 tree-like estimators, and its resultant performance on test set is used to evaluate its importance.

### Part 6: Evaluate the effect of m/z position

For base model, random forest, vanilla MLP and cnn MLP, make the m/z position feature becomes a zero-like vector, while other features remain same. Then train these models on the training set, make comparison between their resultant performance on test set with previous ones.

### Part 7: Inference result evaluation

generate the output using trained models, and then visualise the box plotting of pearson correlation coefficient, distribution of weighted cosine similarity and the comparison between predicted spectrum data and the grounf-truth spectrum data.

