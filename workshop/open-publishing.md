# Open Publishing

## Workshop Description

Open publishing enhances accessibility, transparency, and reproducibility in research. This workshop introduces participants to open publishing principles and practical tools for creating interactive and reproducible scientific documents. Participants will learn how to use Jupyter Book and MyST Markdown to develop and publish open research content efficiently.

This session is ideal for researchers, educators, and students looking to improve their scientific communication. No prior experience with Jupyter Book or MyST Markdown is required, making it accessible to beginners.

### Learning Outcomes

By the end of the workshop, participants will be able to:

- Understand the significance of open publishing in research.
- Utilize Jupyter Book to create structured, interactive documents.
- Apply MyST Markdown for rich content, including citations and equations.
- Publish scientific content online using open-access platforms.
- Implement best practices for accessibility and reproducibility.

### Format

This is an interactive, hands-on workshop. Participants will follow along with demonstrations and practice key concepts through guided exercises.

### Prerequisites

To ensure a smooth learning experience, participants are encouraged to install the following tools before the workshop:

- **uv**: [Installation Guide](https://docs.astral.sh/uv/getting-started/installation/)
- **Jupyter Book**: `pip install -U jupyter-book mystmd`
- **GitHub Account** (for publishing content)

---

## Date and Time

- **Date**: Monday, April 21, 2025
- **Time**: 10:00 AM - 11:00 AM ET
- **Location**: Virtual (Zoom link will be provided upon [registration](https://tiny.utk.edu/openscience-register))

## Instructor

- Name: [Qiusheng Wu](https://geography.utk.edu/people/instructional-faculty/wu-qiusheng)
- Affiliation: [Department of Geography & Sustainability](https://geography.utk.edu), University of Tennessee, Knoxville
- Email: qwu18@utk.edu
- Website: <https://gishub.org>

## Who Should Attend?

This workshop is ideal for:

- Researchers looking to improve their open publishing workflow.
- Students and faculty interested in reproducible research.
- Anyone new to Jupyter Book and MyST Markdown who wants a hands-on introduction.
- Those interested in learning how to automate publishing workflows using GitHub.

No prior experience with Jupyter Book or MyST Markdown is required.

## Registration

To attend, please complete the registration form at [this link](https://tiny.utk.edu/openscience-register). Once registered, you will receive a confirmation email with the Zoom link and preparation instructions.

## Workshop Recording

A recording of the workshop will be available on the [Open Geospatial Solutions](https://www.youtube.com/playlist?list=PLAxJ4-o7ZoPcudAyC050UOrSDr3v9leUP) YouTube channel after the event.

---

## 1. Introduction to Open Publishing

### Why Open Publishing?

- **Reproducibility**: Enables verification and reuse of research.
- **Accessibility**: Expands the reach of scientific knowledge.
- **Transparency**: Increases trust in research findings.
- **Collaboration**: Facilitates teamwork and interdisciplinary research.
- **Automation**: Ensures continuous updates and improvements to documentation.

### Tools for Open Publishing

- **Jupyter Book**: An open-source tool for creating interactive books.
- **MyST Markdown**: A markdown language supporting citations, figures, and equations.
- **GitHub Pages**: A hosting service for publishing online content.
- **GitHub Actions**: Automates publishing workflows.

---

## 2. Hands-on: Creating a Jupyter Book Project

### Setting Up the Environment

```sh
pip install -U jupyter-book mystmd
```

### Creating a New Jupyter Book

```sh
jupyter-book create mybook/
```

### Writing Content with MyST Markdown

- Headings and subheadings
- Citations and references
- Equations and figures
- Interactive content and code execution

### Building and Previewing the Book

```sh
jupyter-book build mybook/
```

---

## 3. Publishing and Best Practices

### Hosting Options

- **GitHub Pages**
- **ReadTheDocs**

### Version Control with GitHub

```sh
# Initialize a Git repository
cd mybook
git init
git add .
git commit -m "Initial commit"
git push origin main
```

### Automating Deployment with GitHub Actions

- Setting up a workflow file for automatic builds.
- Ensuring seamless updates when content changes.

### Licensing and Attribution

- **Creative Commons Licensing**
- **FAIR Principles** (Findable, Accessible, Interoperable, Reusable)

### Ensuring Accessibility and Reproducibility

- Using version control (Git/GitHub)
- Structuring content for clarity and navigation
- Documenting dependencies and software versions

---

## Resources & Further Reading

- [Jupyter Book Documentation](https://jupyterbook.org/)
- [MyST Markdown Guide](https://myst-parser.readthedocs.io/)
- [FAIR Principles](https://www.go-fair.org/fair-principles/)
- [Creative Commons Licensing](https://creativecommons.org/)
- [GitHub Pages Guide](https://pages.github.com/)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)

This hands-on workshop will equip participants with the skills to create, automate, and publish open, interactive, and reproducible scientific content using Jupyter Book, MyST Markdown, and GitHub.

---

Happy coding! 🎉
