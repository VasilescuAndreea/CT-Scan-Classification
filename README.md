**Title: CT Scan Classification Challenge**

## Overview
This project is a machine learning challenge focused on classifying CT scans of lungs. Competitors are tasked with training machine learning models to achieve the highest classification accuracy on a given test set. The dataset includes three folders containing CT scan images, each labeled with a corresponding CSV file indicating the image's class label. The project was implemented using Google Colab, initially in a Jupyter Notebook format (`.ipynb`) and later transformed into a Python script (`.py`).

## Data Explorer
- `train`: Folder with 3900 PNG images of CT scans.
- `validation`: Folder with 15,000 PNG images of CT scans.
- `test`: Folder with 3900 PNG images of CT scans.
- `train_labels.csv`: CSV file indicating labels for the `train` folder.
- `validation_labels.csv`: CSV file indicating labels for the `validation` folder.
- `test_labels.csv`: CSV file indicating labels for the `test` folder.

## Essential Information
- The classifier is non-linear, using Softmax as the activation function and ReLU in the neural network.
- Hyperparameters include the number of layers and features in the network.
- Learning rate is set to 0.001.

## Confusion Matrix
- Provides insight into the model's performance with counts of true positives, true negatives, false positives, and false negatives.

## Observations
- Training for too many epochs may lead to diminishing returns.
- Best achieved accuracy on personal tests: 0.68 on Google Colab and 0.66 on Kaggle.

## Detailed Code Description
1. **Processing `train.txt` Content - Goal: Training**
   - Extracted paths and labels from `train.txt`.
   - Created a dataset and verified the accessibility of images.
   - Initialized a DataLoader for efficient training.

2. **Neural Network Architecture**
   - Empirically determined hyperparameters.
   - Utilized a single input channel due to grayscale images.
   - Set kernel size to 5 for a 5x5 block.

3. **Training Phase**
   - Trained the neural network for 100-300 epochs.
   - Monitored training progress through print statements.
   - Achieved optimization for training time, reducing from 30 minutes to 7-12 seconds.

4. **Testing and Evaluation**
   - Created a DataLoader for the testing phase.
   - Evaluated the neural network's accuracy on the validation set.
   - Generated predictions for the test set and created the `test_submission.txt` file.

## Challenges Encountered
1. Initial difficulties with Anaconda installation on a personal laptop.
2. Issues with document uploading on Google Drive, leading to the decision to use Google Colab.
