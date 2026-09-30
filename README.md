# 😷 Mask or No Mask

A simple **Image Classification** project built with **Python, Tkinter, and ML for Kids**.

This project is designed to recognize whether a person is wearing a **mask** or **not wearing a mask**.

---

## 🧠 How the Project Works

In this project, we first create and train an image classification model using **ML for Kids**.

After training the model, the project is connected to our Python program using the `MLforKidsImageProject` library.

The model is then trained/prepared on the local system when the Python program starts.

The basic workflow is:

```text
Training Images
      ↓
ML for Kids
      ↓
Train the Image Classification Model
      ↓
Connect the Model to Python
      ↓
Local Model Training / Preparation
      ↓
Upload an Image
      ↓
Image Classification
      ↓
Mask / No Mask + Confidence
```

The project contains a set of images for training the model and several separate images that can be used for testing the classifier.

---

## 📁 Project Files

The project contains the following important files:

```text
Mask-or-No-Mask/
│
├── main.py
├── pip.txt
├── mobilenet-v2-tensorflow2-140-224-classification-v2
├── mask.zip
│
└── Test Images
```

### `main.py`

The main Python program.

It creates the graphical interface using **Tkinter**, allows the user to upload an image, sends the image to the trained model, and displays the classification result and confidence percentage.

### `pip.txt`

Contains the Python libraries required by the project.

You can install all required libraries with:

```bash
pip3 install -r pip.txt
```

### `mobilenet-v2-tensorflow2-140-224-classification-v2`

This is one of the downloaded model files used by the project.

### `mask.zip`

Contains the project image data used for the mask classification project.

The project also includes several images for testing the trained classifier.

---

## 🖼️ Image Classification

The model is trained to recognize two classes:

* 😷 **Mask**
* 🚫 **No Mask**

When an image is uploaded, the model returns:

* The predicted class
* The confidence percentage

For example:

```text
result: 'Mask' with 94% confidence
```

---

## 🖥️ Graphical Interface

The application is built with **Tkinter**.

The interface includes:

* 😷 Project title
* 📸 Image display area
* 📁 Upload Image button
* Classification result
* Confidence percentage

The uploaded image is resized to:

```text
280 × 330
```

before being displayed in the application.

---

## 🚀 Installation

### 1. Install Python

Make sure Python is installed on your system.

### 2. Download or clone the project

Download all project files and place them in the same project folder.

### 3. Install the required libraries

Open a terminal inside the project folder and run:

```bash
pip3 install -r pip.txt
```

### 4. Run the project

Run:

```bash
python main.py
```

---

## 🔍 Making a Prediction

After starting the program:

1. Open the application.
2. Click **📁 Upload Image**.
3. Select an image from your computer.
4. The model analyzes the image.
5. The result is displayed on the screen.
6. The application shows the predicted class and its confidence percentage.

Example:

```text
result: 'No Mask' with 87% confidence
```

---

## 🧩 Main Python Components

The project uses:

```python
import tkinter as tk
from PIL import Image, ImageTk
from tkinter import filedialog
from mlforkidsimages import MLforKidsImageProject
```

The ML for Kids project is initialized using:

```python
myproject = MLforKidsImageProject(key)
```

The model is then trained/prepared with:

```python
myproject.train_model()
```

When the user uploads an image, the prediction is performed with:

```python
demo = myproject.prediction(path_image)
```

The predicted class is obtained using:

```python
label = demo["class_name"]
```

and the confidence is obtained using:

```python
confidence = demo["confidence"]
```

The final result is displayed as:

```python
result: 'Class Name' with XX% confidence
```

---

## 🔄 Prediction Process

The image prediction process works like this:

```text
User clicks Upload Image
          ↓
Select an image
          ↓
Read the image path
          ↓
Send image to the ML model
          ↓
Model predicts the class
          ↓
Get class name
          ↓
Get confidence
          ↓
Display result in Tkinter
```

---

## 🛠️ Technologies Used

* **Python**
* **Tkinter**
* **Pillow (PIL)**
* **ML for Kids**
* **MobileNet V2 model**
* **Image Classification**

---

## 📦 Requirements

The required Python packages are listed in:

```text
pip.txt
```

Install them using:

```bash
pip3 install -r pip.txt
```

---

## 🎯 Project Goal

The goal of this project is to create a simple practical example of **Artificial Intelligence and Image Classification**.

Instead of manually checking an image, the trained model can analyze it and predict whether the image belongs to the **Mask** or **No Mask** class.

This project also demonstrates how an image classification model can be connected to a Python desktop application with a graphical interface.

---

## ⚠️ Important Note

The classification result depends on the images used to train the model.

The confidence percentage is the model's prediction confidence and does not guarantee that the prediction is always correct.

For better results, the training dataset should contain enough diverse images with different:

* Faces
* Lighting conditions
* Angles
* Backgrounds
* Types of masks
* Image qualities

---

## 👨‍💻 Author

**Amir**

---

## 📄 License

This project is created for educational and learning purposes.
