[Home](README.md)

# HTML Forms
- forms are html elements that allow you collect info from the user
- there different kind of form elements
  - text input
  - radio buttons / check boxes / drop-down boxes
  - submit/image/upload buttons
- How forms work
  - user fills in form and pushes a button
  - the name of the form and its value it sent to the server
  - the server processes the information
  - the server creates a new page to send back to browser
- forms start with `<form>` element
- every form requires an action attribute so it knows where to send the value
- two methods
  - get: values are added to the end of url specified in action
  - post: values are sent in what are know as HTTP headers
- input types
  - input text creates text box
  - input password, same as above, but blocks out inputted text
  - input textarea, for multiline text boxes
  - radio button
  - checkbox
  - dropdown
  - multiple
  - file input, type="input"
  - submit button, image button
- label element: labels the form
- for attribute: states which control the form belongs to.
- fieldset element: for grouping multiple form controls together
  - legend element: caption for the fieldset
  - form validation: gives messages if form has not been filled out correctly
- there is also date, url,  and email input

# Lists, Forms, Tables
- several CSS properties are made specifically to be used with lists, forms, and tables.
- list-style-type chooses the type of icon is in front of the an li element, or none
- list-style-image chooses an image to be placed in front of the li element
- list-style-position, places the bullet/number either on the outside of the li, default, or inside
- list-style, is shorthand and allows you to combine the above properties
- table properties: width, padding, text-transform(converts table headers to uppercase), letter-spacing, font-size, border, text-align, background, :hover(for table row)
- empty cells, chooses whether or not to show border on empty cells.
- border-spacing, gap between borders
- border-collapse, collapses borders to one border
- styling text inputs: font-size, color, background-color, border, border-radius, background-image, :focus, :hover
- styling buttons: color, background-color, border, text-shadow, :hover, border-radius
- styling fieldsets/legends: color, width, background-color, padding, border, border-radius
- cursor style: auto, crosshair, default, pointer, move, text, wait, help, url()

# Javascript Events
- coder can use js to repsond to events, such as cursor hovering or click
- event handling steps
  - select the element node you want the script to respond to
  - indicate which event on the selected node will trigger the response
  - state the code you want to run
- event handlers
  - in HTML, used as an attribute, `<a onclick="function()">`
    - Bad Code? do not use. evidently we should separate JS and HTML, church and state, etc
  - DOM event handler: element.on*event* = functionName;
    - ```
      var el = document.getElementById('userName');
      el.onclick = checkUserName();
    ```
  - DOM event listener: can deal with more than one function at a time, not always supported by older browsers
    - `element.addEventListener('event', functionName, [, Boolean]);`
    - ```
      var el = document.getElementById('userName');
      el.addEventListener('blur', checkUserName, false);
      ```
    - if needed there is a removeEventListener function
    - if function needs parameters, wrap it in an anonymous function
      ```
      el.addEventListener('blur', function() {
        checkUserName(5);
      }, false); <-- don't forget semicolon!
      ```
- event flow
  - if you hover/click on an html element, you also click on its parent element(s)
  - event bubbling: event starts at most specific node, and flows outward
  - event capturing: event starts at least specific node and works inward to most specific
  - flow only really matters when you have your code has event handlers on an element and one of its ancestors.
  - true = capturing phase
  - false = bubbling phase
- the event object: tells you about the event that happened and on what element.
  - creating many event listeners can slow down a page, event flow allows you to listen for event on parent element.
  - use event object's target property
  - allows you to add new elements without having to attach listeners to them
  - can simplify your code
  - event object has methods to change the default behavior of an element
    - preventDefault
    - stopPropagation: stops event bubbling
    - pg 268 - 269 for good example on event propagation
- use the event object's target property to determine on which element the event happened
