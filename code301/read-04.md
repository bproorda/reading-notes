# CSS Grid

As you expand your toolbelt of CSS tools, one you absolutely have to have is CSS Grid. Unlike Flexbox, it is perfect for designing entire layouts. It is a perfect alternative to use floats, that can generate random behaviors. It allows you to grab of container element, define a grid inside it and then move the elements according to the grid lines. 

It starts with attaching `display: grid | inline-grid;` to the container element. Then you define the grid using `grid-template-columns` and `grid-template-rows`. The coder can also use `grid-template-area`, `grid-area`. This can use define an area as header, footer, etc.

Once you have the grid defined, Grid has a plethora of commands to arrange the elements inside the container. Many commands are the same or similar to flex-box commands, such as justify-content, align-self, 