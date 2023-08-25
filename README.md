# **Covid-19 CT Scan Image Classification**

![image](https://github.com/piyush8227/FullStack/assets/78916771/979369f8-93ec-474c-af96-c9945fecd898)

## **1. Project Description:-**
* In this project, we aim to develop an AI solution to classify CT scan images as COVID-19 positive(COVID) or negative(Non-COVID). 
* The COVID-19 pandemic has highlighted the need for efficient diagnosis, and CT scans have shown promise in aiding detection. Leveraging deep learning techniques, our project focuses on training a model to analyze CT scan images and provide accurate predictions for COVID-19 infection.
* The developed model can assist healthcare providers by offering an additional diagnostic resource, potentially contributing to faster and more accurate patient management during a critical time.

## **2. Dataset Description:-**
* This dataset contains 1252 CT scans that are positive for SARS-CoV-2 infection (COVID-19) and 1230 CT scans for patients non-infected by SARS-CoV-2, 2482 CT scans in total. 
* These data have been collected from real patients in hospitals from Sao Paulo, Brazil. 
* The aim of this dataset is to encourage the research and development of artificial intelligent methods which are able to identify if a person is infected by SARS-CoV-2 through the analysis of his/her CT scans.

## **3. Steps to run the project in system:-**
* Clone or download the repository from Github.
* Download the image data [Zip file](https://drive.google.com/file/d/1iqtiC9krc44QbLFDH0XsElI5cHoy4P56/view?usp=sharing) from here and save it to the root folder of the project.
* After that run the Code file in your desired notebook, eg. Jupyter notebook, Google Collab, VS Code.

## **4. Approach towards problem:-**

  * **Data Preprocessing:**
    * Downloaded the data.zip file and extracted the COVID and Non-COVID directories.
    * Loaded the images into list.
    * Resized the image into fixed sized of 224 X 224 and then converting images to RGB mode.
    * Normalized the pixel values of images.
  
  * **Data Augmentation:**
    * Applied data augmentation techniques on images using Keras preprocessing 'ImageDataGenerator' function.
    * Included rotation, shifting, shear, zoom, and flipping to increase data diversity.
  
  * **Data Generator & Splitting the data:**
    * Combining COVID and Non-COVID data with corresponding labels.
    * Splitting the data into Training and validation sets.
  
  * **Model Building:**
    * We used ResNet50 Model architecture which offers better performance and capacity to capture complex features.
    * Adding custom layers like Average pooling 2D layer, Dense Layers
    * Frozing the layers of the ResNet base model to avoid overwriting learned features.
    * Compiled the model using binary cross-entropy, Adam optimizer and performance metrics as accuracy.
  
  * **Model Training:**
    * Defined early stopping and model checkpoint callbacks.
    * Trained the model using fit method with data generators for training and validation sets.
    * Saved the best model.
  
  * **Model Evaluation and Prediction:**
    * Loaded the best saved model.
    * Evaluated model using metrics like accuracy, precision, recall, F1-Score, and confusion matrix on validation set.
    * Loaded a test image, preprocessed it and used model to predict the class whether COVID or Non-COVID of the test image.
   
## **5. Tech Stack used:-**
* Python
* VS Code Jupyter Notebooks
* Tensorflow, Keras
* Visualization libraries like Matplotlib.Pyplot, and Seaborn.
* Numpy, Pandas, PIL(Pillow module), and Sklearn.


![Colourful Music Concert Event YouTube Thumbnail](https://github.com/piyush8227/FullStack/assets/78916771/2525babb-adfb-486c-8280-e39ed09ab535)

[Video demo for the project](https://youtu.be/Ir-0eR5ZO00)

## **6. References:-**
* **[Keras](https://keras.io/api/)**
* **[TensorFlow](https://www.tensorflow.org/)**
* **[Scikit Learn](https://scikit-learn.org/stable/)**
* **[Articles](https://www.sciencedirect.com/science/article/pii/S1746809422007224)**
* **[Articles](https://www.nature.com/articles/s41598-021-93832-2)**
