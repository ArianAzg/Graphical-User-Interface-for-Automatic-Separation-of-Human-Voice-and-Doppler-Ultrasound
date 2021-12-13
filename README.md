# Graphical-User-Interface-for-Automatic-Separation-of-Human-Voice-and-Doppler-Ultrasound

In this repository, a graphical user interface (GUI) is developed to perform the automatic speech recognition and separation in audio Doppler recordings. In early 1970s and 1980s, audio Doppler recordings were captured in one-channel audio with the presence of human voice. The data remains undesired unless the human voice activity effectively gets separated from audio Doppler ultrasound. An example of of the dataset is shown in figure below:

![image](https://user-images.githubusercontent.com/48659018/145866335-352613e3-eb48-4004-8205-058d1375613c.png)

The recognition task incorporates the Google speech recognizer to detect the presence of human voice together with corresponding timestamps. The detected human speech is then separated as the header of the audio Doppler ultrasound within the developed GUI. An example of separated human voice and Doppler ultrasound is shown below. 


![image](https://user-images.githubusercontent.com/48659018/145867188-82d8c71f-dd1e-4f0c-8643-647dbc5bdfbf.png)

# Steps to Run the GUI

## Setup the Google Speech Recognizer Account
First, you need to create an account on Google Speech Recognizer using your Google account at the following link: 

https://cloud.google.com/

Once the account is set, the asscoiated **.json** file must be download. 

## Setup Environment Variable in OS

- Open the _System Properties_ and click on _Environment Variables_.
- Under the _System Variables_, create a new variable called _GOOGLE_APPLICATION_CREDENTIALS_.
- Set the complete path of **.json** file as the value of this variable.


License and Citation
---------
The codes are licensed under MIT license. 

For any utilization of the code content of this repository, the following paper needs to get cited by the user:

> A. Azarang, L. Blogg, J. Currens, R. Lance, R. Moon, P. Lindholm, V. Papadopoulou, Development of Graphical User Interface for Automatic Separation of Human Voice from Audio Doppler Ultrasound in Diving Experiments, Under Review.
