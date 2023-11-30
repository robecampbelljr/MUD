# MUD
A Multi-User Dungeon

### Framework
This MUD is built using the [evennia] framework. Evennia is a MUD development tool with much of what you need to create a world out of the box. While there are many "tools" to use to create worlds, you are free to modify the source code to create/edit/delete things as you see fit!

[evennia]: https://github.com/evennia/evennia.git

### Purpose
This is a "tutorial world". I will be following the evennia [Evennia Beginner Tutorial]. I will be using this README's in the _Journal/_ folder to for notes during the learning process as well as anecdotal experiences while following the tutorial.

[Evennia Beginner Tutorial]: https://www.evennia.com/docs/latest/Howtos/Howtos-Overview.html#beginner-tutorial

### In This Repository
This repository contains the _BeginnerTutorialWorld_. This world will contain all the code needed to run the world that I have created while following the [Evennia Beginner Tutorial]. If you wish to run the world yourself, you will have to:
1. Clone this repository
2. Navigate to /MUD (the parent directory)
3. Download OR clone [evennia] into the parent directory
4. Install Python 3.10 from the [python downloads] page
5. Install the python virtual environment (venv)
6. Initiate the evenv
7. Update pip and pip's setuptools
8. Install evennia in the virtual environment
9. Navigate to and start the _BeginnerTutorialWorld_

[python downloads]: https://www.python.org/downloads/

# Setup
**NOTE:** The following instructions are intended specifically for MacOS users. It also assumes you have installed and are familiar with **git**. If you need help with **git**, please refer to the official [git installation guide] and/or the official [git cheat sheet] to help you get started.

[git installation guide]: https://github.com/git-guides/install-git
[git cheat sheet]: https://education.github.com/git-cheat-sheet-education.pdf

The following setup guide is an amalgamation of the official [evennia installation guide]. Due to difficulties I faced while following the official guide, I decided to create my own to help you avoid some of those pitfalls.

[evennia installation guide]: https://www.evennia.com/docs/latest/Setup/Installation.html#

### 1. Clone this repository
Cloning this repository to your machine will download the /MUD parent directory to your computer. This is accomplished by opening a terminal on your machine. Then navigate to the folder in which you would like to save this project. Then run the follwoing command:
```
git clone https://github.com/robecampbelljr/MUD.git
```
If you chose to clone the /MUD repository into a folder named _/Projects_, your directory tree should appear as follows:
```
- Projects/
  - MUD/
    - BeginnerTutorialWorld/
    - .gitignore
    - LICENSE
    - README.md
```
### 2. Navigate to /MUD (the parent directory)
Open the MUD/ parent directory by entering the following command into your terminal
```
cd MUD
```

### 3. Download OR clone [evennia] into the parent directory
Depending on your intention with this project, you will want to _download_ OR _clone_ [evennia] into the MUD/ parent folder. If you wish to modify the world, create your own world, and/or use git for version control, _download_ [evennia] into the /MUD parent directory. If you want to just play around in the world that results from my following the tutorial _cloning_ the repository might be easier.

#### Download
To install evennia via _download_:
1.  Navigate to the [evennia] github page
2. Click on the **<> Code** button to open the dropdown
3. Select **Download ZIP** from the dropdown
5. Finally, open the ZIP file and extract the files to the MUD/ parent directory

#### Clone
To _clone_ evennia:
1. Open your terminal and navigate to the MUD/ parent directory
2. Enter the following command into the terminal:
```
git clone https://github.com/evennia/evennia.git
```

Regardless of which method you choose the hierarchy tree should appear as follows:
```
- Projects/
  - MUD/
    - BeginnerTutorialWorld/
    - evennia/
    - .gitignore
    - LICENSE
    - README.md
```
### 4. Install Python 3.10 from the [python downloads] page
In the [evennia venv setup guide] it states that it is compatible with Python 3.10 and Python 3.11.1, but in my experience, using Python 3.11.1 to setup the python virtual environment results in errors in installing and running evennia. However, I have found Python 3.10 to be perfectly stable. Before we go to all the trouble of installing Python 3.10 on your machine, lets make sure it isn't already installed. In your terminal window run the following command to check the version of Python available on your machine:
```
python3.10 -V
```
If Python 3.10 **is** installed you will see:
```
Python 3.10.*
```
If you receive this response, skip to Step 5.

However, if Python 3.10 is **not** installed you will see:
```
bash: python3.10: command not found
```
If this occurs, you can instally Python 3.10 by:
1. Navigating to the [python downloads] page
2. At the top of the page, select your operating system.
3. Scroll down until you see Python 3.10 and click on the link and follow the install instructions.
4. After installation is complete, run the Python version check command above again to verify the installation.

[evennia venv setup guide]: https://www.evennia.com/docs/latest/Setup/Installation-Git.html#virtualenv

### 5. Install the python virtual environment (venv)
To install the python venv in your terminal, ensure you are in the MUD/ parent directory, then running the command:
```
python3.10 -m venv evenv
```
This command instructs Python 3.10 to use the module (-m) called "venv" as a script, which creates the python venv. The final part of the command gives the environment a name. In this case we call it "evenv" meaning "evennia virtual environment"
### 6. Initiate the evenv
To initiate the evnev ensure you are still in the MUD/ parent directory and run the following command:
```
source evenv/bin/activate
```
If everything is working correctly your terminal should have "(evenv)" to the left of your command line as follows:
```
(evenv) ComputerName:MUD Username$ []
```
That (evenv) indicates the virtual environment is running corectly.
### 7. Update pip and pip's setuptools
pip is the Pythong package installer. Before we do anymore work we want to make sure pip and Python's setuptools are up to date. run the following commands:
```
pip install --upgrade pip
pip install --upgrade setuptools
```
### 8. Install evennia in the virtual environment
Now we will install evennia to the virtual environment. We can accomplish this by running the following command:
```
pip install -e evennia
```
This command installs the *evennia* package that we installed in Step 3 in **editable mode** (-e) also known as **development mode**. This allows us to make changes in our code, and those changes will be reflected in the running dev server without having to reinstall the package.
### 9. Navigate to and start the _BeginnerTutorialWorld_
With evennia installed, you can run the BeginnerTutorialWorld. Navigate to the BeginnerTutorialWorld folder and then start the world:
```
cd BeginnerTutorialWorld
evennia start
```
If everything has been installed correctly, you should see the following in your terminal:
```
------------------------------------- Evennia ---
BeginnerTutorialWorld Portal 2.3.0 (rev 57f109c)
    external ports:
        telnet: 4000
        webserver-proxy: 4001
        webclient-websocket: 4002
    internal_ports (to Server):
        webserver: 4005
        amp: 4006

BeginnerTutorialWorld Server 2.3.0 (rev 57f109c)
    internal ports (to Portal):
        webserver: 4005
        amp : 4006
-------------------------------------------------
```
# Congratulations!
You can now connect to and explore the BeginnerTutorialWorld! Once connected, you will be instructed how to create a character and how to login.
# Create your own world
If you want to create your own world within this MUD/ parent directory you can! Following the instructions in the [initialize new game] tutorial on the [evennia docs] page to create your own world and follow the [Evennia Beginner Tutorial] yourself!

[initialize new game]: https://www.evennia.com/docs/latest/Setup/Installation.html#initialize-a-new-game
[evennia docs]: https://www.evennia.com/docs/latest/index.html