# Capstoneplant

# About This Project
 In this project I used JupyterLab as 
my environment. I created a custom 
ipykernel and implemented a 
convolutional neural network using 
the Keras library from TensorFlow. I 
created a UI with Tkinter that lets a 
user upload an image from their 
directory and run it against the 
trained model to identify it as either 
toxic or non-toxic. This UI has a 
login screen with a few users set 
up. I have also integrated metrics 
from matplotlib to view the 
accuracy of the trained data as it 
runs through its batches. I designed 
this project in a way that adding 
more to this model is as simple as 
dragging and dropping .jpg images 
into a folder.(The 'toxic folder' or 
'non-toxic' folder.)

![Program flow-capstone](https://github.com/AlbersSoftware/Capstoneplant/assets/65799182/26097c15-e581-4d6e-8644-0d7b75b36be9)


# Installation Guide And Getting Started!

Installation Guide 
Step 1: Install Anaconda at: https://www.anaconda.com/download

Step 2: run the installer and in advanced settings of the installer tick the box to 'Add Anaconda3 to the system PATH environment variable' 

 ![anaconda-install](https://github.com/AlbersSoftware/Capstoneplant/assets/65799182/74b121bf-333d-46a5-9b1b-0a5c46564e92)

(It will say not recommended but it is fine to do)

Step 3: download git from https://git-scm.com/ 

(Choose 64-bit Git for Windows Setup, open the installer and download git with the already selected settings.)

Step 4: open the command line and type: 
git clone https://github.com/AlbersSoftware/Capstoneplant (enter key)

Step 5: After the git is cloned, type the following in the command line:
 Jupyter lab (enter key)

Step 6: In the jupyter lab, verify the 'Capstoneplant' folder is there. Close jupyter lab and the terminal. (DO NOT TRY TO RUN ANY CELL BLOCKS YET)

Step 7: Create a virtual environment:
 re-open the command line and type: dir (enter key)
cd Capstoneplant (enter key)
python -m venv imageclassification (enter key)
.\imageclassification\Scripts\activate (enter key)
pip install ipykernel (enter key)
Jupyter lab (enter)

(Close the command line and jupyter lab and re-open it)
(If you experience import errors while trying to run the cell blocks, it is most likely because you missed this step. When trying on a different computer I accidentally saved the files to the wrong directory by not closing jupyter lab and the terminal.  It caused the lab to not recognize tensorflow as an import. You can repeat this process by following the steps exactly and creating a new kernel called “imageclassification2” instead of “imageclassification”. Don’t forget to name it as stated in the next step below. You may also need to update the pip if your terminal asks you to do it with: python.exe -m pip install -- upgrade pip)

pip list (enter key) (to verify ipykernel is in the list displayed) 
python -m ipykernel install --name=imageclassification (enter key)
(Close the command line and re-open it)
type in the command line: jupyter lab (enter key)

(Go to the notebook file and change the kernel to ‘imageclassification’, you can now run cell blocks as intended.)

 ![custom-kernal-image](https://github.com/AlbersSoftware/Capstoneplant/assets/65799182/6dac0863-f42b-4729-8e6e-1f3469bec919)


Step8: Download any .jpg picture of poison ivy or poison ivy look-a-like (e.g. Virginia Creeper) from the internet that is clear and just of the plant. You can opt to use the test images or one from the Kaggle set used in the project. We resize the image in the program so size shouldn't make a huge difference. However, I’d stray from images that are large or small for better predictions.


Step9: 'Shift-enter' cell block by cell block through the entire program. The last cell block opens the UI of the program. The login username and password are both 'admin' (all lower-case). If things are taking a while don’t worry, chances are the kernel is busy and you just need to wait a second or perhaps you missed a shift-enter on a cell. You can interrupt the kernel with the stop button and try again block by block.



Step 11: After a successful login click the 'upload files' button and it will prompt open your file directory in a new window. From there, choose the poison ivy picture in .jpg format of your choice that you have downloaded.



Step 12: Next you will see your photo in the UI, when you see that photo there click the 'predict' button. This will run your picture through the Convolutional Neural Network and make a prediction of either (toxic or non-toxic) and print that result to the console along with the associated picture.
 (You can re-upload and re-predict as you desire and close the window with the 'x' in the top right-hand corner of the login page to cancel the program.)

 # User Guide
 General uses:  1. Cell blocks [57]-[60] display visualizations of the data.
 
![metrics-capstoneimage](https://github.com/AlbersSoftware/Capstoneplant/assets/65799182/ecffa0ba-8b2a-417b-bca1-dd5afedb2641)

 2.  Running cell blocks [63]-[64] load the user interface. The username and password are both: admin (in all lower-case).

   ![capstone-loginpage](https://github.com/AlbersSoftware/Capstoneplant/assets/65799182/362de346-a8f6-4ae3-837d-e23c1da5655e)

 3.  The flow of the UI:
Step1- login with proper username and password ‘admin’.
Step2- click the ‘upload files’ button which will prompt open your local directories.
Step3- choice a file in .png format and click the ‘open’ button.
Step4- After seeing your selected image in the UI, click the ‘predict’ button.
Step5- close or minimize the program to view your results in the console. You will see the prediction of either ‘toxic’ or ‘non-toxic’ with the associated picture you have chosen.

 # Creating A New User
 User login set-up:
1. Changing the username and passwords.
 Below is a picture of cell block [64]. In this block there is a function called def login() highlighted in red. In this function there is the names “admin” highlighted in purple that can be changed to anything you want the username and password to be. In orange you can see there is another user which can also be changed to whatever you want the user name and password to be as long as it stays in the “ ” marks.

2. Add a new user
To add another user, you would copy the piece of code in ‘orange’ and paste it below the existing ‘orange code’ but above the ‘else:’ statement and adjust the username and passwords accordingly.

![new-user-capstone](https://github.com/AlbersSoftware/Capstoneplant/assets/65799182/9d4f128f-74c3-4b0b-a9e2-1b1d18050a8c)


# Modifying The Data
Once you download the project through the git command, the project is installed locally on your machine. The file management system makes it easy to modify the data because all you need to do is go to the file path of the folder ‘toxicfolder’ folder and drag in a toxic picture you want or the file path of the ‘nontoxicfolder’ folder and drag in your image. After doing this, go to the notebook lab and confirm they were added successfully to the notebook. If they are, then re-run each cell block in the project so the new images can run through the neural network. (Your file path may be slightly different but here is an example): 

![folder structure capstone](https://github.com/AlbersSoftware/Capstoneplant/assets/65799182/d4b41248-dd56-47d5-ae75-2a2b0239c06a)


# Future Changes
In the future I plan to host this project as a web app and potientially change the UI to IPy-Widgets. The goal for the program would be for a user to modify the data on a desktop computer and a mobile device to take a picture and run it against the trained data. 
