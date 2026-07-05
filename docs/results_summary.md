# Experimental Results

## Dataset

- FER2013
- 4925 images
- 4 emotion classes

## Model

- MobileNetV1 96×96 0.1
- Transfer Learning
- Edge Impulse

## Deployment

- ESP32-S3-EYE
- On-device inference
- Camera Resolution: 240 × 240
- Processing Speed: ~5 FPS

## Accuracy

| Evaluation | Accuracy |
|------------|----------|
| Test Dataset | 60.40% |
| Raspberry Pi 4B + Webcam | 43.65% |
| ESP32-S3-EYE | 39.84% |

## Observations

- Real-time inference performed directly on the ESP32-S3-EYE.
- The system classified four facial emotions:
  - Happy
  - Sad
  - Neutral
  - Surprised
- Lower real-world accuracy was mainly due to variations in lighting, camera angle, facial movement, and background conditions.
