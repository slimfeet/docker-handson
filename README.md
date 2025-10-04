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

# Unpacking the Application
Tensorflow is a web-based machine learning framework backed by three different backend engines that are prompted based on the workload at hand. WASM, WebGL and CPU execute operations based on different metrics or resources that are available on modern browsers. 
- WASM - low-level assembly like language that is compact enough to run on near native speed in ordinary web browsers. Best for high-performance needs without having to rely on GPU.
- WebGL - its an API which allows for GPU accelerated usage, which incorporates physics and image processing. Best suited for parralelized workloads which can benefit greatly from GPU acceleration. Its commonly used in deep learning models which require convolutions and matrix-multiplications.
- CPU - is purely javascript execution based on the local machine's capability. Best serves as a fall back when WASM and WebGL fail.   

