======================
Data Collection
======================
Novaland enables the collection of diverse participant behavior data through an online process.
Just follow a few steps to gather the information.

Upload your project on Heroku
================================
The goal is to deliver the new version of Novaland on the existing server.
The Project is already available on the Heroku Server.

oTree Hub
==================================
There are several ways to upload the project to Heroku. The easiest way is to use "oTreeHub".
oTreehub is a project management tool aimed at simplifying and speeding up the development process of oTree-based studies.

If you don't have a Heroku account or your account is not connected to otreeHub.
Then this must be done before you can upload your project to Heroku using oTreehub.

Upload your project on oTreeHub:
________________________________

    1. Open your project in PyCharm.
    2. Go to the Terminal windows and write:

    .. code-block:: console

        otree zip

    3. PyCharm generates an oTree.zip file for you, located at the project's location.

    4. Open your browser and go to this page:

    .. code-block:: console

        www.otreehub.com

    5. Login or create an account on oTreehub.

    6. Click on "Heroku" in the menu.
    7. Select your project and press the 'Deploy' Button.
    8. Upload your oTree.zip file on the 'Upload code to Heroku' section.
    The Project is now Online in your Heroku account.

Data collection on Heroku
=========================
Open your App:
_______________________
To get an overview of the functions of Heroku, you can open the chapter 'Heroku'.

    1. Open your browser and go to:

    .. code-block:: console

        www.heroku.com

    2. Create an account or login to your account.
    3. The first site that you can see is a overview about your projects.
    4. Select your Novaland Project.



Create a new session
________________________
Different sessions can be created via the Session window.
These sessions are separated from each other.
Various settings can be made, such as the number of participants.
After making all settings.

Individual settings for the session:
________________________________
To be able to make individual settings, these must already be defined in the Settings.py file in PyCharm.

To start a session, you can go to the Session Settings section.
There, you can make settings that are either predefined by oTree or that you can determine yourself in the settings.py file under SESSION_CONFIGS. Under the 'dict' section, you can define individual variables.
In the example code provided, SESSION_CONFIGS is a list of dictionaries, with each dictionary containing key-value pairs representing settings for a particular session configuration.

.. code-block:: console

    SESSION_CONFIGS = [
        dict()
    ]

To define your own variables that can affect the study, you need to open the settings.py file and enter your values under SESSION_CONFIGS.
These values can then be changed when starting the app on Heroku under the Session Settings.

.. code-block:: console

    SESSION_CONFIGS = [
        dict(
            Page1Visible=False;
        )
    ]

For example, the provided variable 'Page1Visible' could be used to either show or hide certain pages using the 'is_displayed' function.
In this case, the 'is_displayed' function could look like:

.. code-block:: console
    class PageName(Page):
        @staticmethod
        def is_displayed(player: Player):
            if player.session.config['Page1Visble'] == True:
                return True
            else:
                return False

