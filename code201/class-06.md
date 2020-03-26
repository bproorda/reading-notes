[Home](README.md)

# JS DOM
- as a browser loads a page, it creates a tree-like model called the Document Object Model.
- the first *node* is the document node, representing the entire body of code.
- each element has its own node, branching out from the document node, down to the elements children.
- the attribute of an element, are not children of the element, but part of. one can use methods to change those attribute.
- the *text node* of an element is the text within that element.
- working with the DOM tree
  1. Access the element(s)
     - using one of the getElementBy... method, can be stored as variable.
  2. work with those elements
     - with creating new elements, one will have to *append* the new node to its parent.
- Accessing elements
  - getElementById('id') often the fastest way
  - querySelector('css selector')
    - if more than one element, it picks the first one.
  - methods that select more than one elements
    - getElementsByClassName
    - getElementsByTagName
    - querySelectorAll
  - if more than one element is selected, it creates a *nodelist*
  - you can either select one from the list, or loop through all of them
  - individual items can be selected through item() method
    - ```
            var element = document.getElementsByClassName('hot');
            var firstItem = element.item(0);
- array syntax is faster
    - ```
            var firstItem = element[0];
- After you select a node, you can access a relative node
  - parentNode
  - previousSibling/nextSibling
  - firstChild/nextChild
- getting/changing node content
  - nodeValue: accesses text node value
  - innerHTML: gets/sets text and mark up
  - textContent/innerText: gets/sets text only
- Adding new element with DOM
  - var newEl = document.createElement('li');
  - var newText = document.createTextNode('quinoa');
  - newEl.appendChild(newText);
  - var position = document.getElementByTageName('ul')[0];
  - position.appendChild(newEl);
- Removing element with DOM
  - var removeEl =  document.getElementsByTagName('li ')[3]; 
  - var containerEl = removeEl .parentNode; 
  - containerEl.removeChild(removeEl); 
- Once you have a node, you an access its attribute nodes
  - getAttribute(): gets value of an attribute
  - hasAttribute(): checks to see if a the node has that attribute
  - setAttribute(): sets the value of the attribute
  - removeAttribute()


  # Object Literals
  - an object created with a list of key:value pairs, separated by commas
  - can include, strings, numbers, arrays, and functions.
  - ```
    var name = {
      key: value,
      name: quay,
      rooms: 40,
      booked: 25,
      checkAvailability: function() {
        return this.rooms - this.booked;
      }
    }
  - this signifies that it looking for the properties rooms, and booked in *this* object
  - to access properties
  - ``` 
      name.key;
      name.rooms;
      name.checkAvailability();
  

# Problem Domain
- the hardest of programming is understanding the problem domain, mostly what you the problem is and what you need to solve it.
- it is important to try to make it easier.
- two ways
  - Make the problem domain easier
  - Get better at understanding the problem domain
- Making the PD easier
  - break it down into simpler problems
- Improve Understanding
  - 


            