# Predicting Eye Diseases with Deep Learning

In this project I used images of the fundus (back surface of the eye) to predict eye diseses 

# 1. Background
Early detection of common ocular diseases is quite difficult since few symptoms are visible in the early stage of diseases. But early detection is important and fundus screening is an economic and effective way to prevent blindness as early as possible that are caused by diabetes, glaucoma, cataract and other diseases. Image classifiaction with deep learning can be used to improve and speed up the dectection. 


# 2. Appproach
## 2.1 Data 
The used dataset is meant to represent ‘‘real-life’’ set of patient information collected by Shanggong Medical Technology Co., Ltd. from different hospitals/medical centers in China. In these institutions, fundus images are captured by various cameras resulting into varied image resolutions. 
Annotations were labeled by trained human. 

**Example from the dataset:**

<img width="733" alt="augmentation" src="https://github.com/Hi-Kay/eye_disease_prediction_deep_learning/blob/main/images/info_dataset.png">


## 2.2 Model Building
Because from most diseses the dataset only contained a few hundered images I used transfer learning. 
I tested 3 different pretrained models:
- VGG16
- Inception
- ResNet50 

I used random search and grid search to optimize the hyperparameter like dropout, learning rate and batch size. 

For the two best models I used fine tuning to improve the models.

The best model was: VGG16 

**Confusion Matrix of best Model**

<img width="733" alt="augmentation" src="https://github.com/Hi-Kay/eye_disease_prediction_deep_learning/blob/main/images/VGG_best_cm.png">


## 2.3 Web Application
On the web application you can upload your fundus image to check for diseses. 
- To build a web application I used flask: https://flask.palletsprojects.com/en/2.2.x/
- For the styling I used simple-css: https://simplecss.org
- To create the prediction graph I used: https://www.chartjs.org

**Demo**

<img width="733" alt="augmentation" src="https://github.com/Hi-Kay/eye_disease_prediction_deep_learning/blob/main/images/web_app.gif">




## Orignal Data Source
- https://odir2019.grand-challenge.org/dataset/
<!-- <img width="733" alt="augmentation" src="https://rumc-gcorg-p-public.s3.amazonaws.com/i/2020/01/21/a5d60b66.png"> -->
- https://www.kaggle.com/datasets/andrewmvd/ocular-disease-recognition-odir5k
