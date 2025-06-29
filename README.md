# DGS Docs

📚 This repository contains the documentation for the **Domain Glossary System (DGS)**.

---

## 🔗 Live Documentation

Visit the full documentation site here:

👉 [https://abhishekmalvadkar.github.io/dgs-docs](https://abhishekmalvadkar.github.io/dgs-docs)

---

## 📁 Project Structure

```
dgs-docs/
├── docs/                  # All Markdown files for documentation
│   ├── index.md
│   ├── project-purpose.md
│   ├── diagrams/
│   │   ├── context-diagram.md
│   │   ├── backend-container-diagram.md
│   │   └── ...
│   ├── stories.md
│   └── event-storming-mvp1.md
├── mkdocs.yml             # MkDocs configuration file
└── .github/
    └── workflows/         # GitHub Actions for deployment
```

---

## 🚀 Getting Started (Local Development)

To run and preview the docs locally:

1. Make sure Python is installed

2. Install MkDocs and required plugins:

   ```bash
   pip install mkdocs-material mkdocs-mermaid2-plugin
   ```

3. Serve the documentation site:

   ```bash
   mkdocs serve
   ```

Then visit: [http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## 🛠️ Built With

* [MkDocs](https://www.mkdocs.org/) – Static site generator for project docs
* [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) – Beautiful and responsive UI theme
* [Mermaid](https://mermaid.js.org/) – Diagrams-as-code for architecture and flows
* [Excalidraw](https://excalidraw.com/) – Visual event storming and collaborative modeling

---

## ✍️ Contributing

Want to help improve the documentation?

1. Fork this repository
2. Create a new branch: `git checkout -b feature/my-update`
3. Make your changes and commit them
4. Push to your fork: `git push origin feature/my-update`
5. Submit a pull request

✅ All contributions are welcome and appreciated!

---

## 👤 Maintainer

**Abhishek Malvadkar**
GitHub: [@abhishekmalvadkar](https://github.com/abhishekmalvadkar)

