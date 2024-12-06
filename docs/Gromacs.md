### Installing Gromacs for Windows Operating System

#### Objectives
```
1. To download and install Gromacs Simulation software for the Windows operating system
2. Run MD simulation for Lysozyme protein
```

#### Installation Instructions
Step-1: Two procedures are available to install Gromacs on Windows. They are
1. Directly installing gromacs on windows operating system using Visual studio software.
2. Installing windows subsystem for linux (WSL) and installing windows in it.
```
We will use the second appraoch which is relatively easy to install gromacs in windows.
```
#### Installing Windows subsystem for linux (WSL)
**Step-1:** Go to microsoft store in your windows system and search for ubuntu

**Step-2**: After installation you may encounter an error stating "An error occurred during installation. Distribution Name: 'Ubuntu' Error Code: 0x80072efe";

To solve the error follow the instructions suggested in the below link: "https://learn.microsoft.com/en-us/answers/questions/1187339/resolving-error-0x80370114-the-operation-could-not"
a) Search for control panel in "windows search bar"

b) In the control panel tick "Virtual Machine Platform", "Windows Hypervisor Platform", "Windows Powershell2.0", "Windows Subsystem for Linux", and "Work Folders Client" and click *OK*.

**Step-3**: Create an username and passoword for WSL.

**Step-4**: Search for ubuntu in the *search bar*, a command prompt terminal will be opened as shown in the screenshot below

**Step-5**: ```Type wsl --update to update the wsl.```

**Step-6**: ```Type sudo apt-get update in the terminal, this update the ubuntu packages uptodate```

**Step-7**: ```Type sudo apt-get upgrade, Upgrade replaces the program with new versions```

**Step-8**: ```Type sudo apt-get install gcc```

**Step-9**: ```Type sudo apt-get install cmake```

**Step-10**: ```Type sudo apt-get install build-essential```

**Step-11**: ```Type sudo apt-get install libfftw3-dev```

The above packages are required for the installation of gromacs.

**Step-12**: Download gromacs package from ```https://manual.gromacs.org/documentation/current/download.html```

**Step-13**: In terminal type ``` wget https://ftp.gromacs.org/gromacs/gromacs-2024.4.tar.gz```

**Step-14**: In terminal type ``` tar -xvzf gromacs-2024.4.tar.gz ```

**Step-15**: In terminal type ``` cd gromacs-2024.4```

**Step-16**: In the directory of gromacs ``` mkdir build and cd build```

**Step-17**: In the terminal type ```cmake .. -DGMX_BUILD_OWN_FFTW=ON -DREGRESSIONTEST_DOWNLOAD=ON```

**Step-18**: In the terminal type ``` sudo make ```

**Step-19**: In the terminal type ``` sudo make check```

**Step-20**: In the terminal type ``` sudo make install```

**Step-21**: In the terminal tyoe ```source /usr/local/gromacs/bin/GMXRC```


**Step-22**: Type gmx in the terminal it should show the below output then your installation is completed. Enjoy!




 








#### References:
1. https://www.youtube.com/watch?v=kCKYkNygc9I


