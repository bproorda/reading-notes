[Home](README.md)

## HTML Lists
- Three kinds of lists in HTML
  - ordered list, every item is numbered. Best for recipes or steps
    -  created with `<ol>` tags
    - list items created with `<li>` tags
    - to specify type of numbering use css, `list-style-type`
  - unordered list, every item has bullet point
    - use `<ul>`
  - definition list, consist of a series of terms and their definition
    - `<dl>` to start the list
    - `<dt>` for the term
    - `<dd>` for the definition
  - lists can also be nested within one another

## CSS Boxes
- In CSS, every element is contained within its own box
  - Box Dimensions, you can specify the width and height of the box
  - you can also use `min-width` or `max-width` to limit the possible size
- Overflow property tells the program what to do if the contents are larger than the box
  - hidden: hides the overflowing content
  - scroll: adds a scroll bar to box
- Box properties
  - Border: separaters edges of one box from another, visible or otherwise
  - Margin: the gap between the borders of two boxes/elements
  - Padding: the space between the border of a box and the content within
- Border properties
  - `border-width` sets thickness of border, can be set to individual sides, top right bottom left
  - `border-style` sets the design of the border, such as solid, dotted, dashed
  - `border-color` does exactly what you think it does
  - you can also set all of these with shorthand: `border: width style color;
- Padding properties
  - you can specify how much padding the box has in pixels or percentages
  - as with borders, you can break down padding into top right bottom left
- Margin properties
  - specify just like you did with padding
  - if there are only two values then: `margin: right-left top-bottom;` (also works for padding)
- Centering content
  - this is for centering a box within its parent box (or page)
  - you must specify the width as less than 100 percent
  - set the right and left margin to auto
  - `margin: top auto bottom auto;` or `margin auto 0`
- Display property
  - allows you to change how an element is displayed, block or inline.
  - inline: treats block element as inline
  - block: treats inline elemnet as block
  - inline-block: displayed like an inline, but retains some block properties
  - none: hides the element from view
- Visibility, either hides or shows element 
- `border-image`
   - takes img, splits it into nine pieces to put around box
   - needs url of img, where to slice img, and what to do with straight edges
     - stretch: streches the img
     - repeat
     - round: like repeat but scales img to fit better
- Box Shadow
  - creates shadow around box
  - properties: horizontal and vertical offset, blur distance, shadow spread
- `border-radius` rounds the corner of the box

## Decisions and Loops
- if else statements allows you to provide two(or more) sets of code, on if the condition is true, one if it is not
- switch statement: provides a list of cases, the case that is true has its code block acted upon
- ``` 
     switch (level)
     case 'One':
     title = "Level 1";
     break; 
     ```
- javascript if given a data type it did not expect will try to convert it, instead of just giving an error, known a type coercion
- this is known as _weak typing_, why it is better to use strict equals or not equal to, ===, !==
- other languages have _strong typing_ requiring user to declare data type of a variable
- due to type coercion, true values can be treated as true or false
- Falsy: treated as false
- Truthy: treated as true
- Loops: check a condition, if it true the code block will run.
  - code will continue to run until condition is false or it hits a break
  - three major kinds, for, while, do while
  - a for loop uses a counter as condtion
  - ```
    for (var i = 0; i < 10; i++) {
        document.write(i);
    }
    ```
  - while loop works like a for loop, but number runs in not determined, usually depends on user input
  - ```
    while ( i <10) {
        document.write(i);
        i++;
    }
    ```
  - do while is the same as while loop, but always runs at least once
  - ```
    do {
        document.write(i);
    } while (i < 10);
  
