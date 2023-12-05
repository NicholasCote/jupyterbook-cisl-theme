Banner Pages
=======================

.. banner::
   :color: rgba(40,40,60,0.8)
   :image: images/mesa-lab.jpg
   :caption: Photo by Carlye Calvin
   :class: dark-banner

Built with |jbook|

This is an example of a banner page. You can modify the examples in this file to 
fit your own content and requirements.

.. raw:: html

   <span class="d-flex justify-content-center py-4">
     <a href="index.html" role="button" class="btn btn-light btn-lg">
       Read more about the Documentation
     </a>
   </span>

Information
------------------------

Banner pages are a great way to break out of a pure documentation site and provide a more 
streamlined look. The sidebar table of contents navigation is removed in the `_config.yml`
file with the following::

   sphinx:
     config:
       html_sidebars:
         banner: []

Resources Used
------------------------

This content is built on top of JupyterBook. The theme is provided by Project Pythia. Additional styling
to match existing NSF NCAR | CISL pages was accomplished by utilizing a lot of the documentation provided 
by both of Jupyter and Project Pythia. A custom HTML footer and navbar have been added along with work to 
the CSS in order to change fonts, backgrounds, and colors. 

Links to Documentation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. raw:: html

   <span class="d-flex justify-content-center py-4">
     <a href="https://jupyterbook.org/en/stable/intro.html">
     <figure>
       <img src="_static/jbook.png">
       <figcaption style="text-align:center">JupyterBook</figcaption>
      </figure>
     </a>
     <a href="https://sphinx-pythia-theme.readthedocs.io/en/latest/">
     <figure>
       <img src="_static/pythia.png">
       <figcaption style="text-align:center">Project Pythia Sphinx Theme Documentation</figcaption>
      </figure>
     </a>
   </span>

This Documentation
--------------------

.. rst-class:: text-center

   Click the button below to read more about this customized JupyterBook.

.. raw:: html

   <span class="d-flex justify-content-center py-4">
     <a href="examples/main.html" role="button" class="btn btn-primary btn-lg">
       Read the documentation
     </a>
   </span>

.. |jbook| image:: images/jupyterbook.svg
   :target: https://jupyterbook.org
