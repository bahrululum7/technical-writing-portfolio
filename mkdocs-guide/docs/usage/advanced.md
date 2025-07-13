![status](https://img.shields.io/badge/status-production--ready-blue)

# Advanced Usage of MkDocs

Once you're comfortable running MkDocs locally and editing basic Markdown files, you can take your documentation to the next level using more advanced features. This section introduces several powerful capabilities that help make your documentation more organized, attractive, and maintainable.

---

## 🎨 Using Themes

MkDocs supports themes to change the appearance of your site. The most popular and widely used theme is **Material for MkDocs**, which offers:

- Responsive design for mobile and desktop
- Built-in search functionality
- Tabs, collapsible sections, and icons
- Enhanced Markdown support

### How to install Material for MkDocs:

```bash
pip install mkdocs-material
```

Then, update your `mkdocs.yml` configuration:

```yaml
theme:
  name: material
```

---

## 🧩 Using Plugins

Plugins allow you to extend MkDocs functionality, such as:

- Generating tables of contents
- Creating image galleries
- Automatic navigation
- Better Markdown features

To use a plugin, install it via `pip` and enable it in `mkdocs.yml`:

```bash
pip install mkdocs-awesome-pages-plugin
```

Example `mkdocs.yml`:

```yaml
plugins:
  - search
  - awesome-pages
```

---

## 🧱 Organizing Your Documentation

For larger projects, it's important to structure your documentation clearly. Group related content using folders inside the `docs/` directory.

Example structure:

```
docs/
├── index.md
├── about.md
├── install/
│   └── installations.md
├── usage/
│   ├── intro.md
│   └── advanced.md
```

Then configure the navigation in `mkdocs.yml`:

```yaml
nav:
  - Home: index.md
  - About: about.md
  - Install Tutorial: install/installations.md
  - Usage:
      - Intro: usage/intro.md
      - Advanced: usage/advanced.md
```

---

## 📁 Static Files (Images, Logos, etc.)

To include logos or images in your documentation:

1. Create an `images/` folder inside `docs/`
2. Add your image files (e.g. `logo.png`)
3. Reference them in Markdown:

```markdown
![Logo](images/logo.png)
```

---

## 🌐 Publishing with GitHub Pages

Once you're happy with your documentation, you can publish it online for free using GitHub Pages.

Steps:

1. In your terminal, run:
   ```bash
   mkdocs build
   ```

2. Then deploy with:
   ```bash
   mkdocs gh-deploy
   ```

3. Your site will be live at:
   ```
   https://yourusername.github.io/your-repo-name/
   ```

> Note: Make sure your repository is public and you’ve enabled GitHub Pages in your repository settings.

---

## ✅ Summary

With advanced features like themes, plugins, structured navigation, and GitHub Pages deployment, MkDocs becomes a powerful tool for creating professional, scalable documentation.

As a technical writer, mastering these tools not only improves the user experience but also demonstrates your ability to deliver high-quality documentation at scale.
