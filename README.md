#  Cat vs Dog Image Classification using CNN

##  Project Overview

This project is a **Cat vs Dog Image Classification** project using a **Convolutional Neural Network (CNN)**.

The model is trained to identify whether an input image belongs to the **Cat** class or **Dog** class.

---

##  Objective

The main objective of this project is to build a deep learning model that can automatically classify images into two categories:

*  Cat
*  Dog

---

##  Dataset Overview

The dataset contains separate folders for training and testing images.

* **Training Images:** 8,005
* **Testing Images:** 2,023
* **Number of Classes:** 2

### Classes

| Class | Label |
| ----- | ----: |
| Cat   |     0 |
| Dog   |     1 |

---

##  Technologies Used

* Python
* NumPy
* Matplotlib
* TensorFlow
* Keras
* CNN (Convolutional Neural Network)
* Jupyter Notebook

---

##  Project Workflow

The project follows these steps:

1. Import required libraries
2. Load the dataset
3. Image preprocessing
4. Data augmentation
5. Create CNN model
6. Compile the model
7. Train the model
8. Use Early Stopping
9. Evaluate the model
10. Visualize Accuracy and Loss
11. Save the trained model
12. Load the saved model
13. Predict new images

---

##  Image Preprocessing

Images are resized to:

**128 × 128 pixels**

Pixel values are normalized using:

**1 / 255**

Data augmentation is also applied to the training images using:

* Shear
* Zoom
* Horizontal Flip

These techniques help the model learn from different variations of images and improve generalization.

---

##  CNN Model Architecture

The CNN model consists of:

* Conv2D Layer – 32 filters
* MaxPooling2D
* Conv2D Layer – 64 filters
* MaxPooling2D
* Flatten
* Dense Layer – 128 neurons
* Dropout – 0.5
* Output Layer – 1 neuron with Sigmoid activation

### Why CNN?

CNNs are commonly used for image classification because they can automatically learn important visual features such as:

* Edges
* Shapes
* Colors
* Patterns
* Object features

---

##  Model Compilation

The model uses:

* **Optimizer:** Adam
* **Loss Function:** Binary Crossentropy
* **Evaluation Metric:** Accuracy

Since this is a binary classification problem, binary crossentropy with sigmoid activation is used.

---

##  Early Stopping

Early Stopping is used to prevent unnecessary training and reduce overfitting.

The model monitors **validation loss** and stops training when the validation performance stops improving.

---

##  Model Performance

The model achieved approximately:

* **Test Accuracy:** 80.82%
* **Test Loss:** 0.4462

This means the model correctly classified approximately **81 out of 100 test images**.

---

##  Accuracy and Loss Analysis

### Accuracy

The training and validation accuracy increased during training, showing that the model learned useful image features.

The final training accuracy was approximately **84.6%**, while validation accuracy was approximately **80.4%**.

The relatively small gap between training and validation accuracy suggests that the model did not show severe overfitting.

### Loss

Training and validation loss decreased during training, indicating that the model was learning and reducing prediction errors.

---

##  Model Saving

The trained model is saved as:

`cat_dog_cnn.h5`

The saved model can later be loaded and used to classify new images without training the model again.

---

##  Prediction

The trained model can accept a new image and predict whether it is:

**Cat  or Dog **

The prediction score is generated using the sigmoid output.

* Score < 0.5 → Cat
* Score ≥ 0.5 → Dog

---

##  Project Structure

```text
Cat-Dog-CNN/
│
├── Cat&Dog CNN Model.ipynb
├── cat_dog_cnn.h5
├── README.md
└── images/
```

---

##  Future Improvements

The model can be improved further by:

* Using a larger CNN architecture
* Increasing image resolution
* Applying more data augmentation
* Using Transfer Learning
* Trying pretrained models such as MobileNet, VGG16 or ResNet
* Hyperparameter tuning
* Adding a Streamlit web application

---

##  Limitations

The model achieves around **80.8% test accuracy**, so it may sometimes misclassify images.

Performance can be affected by:

* Image quality
* Lighting
* Background
* Object position
* Unusual cat or dog images

---

##  Conclusion

The **Cat vs Dog Image Classification** project successfully uses a CNN model to classify images into Cat and Dog classes.

The model achieved approximately **80.82% test accuracy** and learned important image features using convolution and pooling layers.

This project demonstrates how **Deep Learning and CNNs can be used for real-world image classification tasks**.
