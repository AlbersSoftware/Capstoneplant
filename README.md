# Capstoneplant

# About this project
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


# Installation Guide and getting started!

Installation Guide 
Step 1: Install Anaconda at: https://www.anaconda.com/download

Step 2: run the installer and in advanced settings of the installer tick the box to 'Add Anaconda3 to the system PATH environment variable' 
 
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
 


Step8: Download any .jpg picture of poison ivy or poison ivy look-a-like (e.g. Virginia Creeper) from the internet that is clear and just of the plant. You can opt to use the test images or one from the Kaggle set used in the project. We resize the image in the program so size shouldn't make a huge difference. However, I’d stray from images that are large or small for better predictions.

Step9: 'Shift-enter' cell block by cell block through the entire program. The last cell block opens the UI of the program. The login username and password are both 'admin' (all lower-case). If things are taking a while don’t worry, chances are the kernel is busy and you just need to wait a second or perhaps you missed a shift-enter on a cell. You can interrupt the kernel with the stop button and try again block by block.


Step 11: After a successful login click the 'upload files' button and it will prompt open your file directory in a new window. From there, choose the poison ivy picture in .jpg format of your choice that you have downloaded.

Step 12: Next you will see your photo in the UI, when you see that photo there click the 'predict' button. This will run your picture through the Convolutional Neural Network and make a prediction of either (toxic or non-toxic) and print that result to the console along with the associated picture.
 (You can re-upload and re-predict as you desire and close the window with the 'x' in the top right-hand corner of the login page to cancel the program.)