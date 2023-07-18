# Template for Jupyter Book with CISL like theme

['Example Site']('https://nicholascote.github.io/jupyterbook-cisl-theme/')

This is not a custom Sphinx theme. This is a customization of the Project Pythia Sphinx theme and credit goes to the Project Pythia team for putting together a really great looking Sphinx theme that allows for further customization. 

## Jupyter Book basics

### _config.yml

This sets the configuration for the site. The title, author, email, etc. are all defined here as well as the Sphinx customization. The Sphinx customization is where all the navbar links are defined for the site as well as allowing for additional text in the left side table of contents menu. 

### _toc.yml

The table of contents file defines what should be displayed in the left hand table of contents menu and where the text displayed redirects you. The _toc.yml file also defines the format to use (jb-book by default) and the root (homepage) of the documentation site. 

### _static/

The _static directory contains any additional static files or images that should be included in the jupyter book build. This template only uses custom CSS and some custom images but JavaScript can also be supplied to run any custom JS code. 

### _templates/

The _templates directory contains and custom HTML that is going to be used in our site build. The templates used are limited by what the theme is configured to take for input. Since this site is built on the Project Pythia theme it is limited to overriding templates that were used in the Project Pythia build. Documentation on what other templates can be provided can be found on the Pythia Theme documentation [here](https://sphinx-pythia-theme.readthedocs.io/en/latest/about.html#custom-templates).

## Building and Hosting the site

### Install Jupyter Book

Jupyter Book is ultimately a Python package and can be installed via pip or conda/mamba. The Jupyter Book documentation has installation instructions that can be followed [here](https://jupyterbook.org/en/stable/start/overview.html)

### Install the Project Pythia theme

The Project Pythia Sphinx theme is also a Python Package that can be installed via pip. It is included in the cisl-theme/requirements.txt file but also can be installed via 'pip install sphinx-pythia-theme'

### Build the HTML

Once all the content is laid out HTML files can be generated to run and host the content. In the command line, at the root of the documentation (/cisl-theme/), run 'jupyter-book build .'. This will create a _build/ directory that contains all the HTML and other files required for the site. 

### Hosting on GitHub Pages
If GitHub pages is going to be used to host the content the only files required are going to be in /cisl-theme/_build/html. All the files in the html directory should be copied to the root directory of the gh-pages branch of the repository. Once all the files have been copied over a new file called '.nojekyll' needs to be added. This file is empty and only provides the name. This is for GitHub pages to bypass applying any jekyll processing. The site provided has everything it needs to serve content. 

### Other hosting options
More information on publishing books online can be found on the Jupyter Book documentation site [here](https://jupyterbook.org/en/stable/start/publish.html).

## Changes made specifically for CISL

The changes made to tailor this theme for CISL were mostly made to HTML and CSS files. 

### HTML changes

In the _templates folder there are 3 custom HTML files that are being leveraged to change the layout of the navbar and footer specifically. The existing HTML files on the GitHub page for the [Project Pythia Theme](https://github.com/ProjectPythia/sphinx-pythia-theme/tree/main/sphinx_pythia_theme) were utilized and changed to meet the layout of CISL sites. 

The most changes went in to the navbar-menu.html file. Specifically syntax to allow dropdown menus in the navbar were added. This was accomplished by adding a dropdown boolean to the navbar_links section of the _config.yaml file. When the dropdown value is set to *true* the navbar HTML will then go through a for loop to show all the links and names below the dropdown_links tab. 

### CSS changes

A custom css file is used and can be found in _static/style.css. The purpose of this file is to apply styling to fonts, backgrounds, and other HTML objects in order to mimic the look and feel of current CISL sites. 

