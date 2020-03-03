[Home](README.md)

# Domain Modeling
-  the process of creating a conceptual model in code for a specific problem.
- An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an *object-oriented* model.


# HTMl Tables
- a table represents tables in a grid format.
- table structure
    - `<table>` element creates the table element
    - `<tr>` creates a table row
    - `<td>` the cell for table data
    - `<th>` creates the heading for a row or column
    - use colspan attribute to spread a td across more than column
    - rowspan 
    - `<thead>` the headings of a table
    - `<tbody>` where the body of table should be.
    - `<tfooter>` the footer

# Functions, Methods, and Objects
- Creating an object: constructor notation
- use the new keyword and object() constructor function
- after you create the object, you can use the dot notation to add properties
- ```
    var hotel = new Object();
    hotel.name = 'Quay';
    hotel.rooms = 40;
    hotel.booked = 25;
    hotel.checkAvailability = function() {
        return this.rooms - this.booked;
    };
    ```
- use the delete keyword to remove a property, `delete hotel.booked`
- If you need to create several similar objects, you can use constructors to create as a template
- first create the template as similar to above
- ``` 
    function Hotel(name, rooms, booked) {
        this.name = name;
        this.rooms = rooms;
        this.booked = booked;
        this.checkAvailability = function() {
        return this.rooms - this.booked;
    }
    ```
- you create *instances* of this object, use the new keyword
- the properties are used as arguments of the function
    ```
    var quayHotel = new Hotel('Quay', 40, 25);
    var parkHotel = new Hotel('Park, 120, 77);
    ```
- when a an function is defined within an object, it is a *method*
- in a method, *this* refers to the containing object
- with multiple objects created through constuctors, *this* refers to that particular instance
- if a named function is called as method for an object, *this* refers to the containing object
- Arrays are a special type of object, where the index is the key of the key:value pair
- you can combine arrays and objects to make complex data structures
- array of objects or object of arrays

- an **object model** is a group of objects representing things in the real world
- The windown object represents the current browser window/tab, topmost in Browser Object Model
- can return height and width of screen, coordinates of pointer, history, etc
- with the Document Object Model, the topmost object is the document representing loaded webpage
- there are also Math objects, string, objects, number objects, all with associated methods to work with them