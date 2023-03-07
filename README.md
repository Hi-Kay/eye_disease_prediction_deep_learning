# Predicting Eye Diseases with Deep Learning

In this project I used images of the fundus (back surface of the eye) to predict eye diseses 

# 1. Background
# 2. Appproach
## 2.1 Data 

**Example form the dataset:**
<img width="733" alt="augmentation" src="https://github.com/Hi-Kay/eye_disease_prediction_deep_learning/blob/main/images/info_dataset.png">


## 2.2 Model Building
Because from most diseses the dataset only contained a few hundered images I used transfer learning. 
I tested 3 different pretrained models:
- VGG16
- Inception
- ResNet50 

I used random search and grid search to optimize the hyperparameter like learning rate and batch size. 

For the two best models I used fine tuning to improve the models.

The best model was: VGG16 

**Confusion Matrix of best Model**
<img width="733" alt="augmentation" src="https://github.com/Hi-Kay/eye_disease_prediction_deep_learning/blob/main/images/VGG16_best_cm.png">


## 2.3 Web Application
To build a web application I used flask. You can upload your fundus image to check for diseses. 




## Orignal Data Source
- https://odir2019.grand-challenge.org/dataset/
<!-- <img width="733" alt="augmentation" src="https://rumc-gcorg-p-public.s3.amazonaws.com/i/2020/01/21/a5d60b66.png"> -->
- https://www.kaggle.com/datasets/andrewmvd/ocular-disease-recognition-odir5k