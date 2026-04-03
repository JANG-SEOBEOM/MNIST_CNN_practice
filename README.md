# MNIST_CNN_practice

## Overview

* CNN 기반 손글씨 숫자 분류 모델 (MNIST)
* TensorFlow / Keras를 활용한 이미지 분류 프로젝트
* Batch Normalization과 Dropout을 적용하여 성능 및 일반화 능력 개선

---

## Model Architecture

* Conv2D (16 filters, 3x3) + ReLU

* Batch Normalization

* MaxPooling (2x2)

* Conv2D (32 filters, 3x3) + ReLU

* Batch Normalization

* MaxPooling (2x2)

* Dropout (0.5)

* Fully Connected Layer (Dense 64, ReLU)

* Output Layer (Dense 10, Softmax)

---

## Features

* CNN 아키텍처 직접 설계
* 데이터 전처리

  * 정규화 (0 ~ 255 → 0 ~ 1)
  * Reshape (28x28x1)
  * One-hot Encoding
* Batch Normalization을 통한 학습 안정화
* Dropout을 통한 과적합 방지
* 모델 저장 및 재사용 가능
* 이미지 파일 기반 추론 지원

---

## Training Configuration

* Optimizer: Adam
* Loss Function: Categorical Crossentropy
* Batch Size: 32
* Epochs: 10

---

## Results

* Final Training Accuracy: **0.9896**
* Final Training Loss: **0.0329**
* Final Validation Accuracy: **0.9928**
* Final Validation Loss: **0.0240**

---

## Analysis

* Validation accuracy가 training accuracy보다 높은 것으로 보아,
  Dropout 및 Batch Normalization이 효과적으로 작용하여
  과적합 없이 안정적인 일반화 성능을 달성함.

* Training loss와 validation loss 모두 낮은 값을 유지하며 수렴하여
  모델이 데이터 분포를 잘 학습했음을 확인할 수 있음.

---

## How to Run

```bash
building model: mnist.ipynb
prediction: validation.ipynb
```
