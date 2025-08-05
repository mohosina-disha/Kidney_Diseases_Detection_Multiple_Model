# Kidney Disease Classification with Deep Learning

This repository contains four deep learning models for classifying kidney diseases (Normal, Cyst, Tumor, Stone) using the CT-Kidney-Dataset from Kaggle. The models are implemented in Google Colab using TensorFlow and include data augmentation, class balancing, and interpretability features.


# Models

All models are stored in the /models/ directory as .ipynb notebooks :

VGG-16: Transfer learning with pre-trained VGG-16, fine-tuned for kidney disease classification. Achieves ~100% accuracy and robust AUC (~1.00).

ResNet-50: Pre-trained ResNet-50 with custom layers, yielding ~99% accuracy and robust AUC (~1.00).

Custom CNN: 17-layer CNN with Conv2D, BatchNormalization, and Dropout. Achieves ~99.95% accuracy and AUC ~1.00.

Inception V3: Transfer learning with Inception V3, fine-tuned for high accuracy (~99%) and AUC ~1.00.


# Features

Data Preprocessing: Stratified train-validation-test split (70-15-15), extensive data augmentation (rotation, zoom, flips).

Class Balancing: Class weights to handle imbalance (e.g., Tumor and Stone classes have fewer samples).

Interpretability: Saliency maps and Class Activation Maps (CAM) to highlight key image regions for predictions.

Evaluation: ROC curves, confusion matrices, and classification reports for model performance.

Training: Uses Adam optimizer, categorical cross-entropy, and callbacks (EarlyStopping, ReduceLROnPlateau, ModelCheckpoint).

Directory Structure





/models/: Contains .ipynb notebooks for VGG-16, ResNet-50, Custom CNN, and Inception V3.



/README.md: Project overview and instructions.


# Usage

Clone the repository: git clone <repo-url>

Run .ipynb files in Google Colab with the Kaggle dataset.

Load .keras models for inference using TensorFlow.

Refer to notebooks for preprocessing, training, and visualization details.


# Requirements

Python 3.11

TensorFlow, NumPy, Matplotlib, Seaborn, Scikit-learn

Kaggle API for dataset download


# Results

Custom CNN: Accuracy (~99.95%) and AUC (~1.00) with balanced performance across classes.

Inception V3 & ResNet-50: Strong performance (~99% accuracy, AUC ~1.00).

VGG-16: Heighest Accuracy (~100% accuracy).

Visualizations: ROC curves, confusion matrices, saliency maps, and CAM for interpretability.


# License

This project is licensed under the MIT License.