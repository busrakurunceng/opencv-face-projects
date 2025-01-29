# Face Detection and Recognition with OpenCV and Dlib

This repository contains two different Python projects that utilize OpenCV and Dlib for face detection and face recognition. Both scripts capture real-time video from a webcam, process the frames to detect faces, and in the case of recognition, compare detected faces to a set of known faces.

## Requirements

- Python version: 3.11
- Required libraries:
  - OpenCV
  - Dlib
  - NumPy

### To install the required libraries, run:

```bash
pip install opencv-python dlib numpy
```

## Models

The face recognition project requires two pre-trained models:

1. **Dlib's Shape Predictor Model** (`shape_predictor_68_face_landmarks.dat`)
2. **Dlib's Face Recognition Model** (`dlib_face_recognition_resnet_model_v1.dat`)

### To download the models:
- Visit Dlib's official site [here]([http://dlib.net/files/](https://github.com/ageitgey/face_recognition_models/tree/master/face_recognition_models/models) to download the models.
- Place the models in the `models/` folder in the repository.

### Folder structure:
```
- models/
    - shape_predictor_68_face_landmarks.dat
    - dlib_face_recognition_resnet_model_v1.dat
- dataset/
    - [Known face images stored here]
- opencv_face_detection.py
- opencv_face_recognition.py
```

## Scripts

### 1. Face Detection (`opencv_face_detection.py`)

This script uses OpenCV’s Haar Cascade Classifier to detect faces in real-time from a webcam feed. Detected faces are highlighted with rectangles.

#### How to run:
- Ensure the required libraries are installed.
- Run the script to start the webcam feed and see the face detection in action.
- Press 'q' to exit the webcam feed.

### 2. Face Recognition (`opencv_face_recognition.py`)

This script uses Dlib's pre-trained face detection and recognition models to recognize faces in real-time from a webcam feed. It compares the detected faces with a set of known faces stored in the `dataset/` folder. If a match is found, the person’s name is displayed; otherwise, "Unknown" is shown.

#### How to run:
- Ensure the required models are downloaded and placed in the `models/` folder.
- Ensure you have a folder with known faces (images) in `dataset/`.
- Run the script to start the webcam feed and see the face recognition in action.
- Press 'q' to exit the webcam feed.

## Troubleshooting

- If you encounter issues with model loading or face detection, make sure:
  - You are using Python 3.11 (other versions may have compatibility issues).
  - The required models are correctly placed in the `models/` folder.
  - The webcam is properly connected and accessible.

- If you experience any errors or unexpected behavior, feel free to open an issue in the repository. Provide details on:
  - The error message you received.
  - Your operating system and Python version.
  - Steps to reproduce the issue, if applicable.
