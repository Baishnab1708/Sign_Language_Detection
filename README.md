Sign Language Detection
Overview
This project aims to detect sign language gestures using computer vision techniques. It utilizes the MediaPipe library for holistic tracking, enabling real-time recognition of various sign language gestures through video input.
Table of Contents
Installation
Usage
Model Training
Key Features
Contributing
License
Installation
To set up the project, install the required libraries using the following command:
bash
pip install opencv-python mediapipe numpy tensorflow matplotlib
Usage
Data Collection: The script captures video input and collects keypoints for specific sign language actions:
👋 Hello
🙏 Thanks
❤️ I Love You
✔️ Yes
❌ No
🆘 Help
🙇 Please
Run the Script: Execute the main script to start capturing video and collecting data:
bash
python sign_language_detection.py
Model Training: After collecting sufficient data, train the model using the captured keypoints:
python
model.fit(X_train, y_train, epochs=35, callbacks=[tb_callback])
Real-Time Prediction: The model can predict sign language gestures in real-time from the webcam feed.
Model Training
The model architecture consists of:
Bidirectional LSTM Layers: For processing sequences of keypoints.
Dropout Layers: To prevent overfitting.
Dense Layers: For final classification of gestures.
Training Process
Load and preprocess data.
Split into training and testing sets.
Compile the model with an appropriate optimizer and loss function.
Fit the model on training data and evaluate its performance.
Key Features
Real-Time Gesture Recognition: Detects gestures in real-time using video input.
Holistic Tracking: Utilizes MediaPipe's holistic model for accurate landmark detection.
User-Friendly Interface: Displays feedback directly on the video feed.
Contributing
Contributions are welcome! Please fork this repository and submit a pull request for any improvements or bug fixes.
License
This project is licensed under the MIT License - see the LICENSE file for details. Feel free to customize this README further based on your specific project needs! 😊
