# weather-image-classification
Weather Image Classification using SVM, MLP, LightGBM with feature extraction methods (Machine Learning approach), and using Convolutional Neural Networks (Deep Learning approach).

A subset of the original data is included for testing purposes

ML approach:
1. run data_preprocess.ipynb - this takes images from the dataset, converts them to RBG and resizes them to 128x128
2. run feature_extraction.ipynb - this extracts HSV means and stds, Laplace variance, HOG, and LBP features from each image with different parameter combinations for HOG and LBP, and saves each combination
3. run method1_ml.ipynb - this is the main training file. It trains SVM, MLP, and LightGBM on each feature combination, using cross validation and hyperparameter tuning with grid search, saves the best performing pipeline & its confusion matrix for each model seperately for the 2 datasets and outputs classification reports.
4. test_method1.ipynb - loads saved pipelines and tests them with their best feature set combination. saves a comparison table of models

DL approach:
1. run data_preprocess.ipynb - this takes images from the dataset, converts them to RBG and resizes them to 128x128
2. run method2_CNN.ipynb - this is the main training file. It trains basic CNN archituectures with different convolutional blocks and hyperparameters, saves the best performing model & all confusion matrices for the 2 datasets and outputs classification reports.
3. test_method2.ipynb - loads saved CNN models and tests them. Also includes a test demonstration of a single image from both datasets.
