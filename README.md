# Project Overview
The aim of this project is to evaluate and compare the prediction performances of various state of art pre-trained image classification models in classifying 5 types of flowers.
The state of art pre-trained models used in this project are InceptionResNetV2, VGG16, MobileNetV2 and ResNet50V2. The dataset used in this project was obtained from Kaggle. It consists of 5000 images of flowers categorized as Orchid, Sunflower, Tulip, Lotus and Lilly. Each category has 1000 images. Here is the Github link to the code file of the project.
# Methodology
We first implement our own basic CNN model, consisting of 2 convolution layers and one dense layer, as a baseline model. Then the 4 pre-trained models were implemented whereby the base layers were frozen from training, thus, adapting their original weights downloaded from their sources. In this way, we use the base layers as feature extractors. We then customize and train their classification layers to adapt to the 5 classes of flowers of our dataset. Finally, we compare the performance results of our baseline model and of all 4 pre-trained models. To improve the speed and performance of the learning task, we implement the following techniques;
1. Image augmentation: Given the moderate size of the training dataset, we automatically apply image augmentation techniques to increase the size in real time when training each model. Some of the techniques applied are image rotation, shifting, zooming and changes in brightness.
2. BatchNormalization: We normalize the output of each batch of the base layer to reduce the scale to a mean of 0 and a standard deviation of 1. This approach stabilizes the loss function thus increasing the learning speed through the use of higher learning rates. It also provides some regularization and therefore reduces prediction errors.
3. Early stopping: This technique is applied to automatically determine the precise number of training epochs in order to prevent overfitting.
# Summary of Prediction Results 

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/Classification%20Report%20-%20CNN.png)
Classification Report of Baseline CNN

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/Classification%20Report%20-%20VGG16.png)
Classification Report of VGG16

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/Classification%20Report%20-%20InceptionResNetV2.png)
Classification Report of InceptionResNetV2

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/Classification%20Report%20-%20MobileNetV2-%204.png)
Classification Report of MobileNetV2

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/Classification%20Report%20-%20ResNet50V2%20-%202.png)
Classification Report of ResNet50V2
