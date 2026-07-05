# Facial Emotion Recognition in Work Environment using ESP32-S3-EYE

A real-time facial emotion recognition system developed using the **ESP32-S3-EYE** development board and **Edge Impulse**. The system performs on-device emotion classification using a lightweight **MobileNetV1** transfer learning model and recognizes four facial emotions: **Happy, Sad, Surprised, and Neutral**.

The project demonstrates how edge AI can provide low-latency, privacy-preserving emotion recognition for workplace monitoring and human-computer interaction.

---

## Project Overview

Emotion recognition has become an important research area in computer vision and artificial intelligence. This project proposes a lightweight edge computing solution capable of recognizing human emotions directly on an ESP32-S3-EYE without relying on cloud processing.

The system captures facial images using the onboard camera, processes them locally, and classifies them into one of four emotional states in real time.

---

## Objectives

- Develop a real-time facial emotion recognition system.
- Deploy a lightweight machine learning model on ESP32-S3-EYE.
- Perform emotion classification directly on the edge device.
- Reduce latency while preserving user privacy.
- Demonstrate the applicability of edge AI in workplace environments.

---

# Features

- Real-time facial emotion recognition
- Edge AI inference on ESP32-S3-EYE
- Lightweight MobileNetV1 transfer learning model
- Four emotion classes:
  - 😊 Happy
  - 😐 Neutral
  - 😢 Sad
  - 😲 Surprised
- Local image processing without cloud connectivity
- LCD display output
- Low-latency inference using Edge Impulse

---

# Hardware

- ESP32-S3-EYE Development Board
- Built-in Camera
- LCD Display
- USB Connection

---

# Software & Tools

- Edge Impulse
- Arduino IDE / ESP-IDF
- C++
- ESP32 SDK
- FER2013 Dataset

---

# Dataset

The project uses the **FER2013** facial expression dataset.

Dataset details:

- Total images used: **4925**
- Emotion classes:
  - Happy
  - Sad
  - Surprised
  - Neutral

Dataset split:

| Dataset | Images |
|----------|--------:|
| Training | 3940 |
| Testing | 985 |

---

# Machine Learning Model

The model was trained using the **Edge Impulse** platform.

### Model Configuration

- Transfer Learning
- MobileNetV1 96×96 0.1
- Grayscale images
- Input Layer: 9216
- Hidden Layer: 16 neurons
- Output Classes: 4

Detected emotions:

- Happy
- Sad
- Surprised
- Neutral

---

# System Workflow

```text
Camera
   │
   ▼
Capture Face Image
   │
   ▼
Pre-processing
   │
   ├── Face Detection
   ├── Grayscale Conversion
   ├── Resize Image
   ▼
Edge Impulse Model
(MobileNetV1)
   │
   ▼
Emotion Classification
   │
   ▼
Display Result on LCD
```

---

# Methodology

The complete workflow consists of the following stages:

1. Capture facial images using the ESP32-S3-EYE camera.
2. Collect and prepare the FER2013 dataset.
3. Train the model using Edge Impulse.
4. Export the trained model as a C++ library.
5. Deploy the model on the ESP32-S3-EYE.
6. Perform real-time emotion recognition.
7. Display the predicted emotion on the LCD.

---

# Results

## Training Performance

- Dataset Accuracy: **60.4%**

## Real-Time Deployment

- Average processing speed: **5 FPS**
- Camera Resolution: **240 × 240**
- Real-time deployment accuracy: **approximately 60.4%**

### Performance Comparison

| Method | Accuracy |
|---------|----------:|
| Test Dataset | **60.40%** |
| Raspberry Pi 4B + Webcam | 43.65% |
| ESP32-S3-EYE + Built-in Camera | 39.84% |

---

# Applications

- Workplace well-being monitoring
- Employee emotion analysis
- Human-computer interaction
- Smart office systems
- Edge AI applications
- Privacy-preserving AI systems

---

# Future Improvements

- Support additional emotions such as:
  - Fear
  - Disgust
  - Anger
- Improve real-world accuracy using a larger dataset.
- Train with images captured directly from the ESP32-S3-EYE.
- Improve robustness under different lighting conditions.
- Add long-term emotion logging and analytics.

---


# Installation

1. Clone the repository

```bash
git clone https://github.com/yourusername/facial-emotion-recognition-esp32.git
```

2. Open the project in Arduino IDE or ESP-IDF.

3. Install the required ESP32 board package.

4. Add the exported Edge Impulse C++ library.

5. Upload the program to the ESP32-S3-EYE.

---

# Demonstration

The ESP32-S3-EYE continuously captures facial images, performs local inference using the deployed MobileNetV1 model, and displays one of the following emotions on the LCD:

- Happy
- Sad
- Neutral
- Surprised

The entire inference process is performed on the device without requiring cloud communication.

---

# Acknowledgements
- Edge Impulse
- Espressif Systems
- FER2013 Dataset

---

# References

1. Edge Impulse — https://edgeimpulse.com/
2. ESP32-S3-EYE Getting Started Guide — https://github.com/espressif/esp-who
3. FER2013 Dataset — https://www.kaggle.com/datasets/msambare/fer2013

