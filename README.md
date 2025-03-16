# Overview
This project implements an image classification model using the VGG-16 architecture to classify images into 10 different animal categories.
The dataset can be downloaded from [kaggle](https://www.kaggle.com/datasets/alessiocorrado99/animals10)

![image](https://github.com/user-attachments/assets/b9bff808-7008-4ac2-af3a-954594d7ae99)

# Libraries used
- Os
- Numpy
- Pandas
- Matplotlib
- Seaborn 
- Cv2
- Datetime
- Tensorflow
- sklearn

# Data loading workflow
- A DataFrame consisting of two columns (filename, representing the image path, and class, representing the image label) was created, with each row corresponding to an image.
- The data was then split into training, validation, and test sets using the sklearn library with shuffling enabled.
- Each resulting DataFrame was passed to Keras’ ImageDataGenerator for reading images from disk in batches and applying real-time transformations.

# Model architecture
VGG-16 is a convolutional neural network that is 16 layers deep and a pretrained version of the network trained on more than a million images from the ImageNet database.

![model](https://github.com/user-attachments/assets/a2f787d8-bda7-4b71-b3f6-9444f4344303)

# Used Callbacks
1. **ModelCheckpoint** : 
This function of keras callbacks is used to save the model after every epoch.

2. **EarlyStopping** : 
This function of Keras callbacks is used to stop the model training in between, used to stop the model as soon as it gets overfitted.

3. **Learning Rate Reduction** : 
This is a very simple function of callback that can be used to tweak the learning rate over a while, This gives us the desired output based on the respective epoch.

# Model explainability
 1- __Saliency maps__ : is an image that highlights the region on which people's eyes focus first.
 
![125](https://github.com/user-attachments/assets/6bb564e5-e8b7-4467-b057-b357a09cc705)

 2- __Grad-CAM__ (Gradient-weighted Class Activation Mapping). 
 
 ![648d6](https://github.com/user-attachments/assets/d55bc1a1-5be0-4cea-9044-06d06def7adc)

 # Results
- __train loss and validation loss__
  
   ![image](https://github.com/user-attachments/assets/b178d3c0-c0dd-43a5-bbca-1e7f99281534)

- __train and validation accuracy__
  
     ![image](https://github.com/user-attachments/assets/41187aea-33cc-46fe-b78b-e9d40530c7b9)

- __Classification Accuracy__

  ![image](https://github.com/user-attachments/assets/173195ec-f4a6-4523-9811-a9015709e886)

- __Confusion Matrix__
  
  ![image](https://github.com/user-attachments/assets/fecd302f-abe2-4b09-83a3-ca6852b5c17b)

- __Classification report__
  ![image](https://github.com/user-attachments/assets/ea6936d2-9a52-4494-8485-40b2291bc076)

