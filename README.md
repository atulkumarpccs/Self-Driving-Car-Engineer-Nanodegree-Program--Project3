# Project 3 : Behavioral Cloning 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

The third  assignement project  in Term 1 for submission. 


[Udacity Self-Driving Car Engineer Nanodegree](https://www.udacity.com/course/self-driving-car-engineer-nanodegree--nd013)

In this project, your goal is to write a software pipeline to identify the lane boundaries in a video from a front-facing camera on a car. The camera calibration images, test road images, and project videos are available in 
<https://github.com/udacity/CarND-Advanced-Lane-Lines>

## Submission Requirment :

For this project, a reviewer will be testing the model that you generated on the first test track (the one to the left in the track selection options).

 1.``model.py`` - The script used to create and train the model.
 
 2.``drive.py`` - The script to drive the car. You can feel free to resubmit the original drive.py or make modifications and submit your modified version.
 
 3.``model.h5`` - The saved model. Here is the documentation explaining how to create this file. 
 
 4.``writeup_report``- as a markdown or pdf file. It should explain the structure of your network and training approach. The writeup must also include examples of images from the dataset in the discussion of the characteristics of the dataset. While we recommend using English for good practice, writing in any language is acceptable (reviewers will translate). There is no minimum word count so long as there are complete descriptions of the problems and the strategies. See the rubric and the writeup_template.md for more details about the expectations.
 
 5.``video.mp4`` - A video recording of your vehicle driving autonomously at least one lap around the track.
 
 
 ### Acceptance Criteria :
 <https://review.udacity.com/#!/rubrics/322/view>
 
 ### Setup Environmet :
 1. Set up `Starter Kit Installation`
 
   setup by using Anaconda
   <https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md>
   
2. Open the Anaconda Command Prompt.
   example C:\Users\Atul\Anaconda3>
  
3. Run command >>activate carnd-term1

4. Go to the project_submission directory

5. Run >>jupyter notebook P4.ipynb

6. Run shell one by one 

7. Output video take time wait :)

```

Amazon Web Services
Instead of a local GPU, you could use Amazon Web Services to launch an EC2 GPU instance. (This costs money.)

Follow the Udacity instructions to launch an EC2 GPU instance with the udacity-carnd AMI.
Complete the Setup instructions. 

 ### Build Steps :
 ```sh
 1.All steps are based on windows 10 environement.
 
 2.Compute the camera calibration matrix and distortion coefficients given a set of chessboard images.
 
 3.Apply a distortion correction to raw images.
 
 4.Use color transforms, gradients, etc., to create a thresholded binary image.
 
 5.Apply a perspective transform to rectify binary image ("birds-eye view").
 
 6.Detect lane pixels and fit to find the lane boundary.
 
 7.Determine the curvature of the lane and vehicle position with respect to center.
 
 8.Warp the detected lane boundaries back onto the original image.
 
 9.Output visual display of the lane boundaries and numerical estimation of lane curvature and vehicle position.
 
 ```  
   
 ### Known Issues :
 ```sh
 1.Set up is not done for personal Linux environment.
 
 2.Some of package for python are installed manually.
 
 3. AWS setup is not working as per support project so done locally.
 ```
 

