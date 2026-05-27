# Facial Emotion Recognition

A deep learning project for recognizing human emotions from facial expressions using TensorFlow/Keras and the FER2013 dataset.  
The project includes:

- Training a Convolutional Neural Network (CNN)
- Evaluating model performance
- Running inference on test images
- A simple Gradio web interface for real-time emotion prediction

---

## Features

- Image preprocessing and augmentation
- CNN-based emotion classification
- Validation and test evaluation
- Confusion matrix and classification report
- Gradio-powered interactive UI

---

## Dataset

This project uses the **FER2013** dataset.

Expected dataset structure:

```text
train/
    Angry/
    Disgust/
    Fear/
    Happy/
    Neutral/
    Sad/
    Surprise/

test/
    Angry/
    Disgust/
    Fear/
    Happy/
    Neutral/
    Sad/
    Surprise/
```

Each folder should contain corresponding facial expression images.

---

## Tech Stack

- Python
- TensorFlow / Keras
- NumPy
- scikit-learn
- Pillow (PIL)
- Gradio

---

## Installation

Install the required dependencies:

```bash
pip install tensorflow numpy scikit-learn pillow gradio
```

---

## Model Training

The notebook performs the following steps:

1. Loads and preprocesses image data
2. Applies data augmentation
3. Builds a CNN model
4. Trains the model using:
   - EarlyStopping
   - ReduceLROnPlateau
   - ModelCheckpoint
5. Saves the best trained model

Key configuration:

```python
IMG_HEIGHT, IMG_WIDTH = 48, 48
BATCH_SIZE = 64
```

---

## Model Evaluation

The notebook evaluates the trained model using:

- Confusion Matrix
- Classification Report
- Accuracy metrics

Example evaluation tools used:

```python
from sklearn.metrics import classification_report, confusion_matrix
```

---

## Running the Gradio App

The project includes a simple Gradio interface for emotion prediction.

Before running:
- Ensure `best_model.keras` exists in the project directory.

Run the app:

```python
python app.py
```

Or launch directly from the notebook.

---

## Emotion Classes

The model predicts the following emotions:

- Angry
- Disgust
- Fear
- Happy
- Neutral
- Sad
- Surprise

---

## Image Preprocessing

Input images are:

- Converted to grayscale
- Resized to 48x48
- Normalized to pixel range `[0, 1]`

---

## Example Workflow

1. Upload a facial image
2. The image is preprocessed
3. The trained CNN predicts the emotion
4. Gradio displays prediction probabilities

---

## File Structure

```text
project/
│
├── facial_emotion_recognition_code.ipynb
├── best_model.keras
├── train/
├── test/
└── README.md
```

---

## Future Improvements

- Improve model accuracy with transfer learning
- Add webcam/live video prediction
- Deploy using Hugging Face Spaces or Streamlit
- Add real-time face detection

---

## License

This project is for educational and research purposes.
