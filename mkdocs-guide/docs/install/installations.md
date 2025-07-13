![status](https://img.shields.io/badge/status-production--ready-blue)

# What is MkDocs

**MkDocs** is a modern, fast, and lightweight static site generator designed for creating project documentation.  
It allows you to write your content in Markdown and build a full-featured website with just a few commands.

Whether you're documenting an open-source project or creating internal manuals, MkDocs makes the process smooth and efficient.

---

## ⚙️ Installation on Windows & Linux

Follow the steps below to install MkDocs on your computer. You only need a working Python environment and internet connection.

=== "Windows"

    1. Download the latest version of Python from [python.org](https://python.org)
    2. Run the installer. IMPORTANT: Make sure to check the box **"Add Python to PATH"**
    3. Open the Command Prompt:
        - Press `Windows + R`
        - Type `cmd` and press Enter
    4. Check if Python is installed:
        Type: `python --version`  
        If successful, it will return a version like `Python 3.11.5`
    5. Install MkDocs using pip:
        `pip install mkdocs`
    6. Verify MkDocs installation:
        `mkdocs --version`  
        You should see the version of MkDocs installed.

    !!! note
        If Python is not recognized, try reinstalling it and ensure "Add to PATH" is checked during setup.

=== "linux"

    1. Update your package manager (recommended):
        `sudo apt update`
    2. Install Python and pip (Python’s package manager):
        `sudo apt install python3 python3-pip`
    3. Check your Python version:
        `python3 --version`  
        It should display something like `Python 3.10.12`
    4. Install MkDocs:
        `pip3 install mkdocs`
    5. Verify installation:
        `mkdocs --version`  
        If successful, the installed version will appear.

    !!! note
        You may need to use `python3` and `pip3` instead of `python` and `pip` on Linux.

---

## 🔧 Basic MkDocs Commands

Here are some essential MkDocs commands you’ll use regularly:

- `mkdocs new "project_name"` – Create a new MkDocs project folder  
- `mkdocs serve` – Start a live preview server at `localhost:8000`  
- `mkdocs build` – Build the static site into the `site/` folder  
- `mkdocs --version` – Display the installed version of MkDocs

---

## 🚨 Common Installation Issues

**❌ Problem:** `'python' is not recognized as an internal or external command`

**✅ Solution:**  
This usually means Python wasn't added to your system PATH.  
Reinstall Python and **make sure to check "Add Python to PATH"** during installation.

---

With MkDocs installed, you're now ready to start building beautiful documentation sites with just Markdown and a few commands. 🎉
