# Welcome to ES140X

Follow these instructions if you are a Windows or Linux User.
Below are set of instructions to help you effectively participate 
in this class, ES140X: Introduction to Engineering. 

- [Watch videos on Brightspace](#watch-videos-on-brightspace)
- [Set up Windows Subsystems for Linux](#set-up-windows-subsystems-for-linux)
- [How to open your terminal](#how-to-open-your-terminal)
- [Download this repository](#download-this-repository)
- [Set up your Anaconda environment](#set-up-your-anaconda-environment)
- [Access an assignment or class in Jupyter](#access-an-assignment-or-class-in-jupyter)

<br />
<br />
<br />


## Watch videos on Brightspace

We have created a few videos to assist with some of the set up steps. The videos are hosted on Brightspace under the Videos section of this class. We recommend that you watch through the videos in order first to get an understanding of what you need to be doing here. Then, continue through this document and replicate what has been shown in the videos, using them as a second source.
<br />
<br />
<br />

## Set up Windows Subsystems for Linux 

For Windows machine, we recommend students to use the Windows Subsystems for Linux (WSL). If you are a Linux user, you can skip this section. The following link may provide additional information if the steps below give you trouble   https://docs.microsoft.com/en-us/windows/wsl/install-win10  
If you have any issues during this process, please contact one of the TAs  
1. Go to the cortana search bar in the bottom left of your screen and look for "Windows Powershell"
2. Open the powershell by right clicking the icon and selecting "Run as administrator"
3. Copy and paste this single line of code into the terminal that opens up. You may have to right click to paste text into your terminal. Control-V may work as well.  
      `dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart`
4. Restart your computer by selecting restart from the power options in the lower left menu of your windows bar.
5. Copy and paste this web address into the search bar of any web browser.  
    https://www.microsoft.com/en-us/p/ubuntu-2004-lts/9n6svws3rx71?rtc=1&activetab=pivot:overviewtab
6. Select the large blue "Get" button to open this app entitled Ubuntu in a Microsoft Store window. Select Get again in the windows store and then Install will appear. Hit the install button. Ubuntu will be the equivalent linux terminal you will use moving forwards.
7. In the same blue box, hit the Launch button that has now appeared. This will open Ubuntu for the first time on your device. It will open a black terminal window and will say “Installing, this may take a few minutes...” 
8. Enter a UNIX username once prompted. I would recommend using ""firstnamelastname"". No capitals or other symbols are allowed.
9. Enter a password for this username. I recommend using your computer’s login password.
10. Retype the password when prompted.
11. To open a new terminal in the future, just type Ubuntu into the cortana search bar and run as administrator. This will be the terminal you use to navigate directories and files in future steps.
12. In order to get into your C drive from this linux subsystem home directory, input `cd \mnt/c/Users`. Use `ls` to see which files and folders are available to you in your current directory.
13. You may need some practice to feel more comfortable working with the terminal. 
        We recommend you to work throught this [tutorial](https://swcarpentry.github.io/shell-novice/)
        to learn more about basic terminal command. 
 <br />
 <br />
 <br />


## How to open your terminal

#### Linux 
You can open the terminal application on Linux by either:
1. Press “Ctrl+Alt+T”
2. Search for “terminal” 

#### Windows
0.  For Windows users, make sure you have set up the Windows Subsystem for Linux (WSL) for your machine. If not, you can follow the instruction [here](#set-up-windows-subsystems-for-linux).
1. Once you log into your WSL, you will be automatically put in a terminal. You can also open up a terminal window by searching for and opening the app Ubuntu.
  <br />
  <br />
  <br />


## Download this repository

This repository contains software and files neccessary for activities in this class, so we ask you to download this repository and put it in a location convienient for later reference. We recommend you put it in your home directory using the commands below:  
`cd $HOME`   <br/>
`mkdir ES1403_class`  <br/>
`cd ES1403_class`  <br/>
`git clone https://github.com/2021-mccabe-vanderbilt-es1403/ES140X.git` <br/>
<br />
<br />
<br />

## Set up your Anaconda environment

Anaconda is a free, open-source distribution of the Python and R programming language for scientific computing, that aims to simplify package management and deployment. In this class, we will use Anaconda to manage our Python environment. 


#### Linux and Windows (Windows Subsystem for Linux)
0. For Windows users, make sure you have set up the Windows Subsystem for Linux (WSL) for your machine. If not, you can follow the instruction [here](#set-up windows-subsystems-for-linux).  
1. Go to this link https://docs.conda.io/en/latest/miniconda.html and select the **Linux** installer for Python 3.8 with 32-bit or 64-bit depends on your computer (use this link if you are unsure https://itsfoss.com/32-bit-64-bit-ubuntu/). 
   <\t> **Note**  Even if you are using Windows download for ***Linux***
2. Right click on the correct version and select “Copy link address”
3. Open your terminal and download the file with the copied link  
    `cd $HOME`  
    `curl -O <The link you just copied>`  
4. Once the downloads finish, type `ls` and make sure you can identify the downloaded file (should look something like “Miniconda3-***-Linux-x86_**.sh”) , then   
    `bash <The file you just download>`
5. Restart your terminal session and type `conda --version` to make sure the installation finishes. 
6. In your terminal, `cd` into the folder (ES140X).
If you followed the above [instructions](#Download-this-repository) and put this repository at your home directory, you can change into that folder by  
`cd ~/ES1403_class/ES140X`
7. If you don’t know how to do this, make sure you watch the video labeled `classroom_walkthrough.mp4` from Brightspace before continuing.
8. Create and activate a new conda environment by typing in the terminal window:
    `conda env create -f environment.yml`  
    If prompted you may need to update your conda environment and rerun the above commands.
9. When the command has successfully executed then type:  
    `conda activate class37`   
**Note:** You will need this command whenever starting up a new terminal to access the class materias
  <br />
  <br />
  <br />

## Access an assignment or class in Jupyter

1. Follow the link that will be sent out through email to a specific assignment. Accept the assignment, and let a copy be made to your GitHub account.  <br/>  <br/>
<\t> **Note** from time to time, accepting the assignment will work, but the green bar will not complete and notify you that your copy is ready. Don't worry about it, as soon as you hit accept, the assignment will be available to you. Exit from that browser window, and in a new one navigate to your GitHub account. Under the 2020-mccabe-vanderbilt-es140X classroom, you should be able to find all of your assignments. It can be found from your GitHub homepage, in the left column under organizations. 
2. Once on your repositories GitHub page, look for a large green button with **Code** in white letters. Click on it to open a drop down box, and copy the URL that is there. 
3. In a terminal window, use the `cd` command to navigate to the ES1403_class directory. It should be located at `~/ES1403_class`.
4. Run the following command: `git clone <the-url-you-just-copied>`. This will make a local copy of the repository at GitHub.com. 
**MAKE SURE YOU ARE NOT IN THE ES140X DIRECTORY WHEN YOU CLONE A NEW REPOSITORY. JUST CLONE IT TO THE ES1403_class DIRECTORY.**
Use `pwd` to check what directory you currently are in.
5. Use the `ls` command to view all of the files in that directory, and you should see a new directory titled the same as the repository you just copied.
6. `cd` into the cloned assignment you just installed. If you don’t see the assignment on your local machine, watch the `classroom_walkthrough.mp4` video for additional help.
7. Type `jupyter notebook` into your terminal
8. The jupyter notebook will be open as one tab in your default browser  
If this doesn't occur automatically, look a the output from your jupyter notebook command. You should see a web link that looks something like `http://localhost:8888/?token=fd014533bc5780c313dfd1803838a89c6a90cdcd75d0cb2b` Copy that link by highlighting it and using ctrl-c. Then, paste the link into the web browser of your choice. We recommend Google Chrome.
9. Click on folders to navigate through them, or on files to open them. Text files will open with a built in text editor. Jupyter notebook files have the extension .ipynb. These are the files where you execute python code, and where we'll run our assignments from.

