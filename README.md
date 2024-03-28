##Vision-based Lane Detection System for Autonomous Vehicle
Overview
This repository contains the code implementation for a vision-based lane detection system designed for autonomous vehicles. The system utilizes computer vision techniques to detect and track lane markings on the road, providing crucial information for autonomous navigation.

Features
Training Deep Learning Models: The system includes implementations of Semantic Segmentation Deep Learning models such as SCNN and Fast-SCNN for extracting lane markings from images obtained by a stereo setup mounted on a car.
Integration with ROS: The trained model is deployed over a ROS (Robot Operating System) node to seamlessly integrate with the local planner of the autonomous vehicle.
Data Preprocessing: Preprocessing techniques such as camera calibration, perspective transformation, and thresholding are applied to enhance the quality of input images.
Real-time Processing: The system is capable of processing live video streams or recorded video files to detect lane markings in real-time.

Project Goals
The primary objectives of this project include:

Compute the camera calibration matrix and distortion coefficients using chessboard images.
Apply distortion correction to raw images captured by the vehicle's camera.
Implement a perspective transform to obtain a "birds-eye view" of the road.
Utilize color transforms, gradients, etc., to create a thresholded binary image highlighting lane markings.
Detect lane pixels and fit polynomials to define the lane boundaries.
Determine the curvature of the lane and the vehicle's position concerning the lane center.
Warp the detected lane boundaries back onto the original image to visualize the results.
Output a visual display of the lane boundaries along with numerical estimations of lane curvature and vehicle position.

Project Structure
camera_cal: Contains chessboard images for camera calibration.
test_images: Includes images for testing the lane detection pipeline on single frames.
challenge_video.mp4: An optional challenge video to test the pipeline under more complex conditions.
harder_challenge.mp4: Another optional challenge video presenting more difficult scenarios.

Usage
Environment Setup:
Use the provided environment.yml file to set up the required environment:
conda env create -f environment.yml
Activate the environment:
Windows: conda activate carnd
Linux, MacOS: source activate carnd
Running the Pipeline:
To process a single image:
python main.py INPUT_IMAGE OUTPUT_IMAGE_PATH
To process a video:
python main.py --video INPUT_VIDEO OUTPUT_VIDEO_PATH
Additional Notes
Feel free to explore and extend the project by capturing your own videos and calibrating the camera accordingly.
The challenge videos provided offer more complex scenarios for testing the robustness of the lane detection system.
Usage
Clone the repository: git clone https://github.com/Suyashspidy/Vison-based-Lane-Detection-system-for-Autonomous-Vehicle.git
Navigate to the project directory: cd vision-based-lane-detection
Run the main script to process video data: python main.py --input_video <input_video_path> --output_video <output_video_path>
Optionally, modify the script parameters or configurations as needed.
Contributing
Contributions are welcome! If you have any suggestions, bug fixes, or improvements, please feel free to open an issue or submit a pull request.

License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
This project was inspired by the need for robust lane detection systems in autonomous vehicle technology.
Special thanks to the open-source community for providing valuable resources and libraries.
