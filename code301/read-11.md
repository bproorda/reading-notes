# EJS

EJS (embedded javascript) allows the user to embed javascript into html, including variables, for loops, forEach. It is used with express and node.js to as a templating engine to render javascript to browser. EJS uses `<%= %>` to wrap js code inside html.
- use `app.set('view engine', 'ejs');` and `res.render()`
- requires the ejs extension, use the `npm install`
- EJS allows the code include if statements using: `<% if( exmapleVar === "JavaScript") { %>`
  - note that these tags do not use the `=`, 
  - the if code block can include ejs and plain html
- can also use for loops 
  `<% for(var i = 1; i <= 10; i++) { %>  <%= i %>  <%  } %>`
- EJS comments: `<%# this will output the numbers from 1 - 10 %>`
- code that is reused multiple times they are called *partials*
- single variables do require the =, `<%= tagline %>`


