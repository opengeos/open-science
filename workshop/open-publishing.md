# Open Publishing

## Workshop Description

Open publishing enhances accessibility, transparency, and reproducibility in research. This workshop introduces participants to open publishing principles and practical tools for creating interactive and reproducible scientific documents. Participants will learn how to use Jupyter Book and MyST Markdown to develop and publish open research content efficiently.

This session is ideal for researchers, educators, and students looking to improve their scientific communication. No prior experience with [Jupyter Book](https://jupyterbook.org/) or [MyST Markdown](https://mystmd.org) is required, making it accessible to beginners.

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

- **Date**: Monday, April 22, 2025
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

## Introduction to Open Publishing

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

## Workshop Modules

### Module 1: Setup and Environment

- Introduction to MyST
- Setting up your environment
- Creating your first MyST project

### Module 2: Basic Document Structure

- Page frontmatter
- Adding citations
- Inserting and referencing figures
- Adding tables and other content types

### Module 3: Interactive Documents

- Adding executable code cells
- Running notebooks within MyST
- Cross-referencing content
- Creating interactive elements

### Module 4: Publishing and Distribution

- Exporting to different formats (PDF, Word, LaTeX)
- Deploying to GitHub Pages
- Customizing templates and themes
- Building a TOC structure

## Detailed Schedule

### Module 1: Setup and Environment

#### Setup Instructions

```bash
# Create and activate conda environment
conda create -n myst-workshop python=3.12
conda activate myst-workshop

# Install required packages
conda install -c conda-forge mystmd
conda install -c conda-forge texlive-core latexmk jupyterlab-myst ipykernel

# Verify installation
myst -v
```

**VS Code Extension**: Install [MyST-Markdown](https://marketplace.visualstudio.com/items/?itemName=ExecutableBookProject.myst-highlight)

#### Your First MyST Project

```bash
# Clone starter template
git clone https://github.com/jupyter-book/mystmd-quickstart.git
cd mystmd-quickstart

# Start the MyST server
myst start
```

#### Core MyST Commands

```bash
# Initialize a new project
myst init

# Start the preview server (with execution)
myst start --execute

# Clean build files
myst clean
myst clean --all
myst clean --templates --cache
```

### Module 2: Basic Document Structure

#### Project Configuration

Edit `myst.yml`:

```yaml
# See docs at: https://mystmd.org/guide/frontmatter
version: 1
project:
  id: ab440adc-2db2-4534-8548-ad2b03879434
  title: Introduction to GIS Programming
  github: https://github.com/jupyter-book/mystmd-quickstart
site:
  template: book-theme
  options:
    favicon: images/favicon.ico
    logo: images/logo.png
```

#### Page Frontmatter

```yaml
---
title: Introduction to GIS Programming
subtitle: Using Python for GIS Applications
authors:
  - name: Your Name
    affiliations:
      - Your University
    orcid: 0000-0000-0000-0000
    email: your.email@example.com
license: CC-BY-4.0
keywords: GIS, python, geospatial, mapping
abstract: |
  This tutorial introduces geospatial analysis techniques using Python libraries and demonstrates how to effectively visualize and analyze geographic data.
kernelspec:
  name: python3
  display_name: Python 3
---
```

#### Adding Citations

To cite using DOI:

```
Change (Smith et al., 2020) to [](https://doi.org/10.XXXX/XXXXX)
```

To cite using BibTeX:

```
{cite:p}`myst2023,jupyterbook2021`
```

#### Figures and Images

Basic figure:

```
:::{figure} ./images/map.png
:label: my-map-figure
:alt: GIS map showing population density
:align: center

Map showing population density in the study area.
:::
```

Remote image with alignment:

```
:::{figure} https://example.com/path/to/image.png
:align: right
:width: 40%

Caption for the figure.
:::
```

#### Cross-references

Reference a figure:

```
See [](#my-map-figure) for the spatial distribution.
```

### Module 3: Interactive Documents

#### Adding Code Cells

In a Markdown file:

````
```{code-cell}
:label: simple-map
import geopandas as gpd
import matplotlib.pyplot as plt

# Load example data
world = gpd.read_file(gpd.datasets.get_path('naturalearth_lowres'))

# Plot
fig, ax = plt.subplots(figsize=(10, 6))
world.plot(ax=ax)
plt.title('World Map')
plt.axis('off')
````

#### Adding Labels to Code Cells

In notebooks:

```python
#| label: population-map
import geopandas as gpd
world = gpd.read_file(gpd.datasets.get_path('naturalearth_lowres'))
world.plot(column='pop_est', legend=True)
```

Then reference:

```
See the population distribution map in [](#population-map).
```

#### Executing Notebooks

Make sure to add this to frontmatter:

```yaml
kernelspec:
  name: python3
  display_name: Python 3
```

Then run:

```bash
myst start --execute
```

#### Interactive Elements

Create a dropdown:

```
:::{note} Solution to Exercise 1
:class: dropdown
Here we see that the spatial autocorrelation is positive with a Moran's I value of 0.68.
:::
```

### Module 4: Publishing and Distribution

#### Exporting to Various Formats

For Word documents:

```yaml
---
exports:
  - format: docx
---
```

For PDF:

```yaml
---
exports:
  - format: pdf
    template: volcanica
    article_type: Report
---
```

For LaTeX:

```yaml
---
exports:
  - format: tex
    template: volcanica
    article_type: Report
    output: arxiv.zip
---
```

Build command:

```bash
myst build your_document.md
```

#### Deploying to GitHub Pages

1. Run `myst init --gh-pages`
2. Modify workflow file:

```yaml
jobs:
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Setup Pages
        uses: actions/configure-pages@v3
      - uses: actions/setup-node@v4
        with:
          node-version: 18.x
      - name: Install MyST Markdown
        run: |
          npm install -g mystmd
          pip install -r requirements.txt
          pip install ipykernel
          python -m ipykernel install --user
      - name: Build HTML Assets
        run: myst build --html --execute
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: "./_build/html"
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

3. Create a new GitHub repository
4. Push your content
5. Enable GitHub Pages in repository settings

#### Managing Table of Contents

Update TOC:

```bash
myst init --write-toc
```

Customize TOC:

```yaml
toc:
  - file: README.md
  - file: 01-introduction.md
  - title: Geospatial Analysis
    children:
      - file: chapters/spatial-data.ipynb
      - file: chapters/visualization.ipynb
```

Enable section numbering:

```yaml
project:
  numbering:
    heading_1: true
    heading_2: true
```

## Demos

- [MyST Demo](https://github.com/giswqs/myst-demo)
- [Geemap Book](https://book.geemap.org)
- [Introduction to GIS Programming](https://geog-312.gishub.org)
- [Geographic Software Design](https://geog-510.gishub.org)

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
