# Image-Caption-Generator

## About
Image captioning refers to generating textual descriptions or captions for images using machine learning and NLP techniques.

The image caption generator uses deep learning and computer vision to recognize the context of an image and annotate it with relevant captions. The process involves labeling the image with English keywords using the data obtained during model training, building a CNN model to extracting relevant features from the image and feeding these features to an LSTM model which generates the image caption.

Image captioning has various applications in various fields including biology, business, the internet, and in applications such as self-driving cars wherein it could describe the scene around the car, and CCTV cameras where the alarms could be raised if any malicious activity is observed. Image captioning can help in assisting the visionless with text-to-speech through real-time input about the scenario over a camera feed.

## Dataset
For this project, we are using the public dataset available at Kaggle: https://www.kaggle.com/datasets/shadabhussain/flickr8k 

The dataset contains around 8091 images and 5 captions for each image (5 * 8091 = 40455 captions).The zip file is approximately over 1 GB in size.

## Methodolody

![image](https://github.com/user-attachments/assets/8e95b17a-291e-493f-8c74-668983213cbf)

Architecture model diagram 

### VGG16 Model
We utilized a pre-trained VGG16 network for our analysis. The VGG16 model has been obtained from the following source: 
https://github.com/fchollet/deep-learning-models/releases/download/v0.1/vgg16_weights_tf_dim_ordering_tf_kernels.h5 

The VGG16 model is designed to process input images of dimensions (224, 224, 3) through a series of deep Convolutional Neural Network (CNN) layers, ultimately producing a tensor of shape (?, 1000), representing 1,000 different classes. 

### LSTM
![image](https://github.com/user-attachments/assets/9b48d2a1-265b-4268-9261-e12322602131)

LSTM model is been used beacuse it takes into consideration the state of the previous cell's output and the present cell's input for the current output. This is useful while generating the captions for the images.

## Evaluation
The generated captions are compared to the actual captions from the dataset and evaluated using BLEU scores as the evaluation metrics. A score closer to 1 indicates that the predicted and actual captions are very similar. As the scores are calculated for the whole test data, we get a mean value which includes good and not so good captions.

## Output
![image](https://github.com/user-attachments/assets/9c47527d-aa2c-48a0-b78b-c80d3efd3d21)






