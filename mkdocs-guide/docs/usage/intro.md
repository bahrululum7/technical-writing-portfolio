![status](https://img.shields.io/badge/status-production--ready-blue)

# Getting Started with MkDocs

**MkDocs** is a static site generator that helps you create professional documentation websites from plain text files.  
It’s specifically designed for technical documentation and widely used in both open-source and enterprise environments.

One of MkDocs' greatest advantages is its simplicity. You write in **Markdown**, a lightweight and easy-to-learn markup language, and MkDocs turns it into a fully functional website.

This guide walks you through how to run MkDocs for the first time on your local machine.

---

## 🛠️ Requirements

Before getting started, make sure you have:

- [Python 3.x](https://www.python.org/)
- `pip` (Python package installer)
- MkDocs installed via pip:
  
  ```bash
  pip install mkdocs
  ```

- A text editor (e.g., Visual Studio Code)
- A terminal application (e.g., Git Bash, CMD, or Terminal)

Once these are ready, you can start working with MkDocs locally.

---

## 🚀 Previewing Your Documentation Locally

To see your documentation site in your browser:

1. Open your terminal or command prompt.

2. Navigate to your MkDocs project folder. For example:

   ```bash
   cd C:\Users\YourName\technical-writing-portfolio\mkdocs-guide
   ```

3. Start the development server:

   ```bash
   mkdocs serve
   ```

4. Open your browser and visit:

   ```
   http://127.0.0.1:8000/
   ```

You should now see your documentation site live.

---

## 🔁 Real-Time Editing

While the development server is running, you can edit any `.md` file inside the `docs/` folder.  
MkDocs will automatically detect changes, rebuild the site, and refresh the browser — a feature known as **live reload**. This makes the editing process smooth and immediate.

---

## 📌 Why Local Preview Matters

Previewing your documentation locally allows you to:

- Verify layout and structure before publishing
- Catch formatting issues early
- Improve the reading experience
- Apply quick changes without deploying

This workflow follows modern **Docs-as-Code** practices, where documentation is treated like source code — stored in plain text, version-controlled, and collaboratively edited.

---

## ✅ Summary

You’ve just learned how to:

- Set up your environment for MkDocs
- Run your documentation site locally
- Edit content with instant results

You're now ready to move forward and explore more advanced features.

➡️ Continue to: [Advanced Usage](advanced.md)
