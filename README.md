The purpose of this project is to develop an AI system for the detection and
classification of degenerative lumbar conditions using DICOM images. The problem requires
a multi-label classification model that can classify five degenerative conditions across five
lumbar spine levels (L1/L2 to L5/S1) with three severity scores (Normal/Mild, Moderate, or
Severe). We have been tasked with classifying five degenerative conditions in lumbar spine
MR images across multiple intervertebral disc levels. For each level, the AI model should
predict the severity for each of the following conditions.

This is a Multi-Label Classification problem since we have multiple conditions (labels) for each image. For each intervertebral level (L1/L2 to L5/S1), we will predict five degenerative conditions, each with three possible classes (Normal/Mild, Moderate, Severe).

we will leverage deep learning, specifically Convolutional Neural Networks (CNNs), combined with the available labeled data. The problem requires a multi-label classification model that can classify five degenerative conditions across five lumbar spine levels (L1/L2 to L5/S1) with three severity scores (Normal/Mild, Moderate, or Severe).

We have been tasked with classifying five degenerative conditions in lumbar spine MR images across multiple intervertebral disc levels. For each level, the AI model should predict the severity for each of the following conditions:

1)Left Neural Foraminal Narrowing (LNFN)
2)Right Neural Foraminal Narrowing (RNFN)
3)Left Subarticular Stenosis (LSS)
4)Right Subarticular Stenosis (RSS)
5)Spinal Canal Stenosis (SCS) Each of these conditions has severity scores ranging from Normal/Mild, Moderate, or Severe.

We have used deep learning frameworks like TensorFlow and keras, which is a neural network library and is available as an open-source project to facilitate deep learning model development. Keras abstracts most of the complexity usually associated with deep learning and offers an intuitive interface for model development and training
Used a CNN architecture that can extract features from medical images. Since medical images are complex, start with a pre-trained model (like ResNet or EfficientNet) to perform transfer learning.
We will fine-tune a ResNet50 model pre-trained on ImageNet and add custom layers for multi-label classification.
The output layer has 15 neurons (5 conditions * 3 severity levels), and we use a softmax activation because each output corresponds to a class (Normal/Mild, Moderate, Severe).
The input data will consist of preprocessed images of shape (224, 224, 3).
We need to provide corresponding multi-label encodings for each of the five conditions across five spine levels.
Loss Function: Used categorical_crossentropy for multi-class classification.
