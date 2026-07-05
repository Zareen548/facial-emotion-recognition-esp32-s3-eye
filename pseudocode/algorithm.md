# Pseudocode: Facial Emotion Recognition on ESP32-S3-EYE

```text
START

Initialize ESP32-S3-EYE board
Initialize camera module
Initialize LCD display
Load trained Edge Impulse emotion recognition model

WHILE device is powered ON:

    Capture image frame from camera

    Detect face region from captured frame

    IF face is detected THEN

        Crop face region

        Convert image to grayscale

        Resize image to 96 × 96 pixels

        Normalize pixel values

        Send processed image to trained model

        Run inference on ESP32-S3-EYE

        Get prediction scores for:
            Happy
            Sad
            Surprised
            Neutral

        Select emotion class with highest confidence score

        Display detected emotion on LCD screen

        OPTIONAL:
            Store detected emotion
            Store confidence value
            Use logged data for workplace emotion analysis

    ELSE

        Display "No face detected"

    END IF

    Wait briefly before processing next frame

END WHILE

STOP
```
