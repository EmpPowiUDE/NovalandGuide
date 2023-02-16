======================
oTree Project
======================

An oTree project consists of several components, including:

    **The settings.py file**

    This file contains various configuration settings for the oTree project, including the PARTICIPANT_FIELDS and SESSION_CONFIGS.

    **Applications**

    Applications are the individual components of an oTree project that define the different parts of the experiment. Each application has its own set of models, views, and templates.

    **Models**

    Models are Python classes that define the data structure for the application and store the data in a database.

    **Views**

    Views define the logic for how data is displayed and processed in the application.

    **Templates**

    Templates define the HTML files used to render the pages of the application.

    **Static files**

    These are any additional files required for the application, such as images, JavaScript files, and CSS stylesheets.

    **Participants**

    Participants are the individuals who participate in the experiment. The information about each participant is stored in the database, and can be accessed and used throughout the project.

    **Sessions**

    A session is a single instance of an oTree experiment. Participants are grouped into sessions, and each session has its own set of parameters, such as the number of participants and the timing of events.

Apps
====================
An oTree app is a component of an oTree project, and represents a single task or game that participants can complete in the experiment.
An oTree app typically consists of a series of pages, each of which presents a task or question for the participant to answer, as well as models and views that define the behavior and logic of the app.
The app may also include custom templates and CSS styles to control the appearance of the pages and elements, as well as custom JavaScript code to handle user interactions and events.
The structure and behavior of an oTree app is defined using the Python programming language, and the platform provides a set of tools and libraries to make it easy to create and manage the components of the app.


__init__.py
==============================

BaseConstants

Subsession

Group

Player
    models
        FloatField
        StringField
            widgets - Radioselect



Settingy.py file
==============================
The settings.py file in an oTree project contains various configuration settings and parameters for your oTree experiment or application. These settings control various aspects of your experiment such as the number of rounds, the number of participants per group, the name of the application, the language to be used, and other settings related to the behavior and appearance of your experiment.
You can modify the settings.py file to customize your experiment to meet your specific needs.

SESSION_CONFIGS:
____________________________
In the context of an oTree project, SESSION_CONFIGS is a list of dictionaries in the settings.py file that define the different sessions or conditions in your experiment. Each dictionary in the list represents a different session configuration, and contains the various settings and parameters for that particular session, such as the number of rounds, the number of participants per group, and the name of the session.
The SESSION_CONFIGS list allows you to specify multiple different sessions with different configurations, and participants can be randomly assigned to one of these sessions during the experiment.
By using different session configurations, you can run experiments with different treatments, parameters, and conditions.

This is a list of dictionaries that define different sessions or conditions in your experiment. Each dictionary in the list represents a different session configuration, and contains the various settings and parameters for that particular session.
Here's an example of how you might use this function:

.. code-block:: console

    SESSION_CONFIGS = [
    // It is possible to name several apps.
    // App 1:
    {
        name='project_Name_1',                       // The name of the project
        display_name_1='Project_Display_name_1',     // The Name that is displayed when you start the app
        num_demo_participants=3,                     // Number of the participants
        app_sequence=['app_1', 'app_2],              // All apps that will be represented in this project.
    },
    // App 2:
    {
        name='project_name_2',
        display_name='Project_Display_name_2',
        num_demo_participants=5,
        app_sequence=['app_3', 'app_4],
    },]

**'name'**

 This is a string that gives the session a unique identifier.

.. code-block:: console

    name='ProjectName'


**'display_name'**

 This is a string that gives the session a human-readable name.

.. code-block:: console

    display_name='Novaland'

**'num_demo_participants'**

 This is an integer that sets the number of demo participants for the session.


.. code-block:: console

    num_demo_participants=3;


**'app_sequence'**

 This is a list of strings that determines the order in which apps will be run in the session.

.. code-block:: console

    app_sequence:['App_Name_1', 'App_Name_2', ...]



PARTICIPANT_FIELDS
_______________________
Is a list of fields that you can use to store information about each participant in your experiment.
Each field is defined as a tuple, with the first element being the field name, and the second element being the field type.

The information stored in these fields can then be used in the oTree app to personalize the experience for each participant, or to gather data for analysis.
Its storing information about one participant that can be used across the entire project, not just within individual apps.

Example:
We create a variable in Settings.py that can be used for a participant for the whole project.
This data is stored there and therefore can be replayed in other apps.


Create participant value

    Settings.py:

    .. code-block:: console

        PARTICIPANT_FIELDS = ['ValueName1', 'ValueName2', ...]


Save value in the participant variable:

    __init__.py file in app:

    .. code-block:: console

        player.participant.ValueName1 = Value_1
        player.participant.ValueName2 = Value_2

Use saved values:

    __init__.py file in app:

    .. code-block:: console

        New_Value_1 = player.participant.ValueName1
        New_Value_2 = player.participant.ValueName2



SESSION_FIELDS
__________________
Is a list of fields that you can use to store information about each session in your experiment.
Each field is defined as a tuple, with the first element being the field name, and the second element being the field type.

The information stored in these fields can then be used in the oTree app to determine which treatments or conditions a participant will experience in a particular session, or to gather data for analysis.
This allows you to centralize important information that will be referenced and utilized throughout the experiment, providing a unified and consistent source of data for all components of the project.

This field was used in Novaland mainly to get information from all participants and store them all in one variable.


Example:

Create an Settings Field:

**settings.py file:**

.. code-block:: console

    SESSION_FIELDS = ['Variable_1', 'Variable_2', ...]

Save a value in a session field:

**__init__.py**

.. code-block:: console

    player.session.Variable_1 = Value_1
    player.session.Variable_2 = Value_2

Use a saved session value:

**__init__.py**

.. code-block:: console

    New_Value_1 = player.session.ValueName1
    New_Value_2 = player.session.ValueName2


LANGUAGE_CODE
____________________

This is a string value that sets the language used in your experiment.

.. code-block:: console

    LANGUAGE_CODE = 'de'

ADMIN_USERNAME
____________________
The ADMIN_USERNAME in the settings.py file in an oTree project refers to the username used by the administrator of the platform.
This username is used to log in to the oTree administration interface, which provides access to various tools and features for managing the platform, such as monitoring participant progress, viewing data, and controlling the flow of the experiment.
The ADMIN_USERNAME setting allows you to specify the username that will be used by the platform administrator.


Example:

.. code-block:: console

    ADMIN_USERNAME = 'admin'


ADMIN_PASSWORD = environ.get('OTREE_ADMIN_PASSWORD')

SECRET_KEY = '6079585529411'

DEBUG
_____________________________
Debug is a Boolean value that controls whether oTree should run in debug mode or not.
In debug mode, detailed error messages are displayed and the performance is slower.


Example:

.. code-block:: console

    DEBUG = False


Static
=========================
A directory that contains any static assets such as images, fonts, or other files that are needed by the app.

Template
===========================
A directory that contains the HTML templates for the pages in the app, as well as any custom CSS and JavaScript files used by the templates.