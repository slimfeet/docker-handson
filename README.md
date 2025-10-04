# Running a Face Detection Tensorflow App with Docker
This project demonstrated the seamless integration of Tensorflow.js with Docker for the purpose of testing a Face Detection application. The learning outcomes from this project included:  
- Implementation of a face detection web application with TensorFlow.js
- Containerization of a TensorFlow.js application using Docker
## Step 1: Clone the Face Detection Web App
![Clone Tensorflow App](1.PNG)
This gets the application files copied to the local machine. 
## Step 2: Build the App into a Docker Image
![Build image](3.PNG)
It is necessary that before running the application as a container, its important to build it into an image. Ensure you are in the TensorJS-Face-Detection directory when building the docker image. Name the image face-detection-tensorjs
## Step 3: Run the image as a Container
`docker run -p 80:80 face-detection-tensorjs`
This command runs the container and maps it to port 80 in the container, and port 80 on my local machine.
## Step 4: Access the App on port 80
![Access app](4.PNG)
When accessing http://localhost:80, the user is prompted to allow access to camera. Upon approving access, the face detection app triggers begins face detection, as shown in the visible land marks and the reddish rectangular frame. 


