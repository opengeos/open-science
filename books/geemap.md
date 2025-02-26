# Earth Engine and Geemap

## Book Website

The official website for this book is [https://book.geemap.org](https://book.geemap.org).

[![book](https://images.geemap.org/book.png)](https://book.geemap.org)

## Introduction

[Google Earth Engine](https://earthengine.google.com) (GEE) is a cloud computing platform with a [multi-petabyte catalog](https://developers.google.com/earth-engine/datasets) of satellite imagery and geospatial datasets. During the past few years, GEE has become very popular in the geospatial community and it has empowered numerous environmental applications at local, regional, and global scales. GEE provides both JavaScript and Python APIs for making computational requests to the Earth Engine servers. Compared with the comprehensive [documentation](https://developers.google.com/earth-engine) and interactive IDE (i.e., [GEE JavaScript Code Editor](https://code.earthengine.google.com)) of the GEE JavaScript API, the GEE Python API has relatively little documentation and limited functionality for visualizing results interactively. The **geemap** Python package was created to fill this gap. It is built upon a number of open-source Python libraries, such as the [earthengine-api](https://pypi.org/project/earthengine-api), [folium](https://python-visualization.github.io/folium/), [ipyleaflet](https://github.com/jupyter-widgets/ipyleaflet), and [ipywidgets](https://github.com/jupyter-widgets/ipywidgets). Geemap enables users to analyze and visualize Earth Engine datasets interactively within a Jupyter environment with minimal coding.

This book takes a hands-on approach to help you get started with the GEE Python API and geemap. You'll start with the fundamentals of geemap by creating and customizing interactive maps. You'll then learn how to load cloud-based Earth Engine datasets and local geospatial datasets onto the interactive maps. As you advance through the chapters, you'll walk through practical examples of using geemap to visualize and analyze Earth Engine datasets, and will learn about exporting data from Earth Engine. You will also learn about more advanced topics such as building and deploying interactive web apps with Earth Engine and geemap.

## Who this book is for

This book is for students, researchers, and data scientists who want to utilize the Python ecosystem of diverse libraries and tools to explore Google Earth Engine. Whether you are a new user looking to harness the power of Earth Engine or an experienced user already familiar with the Earth Engine JavaScript API, this book is for you!

## What this book covers

**Chapter 1** _Introducing GEE and geemap_: provides an introduction to using the GEE Python API and setting up a Python environment for using geemap.

**Chapter 2** _Creating Interactive Maps_: teaches readers how to create and customize interactive maps using various plotting backends.

**Chapter 3** _Using Earth Engine Data_: covers the basic data types of Earth Engine and teaches how to search for and load Earth Engine datasets onto an interactive map.

**Chapter 4** _Using Local Geospatial Data_: teaches how to load local vector and raster datasets onto an interactive map and how to download data from OpenStreetMap.

**Chapter 5** _Visualizing Geospatial Data_: covers various tools and techniques for visualizing geospatial data, such as split-panel maps, linked maps, and timeseries inspector. This chapter also covers creating map elements such as color bars, legends, and labels.

**Chapter 6** _Analyzing Geospatial Data_: covers statistical methods and machine learning techniques for analyzing geospatial data, such as zonal statistics, unsupervised classification, supervised classification, and accuracy assessment.

**Chapter 7** _Exporting Earth Engine Data_: teaches how to export vector and raster data from Earth Engine and how to download thousands of image chips from Earth Engine within a few minutes.

**Chapter 8** _Making Maps with Cartoee_: teaches how to create publication-quality maps using the cartoee module. This chapter covers plotting Earth Engine data on the map and customizing map projections.

**Chapter 9** _Creating Timelapse Animations_: provides practical examples of using geemap to create timelapse animations from satellite and aerial imagery, such as Landsat, GOES, MODIS, and NAIP.

**Chapter 10** _Building Interactive Web Apps_: teaches how to build interactive web apps with Earth Engine and geemap from scratch. This chapter also covers deploying web apps to the cloud for public access.

**Chapter 11** _Earth Engine Applications_: covers various Earth Engine applications, such as surface water mapping, forest cover change analysis, flood mapping, and global land cover mapping.

## To get the most out of this book

This book assumes that you are at least a Python novice, which means that you are comfortable with the basic Python syntax, such as variables, lists, dictionaries, loops, and functions. If you know how to make lists and define variables and have written a `for` loop before, you have enough Python knowledge to get started! To get the most out of this book, we highly encourage you to type the code yourself in a Jupyter environment (e.g., Jupyter notebook, JupyterLab, Google Colab). This will help you understand the code and help you understand the book. You can also download the code examples from the book's GitHub repository at <https://github.com/giswqs/geebook>. Doing so will help you avoid any potential errors related to the copying and pasting of code.

## Download Jupyter notebook examples

You can download the Jupyter notebook examples for this book from the book's GitHub repository at <https://github.com/giswqs/geebook>. If there's an update to the code, it will be updated in this GitHub repository.

## Conventions used

There are a number of text conventions used throughout this book.

`Code in text`: Indicates code words in text, folder names, filenames, file extensions, pathnames, URLs, etc. Here is an example: Set `EARTHENGINE_TOKEN` as a system environment variable to your Earth Engine API key.

A block of Python code is set as follows:

```{code-cell}
import geemap
# Create an interactive map
m = geemap.Map(center=[40, -100], zoom=4)
m
```

**Bold**: Indicates a new term, an important word, or words that you see onscreen. For
instance, words in menus or dialog boxes appear in bold. Here is an example: Click on **Advanced settings** to set `EARTHENGINE_TOKEN` as an environment variable.

## Get in touch

Feedback from our readers is always welcome.

**Questions:** If you have any questions about the materials covered in the book, please visit <https://github.com/giswqs/geebook/discussions> to ask questions and share ideas.

**Errata:** Although we have tried our best to ensure the accuracy of the book content, mistakes do happen. If you find any mistake in the book, we would be grateful if you report it to us. Please visit <https://github.com/giswqs/geebook/issues> and submit an issue.
