# Skin Disease Detection using Deep Learning (ResNet50)

## Project Overview
This project implements a deep learning-based skin disease classification system using PyTorch and transfer learning with ResNet50. The model is trained to classify RGB images of skin conditions into five disease categories.

The goal of this project is to demonstrate how convolutional neural networks (CNNs) can be applied in medical image analysis to assist in the early detection of skin diseases.

---

## Disease Classes
The model predicts the following five skin conditions:

- Acne
- Chickenpox
- Fungal Infection
- Impetigo
- Psoriasis

---

## Dataset
The dataset used in this project was obtained from Kaggle and contains labeled RGB images of the five skin diseases. Each class is stored in separate folders and loaded using `torchvision.datasets.ImageFolder`.

### Dataset Split
- Training Set: 70%
- Validation Set: 15%
- Test Set: 15%

---

## Data Preprocessing and Augmentation
To improve model generalization and robustness, several preprocessing and augmentation techniques were applied:

- Image resizing
- Random resized cropping
- Horizontal flipping
- Random rotation
- Color jitter
- Normalization

These transformations help the model learn invariant features under different lighting and orientation conditions.

---

## Handling Class Imbalance
Since the dataset contains different numbers of images per class, WeightedRandomSampler was used during training to balance the sampling probability so that minority classes appear more frequently.

---

## Model Architecture
The model uses a pretrained **ResNet50** architecture with transfer learning. The final fully connected layer was modified to output predictions for the five skin disease classes.

Framework: PyTorch  
Base Model: ResNet50 (Pretrained on ImageNet)

---

## Training Configuration

Epochs: 15  
Optimizer: Adam  
Loss Function: CrossEntropyLoss  
Learning Rate: 0.0001  
Batch Size: 32  

---

## Model Performance

Test Accuracy: 99.26%

Evaluation metrics used:

- Precision
- Recall
- F1 Score
- Confusion Matrix

The confusion matrix helps visualize how well the model distinguishes between different disease classes.

---

## External Image Testing
The trained model was also tested on external images not included in the dataset to evaluate real-world performance. The model predicts the disease class along with a confidence score.

---

## How to Run
1. Clone the repository
2. Install dependencies using the provided requirements file
3. Open the notebook
4. Run the cells sequentially to train or test the model

---

## Future Work
Future improvements include integrating the image classification model with a small language model to generate explanations and guidance for detected skin diseases, creating a multimodal AI system.

---

## Pretrained Model

The trained model weights can be downloaded from the link below:

https://drive.google.com/file/d/16UfWNLoAFsdUQyUv_Yh40xGhackVik64/view?usp=sharing

After downloading, place the file in the project directory before running the notebook.

---

## Disclaimer
This project is intended for educational and research purposes only and should not be used as a substitute for professional medical advice.