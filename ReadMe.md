# Object Classification using Keras, TensorFlow, and Tranfer Learning
Dataset Link: https://drive.google.com/open?id=1LMZOq-8wsXgox_4yIdU2Z_GMhKYhiTKM

Image Augmentation was used to increase the datset size and to increase variance in each class by rotating, resizing, shifting, shearing and so.

## A General ML Framework:
![](https://github.com/E-B-Manohar/Black-Hole-Source/blob/master/Images/References/DS/a%20general%20ml%20model.png)

## Summary
Object Classification Transfer Learning Model Comparision Report.pdf
(The training is done using Google's Colab using GPUs.)
### Models used:
Xception (Loaded from Keras library)
MobileNetV2
AlexNet
FaceNet (Manually loaded weights from internal storage)
Custom NN (~10 layer NN, trained for hours with lots of epochs. Reason is that the NN has no clue about any feature in the given dataset and took a lot of time and effort to understand the images)


## Loss function
categorical_crossentropy - since the problem statement is about classifing the images and there are more than 2 classes or multiclasses.

## Accuracy
The validation accuracy of various models are very high as the transfer learning method is used. The reason for this is the pretrained models has already figured out most of the features by understanding 1000 class images with lot of variance.
Because of this reason, the training time is short and the best results are achieved from vey less number of epochs.

# Model Comparisons:
Xception Performance:
![](https://github.com/E-B-Manohar/Object-Classification-with-Keras-using-Transfer-Learning/blob/master/Xception%20Accuracy%20Result.png)

MobileNetV2 Performance:
![](https://github.com/E-B-Manohar/Object-Classification-with-Keras-using-Transfer-Learning/blob/master/MobileNetV2%20Accuracy%20Result.png)

FaceNet Performance:
![](https://github.com/E-B-Manohar/Object-Classification-with-Keras-using-Transfer-Learning/blob/master/FaceNet%20Accuracy%20Result.png)



Conclusion:
Xception is the best Neural Network that has understood most of the complex kernals/filters/features of wide range of images. 
Xception is Inception inspired model and has various applications to recognize wide set of images.

MobileNetV2 is obviously built for portable devices like smart phones, surveillance devices to track objects and recognize them.
Hence the small memory size.

FaceNet is mainly focused on detecting various faces and clustering the similar faces in applications like Face Clustering. Clearly, the features/kernals learnt are for only faces, yet the trainability has resulted in such great performance.
