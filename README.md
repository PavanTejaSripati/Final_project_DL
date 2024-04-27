# Final_project_DL

# Action Recognition

This project focuses on developing a hand gesture recognition system for sign language communication. The process begins with detecting key points on the face, pose, and hands using the Mediapipe library. These key points are then captured in real-time from a live video feed and saved as numpy arrays for each frame, organized into folders based on predefined actions (such as 'HI', 'Like', 'Thanks'). The data is preprocessed to create sequences of 30 frames per action, which are split into train, validation, and test sets. Three different models are trained on this preprocessed data: an LSTM model for sequence classification, a CNN model for sequence classification, and a Temporal Convolutional Network (TCN) model. These models are evaluated on the test set, with metrics such as accuracy and F1 score calculated. The trained models are then used for real-time inference, predicting actions from live video feed and displaying the recognized gestures along with confidence levels in real time. The project aims to provide a robust system for interpreting sign language gestures through Deep learning techniques

## Installation

1. Clone the repository.
2. Install dependencies
3. Configure the environment variables.
4. Run the project

## Usage

Start running the code then cv2.VideoCapture appears(VideoCapture(0)) means that you want to capture video from the default camera device (usually the webcam) connected to your computer where we can show our hand to detect the hand,posture and face.This code opens a window displaying the live video feed from the default camera. Pressing 'q' will exit the loop and close the window.

You will get the image with the dectections on face and hand which will let you know that you have ran the code correctly.

Code will extract the key points where the extract_keypoints function encapsulates the above process, taking results as input and returning a concatenated numpy array containing pose, face, left hand, and right hand keypoints.

This code sets up a directory structure to organize video frames data, with separate directories for each action and each sequence of frames within those actions. This organization facilitates storing and accessing the video data for further processing or analysis.

Now its time to test and train the data where this code captures video frames in real-time, detects landmarks using the MediaPipe Holistic model, and saves the extracted keypoints as NumPy arrays in a structured directory hierarchy for each action sequence.

cap.release()
cv2.destroyAllWindows() --> This ensures that resources are properly released and all windows are closed before the program exits.

After this you can run the codes of LSTM,CNN,TCN then you can continue with real time testing.

Real time testing: This code segment captures real-time video frames from the webcam (cv2.VideoCapture(0)) and processes them using the MediaPipe Holistic model (mp_holistic.Holistic) to detect human poses and gestures.

All the models are being saved in the Hierarchical Data Format (HDF5), which is a file format commonly used for storing large amounts of numerical data. The .h5 extension indicates that the file is in HDF5 format.


## Contributing

We welcome contributions!

## Contact

"Sripati, Pavan Teja" <psrip2@unh.newhaven.edu>; 
"Chigicherla, Saikrishna" <schig4@unh.newhaven.edu>;
"Tankashala, Komal" <ktank1@unh.newhaven.edu>



