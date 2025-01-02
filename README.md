# Trigger Word Detection

Trigger word detection is a speech recognition task that enables devices to respond when a specific word is detected. In this project, we develop a system that detects the word **"activate"** and produces a chiming sound. This functionality is similar to voice assistants like Amazon Alexa, Google Home, or Apple Siri.

---

## **Project Overview**

The goal of this project is to:

1. Create a speech dataset with both positive and negative examples.
2. Build and train a deep learning model using 1-D convolutional layers, GRU layers, and dense layers.
3. Detect the trigger word "activate" in audio clips and respond with a chime.

This project can be extended to perform actions such as:
- Launching apps.
- Controlling IoT devices like lights or speakers.
- Triggering any event upon detecting the word "activate."

---

## **Dataset Creation**

- A speech dataset is synthesized by embedding audio clips of the word **"activate"** (positive examples) and other random words (negative examples) into diverse background sounds.
- Background environments include settings such as libraries, homes, offices, and open spaces.

The dataset is designed to replicate real-world scenarios to improve the model's robustness.

---

## **Model Architecture**

The trigger word detection model uses the following architecture:

1. **Convolutional Layer**: Extracts audio features from spectrograms.
2. **Two GRU Layers**: Captures temporal dependencies in the audio data.
3. **Dense Layer**: Outputs a signal when the trigger word is detected.

Below is the model's architecture:

![Model Architecture](images/model.png)

---

## **Steps to Implement**

1. **Data Synthesis**
   - Create a dataset by combining audio clips of words and background sounds.
   - Label data with positive and negative examples.

2. **Model Training**
   - Train the model using spectrograms of the audio data.
   - Use Keras to implement convolutional, GRU, and dense layers.

3. **Prediction**
   - The trained model detects the trigger word "activate" and produces a chime.

![Audio Signal Representation](images/sound.png)

---

## **Technologies Used**

- **Python Libraries**: `numpy`, `pydub`, `keras`, `tensorflow`
- **Deep Learning**: Convolutional layers, GRU layers, Dense layers
- **Audio Processing**: Spectrogram generation, data augmentation

---

## **Applications and Extensions**

- Automate tasks such as launching apps or controlling smart devices.
- Enhance the project to detect multiple trigger words.
- Adapt the model for low-power edge devices.

---

## **How to Run**

1. Install the required dependencies:
   ```bash
   pip install numpy pydub keras tensorflow
   ```
2. Clone this repository:
   ```bash
   git clone <repository_url>
   cd trigger-word-detection
   ```
3. Run the dataset synthesis script.
4. Train the model using the training script.
5. Use the prediction script to detect the trigger word.

---

## **Future Work**

- Expand the dataset with more background environments.
- Optimize the model for real-time performance.
- Integrate the model with IoT devices for practical applications.

---

Feel free to explore and extend this project! 🚀
