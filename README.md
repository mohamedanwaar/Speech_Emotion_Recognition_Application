Here’s the `README.md` as per your request with the original input format preserved:

---

# Emotion Recognizer Application

## Project Description
 The Emotion Recognizer Application is a Speech Emotion Recognition system that processes audio files to predict emotions such as happiness, sadness, anger, and more from speech. It allows users to either upload 
 an audio file or record one directly through the app. The app integrates with a backend API for storing recordings and performing emotion predictions using a pre-trained model.
 The project encompasses the entire pipeline, including data collection, augmentation, feature extraction, and classification using a Convolutional Neural Network (CNN). The workflow begins with uploading and 
 combining datasets, progresses through data preprocessing and feature extraction, and culminates in predicting emotions. The results and insights, including performance metrics, are showcased in a user-friendly 
 mobile application.
---

## Features

- **Audio Upload**: Upload audio files (supported formats: .wav, .mp3).
- **Audio Recording**: Record audio directly using the app's microphone functionality.
- **Prediction**: Predict the emotion from the uploaded/recorded audio.
- **History Management**: View and play back previously uploaded or recorded audio files.

---

## Usage

### Recording or Uploading Audio
- **Record Audio**: Click the microphone button to record audio directly in the app.
- **Upload Audio**: Click the upload button to select and upload an audio file.

### Predicting Emotion
- After recording or uploading an audio file, click the **Predict** button.
- The emotion prediction result will appear in the message box below the prediction button.

### Viewing History
- Click the **History** button to view all uploaded or recorded audio files.
- Play a selected audio file from the history.

---
## Backend Endpoints

### `/upload` [POST]
Upload an audio file and associate it with a user.

- **Request**: Form data with `user_id` and `file`.
- **Response**:
  - Success: `{"message": "File uploaded successfully"}`
  - Error: `{"error": "Error message"}`

### `/recordings/<user_id>` [GET]
Retrieve all recordings for a specific user.

- **Response**:
  - Success: List of recordings with file paths and timestamps.
  - Error: `{"error": "No recordings found"}`

### `/predict` [POST]
Predict emotion from an uploaded or recorded audio file.

- **Request**: Form data with `file`.
- **Response**:
  - Success: Predicted emotion.
  - Error: `{"error": "Error message"}`

## Project Structure:  

```
Speech_Emotion_Recognition_Application/
│
├── image_and_audio/
│   ├── angry/
│   │   ├── angry_spectrogram.png
│   │   ├── angry_waveplot.png
│   │   ├── angry.wav
│   ├── calm/
│   │   ├── calm_spectrogram.png
│   │   ├── calm_waveplot.png
│   │   ├── calm.wav
│   ├── disgust/
│   │   ├── disgust_spectrogram.png
│   │   ├── disgust_waveplot.png
│   │   ├── disgust.wav
│   ├── fearful/
│   │   ├── fearful_spectrogram.png
│   │   ├── fearful_waveplot.png
│   │   ├── fearful.wav
│   ├── happy/
│   │   ├── happy_spectrogram.png
│   │   ├── happy_waveplot.png
│   │   ├── happy.wav
│   ├── neutral/
│   │   ├── neutral_spectrogram.png
│   │   ├── neutral_waveplot.png
│   │   ├── neutral.wav
│   ├── sad/
│   │   ├── sad_spectrogram.png
│   │   ├── sad_waveplot.png
│   │   ├── sad.wav
│   ├── surprised/
│   │   ├── surprised_spectrogram.png
│   │   ├── surprised_waveplot.png
│   │   ├── surprised.wav
│
├── Model/
│   ├── __pycache__/
│   ├── After_Augmentor.png
│   ├── Before_Augmentor.png
│   ├── Classification_Report_Heatmap.png
│   ├── Confusion_Matrix.png
│   ├── Data_Augmentation.py
│   ├── encoder.pkl
|   ├── rav_data.csv
|   ├── tess_data.csv
│   ├── Exploration_data.py
│   ├── Features_Extraction.py
│   ├── get_data.py
│   ├── main_Speech_Emotion_recognition.py
│   ├── Model_build.py
│   ├── Pre_processing.py
│   ├── scaler.pkl
│   ├── speech_emotion_cnn_model.h5
│   ├── speech_emotion_cnn_model.keras
│   ├── tempCodeRunnerFile.py
│   ├── Train_vs_Val_Accuracy_for_CNN.png
│   ├── train_vs_val_loss_for_CNN.png
│
├── Backend.py
├── cnn.py
├── emotionrecognizer.db
├── For_prediction.py
├── mainApp.py
├── requirements.txt
├── Upload.py
```

---

## Execution Instructions:

Follow these steps to set up and execute the project:

1. **Create a Virtual Environment**:
   Open a terminal and run:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   ```

2. **Upgrade Pip**:
   ```bash
   python.exe -m pip install --upgrade pip
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run Each Model Script Sequentially**:
   ```bash
   python Model/get_data.py
   python Model/Exploration_data.py
   python Model/Data_Augumentation.py
   python Model/Features_Extraction.py
   python Model/Pre_processing.py
   python Model/Model_build.py
   python Model/main_Speech_Emotion_recognition.py
   ```

5. **Wait for the Model to Finish Training**.

6. **Execute Supporting Scripts**:
   ```bash
   python test_model.py
   python conn.py
   python Upload.py
   python Backend.py
   ```

7. **Open a New Terminal**:
   Activate the virtual environment again:
   ```bash
   .venv\Scripts\activate
   ```

8. **Run the Frontend Application**:
   ```bash
   python mainApp.py
   ```

---

### Benefits of this Project  

The primary objective of the Speech Emotion Recognition (SER) Deep Learning Project is to create a robust system that accurately detects and classifies human emotions from speech using advanced deep learning techniques. This innovation bridges the gap between human emotional expression and machine understanding, enabling the development of more empathetic and context-aware applications.

---

### Importance and Applications of SER  

1. **Customer Service**:  
   - Improves interactions in call centers by identifying and addressing customer emotions.

2. **Healthcare**:  
   - Assists in diagnosing and monitoring mental health conditions by analyzing emotional states.

3. **Entertainment**:  
   - Enhances user experience in gaming, virtual reality, and virtual assistants.

4. **Education**:  
   - Augments e-learning platforms by tailoring content to the emotional state of students.

--- 


