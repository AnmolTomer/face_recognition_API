# face_recognition_API

Face Recognition Web App Made with Flask.

## Development Life Cycle

- The development life-cycle followed to build this project was:

  - Understanding Data 📊🧠
  - Image Analysis 📷📸
  - Predictive Modelling 🚀⏱
  - Model Selection 🎯✅
  - Rest APIs in Flask 💻👩🏻‍💻✨

## 1. Setting Up Your Development Environment

### NOTES:

- We start by gathering data which is initially in highly unstructured form. Then we use image processing techniques in OpenCV to understand the data.
- After doing data preprocessing and EDA we move on to extracting features from images like computing Eigen Images with PCA and similar value decomposition.
- With Eigen Images we train the ML model and learn to test our model before deploying it, if required we will tune our model for best results.
- Once ML model is ready we will develop Web Server Gateway Interface in Flask. Frontend will use HTML,CSS and Bootstrap and Backend will be Python.
- We try to create a image processing application which tried to detect the face and then classify the gender into 2 classes MALE or FEMALE.

### Setup Venv - Windows

```bash
pip install --user virtualenv
python -m venv face_recognition
.\face_recognition\Scripts\activate
```

### Setup Venv - Linux

```bash
pip install --user virtualenv
python -m venv face_recognition
source face_recognition/bin/activate
```

### Installing OpenCV

- First install other dependencies such as numpy, sklearn, just run `pip install -r .\requirements.txt`
- `pip install opencv-python` to install opencv.
- To check if OpenCV installed properly, start your environment (face_recognition) in our case and type `python` >> `import cv2`.
  ![](https://i.imgur.com/oVAHcse.png)

## 2. Intro to Image Processing

### Goals ⚡🎯🎯

- Master the fundamentals of writing OpenCV Scripts.
- Learn core elements such as values, depth, coloring.
- Create OpenCV function to facilitate code reuse.
- Understand advanced array in numpy and visualization.
- Learn to use object detection models to identify faces in images and videos.

### Understanding Images

- To read images we do the following:

![](https://i.imgur.com/ezFMbA5.png)
