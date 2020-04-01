# Flexbox #

    While many developers are enamored with CSS, plenty others, myself included, are driven near to insanity by it. For those of us in the latter group, we can be grateful that modules have been made to make our lives a little easier. A particularly handy one is Flexbox. Flexbox works to make it easier to align, lay out, space out items in a container. It even works when the items are dynamically generated and/or with unknown sizes. The idea behind flexbox is that it gives the parent container the ability to alter its childrens dimensions and order.

    To use Flexbox, the coder has to start by changing the CSS property display to flex for the parent container
     .container { display: flex;}
     After this is done, the coder can apply CSS flexbox to items inside the container in lots of interesting and handy ways. A good example is  .item {flex-direction: row-reverse}  This keeps items in a row, but reverses the order of the items. This property can be used to create rows, columns, and reverse both. Another property is flex-wrap, it sets whether or not the items take up a single line, multiple lines, or multiple lines from bottom to top. These two properites, flex-direction and flex-wrap, can be written shorthand with the flex-flow property. 

     Below are some more Flex box properties:
     - order: changes the order in which the items are displayed, default value is 0,
     - flex-grow: expands one(or more) of the children as space is available
     - flex-shrink: opposite of above
     - flex-basis: defines default size of item
     - flex: shorthand for the grow, shrink, and basis
     - justify-content: defines alignment of items along main axis, including spacing
     - align-items: defines alignment of items along cross axis
     - align-self: aligns individual item, overriding other values
     - align-content: defines alignment with cross axis when there is extra space, similar to justify-content
    
    While Flexbox is best for smaller applications or components of a large site, as you can see from the possible properties, it is very useful! A great tutorial to learn more is [Flexbox Froggy](https://flexboxfroggy.com/).