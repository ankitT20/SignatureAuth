# Signature Authentication Models

This repository hosts models for signature authentication.

ARP 455 - Minor Project

## Dataset Information

### BhSig260Hindi
The BhSig260Hindi dataset consists of 260 Hindi signatures collected from different individuals. It is primarily used for Hindi signature verification tasks. Each signature in the dataset is labeled with the corresponding identity of the individual who provided the signature. The dataset captures the variability present in Hindi signatures, including different writing styles, stroke patterns, and sizes. It is a valuable resource for training and evaluating signature verification models specifically designed for Hindi signatures.

### BhSig260Bengali
The BhSig260Bengali dataset comprises 260 Bengali signatures obtained from various individuals. It is specifically designed for Bengali signature verification tasks. Similar to the BhSig260Hindi dataset, each signature in this dataset is associated with the identity of the individual who provided the signature. The dataset encompasses a range of Bengali signature characteristics, such as different writing speeds, pen pressure variations, and overall style differences. It serves as a valuable benchmark for evaluating the performance of signature verification models on Bengali signatures.

### Cedar
The Cedar dataset is a comprehensive collection of signatures captured from multiple writers. It serves as a benchmark for signature verification research and development. The dataset includes signatures from various individuals, capturing a wide range of writing styles, patterns, and characteristics. It is designed to be a challenging dataset for signature verification tasks, with variations in signatures caused by different writing utensils, writing conditions, and writing habits. The Cedar dataset is widely used in the signature verification community to evaluate and compare the performance of different models and algorithms.

## Trained Models

The repository includes the following trained models:

### Model1_SCNN
Signature verification model based on SCNN architecture.  
SCNN stands for "Signature Convolutional Neural Network." It is a specialized deep learning architecture tailored for signature verification tasks. The SCNN is designed to extract unique features from signature images, focusing on both global and local patterns that distinguish genuine and forged signatures.  
> SCNNs are often lightweight models that use custom convolutional layers and pooling mechanisms optimized for signature data. They prioritize computational efficiency while maintaining high accuracy.  

### Model2_SigNetSiamese
Signature verification model based on the Siamese network architecture using the SigNet model.  
SigNet is a pre-designed deep learning model explicitly created for signature verification. In this case, the SigNet model is used within a Siamese network architecture to compare pairs of signatures and determine their similarity.  
> SigNet focuses on extracting discriminative features from signatures. When paired with a Siamese architecture, it computes a distance metric (e.g., Euclidean distance) between feature representations of two signatures, deciding if they are from the same person.  

### Model3_Resnet50
Signature verification model based on the ResNet-50 architecture.  
ResNet-50 is a deep convolutional neural network architecture consisting of 50 layers. ResNet (Residual Networks) uses "residual connections," which help mitigate the vanishing gradient problem in deep networks.  
> ResNet-50 excels in extracting complex and hierarchical features from images, making it suitable for tasks like signature verification. Its depth allows it to learn intricate signature patterns, but it does not compare two signatures directly—it's used as a feature extractor.  

### Model4_Resnet50Siamese
Signature verification model based on the Siamese network architecture using the ResNet-50 model.  
This is a Siamese network architecture where ResNet-50 is used as the feature extractor for each input signature image.  
> Each branch of the Siamese network processes an input signature through ResNet-50, generating feature vectors. These vectors are then compared to compute the similarity or dissimilarity score. The combination of ResNet-50's deep feature extraction and the Siamese framework enhances its ability to detect subtle differences between signatures.

### Model5_Resnet18Siamese
Signature verification model based on the Siamese network architecture using the ResNet-18 model.  
Similar to the ResNet50Siamese model, but it uses ResNet-18 as the feature extractor. ResNet-18 is a shallower version of ResNet, with only 18 layers.  
> ResNet-18 is faster and computationally lighter than ResNet-50. While it may not extract features as deeply, it still performs well for signature verification tasks, especially when speed or resource constraints are important.

### Model6_EfficientNetB0Siamese
Signature verification model based on the Siamese network architecture using the EfficientNet-B0 model.  
This model employs EfficientNet-B0, a highly efficient convolutional neural network architecture, within a Siamese framework. EfficientNet-B0 is known for achieving a good balance between accuracy and computational efficiency by scaling depth, width, and resolution effectively.  
> The EfficientNet-B0 backbone provides lightweight but powerful feature extraction for signature images. Its integration into a Siamese network makes it well-suited for mobile or low-resource environments where signature verification is needed.

These models are trained to perform signature verification tasks, which involve determining the authenticity of a given signature. The models are capable of differentiating between real and forged images of signatures, providing a mechanism to detect fraudulent or unauthorized signatures.

## Usage

To use these pre-trained models, follow the instructions below:

1. Clone the repository:

```git clone https://github.com/ankitT20/SignatureAuth/```

2. Install the necessary dependencies (if any) specified in the import of each file.

> Use Google Colab , GPU & high memory needed  

View notebook on Google Colab
```
https://drive.google.com/drive/folders/1Uq7o-5rhrb3gN38-dSTJQO4IoB_yoiJL
```
### Siamese Neural Network
A Siamese Neural Network (Siamese NN) is a type of neural network architecture designed to compare two inputs by learning their similarity. It consists of two identical sub-networks (sharing the same weights and architecture), each processing one of the two inputs. The outputs from both networks are then combined (usually by computing a distance or similarity metric) to determine whether the two inputs are related or not.

How it works:

1. Input Pairs: Two inputs (e.g., two images, texts, or signals) are fed into the two identical branches of the network.


2. Feature Extraction: Each branch extracts features independently using the same set of weights.


3. Comparison: The extracted features from both branches are compared using a distance function (e.g., Euclidean distance, cosine similarity).


4. Output: The output is typically a similarity score or classification indicating whether the inputs are similar or different.



> Siamese NNs are particularly useful for tasks like signature verification, face recognition, and anomaly detection, where the goal is to determine the similarity between two data points.



Example Applications:

Signature Verification: Comparing a handwritten signature to a stored one to verify authenticity.

Face Verification: Matching two face images to determine if they belong to the same person.

One-shot Learning: Learning to recognize new classes with very few examples, as Siamese NNs focus on relationships rather than absolute classifications.


> Key Advantage: Siamese networks generalize well even with limited labeled data, as they compare inputs rather than classifying individual samples.



<!-- 
c:; cd 'C:\Users\ANKIT\Documents\VScode\SignatureAuth'; git add .; git commit -a -m "additional commit"; git push -u origin main;
git init
git branch -M main
git remote add origin https://github.com/ankitT20/SignatureAuth.git
 -->
