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

### Model2_SigNetSiamese
Signature verification model based on the Siamese network architecture using the SigNet model.

### Model3_Resnet50
Signature verification model based on the ResNet-50 architecture.


<!-- 
c:; cd 'C:\Users\ANKIT\Documents\VScode\SignatureAuth'; git add .; git commit -a -m "additional commit"; git push -u origin main
git init
git branch -M main
git remote add origin https://github.com/ankitT20/SignatureAuth.git
 -->
