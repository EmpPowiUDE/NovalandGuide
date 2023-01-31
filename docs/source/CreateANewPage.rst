======================
Create a new page
======================


Creating a HTML file
=====================
To work on a new page in Novaland you have to create first a new page in an existing app.
To do this click the right mouse button on the app or one of the phases we have already defined, click on "New" and then on "HTML File".

.. code-block:: console
    [click the right mouse button on the app / phase] -> [New] -> [HTML File]

Structure of the page
====================
A page in oTree consists of many different programming languages and functions of oTree, which converge and can be used there.
The basic scheme of the already existing pages in Novaland looks like this in the front-end:

Django
=====================
The basic programming language, which is necessary to work with all other languages, is Django.
It is based on the programming language 'Python' and is a web framework that is used to create dynamic pages, web applications or web services.
For Novaland we basically need the functions to create a "block" in which we can work with the other languages.
A Django code always follows this structure {% code %}.
Therefore we need a block start and a block end and they are written like this:

.. code-block:: console
    {% block title %}
    ...
    {% endblock %}

The visual representation of the page
=====================
Visual representation of the page:
In order for the newly created page to adapt to the style of the already existing pages, you must link the already prescribed 'stylesheet'. This is based on a CSS written code, which is integrated in the project under the "_static" folder.
Therefore, in the first step you need to access the Statics folder via Django.

.. code-block:: console
    {% load staticfiles %}


In the second step, you link the stylesheet to your project using HTML.

.. code-block:: console
    <link href="{% static 'NovalandStyle.css' %}" rel="stylesheet">


Here is a template to apply to their HTML site:

.. code-block:: console
    {% block style %}
    {% load staticfiles %}
    <link href="{% static 'NovalandStyle.css' %}" rel="stylesheet">
    {% endblock %}

Add text
=====================
If you want to write a text on your page, it must be in a block, as already described above in the chapter 'Django'.
A page always consists of a title and the content.

Title
----------------------
To convert the text you wrote to a title, you need to write it between the 'h1' element and retrieve the 'h1' class from the stylesheet.

Example:

.. code-block:: console
    <h1 class="h1"> Title Text </h1>

Content
----------------------
The content text is written in a different block than the title.
This is written between a 'p' element, i.e. a paragraph or text paragraph element.

.. code-block:: console
    :linenos:

    <p class="p"> Content Text </p>

Basic HTML elements for working with text
-----------------------------------------

+----------------------------+--------------------------------+
| Element                    |      Description               |
+============================+================================+
| <br>                       |      Line break                |
+----------------------------+--------------------------------+
|   <strong> ... </strong>   |      Text displayed in bold    |
+----------------------------+--------------------------------+
| <i> ... </i>               |      Text displayed in italic  |
+----------------------------+--------------------------------+

Add functions
====================
With the help of JavaScript, various functions can be integrated on the page.
The JavaScript code is written between a 'script' element.

.. code-block:: console
    <script> javascript code </script>


Buttons
===================
Buttons can be equipped with different functions. These are being triggered when the button is pressed.

Standard oTree Button
------------------------
If you want to give the participants the possibility to call the next page, you can use oTree's own Django button.
This allows you to have all the built-in form fields filled out by the participants before they can call the next page.

.. code-block:: console
    {% next button %}

Costumized Button
=====================
The creation of costumized buttons is needed to give the button more than just the "Next" function.
All necessary functions, which have already been used in Novaland, are listed in this chapter.

HTML Button Overview
=====================
A costumized button in HTML code consists of several elements.

The ground structure
------------------------
For the visual representation of the button and for the integration of the functions, the button is written inside the 'Button' tag, which enables certain functions.

.. code-block:: console
    <button Button Properties> Button Text </button>


The style of the button
--------------------------
The stylesheet is used for the visual representation.
This can be retrieved with the 'class' attribute.

.. code-block:: console
    <button class='button'> Button Text </button>