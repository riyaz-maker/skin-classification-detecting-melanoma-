# Skin Cancer Classification: Detecting Melanoma
This repository contains the code and resources for a deep learning project focused on the classification of skin lesions, specifically for detecting melanoma. The project explores the use of hybrid models that use both image data and patient metadata to improve classification accuracy. Two different convolutional neural network (CNN) backbones, EfficientNet-B3 and ResNet-50, are implemented and evaluated.

## Key Features
### Hybrid Deep Learning Models:
Combines CNN-based image feature extraction with metadata processing (patient age and sex) for a more holistic classification approach.
Two Advanced Architectures:
EfficientNet-B3, ResNet-50
### Attention and Modulation Mechanisms:
Efficient Channel Attention (ECA): A lightweight channel attention module to enhance informative features.
Feature-wise Linear Modulation (FiLM): A technique to dynamically adjust image features based on metadata.
Training Techniques:
Focal Loss: To address class imbalance between melanoma and non-melanoma lesions.
OneCycleLR Scheduler: For efficient and effective learning rate scheduling.
Data Augmentation: Using Albumentations and torchvision to create a more robust model.
### Model Interpretability:
Grad-CAM: Generates heatmaps to visualize the regions of the image that the model focuses on for its predictions.
Models are evaluated using multiple metrics including ROC AUC, Accuracy, Sensitivity, and Specificity.
## Architecture Overview
Image Feature Extraction: A pre-trained CNN backbone (EfficientNet or ResNet) extracts high-level features from the input skin lesion image.
Attention: An ECA block is applied to the final feature map from the backbone to refine channel-wise features.
Metadata Integration: A FiLM layer modulates the image features using the patient's metadata, allowing the model to learn context-specific representations.
Classification Head: A multi-layer perceptron (MLP) processes the combined image and metadata features to produce the final classification (Melanoma vs. Non-Melanoma).
## CAM images:
![CAM_ISIC_0012092_p0 32](https://github.com/user-attachments/assets/82e2b7a4-6ff8-4a6c-8f4e-57a68f523378)
![CAM_ISIC_0012086_p0 26](https://github.com/user-attachments/assets/785b8f96-0415-4749-9e96-d10997983b4c)
## Future Improvements:
Ensemble Models: Combine the predictions from both the EfficientNet and ResNet models to potentially improve performance.
