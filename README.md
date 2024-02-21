# **UFC 파이터 이미지 분류 프로젝트**
## **개요**
이 프로젝트는 UFC 파이터의 이미지를 정확하게 식별하고 분류할 수 있는 이미지 분류 모델을 개발하는 것을 목표로 합니다. 본 모델은 컨볼루션 신경망(CNN)을 사용하여 준비된 데이터셋에서 파이터들의 시각적 특징을 바탕으로 서로 다른 파이터들을 구별하도록 학습합니다.

본 프로젝트에서 가장 중요한 점은 포즈, 조명, 배경, 장비 등에 따라 다양한 형태로 달라지는 파이터 이미지를 정확하게 분류하는 것입니다. 이러한 변이성으로 인하여 다른 파이터의 이미지와 구별하면서도 같은 파이터의 다른 이미지들 간의 일관된 특징을 식별하는 일이 도전적인 일입니다.

## **해결책**
이 도전과제를 해결하기 위하여 파이터의 이미지에서 미묘한 시각적 패턴을 포착하도록 맞춤화된 CNN 기반 모델을 개발했습니다. 해결책은 다음의 몇 가지 주요 단계를 포함합니다:

**데이터 준비:** 파이터 클래스에 해당하는 라벨이 붙은 이미지를 수집하고, 이 데이터셋을 학습과 검증으로 분할하여 모델이 새로운 이미지도 분별할 수 있도록 합니다.  
**모델 구조:** CNN 모델은 이미지의 계층적 패턴에서 추출하고 배우도록 설계된 여러 레이어로 구성됩니다. 모델은 에지나 텍스쳐같은 로우레벨 특징들을 캡쳐하기 위한 컨볼루션 레이어로 시작하여 점차 각 파이터의 독특한 시각적 특징을 정의하는 더 추상적인 기능들로 발전합니다.  
**훈련 및 평가:** 모델은 분류 오류를 최소화하는 데 중점을 두고 훈련 데이터셋을 사용하여 훈련됩니다. 성능은 검증 세트에서 평가되어 정확성과 일반화 능력을 보장합니다.  

## **구현 세부사항**
**데이터 증강:** 모델의 강건성을 향상시키기 위해 로테이션, 스케일링, 수평 뒤집기와 같은 데이터 증강 기술이 사용됩니다.  
**최적화:** 모델은 최상의 성능을 달성하기 위해 세밀하게 조정된 이진 교차 엔트로피 손실 함수(binary cross-entropy loss function)와 함께 Adam 최적화기를 사용합니다. 


# **Fighter Image Classifier Project**

## **Overview**
This project aims to develop an image classification model that can accurately identify and classify images of fighters. Utilizing a convolutional neural network (CNN), the model learns to distinguish between different fighters based on their visual features from a curated dataset.

## **Problem Statement**
The challenge lies in accurately classifying images of fighters, which may vary significantly in terms of pose, lighting, background, and equipment. Such variability introduces complexity in identifying distinctive features that are consistent across different images of the same fighter while differentiating them from images of other fighters.

## **Solution**
To address this challenge, we developed a CNN-based model tailored to capture the nuanced visual patterns present in images of fighters. The solution involves several key steps:

**Data Preparation:** Images are collected and labeled with their corresponding fighter class. This dataset is then split into training and validation sets to ensure the model can generalize well to new, unseen images.

**Model Architecture:** The CNN model consists of several layers designed to extract and learn from the hierarchical patterns in the images. Starting with convolutional layers to capture low-level features such as edges and textures, the model progressively builds up to more abstract features that define each fighter's unique visual signature.

**Training and Evaluation:** The model is trained using the training dataset with a focus on minimizing classification error. Performance is evaluated on the validation set to ensure accuracy and the ability to generalize.

## **Implementation Details**
**Data Augmentation:** To enhance the robustness of the model, data augmentation techniques such as rotation, scaling, and horizontal flipping are employed.

**Optimization:** The model uses the Adam optimizer with a binary cross-entropy loss function, fine-tuned to achieve the best performance.  

