======================
Installation
======================

Development Environment
=======================
Feel free to use any preferred development environment.
The following guide is primarily crafted for use with the 'PyCharm' development platform.

Download PyCharm
------------------------
The advantage of PyCharm is that it has been developed especially for Python.

Download Pycharm:

.. code-block:: console

    `Download Pycharm <SO>`_.

.. _SO: https://www.jetbrains.com/de-de/pycharm/download

oTree
========================
Novaland is a project build on the 'oTree' plattform.
oTree is a platform for conducting behavioral research and experiments.

Install oTree
-----------------------
To install oTree in PyCharm, follow these steps:

    1. Open the 'Terminal' window in PyCharm

    2. Type:

    .. code-block:: console

        pip install otree

    in the terminal and press enter

    3. The installation process of oTree in PyCharm will now begin


GitHub
========================
The project is uploaded to Github. The first step is to Sign in or to create an account on GitHub.
Download GitHub for your Computer.

.. code-block:: console

    https://desktop.github.com/


When you are logged in you need to download this repository.

.. code-block:: console

   https://github.com/Nordwindfeld/Novaland.git

Save this folder to your computer and then open it in PyCharm.

Install Django
-----------------------

    1. Open PyCharm

    2. Click on 'file' in the menu

    3. Choose 'Settings'

    4. Go to 'Languages & Frameworks'

    5. Choose Django

    6. Press the 'Enable Django Support' button or check if the button is already enabled

    7. Under 'Django project root' select the project on your computer


oTree.zip
=========

Once everything is installed, if you are collaborating with others and want to share projects with each other, you can use otree.zip files.
otree.zip files are compressed files that contain all the files and folders necessary to transport or share an oTree project more easily.
They allow you to package your entire project into a single file that can be easily transferred to another computer or shared with others.

Create a oTree.zip
_________________

    1. Open the oTree project.
    2. Enter the following command in the terminal:

.. code-block:: console

    otree zip

    3. The system will then save the project in the project folder.

open a oTree.zip
_______________________

To open an otree.zip file, follow these steps:

    1. Save the otree.zip file in the folder where you want the project to be located.
    2. Open the oTree project.
    3. Use the cd command to navigate to the appropriate folder:

.. code-block:: console

    cd C:\Documents\Novaland

    4. Enter the command otree unzip followed by the name of the otree.zip file in the terminal:

.. code-block:: console

    otree unzip ProjectName.otreezip

    5. Open the new folder in PyCharm.
