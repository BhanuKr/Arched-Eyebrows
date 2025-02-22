# Arched Eyebrows Detection using ResNet18

## Overview
This project aims to classify images based on the presence of the 'Arched Eyebrows' attribute using ResNet18. The dataset used is a subset of CelebA, with images and corresponding attribute labels. The model is trained on the training set and evaluated using precision, accuracy, F1 score, ROC curve, and confusion matrix.

## Dataset
- **Dataset Name**: CelebA (Subset)
- **Files Used**:
  - `image_align_celeba/` (Folder containing images)
  - `face_image_attr.csv` (Contains attributes for each image)
  - `face_image_eval_partition.csv` (Specifies dataset split: train (0), validation (1), test (2))

## Model
- **Architecture**: ResNet18
- **Framework**: PyTorch
- **Loss Function**: Binary Cross-Entropy Loss
- **Optimizer**: Adam
- **Metrics Used**:
  - Accuracy
  - Precision
  - Recall
  - F1 Score
  - ROC Curve
  - Confusion Matrix

## Installation
To set up the environment, run:
```bash
pip install -r requirements.txt
```
## Training 
To train the model, run:
```bash
python train.py --epochs 10 --batch_size 32 --lr 0.001
```
## Evaluation
To evaluate the model, run:
```bash
python evaluate.py --model_path models/resnet18.pth
```
## Results
The model performance is evaluated using the test set.
Key evaluation metrics include accuracy, precision, recall, F1 score, and ROC-AUC.
The confusion matrix is used to analyze misclassifications.

## Repository Structure
The project directory is structured as follows:
```bash
├── image_align_celeba/          # Image dataset folder
├── face_image_attr.csv          # Attributes file
├── face_image_eval_partition.csv# Dataset split file
├── train.py                     # Training script
├── evaluate.py                  # Evaluation script
├── model.py                     # ResNet18 model definition
├── requirements.txt             # Dependencies
├── README.md                    # Project documentation
```

## Dataset
CelebA - https://www.dropbox.com/scl/fi/7m0pt1dkmwbkr3byv5r2j/face_images.zip?rlkey=r2gqsdvuyvpqqk4a7bjd9kcvv&st=nj7wl35d&dl=1

