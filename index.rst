
.. toctree::
   :maxdepth: 2
   :caption: Contents:

   index



Max Script Online (MSO)
=======================


What is Max Script Online (MSO)
********************************
Max Max Script Online (MSO) is a modern easy to use tool for HTML. It is a
JavaScript Library that can makes coding with more then one HTML page easy.
You can code you Navigation only once for more then one HTML page.


Step 1: Code the Template
**************************

Coding your template is just like coding a regular HTML page. I will put
the following code into *template.html*

.. code-block:: html
    :linenos:

    <!DOCTYPE html>
    <html lang="en">
        <body>
            <!-- This is a navigation. We will create these pages later -->
            <a href="index.html">Home</a> / <a href="index.html">About</a>
            <br>
            <h1 style="color: darkgreen"><{Title}></h1>
            <{Body}>
        </body>

    </html>

This looks like an html page, but what about **<{Body}>** and **<{Title}>**
tag objects? This is a placeholder for where code will go later on. You
can call them whatever you want as long as it starts with **<{** and ends
with **}>**.


Step 2: Make the page
**************************

Now we have to apply the template. The basic skeleton for these pages looks
like the following. I will put the code in *index.html*

.. code-block:: html
    :linenos:

    <!DOCTYPE html>
    <script src="https://centillionware.com/js/mso.js"></script>
    <body onload="MsoSetup('', [])">

    </body>

Okay. What did we do? On line 2 we imported Max Script Online (MSO).
On the next line we have the body element and when the it loads it
executes **MsoSetup**. The first parameter in **MsoSetup** is 