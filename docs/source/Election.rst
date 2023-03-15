======================
Election
======================
Elections in Novaland play a significant role as they have an impact on the income of participating individuals.
Throughout Novaland, parties are introduced and each participating person can choose a party.
In this chapter, we will discuss all the elements that deal with the elections.

Introduce Parties
==========================
To introduce the parties, it is sufficient to show a text with the corresponding image on the page to the participating individuals.
Columns are used to ensure that the text is displayed next to the image.
These columns can be modified in terms of style using CSS code on the page or in the stylesheet.
The following CSS code can be used to style the columns:

.. code-block:: console

    {% block style %}
    {% load staticfiles %}
    <link href="{% static 'NovalandStyle.css' %}" rel="stylesheet" type="text/css" />
        <style>
        .column1{
            float: left;        # Determines which side the column should be aligned to
            width: 70%;         # Percentage of the screen width
            padding: 10px;      # The amount of space to be left around the object
            height: 200px;      # The height of the column
    }
        }
       .column2{
            float: right;
            width: 30%;
            padding: 10px;
            height: 200px;
        }
        </style>
    {% endblock %}

With this CSS code, the text can be placed in one column and the image in the other column.

.. code-block:: console

    <h2> Social Party Novaland </h2>
    <hr>
    <br>
    <div class="row">
        <div class="column1">
            <p class="p"> The SPN (Social Party Novaland) wants <strong>more social benefits, even if that means higher taxes and levies.</strong>
                <br>
    The incomes of people with <strong>high incomes should decrease by about 5%, while the incomes of people with <strong>low incomes should increase by about 10%</strong>.</strong>.

                <br>
                The SPN wants to <strong>restrict the opportunities for foreigners to immigrate to Novaland.</strong></p>
                <br><br>
            <button class='button' type='button' onclick='Next()'> Next </button>
        </div>
        <div class="column2">
            <img src="{% static 'phase_3/SPN.png' %}" width="80%">
        </div>
    </div>

    This code displays the Social Party Novaland (SPN) and their policies.
    The text provides an overview of the party's political stance and their plans for the country.
    The image shows the party's logo or a representative image of the party.
    By using columns and CSS code, the page layout is structured, and the text and images are presented in a visually appealing way.

Basic code for selecting a political party.
===========================================
To select a political party as a participant, once all the parties have been introduced, we provide an overview of all the parties using Rows, which display the parties in a 2 x 2 grid. If you require more or fewer parties, this can be customized accordingly.
To create a user-friendly interface, we add a radio button to each image. When you click on the image, the corresponding radio button is selected.
The following code creates an HTML page with four images of party logos and radio buttons for selecting a party. The images are arranged in two rows with two columns each, with each column containing a logo and an associated radio button.

Election HTML Code:

.. code-block:: console

    {% block content %}
    # First Row
    <div class="row">
        <div class="column3">       # First Party
            <img src="{% static 'Party1PNG' %}" width="30%" class="center" onclick="Party1()">      # Party Image 'Party1PNG' from the static folder + 'onclick' function 'Party1()'
            <p class="p" style="text-align: center"> <input type="radio" id="election1" name="Party" value="Party 1"> Party 1 </p>      # Radio button with the id'election1', the name 'Party and the value 'Party 1'
        </div>

        <div class="column3">
            <img src="{% static 'Party2PNG.png' %}" width="30%" class="center" onclick="Party2()">
           <p class="p" style="text-align: center"> <input type="radio" id="election2" name="Party" value="Party 2">  Party 2 </p>
        </div>
    </div>
        <br>
    # Second Row
    <div class="row">
        <div class="column3">
            <img src="{% static 'Party3PNG.png' %}" width="30%" class="center" onclick="Party3()">
            <p class="p" style="text-align: center"> <input type="radio" id="wahlen3" name="Party" value="Party 3">  Party 3 </p>
        </div>

        <div class="column3">
            <img src="{% static 'Party4PNG.png' %}" width="30%" class="center" onclick="Party4()">
            <p class="p" style="text-align: center"> <input type="radio" id="wahlen4" name="Party" value="Party 4">  Party 4 </p>
        </div>
    </div>
    {% endblock %}

    {% block script %}
    <script>    # Javascript are to define the functions
        function Party1(){
            document.getElementById("Election1").checked = true
        }
        function Party2(){
            document.getElementById("Election2").checked = true
        }
        function Party3(){
            document.getElementById("Election3").checked = true
        }
        function Party4(){
            document.getElementById("Election4").checked = true
        }

    </script>
    {% endblock %}


Code Explanation
________________________
We will now discuss individual elements from the code to ensure better understanding.
If you have understood everything in the above code, you can skip this subsection.

Radio Buttons
___________________________
To allow participants to choose between the parties, we create radio buttons that can be clicked by the participants.
These buttons contain the names of the parties to choose from

.. code-block:: console

    <p class="p" style="text-align: center"> <input type="radio" id="election1" name="Party" value="Party 1"> Party Name 1 </p>
    <p class="p" style="text-align: center"> <input type="radio" id="election2" name="Party" value="Party 2"> Party Name 2 </p>

The input field is set to type 'radio' so that it gets the design and functionality of a radio button.
To link the radio buttons together so that only one option can be selected, the 'name' attribute must be the same.
Additionally, the 'name' attribute links the selection to the backend form field, which must have the same name.
The 'value' is the content that will be transferred to the 'Party' form field.

Clickable pictures
______________________
To link the selection function to the images, we give the images an 'onclick' attribute to trigger a JavaScript function.

.. code-block:: console

    <img src="{% static 'Party1PNG' %}" width="30%" class="center" onclick="Party1()">

This JavaScript function, triggered by the onclick function, triggers the corresponding radio button.

.. code-block:: console

    If the radio button looks like this:
        <p class="p" style="text-align: center"> <input type="radio" id="election1" name="Party" value="Party 1"> Party Name 1 </p>

    Then this is the desired function for it:
        function Party1(){
                document.getElementById("election1").checked = true
            }


Save the election value in the backend
=========================================
To save the selection of participants, we simply use a form field with the term 'Party' in the backend, in the init.py file.

init.py:

.. code-block:: console

    class PageName(Page):
        form_model = 'player'
        form_fields = ['Party']

In the HTML Election code, we selected a value named 'Party' to trigger exactly this variable in the backend and store the information there.
It is important that the name of the input field is exactly the same as the name in the 'form_field'.
