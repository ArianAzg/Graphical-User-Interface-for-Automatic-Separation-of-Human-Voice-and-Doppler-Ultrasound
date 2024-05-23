# Graphical User Interface for Automatic Separation of Human Voice and Doppler Ultrasound 

In this repository, a graphical user interface (GUI) is developed to perform the automatic speech recognition and separation in audio Doppler recordings. In early 1970s and 1980s, audio Doppler recordings were captured in one-channel audio with the presence of a human voice. The data remains undesired unless the human voice activity effectively gets separated from audio Doppler ultrasound. An example of the dataset is shown in the figure below:

<p align="center">
<img src="https://user-images.githubusercontent.com/48659018/145866335-352613e3-eb48-4004-8205-058d1375613c.png" width="600" align="center">
    <br>
    <em>Figure reprinted with permission [1].</em>
</p>

The recognition task incorporates the Google speech recognizer to detect the presence of human voice together with corresponding timestamps. The detected human speech is then separated as the header of the audio Doppler ultrasound within the developed GUI. An example of a separated human voice and Doppler ultrasound is shown below. 

<p align="center">
<img src="https://user-images.githubusercontent.com/48659018/145867188-82d8c71f-dd1e-4f0c-8643-647dbc5bdfbf.png" width="600" align="center">
    <br>
    <em>Figure reprinted with permission [1].</em>
</p>

# How to Run

## Setup the Google Speech Recognizer Account
First, you need to create an account on Google Speech Recognizer using your Google account at the following link: 

https://cloud.google.com/

Once the account is set, the associated **.json** file must be downloaded. 

## Setup Environment Variable in OS

- Open the _System Properties_ and click on _Environment Variables_.
- Under the _System Variables_, create a new variable called _GOOGLE_APPLICATION_CREDENTIALS_.
- Set the complete path of **.json** file as the value of this variable.

Requirements
------------

The code is written in Python 3 and uses Keras as well as MATLAB. The latest versions (at the time of this writing) of Tensorflow, Sklearn, Networkx, Numpy, and Scipy are used. These packages can be installed using the following command:
    
    $ pip install -r requirements.txt

## GUI Structure

The GUI structure is shown below:

<p align="center">
<img src="https://user-images.githubusercontent.com/48659018/145888683-fe2d3cba-1868-49c2-ac61-9568c72823a0.png" width="400" align="center">
        <br>
    <em>Figure reprinted with permission [1].</em>
</p>

The functionality of each button is described as follows:
- **Select file:**
By clicking on the Select file button, the generic path in MS Windows will be opened and the end-user must select the denoised file for further processing.

- **Start to process:**
This button applies the Google speech recognizer on the 1-minute audio segments on the fly. When the last audio segment gets processed, the program notifies the end-user to move forward with the next step.

- **Audio chunking and selection:**
During the experimental studies recorded in the post-dive audio files, the examiner provided details about the experiment and change of subject and normally it takes more than 3 seconds. This practical assumption is required to only select human voice segments above this threshold. By clicking this button, these files get pruned from all detected human voice activity for final verification in the next step. 
- **Play and save:**
In this step, the separated human voice and Doppler ultrasound audio components are displayed to the end user.

## License

The codes are licensed under GPL-2.0 license.

## Citation

For any utilization of the code content of this repository, the following paper needs to get cited by the user:

> 1. Azarang A, Blogg SL, Currens J, Lance RM, Moon RE, Lindholm P, et al. (2023) Development of a graphical user interface for automatic separation of human voice from Doppler ultrasound audio in diving experiments. PLoS ONE 18(8): e0283953. https://doi.org/10.1371/journal.pone.0283953

## Contact

For bug reports and feature requests please contact us at: aazarang@unc.edu.
