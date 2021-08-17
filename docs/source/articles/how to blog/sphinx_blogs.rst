.. _blog1:

Creating readmedocs documentation
=================================
MkDocs is a documentation generator that focuses on speed and simplicity.
It has many great features including:

* Preview your documentation as you write it
* Easy customization with themes and extensions
* Writing documentation with Markdown


Why create documentation ?
--------------------------

Creating a readmedocs is very simple and all developer should prepare documentation for their project so it's easy for other developer to understand it's usage and implement it.
It saves a lot of time and repetitive work reading the code and trying to understand how to use it.

readmedocs provide a very nice simplistic format to document all the neccessary details. Almost all python documentation are written in this format.

It uses `Sphinx <https://www.sphinx-doc.org/en/master/>`_ , Sphinx is a powerful document generator that can generate documentation in html, pdf and epub format from  reStructuredText or Markdown format.

Using `readthedocs theme <https://github.com/readthedocs/sphinx_rtd_theme>`_ you can easily generate the documentation in this format.


Installation Guide 
------------------

install Sphinx :

.. prompt:: bash $

    pip3 install sphinx

To start a project, create a docs directory root of project. This will be helpful in hosting documentation on `readthedocs <http://readthedocs.org/>`_ 

.. prompt:: bash $

    mkdir docs
    cd docs

To generate the required files for starting documentation

.. prompt:: bash $

    sphinx-quickstart

It will generate a ``conf.py`` which is used to store the configuration, theme and extensions for sphinx and ``index.rst`` which is base reStructuredText file with some text for getting started. For more detail on syntax of RST and how to write it you can read `here <https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html#rst-primer>`_.

Now from the given file, default html and pdf can be generated using

.. prompt:: bash $

    make html
    make latexpdf




There are bunch of sphinx extension available that makes creating documentation even more easy. Some of the most useful extensions are

* `sphinx-autobuild <https://github.com/executablebooks/sphinx-autobuild>`_ : This extension helps to preview realtime changes and auto reload the generated html files in browser. 
* `sphinx-copybutton <https://sphinx-copybutton.readthedocs.io/en/latest/>`_ : It adds copy button to code snippets making it easy for reader to follow along. 
* `sphinx-hoverxref <https://sphinx-hoverxref.readthedocs.io/en/latest/>`_ : Adds tooltips on cross references of the documentation with the content of the linked section.
* `myst_parser <https://myst-parser.readthedocs.io/en/latest/>`_ : You can use Markdown using MyST and reStructuredText in the same Sphinx project.


There are also bunch of different `themes <https://sphinx-themes.org/>`_ available to chose from.

Hosting documentations 
----------------------

`readthedocs <http://readthedocs.org/>`_ provides free hosting for documentation and it is very easy to use.

just follow these steps :


 - push your project on github.
 - signup on `readthedocs <http://readthedocs.org/>`_ using github id.
 - select the repo.
 - press build.
  
That's it. And your documentation will be hosted in minutes. It will also get automatically updated with each push on github.

