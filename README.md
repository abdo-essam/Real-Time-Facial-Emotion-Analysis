# Real-Time-Facial-Emotion-Analysis
The code you provided is for real-time facial emotion analysis using a pre-trained model. Here's a breakdown of the code:
1.	The code loads a pre-trained model using load_model from Keras. Make sure you have the "best_model.h5" file in the same directory as your script.
2.	The code initializes the Haar cascade classifier for face detection using cv2.CascadeClassifier. The XML file containing the Haar cascade model is loaded using cv2.data.haarcascades + 'haarcascade_frontalface_default.xml'.
3.	The code captures frames from the webcam using cv2.VideoCapture(0). It loops over the frames and performs face detection and emotion analysis on each frame.
4.	For each frame, the code detects faces using face_haar_cascade.detectMultiScale and draws rectangles around the detected faces using cv2.rectangle.
5.	The region of interest (ROI) containing the face is extracted and resized to 224x224 pixels, which is the input size expected by the pre-trained model.
6.	The pre-processed face image is fed into the model using model.predict to obtain the emotion predictions.
7.	The predicted emotion is determined by finding the maximum value in the predictions and mapping it to the corresponding emotion label.
8.	The predicted emotion label is overlayed on the frame using cv2.putText.
9.	The frame is then resized and displayed in a window using cv2.imshow.
10.	The loop continues until the 'q' key is pressed, at which point the program exits.
Make sure you have the necessary dependencies installed (Keras, OpenCV, and others) and that you have a working webcam connected to your system. You may need to modify the code if your webcam is not the default device (0).
