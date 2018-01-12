======================
Javascript and jQuery
======================

In order to make the web page interactive we'll need to write some javascript. A lot of the code we write will be to update, read, and listen to events from the elements of our page. We do these things with a javascript library called jQuery.


===========================
Create the javascript file
===========================

Just like our css file, we'll create a js file and include it in our page. Call it *tutorial.js* and put it in the same folder as your html and css files.

To include the script in your page create a *script* tag and add it before the end of the body in your html page. The script tag will have a *src* attribute which tells it the location of the file:

.. code-block:: html
  <script src="/tutorial.js"></script>


===========================
jQuery
===========================

jQuery is similar to css in that it needs a selector to find the elements we want to look at, change, or listen to. This is how you select elements in jQuery:

.. code-block:: javascript
  $('selector goes here...')

So if we wanted to select all buttons on the page we'd do this:

.. code-block:: javascript
  $('button')

So how do we know if our selector worked? We can check how many elements jQuery found with the *length* property:

.. code-block:: javascript
  $('button').length

Now that we've selected our buttons let's do something with them. Let's start by geting the text inside of the buttons:


.. code-block:: javascript
  var text = $('button').text();

Now the text is stored inside of the *text* variable. Let's use it to set the button's text:

.. code-block:: javascript
  var text = $('button').text(text + text);

Great! Now let's trigger this code every time the button is clicked:

.. code-block:: javascript
  var text = $('button').text(text + text);

  $('button').on('click', function() {
    var text = $(this).text();
    $(this).text(text + text);
  });

In the above code we use the *on* function to handle an event on our selected elements. The first parameter the on function needs is the type of event, which is *click* in this case. THe second parameter needed is a function to run code when the event is triggered.

Also notice how we  *$(this).text()* inside function instead of *$('button').text()* like we did before. That's because inside event handlers *$(this)* gives you the element that triggered the event. *$('button')* selects all buttons on the page, but we really just want to select the button that triggered the event in this case.

Now the button's text will double every time you click on it.