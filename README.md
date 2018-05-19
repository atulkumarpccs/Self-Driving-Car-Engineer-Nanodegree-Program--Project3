# Project 3 : Behavioral Cloning 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

The third  assignement project  in Term 1 for submission. 


[Udacity Self-Driving Car Engineer Nanodegree](https://www.udacity.com/course/self-driving-car-engineer-nanodegree--nd013)

In this project, you will use what you've learned about deep neural networks and convolutional neural networks to clone driving behavior. You will train, validate and test a model using Keras. The model will output a steering angle to an autonomous vehicle.

We have provided a simulator where you can steer a car around a track for data collection. You'll use image data and steering angles to train a neural network and then use this model to drive the car autonomously around the track.

<https://github.com/udacity/CarND-Behavioral-Cloning-P3>

## Submission Requirment :

For this project, a reviewer will be testing the model that you generated on the first test track (the one to the left in the track selection options).

 1.``model.py`` - The script used to create and train the model.
 
 2.``drive.py`` - The script to drive the car. You can feel free to resubmit the original drive.py or make modifications and submit your modified version.
 
 3.``model.h5`` - The saved model. Here is the documentation explaining how to create this file. 
 
 4.``writeup_report``- as a markdown or pdf file. It should explain the structure of your network and training approach. The writeup must also include examples of images from the dataset in the discussion of the characteristics of the dataset. While we recommend using English for good practice, writing in any language is acceptable (reviewers will translate). There is no minimum word count so long as there are complete descriptions of the problems and the strategies. See the rubric and the writeup_template.md for more details about the expectations.
 
 5.``video.mp4`` - A video recording of your vehicle driving autonomously at least one lap around the track.
 
 The Project
---
The goals / steps of this project are the following:
* Use the simulator to collect data of good driving behavior 
* Design, train and validate a model that predicts a steering angle from image data
* Use the model to drive the vehicle autonomously around the first track in the simulator. The vehicle should remain on the road for an entire loop around the track.
* Summarize the results with a written report

### Dependencies
This lab requires:

* [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit)

The lab enviroment can be created with CarND Term1 Starter Kit. Click [here](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) for the details.

The following resources can be found in this github repository:
* drive.py
* video.py
* writeup_template.md

The simulator can be downloaded from the classroom. In the classroom, we have also provided sample data that you can optionally use to help train your model.

## Details About Files In This Directory

### `drive.py`

Usage of `drive.py` requires you have saved the trained model as an h5 file, i.e. `model.h5`. See the [Keras documentation](https://keras.io/getting-started/faq/#how-can-i-save-a-keras-model) for how to create this file using the following command:
```sh
model.save(filepath)
```

Once the model has been saved, it can be used with drive.py using this command:

```sh
python drive.py model.h5
```

The above command will load the trained model and use the model to make predictions on individual images in real-time and send the predicted angle back to the server via a websocket connection.

Note: There is known local system's setting issue with replacing "," with "." when using drive.py. When this happens it can make predicted steering values clipped to max/min values. If this occurs, a known fix for this is to add "export LANG=en_US.utf8" to the bashrc file.

#### Saving a video of the autonomous agent

```sh
python drive.py model.h5 run1
```

The fourth argument, `run1`, is the directory in which to save the images seen by the agent. If the directory already exists, it'll be overwritten.

```sh
ls run1

[2017-01-09 16:10:23 EST]  12KiB 2017_01_09_21_10_23_424.jpg
[2017-01-09 16:10:23 EST]  12KiB 2017_01_09_21_10_23_451.jpg
[2017-01-09 16:10:23 EST]  12KiB 2017_01_09_21_10_23_477.jpg
[2017-01-09 16:10:23 EST]  12KiB 2017_01_09_21_10_23_528.jpg
[2017-01-09 16:10:23 EST]  12KiB 2017_01_09_21_10_23_573.jpg
[2017-01-09 16:10:23 EST]  12KiB 2017_01_09_21_10_23_618.jpg
[2017-01-09 16:10:23 EST]  12KiB 2017_01_09_21_10_23_697.jpg
[2017-01-09 16:10:23 EST]  12KiB 2017_01_09_21_10_23_723.jpg
[2017-01-09 16:10:23 EST]  12KiB 2017_01_09_21_10_23_749.jpg
[2017-01-09 16:10:23 EST]  12KiB 2017_01_09_21_10_23_817.jpg
...
```

The image file name is a timestamp of when the image was seen. This information is used by `video.py` to create a chronological video of the agent driving.

### `video.py`

```sh
python video.py run1
```

Creates a video based on images found in the `run1` directory. The name of the video will be the name of the directory followed by `'.mp4'`, so, in this case the video will be `run1.mp4`.

Optionally, one can specify the FPS (frames per second) of the video:

```sh
python video.py run1 --fps 48
```

Will run the video at 48 FPS. The default FPS is 60.

#### Why create a video

1. It's been noted the simulator might perform differently based on the hardware. So if your model drives succesfully on your machine it might not on another machine (your reviewer). Saving a video is a solid backup in case this happens.
2. You could slightly alter the code in `drive.py` and/or `video.py` to create a video of what your model sees after the image is processed (may be helpful for debugging).

### Tips
- Please keep in mind that training images are loaded in BGR colorspace using cv2 while drive.py load images in RGB to predict the steering angles.

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

5. Follow the above instructions & cloning cheatsheet

6. Output video take time wait :)

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
 
 ### From Git to Github :
 
 
 1. Cloning the repository by using command ```git clone Self-Driving-Car-Engineer-Nanodegree-Program--Project3 ```.
 
 2. Make changes and run the command ```git status``` for changed in local repository.
 
 3. Add all files in one command  ```git add .```
 
 4. Commit the code base by ```git commit -m "your comment" ```
 
 5. Check the github repository if you done change on github ```git pull origin master```
 
 6. Push your code by ```git push origin master```
 
 
 ### Project Support :
 
1. Udacity Link showcasing how to start working on this

<https://www.youtube.com/watch?v=rpxZ87YFg0M&feature=youtu.be>

2. Slack Channel
<#s-t1-p-behavioral-clo>


