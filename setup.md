## Python / Sunpy tutorial for summer students 2022

### Installation guide
For the purposes of this presentation, we will be using [Anaconda](https://www.anaconda.com/distribution/) for managing our python distribution and additional packages, [jupyter notebooks](https://jupyter.org/try) as our IDE and of course [python](https://www.python.org/) as our programming language.

## 1. Installing Anaconda
Should you already have Anaconda installed, skip to step 2.

### 1.1. Installation under Windows
- [Download the Anaconda installer](https://www.anaconda.com/distribution/#windows) (Python 3.9 version)
- Anaconda is about 3 GB, make sure there's enough disk space available
- Double click the installer to launch
- Click Next
- Read the licensing terms and click "I Agree"
- Select an install for "Just Me" and click Next
- Select a destination folder to install Anaconda and click Next, you can use the default (for example `C:\Users\<user>\anaconda3`)
- Check only "Register Anaconda3 as my default Python 3.9"
- Click the Install button
- Click Next
- Anaconda will ask you to install PyCharm, which is another IDE that we will not use. Click Next to skip
- If the installation was successful, click Finish
- Verify your installation by doing the following:
    - Click Start, search or select "Anaconda Prompt" from the menu (alternatively: search or select "Anaconda Navigator" and launch "Anaconda Prompt" from there)
    - This will open a Terminal in a new window. Enter `conda list`
    - Enter `python`, wait until it is loaded and enter `quit()`
- If any of the above commands lead to errors, refer to step 1.5.

### 1.2. Installation under Linux
- [Download the Anaconda installer](https://www.anaconda.com/distribution/#linux) for Linux (Python 3.9 version)
- In a terminal enter `bash ~/Downloads/Anaconda3-2022.05-Linux-x86_64.sh` (alternatively `bash <file you just downloaded.sh>`)
- Hit Enter to view license terms, scroll to the bottom and enter "Yes"
- The default path of installation is `/home/<user>/anaconda3`. It is recommended to use this as your install location (but you may enter a different path at this point). Hit Enter.
- It is recommended to initialize Anaconda3 by typing "yes"
- Close the current terminal window and open a new one
- Run the command `conda config --set auto_activate_base False`
- Verify your installation by doing the following:
    - Enter `conda list`
    - Enter `python`, wait until it is loaded and enter `quit()`
- If any of the above commands lead to errors, refer to step 1.5.

### 1.3. Installation under macOS
- [Download the graphical Anaconda installer](https://www.anaconda.com/distribution/#macos) for macOS (Python 3.9 version)
- Double-click the downloaded file and click continue to start the installation
- Answer the prompts on the Introduction, Read Me, and License screens
- Click the Install button to install Anaconda in your `~/opt` directory (which is recommended, you can click the "Change Install Location" button to install in another location)
- On the Destination Select screen, select Install for me only
- Click Continue
- Anaconda will ask you to install PyCharm, which is another IDE that we will not use. Click Continue to skip
- If the installation was successful, click Close
- Verify your installation by doing the following:
    - Hit Cmd+Space, type either "Anaconda Prompt" or "Anaconda Navigator" and start the program (if you started "Anaconda Navigator", you can launch "Anaconda Prompt" from there)
    - This will open a Terminal in a new window. Enter `conda list`
    - Enter `python`, wait until it is loaded and enter `quit()`
- If any of the above commands lead to errors, refer to step 1.5.

### 1.4. Updating an existing version of Anaconda
Windows: Open the Start Menu and launch Anaconda Prompt (either by typing it in the search bar, or via Anaconda Navigator)

Linux and macOS: Open a terminal window
- type the following two commands:
```bash
conda update conda
```

### 1.5. Troubleshoot
- Refer to https://docs.continuum.io/anaconda/user-guide/troubleshooting/
- or contact me (mwaidele@stanford.edu)

## 2. Downloading the tutorial repository
All of the material for the tutorial will be located in my [GitHub-repository](https://github.com/mwaidele/py_sunpy_SummerStudents2022). Although it can be easily viewed and accessed there, it is more convenient to download the whole repository on your local device.

### 2.2. Downloading via `git` (recommended)
If you have `git` installed, you can clone the repository. 
- Make a new directory for the lecture material (for example `~/lectures`)
- In a terminal window, type 
```bash
git clone https://github.com/mwaidele/py_sunpy_SummerStudents_2022.git
```

### 2.1. Downloading via Browser
- [Download my GitHub repo](https://github.com/mwaidele/py_sunpy_SummerStudents2022/archive/refs/heads/master.zip)
- Click "Save File"
- Move the downloaded file (should be in your `Downloads/` directory) into any folder you would like to store the lecture material
- Extract all files (double click the .zip file)
- After extraction, rename the folder that was created to `py_sunpy_SummerStudents2022`

## 3. Setup the lecture environment
In order to make sure all the necessary packages to use `sunpy` are installed, a virtual environment specifically for this tutorial can be installed.

Windows: Open the Start Menu and launch Anaconda Prompt (either by typing it in the search bar, or via Anaconda Navigator)

Linux and macOS: Open a terminal window

- Navigate your directory to the lecture material via (windows):
```bash
cd <your_dir>\py_sunpy_SummerStudents2022
```
(Linux and macOS):
```bash
cd <your_dir>/py_sunpy_SummerStudents2022
```
where `<your_dir>` is the folder in which you extracted the .zip file (or cloned the repo into via `git`)

- Type the following command
```bash
conda config --add channels conda-forge
conda env create -f pyTUT.yml
```
- The installation will take about 10 minutes
- Type 
```bash
conda activate pyTUT
ipython kernel install --user --name=pyTUT
jupyter notebook
```
- Click "Quit" in the upper right in the browser tab that just opened and close the tab
- Type `conda deactivate`

You should be all set up and ready for the tutorial now. If you have any issues, please feel free to contact me (mwaidele@stanford.edu).
