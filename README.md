# Transfer-Learning-for-Image-Classification
Implementation of transfer learning for image classification using TensorFlow and TensorFlow Hub. This project utilizes MobileNetV2 for feature extraction and fine-tunes a model to classify images of flowers.

# Dataset
The dataset used in this project is the "Flower Photos" dataset, which includes images of five types of flowers: roses, daisies, dandelions, sunflowers, and tulips. The dataset is sourced from TensorFlow and contains images organized into separate folders for each flower type. Images are resized to 224x224 pixels for input.

Source: Flower Photos Dataset
Number of Classes: 5
Image Size: 224x224 pixels
# Preprocessing
Image Loading and Resizing: Images are resized to 224x224 pixels to fit the input size of the model.
Normalization: Pixel values are scaled to the range [0, 1] by dividing by 255.
Data Splitting: The dataset is split into training and testing sets.
# Model Architecture
The model utilizes MobileNetV2 from TensorFlow Hub as a feature extractor. MobileNetV2 is pre-trained on ImageNet and used to extract features from images. A dense layer is added to MobileNetV2's output to perform classification into five flower categories.

Feature Extractor: MobileNetV2
Input Shape: 224x224 pixels with 3 colour channels (RGB)
Classification Layer: Dense layer with 5 units, corresponding to the number of flower classes

# Model Summary
Total Parameters: 2,264,389
Trainable Parameters: 6,405
Non-trainable Parameters: 2,257,984 (from MobileNetV2)
Training and Evaluation
Compilation:
Optimizer: Adam
Loss Function: SparseCategoricalCrossentropy
Metrics: Accuracy
Training: The model is trained for 5 epochs.
Evaluation: The model achieved a test accuracy of 85.2%.
