# Project Overview
The aim of this project is to evaluate and compare the prediction performances of various state of art pre-trained image classification models in classifying 5 types of flowers.
The state of art pre-trained models used in this project are InceptionResNetV2, VGG16, MobileNetV2 and ResNet50V2. The [dataset](https://www.kaggle.com/datasets/kausthubkannan/5-flower-types-classification-dataset) used in this project was obtained from Kaggle. It consists of 5,000 images of flowers categorized as Orchid, Sunflower, Tulip, Lotus and Lilly. Each category has 1,000 images. [Here](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/Flower%20Type%20Classfication%20-%20%20Transfer%20Learning%206%20-%20SGD%20-%20BatchNom.ipynb) is the Github link to the code file of the project.
# Methodology
We first implement our own basic CNN model, consisting of 2 convolution layers and one dense layer, as a baseline model. Then the 4 pre-trained models were implemented whereby their base layers were frozen from training, thus, adapting their original weights downloaded from their sources. In this way, we use the base layers as feature extractors. We then customize and train their classification layers to adapt to the 5 classes of flowers of our dataset. We use the same structure of the classification layer for all pre-trained models for easy comparison. Finally, we compare the performance results of our baseline model and of all 4 pre-trained models. To improve the speed and performance of the learning task, we implement the following techniques;
1. Image augmentation: Given the moderate size of the training dataset, we automatically apply image augmentation techniques to increase the size in real time when training each model. Some of the techniques applied are image rotation, shifting, zooming and changes in brightness.
2. BatchNormalization: We normalize the output of each batch of the base layer to reduce the scale to a mean of 0 and a standard deviation of 1. This approach stabilizes the loss function thus increasing the learning speed through the use of higher learning rates. It also provides some regularization and therefore reduces prediction errors.
3. Early stopping: This technique is applied to automatically determine the precise number of training epochs in order to prevent overfitting.
# Prediction Result Summary 
Below are confusion matrices and classification reports of the evaluated models for the prediction of 5 types of flowers:

A. Confusion Matrix and Classification Report of Baseline CNN

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/ROC%20-%20CNN%2060%25.png)

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/Classification%20Report%20-%20CNN.png)

B. Confusion Matrix and Classification Report of VGG16

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/ROC%20-%20VGG16%2050%25.png)

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/Classification%20Report%20-%20VGG16.png)

C. Confusion Matrix and Classification Report of InceptionResNetV2

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/ROC%20-%20InceptionResNetV2%2050%25.png)

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/Classification%20Report%20-%20InceptionResNetV2.png)

D. Confusion Matrix and Classification Report of MobileNetV2

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/ROC%20-%20MobileNetV2%2050%25.png)

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/Classification%20Report%20-%20MobileNetV2-%204.png)


E. Confusion Matrix and Classification Report of ResNet50V2

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/ROC-%20ResNet50V2%2050%25.png)

![](https://github.com/Popseli/Multiclass-Image-Classification-with-Transfer-Learning/blob/main/Classification%20Report%20-%20ResNet50V2%20-%202.png)

It can be observed that all 4 pre-trained models have achieved better performances across all metrics than the baseline CNN. The last three pre-trained models achieved the highest accuracy rates compared to the rest. One common observation across all models is that they have all attained the lowest prediction errors for the flower type 'sunflower'. However, with further adjustments to the models including training of some of the base layers and tuning of classification layers, the performances of the models can be improved.
