===================
Buttons
===================
Buttons can be equipped with different functions. These are being triggered when the button is pressed.

Standard oTree Button
------------------------
If you want to give the participants the possibility to call the next page, you can use oTree's own Django button.
This allows you to have all the built-in form fields filled out by the participants before they can call the next page.

.. code-block:: console
    :linenos:

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
    :linenos:

    <button Button Properties> Button Text </button>


The style of the button
--------------------------
The stylesheet is used for the visual representation.
This can be retrieved with the 'class' attribute.

.. code-block:: console
    :linenos:

    <button class='button'> Button Text </button>