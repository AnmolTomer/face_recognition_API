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

## 3. Build Face Recognition Model

### Goals ⚡🎯🎯

- Learning to preprocess images data.
- Learn to use powerful feature engineering technique like PCA to get Eigen Images.
- Training Images with SVM.
- Evaluation and Tuning of your Machine Learning model.

- Sequence in which we will proceed:

![](https://i.imgur.com/i0s7IhM.png)

### 3.1 Machine Learning Pipeline Architecture

- Create a Gender Classification Model and Integrate to Flask App.
- Task is to develop a ML model which should automatically detect and classify genders.

- `Deliverables:`
- Develop a Flask app and integrate a ML model.
- User will upload an image and app has to detect the face and identify gender.

- `High Level Diagram:`

![](https://i.imgur.com/uxOAwbq.png)

- `ML Model Application Flow:`

![](https://i.imgur.com/HRn53jx.png)

### 3.2 Understanding Data

- If you look at dataset from the link [Faces Only 1 GB](https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/) you will see that data is highly unstructured as the coordinates of face isn't same plus the dimension of each and every image is different as well.
- We need to extract the faces and store them in a separate folder. We will crop the face using harr cascade classifier and we will then send that to male or female folder named as Crop_Male and Crop_Female.

![](https://i.imgur.com/JX3RRdY.png)

### 3.3 Crop Faces from Images

- Ref 03_01_crop_faces.ipynb.
- Go to this [link](https://drive.google.com/drive/folders/18b7bVs0rolocCxLC-PV9ydu4dq1q3yVg?usp=sharing) and download the male and female folder before running crop_faces notebook, it contains the images that will be used for training.
- Place those folders inside `./data/`.
