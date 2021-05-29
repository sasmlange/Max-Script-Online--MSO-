
.. toctree::
   :maxdepth: 2
   :caption: Contents:

   index



Max Script Online (MSO)
=======================


What is Max Script Online (MSO)
********************************
Max Script Online (MSO) is a modern easy to use tool for HTML. It is a
JavaScript Library that can make coding with more than one HTML page easy.
You only need to code your navigation once for more than one HTML page.


Step 1: Code the Template
**************************

Coding your template is just like coding a regular HTML page. I will put
the following code into *template.html*

.. code-block:: html

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

    <!DOCTYPE html>
    <script src="https://centillionware.com/js/mso.js"></script>
    <body onload="MsoSetup('', [])">

    </body>

Okay. What did we do? On line 2 we imported Max Script Online (MSO).
On the next line we have the body element and when it loads it
executes **MsoSetup**. The first parameter in **MsoSetup** is for the
path to your template. I will put **template.html**. Most modern browsers
do not support reading from a file that is not on the same server. The
next parameter is for all the placeholders. To add them to the parameters
they are added in the JavaScript list.

.. code-block:: html

    <!DOCTYPE html>
    <script src="https://centillionware.com/js/mso.js"></script>
    <body onload="MsoSetup('template.html', ['Title', 'Body'])">

    </body>

All right! We added the parameters! Now we have to specify what goes into the
placeholders. You can do this by using any html tag. To mark what placeholder
it is, the id of the tag must be one of the placeholders. I will use **div**.

.. code-block:: html

    <!DOCTYPE html>
    <script src="https://centillionware.com/js/mso.js"></script>
    <body onload="MsoSetup('template.html', ['Title', 'Body'])">
        <div id="Title">Home Page</div>
        <div id="Body">
            This is the best body that has <b>bold</b> text.
        </div>
    </body>

Okay! We have set the placeholders.


Step 3: Testing the page
**************************

To test the page, you cannot just double click on it in your files. For
safety reasons you can only run this on http:// or https://.


