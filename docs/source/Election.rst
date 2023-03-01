======================
Election
======================
Elections in Novaland play a significant role as they have an impact on the income of participating individuals.
Throughout Novaland, parties are introduced and each participating person can choose a party.
In this chapter, we will discuss all the elements that deal with the elections.

Introduce Parties
_______________________________
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
            float: left;        // Determines which side the column should be aligned to
            width: 70%;         // Percentage of the screen width
            padding: 10px;      // The amount of space to be left around the object
            height: 200px;      // The height of the column
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

Participants wählen eine Partei
____________________________________________
Wenn alle Parteien vorgestellt worden sind, können die Participants sich für eine Partei entscheiden, dafür erstellen wir eine Übersicht mit allen Parteien.
Dazu erschaffen wir Rows, welche die Parteien nebeneinander darstelen lassen kann.

.. code-block:: console

    {% block content %}
    <div class="row">   // Wir erstellen eine Row in welcher zwei Parteinen nebeneinander dargestellt werden können
        <div class="column3">
            <img src="{% static 'phase_3/KPN.png' %}" width="30%" class="center" onclick="SHOWKPN()">
            <p class="p" style="text-align: center"> <input type="radio" id="wahlen1" name="Partei" value="Konservative Partei Novaland"> Konservative Partei Novaland </p>
        </div>

        <div class="column3">
            <img src="{% static 'phase_3/LPN.png' %}" width="30%" class="center" onclick="SHOWLPN()">
           <p class="p" style="text-align: center"> <input type="radio" id="wahlen2" name="Partei" value="Liberale Partei Novaland">  Liberale Partei Novaland </p>
        </div>
    </div>
        <br>

    <div class="row">
        <div class="column3">
            <img src="{% static 'phase_3/SPN.png' %}" width="30%" class="center" onclick="SHOWSPN()">
            <p class="p" style="text-align: center"> <input type="radio" id="wahlen3" name="Partei" value="Soziale Partei Novaland">  Soziale Partei Novaland </p>
        </div>

        <div class="column3">
            <img src="{% static 'phase_3/PPN.png' %}" width="30%" class="center" onclick="SHOWPPN()">
            <p class="p" style="text-align: center"> <input type="radio" id="wahlen4" name="Partei" value="Partei Progressives Novaland">  Partei Progressives Novaland </p>
        </div>
    </div>
    {% endblock %}