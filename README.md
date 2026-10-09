# 🎭 Real-Time Face Emotion Detection Using Deep Learning

## 📌 Project Overview

Real-Time Face Emotion Detection is a computer vision application that detects human faces through a webcam and predicts the facial emotion using a trained deep learning model.

The system uses OpenCV for face detection and TensorFlow/Keras for emotion classification. It processes live video frames, identifies faces, extracts facial regions, and classifies each detected face into one of five emotion categories: **Angry, Happy, Neutral, Sad, and Surprise**.

This project demonstrates the practical application of deep learning, image processing, and computer vision for real-time facial expression recognition.

## 🎯 Objectives

- Detect human faces from a live webcam feed.
- Process facial images using image preprocessing techniques.
- Predict facial emotions using a trained deep learning model.
- Display the predicted emotion directly on the webcam window.
- Understand the integration of OpenCV with TensorFlow/Keras.

## ✨ Features

- **Real-Time Detection:** Processes webcam frames continuously.
- **Face Detection:** Uses OpenCV's Haar Cascade classifier to locate faces.
- **Emotion Classification:** Predicts one of five emotion categories.
- **Image Preprocessing:** Converts detected faces to grayscale, resizes them to 48 × 48 pixels, and normalizes pixel values.
- **Live Visualization:** Displays a rectangle around detected faces and labels the predicted emotion.
- **Easy Exit:** Press `Q` to close the webcam window.
- **Modular Implementation:** Separates model loading, face detection, preprocessing, and prediction.

## 🧠 Emotion Categories

The model predicts the following facial expressions:

1. Angry
2. Happy
3. Neutral
4. Sad
5. Surprise

The model selects the category with the highest predicted score.

## 🛠️ Technologies Used

- **Python** — Main programming language.
- **OpenCV** — Webcam access, image processing, and face detection.
- **TensorFlow** — Deep learning framework.
- **Keras** — Loading the trained model and generating predictions.
- **NumPy** — Numerical operations and array processing.
- **Spyder IDE** — Development and execution environment.
- **Anaconda** — Python environment and package management.

## ⚙️ System Requirements

- Python 3.x
- A webcam
- Anaconda or another Python environment
- A compatible TensorFlow installation
- OpenCV 4.x
- Trained model architecture and weights files

## 📂 Project Structure

```text
Face-Emotion-Detection/
│
├── cam.py
├── modelGG.json
├── model1GG.weights.h5
├── requirements.txt
├── README.md
└── .gitignore
```

*Adjust the filenames and folder structure to match your actual repository.*

## 🚀 Installation and Setup

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd Face-Emotion-Detection
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your repository URL.

### 2. Create and activate a Python environment

```bash
conda create -n tensorflow_env python=3.10 -y
conda activate tensorflow_env
```

Use a Python version compatible with the TensorFlow version you install.

### 3. Install the required packages

```bash
pip install tensorflow opencv-python numpy
```

If your code imports additional packages, install those as well.

### 4. Prepare the trained model files

Place the model architecture JSON file and trained weights file in the appropriate locations. Update the paths in `cam.py` if necessary.

### 5. Run the application

```bash
python cam.py
```

Allow camera access if prompted. The application should open a webcam window and display the predicted emotion for each detected face.

Press `Q` to stop the application.

## 🔍 How It Works

1. **Model Loading:** Loads the model architecture from a JSON file and restores its trained weights.
2. **Webcam Initialization:** Opens the default webcam using OpenCV.
3. **Frame Capture:** Reads video frames continuously.
4. **Face Detection:** Converts each frame to grayscale and detects faces using a Haar Cascade classifier.
5. **Region Extraction:** Crops each detected face and resizes it to 48 × 48 pixels.
6. **Preprocessing:** Normalizes pixel values to the range 0–1 and converts the image into the input format expected by the model.
7. **Emotion Prediction:** The trained model generates prediction scores for the five emotion classes.
8. **Result Display:** Displays a bounding box and the predicted emotion on the video frame.
9. **Termination:** Releases the webcam and closes the display window when the user presses `Q`.

## 📈 Expected Output

When the application runs successfully:

- A live webcam window appears.
- Detected faces are highlighted with rectangles.
- An emotion label appears near each detected face.
- A "No Face Found" message appears when no face is detected.

The prediction quality depends on the training dataset, model architecture, lighting, camera quality, and input image conditions.

## 🔮 Future Enhancements

- Improve model accuracy using larger and more diverse datasets.
- Add confidence scores for each emotion prediction.
- Support multiple face tracking across video frames.
- Build a graphical user interface using Streamlit or Tkinter.
- Evaluate model performance using precision, recall, F1-score, and a confusion matrix.
- Optimize inference speed for real-time applications.

## ⚠️ Limitations

- Facial expressions do not reliably reveal a person's actual emotional state.
- Predictions may be affected by lighting, camera angle, occlusion, and image quality.
- The model recognizes only the five emotion categories for which it was configured.
- Predictions are estimates and should not be treated as definitive psychological assessments.

## 🔐 Privacy Considerations

This application processes webcam frames locally when run on your computer. Do not add captured images, videos, or personal data to the repository without appropriate consent.

## 👩‍💻 Author

**Your Name**

GitHub: YOUR_GITHUB_USERNAME

## 📜 License

Choose an appropriate open-source license, such as the MIT License, if you want others to reuse and modify your project.

## ⭐ Acknowledgment

This project was developed as a practical implementation of deep learning and computer vision concepts using Python, OpenCV, and TensorFlow/Keras.

If you find this project useful, consider giving the repository a star on GitHub.
