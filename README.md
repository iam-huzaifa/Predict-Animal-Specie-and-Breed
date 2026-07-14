# Cat and Dog Species & Breed Classification using Keras Functional API

## Overview

This project is a deep learning application that classifies images of cats and dogs. The model is built using the **Keras Functional API** and demonstrates how transfer learning can be applied to solve an image classification problem with multiple outputs.

The project predicts:

* **Species** (Cat or Dog)
* **Breed** (Specific breed of the animal)

This project was developed as a learning exercise to understand:

* Building multi-output models using the Keras Functional API
* Applying transfer learning for computer vision tasks
* Preparing image datasets using TensorFlow
* Training and evaluating deep learning models

---

## Features

* Multi-output image classification model
* Built using the **Keras Functional API**
* Transfer learning with a pre-trained CNN backbone
* TensorFlow data pipeline using `image_dataset_from_directory`
* Data preprocessing and normalization
* Model training with callbacks
* Performance evaluation on validation and test datasets

---

## Technologies Used

* Python
* TensorFlow
* Keras Functional API
* NumPy
* Matplotlib


---

## Model Architecture

The model uses a **pre-trained CNN** as the feature extractor through **transfer learning**.

The extracted features are shared between two output branches:

1. **Species Classification**

   * Binary classification
   * Predicts whether the image is a cat or a dog

2. **Breed Classification**

   * Multi-class classification
   * Predicts the breed of the animal

This architecture demonstrates how the Functional API allows multiple outputs to share the same feature extraction backbone.

---

## Dataset

The dataset contains images of cats and dogs along with:

* Species labels
* Breed labels

The dataset is divided into:

* Training set
* Validation set

---

## Training

During training, the following techniques were used:

* Transfer Learning
* Image normalization
* Mini-batch training
* Validation monitoring
* Model checkpointing
* Early stopping

---

## Results

### Species Prediction

The model performs well at identifying whether an image belongs to a **cat** or a **dog**.

### Breed Prediction

The model achieves noticeably lower performance when predicting the **breed** of the animal.

This limitation is expected because the project relies only on **transfer learning with a frozen pre-trained backbone**. While the extracted features are sufficient for distinguishing between cats and dogs, they are not specialized enough to capture the subtle visual differences between many breeds. As a result, breed classification performance is significantly lower than species classification.

This project is intended primarily as a learning exercise to understand multi-output classification using the Keras Functional API rather than to achieve state-of-the-art breed recognition.

---

## Limitations

* Breed prediction accuracy is relatively low.
* The feature extractor was kept frozen during transfer learning, limiting its ability to learn fine-grained breed-specific features.
* Some breeds have very similar visual characteristics, making classification more challenging.

---

## Future Improvements

Possible improvements include:

* Fine-tune the pre-trained backbone by unfreezing the top layers after transfer learning.
* Experiment with more powerful architectures such as ConvNeXt.
* Apply stronger data augmentation techniques.
* Address class imbalance problem.
* Tune hyperparameters such as learning rate, batch size, and dropout.
* Train for additional epochs after fine-tuning to improve breed classification performance.

---

## Learning Outcomes

This project helped in understanding:

* Keras Functional API
* Multi-output neural networks
* Transfer learning
* Image preprocessing with TensorFlow
* Training deep learning models
* Evaluating multiple prediction tasks
* Building an end-to-end computer vision pipeline

---

## Conclusion

This project demonstrates how to build a multi-output image classification model using the **Keras Functional API** and **transfer learning**. The model successfully classifies the species of cats and dogs, while breed prediction remains challenging due to the frozen transfer learning backbone. In future work, **fine-tuning the pre-trained model** is expected to improve feature learning and significantly enhance breed classification performance.
