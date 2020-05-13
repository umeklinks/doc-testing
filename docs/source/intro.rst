.. _settingup:

Setting up Sphinx
=================

This section will teach you how to set up Sphinx to start your documentation.

	* Download and install Python if not installed, for your PC https://www.python.org/downloads/


Linux Debian/Ubuntu
-------------------

Install either python3-sphinx using **apt-get**:

$ apt-get install python3-sphinx

If it not already present, this will install Python for you.

RHEL, CentOS
------------

Install python-sphinx using yum:

$ yum install python-sphinx code

If it not already present, this will install Python for you.

Other distributions
-------------------

Most Linux distributions have Sphinx in their package repositories. Usually the package is called python3-sphinx, python-sphinx or sphinx. Be aware that there are at least two other packages with sphinx in their name: a speech recognition toolkit (CMU Sphinx) and a full-text search database (Sphinx search).

macOS
-----

Sphinx can be installed using Homebrew, MacPorts, or as part of a Python distribution such as Anaconda.

Homebrew
--------

$ brew install sphinx-doc code

For more information, refer to the package overview.

MacPorts
--------

Install either python3x-sphinx using **port**:

$ sudo port install py38-sphinx code

To set up the executable paths, use the port select command:

$ sudo port select --set python python38 code
$ sudo port select --set sphinx py38-sphinx code

For more information, refer to the package overview.

Anaconda
--------

$ conda install sphinx code


Installation from PyPI
----------------------

Sphinx packages are published on the Python Package Index. The preferred tool for installing packages from PyPI is **pip**. This tool is provided with all modern versions of Python.

On Linux or MacOS, you should open your terminal and run the following command.

$ pip install -U sphinx

On Windows, you should open Command Prompt (⊞Win-r and type **cmd**) and run the same command.

C:\> pip install -U sphinx

After installation, type **sphinx-build --version** on the command prompt. If everything worked fine, you will see the version number for the Sphinx package you just installed.

Installation from PyPI also allows you to install the latest development release. You will not generally need (or want) to do this, but it can be useful if you see a possible bug in the latest stable release. To do this, use the --pre flag.

$ pip install -U --pre sphinx


Docker
------

Docker images for Sphinx are published on the Docker Hub. There are two kind of images:

	- sphinxdoc/sphinx

	- sphinxdoc/sphinx-latexpdf

Former one is used for standard usage of Sphinx, and latter one is mainly used for PDF builds using LaTeX. Please choose one for your purpose.

**Note**

sphinxdoc/sphinx-latexpdf contains TeXLive packages. So the image is very large (over 2GB!).

**Hint**

When using docker images, please use docker run command to invoke sphinx commands. For example, you can use following command to create a Sphinx project:

$ docker run -it --rm -v /path/to/document:/docs sphinxdoc/sphinx sphinx-quickstart

And you can following command this to build HTML document:

$ docker run --rm -v /path/to/document:/docs sphinxdoc/sphinx make html

For more details, please read README file of docker images.

Installation from source
------------------------

You can install Sphinx directly from a clone of the Git repository. This can be done either by cloning the repo and installing from the local clone, on simply installing directly via **git.**

$ git clone https://github.com/sphinx-doc/sphinx
$ cd sphinx
$ pip install .

$ pip install git+https://github.com/sphinx-doc/sphinx

You can also download a snapshot of the Git repo in either tar.gz or zip format. Once downloaded and extracted, these can be installed with **pip** as above.

.. figure:: /images/back_image.png
   :alt: Just an image
   :scale: 200 %

   *Just a random image*