![status](https://img.shields.io/badge/status-in%20progress-yellow)

# What is MKDocs
MKDocs is a static site generator based on Python that is easy to use.  
It’s suitable for documenting open-source projects or internal team documentation.  
Below is a tutorial on how to install MKDocs on Windows OS.

## Installation on Windows & Linux

=== "Windows"

    1. Install Python from [python.org](https://python.org)
    2. Open the downloaded installer and run it. Don’t forget to tick **"Add Python to PATH"**
    ![Alt Text](../images/installpython.png)
    3. Open CMD (Command Prompt) on your Windows:
        - Press Windows key + R
        - Type `cmd`
        - Hit Enter
    4. Check your Python version:
        Type: `python --version`  
        If Python is installed, continue to step 5.
    5. Run: `pip install mkdocs`
    6. When the process is done, check with:  
       Type: `mkdocs --version`  
       If it works, your MkDocs version will appear.
    
    !!! note 
        Make sure Python is installed before installing MkDocs.


=== "linux"
    1. Update your package manager (optional but recommended):
        sudo apt update
    2. Install Python and pip (Python’s package manager):
        sudo apt install python3 python3-pip
    3. Check your Python version:
        Type:
        python3 --version

        If Python is already installed, you will see a version number like `Python 3.x.x`.

    4. Install MkDocs:
      Type:
      pip3 install mkdocs

    5. After the installation is done, check if it works:
       Type: 
       mkdocs --version

     If everything went well, it will show the version of MkDocs you just installed.
    !!! note 
        Make sure Python is installed before installing MkDocs.

## MKDocs Basic Instructions

- `mkdocs new "name_folder"` : Create a new MkDocs project
- `mkdocs serve` : Run local server to preview site
- `mkdocs build` : Generate static site files
- `mkdocs --version` : Show MkDocs version

## General Problems During Installation

**Problem: Python not recognized in CMD**

- Solution: Uninstall Python, then reinstall with the **"Add Python to PATH"** option checked.


