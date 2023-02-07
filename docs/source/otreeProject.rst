======================
oTree Project
======================

Apps
====================

__init__.py
__________________________________


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

 Create an Settings Field.
settings.py file:

SESSION_FIELDS = ['PARTEI', 'SPENDE', 'BRANDBETROFFENE']


LANGUAGE_CODE
____________________

This is a string value that sets the language used in your experiment.

.. code-block:: console

    LANGUAGE_CODE = 'de'

ADMIN_USERNAME = 'admin'

ADMIN_PASSWORD = environ.get('OTREE_ADMIN_PASSWORD')

SECRET_KEY = '6079585529411'

DEBUG = False

use_browser_bots = False

Add Pictures
========================


Waiting Pages
===========================
