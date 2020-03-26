[Home](README.md)

1.  **HTML Text**

    1.  There two kinds of tags that affect text

        1.  Structural: elements to describe both headings and paragraphs

        2.  Semantic: provides extra information such as where emphasis is,
            abbreviations, quotes

    2.  Headings

        1.  h1 for main headings, usually one per page

        2.  h2-h6 are sub-headings, decreasing in size

    3.  paragraphs p

    4.  b for bold, i for italic

    5.  sup for superscript, sub for subscript

    6.  line break: \<br /\> Horiz line \<hr /\>

    7.  strong for bold

    8.  em for italic

    9.  blockquote, q for shorter quote

    10. abbr for abbreviation

    11. ins underlines text to show something was inserted

    12. s to strike through deleted item

2.  **Introducing CSS**

    1.  CSS allows you to create rules for how elements should appear

    2.  Works by understanding there is an invisible box around every element

    3.  Selector {property:value;}

    4.  You can specify more than one element by separating them with commas

    5.  Multiple declarations are separated with semicolons

        1.  H1, h2, h3 {declaration; declaration}

    6.  Connecting CSS to HTML

        1.  Use style tags in html file

        2.  Can be used inline with an html element, \<p style=”color=black”\>

        3.  Best way: link to css file: \<link href="css/styles.css"
            type="text/css" rel="stylesheet" /\>

    7.  Cascade rules

        1.  Last rule trumps previous

        2.  The more specific selectors trump the less specific

3.  **Basic JavaScript Instructions**

    1.  Statement: an individual instruction/step

    2.  Comment: explain to the developer more information about the code

    3.  Variable: a way to temporary store a value for use by the program

        1.  Must be declared and have value assigned to them

        2.  Var name = value;

    4.  Data types

        1.  Numbers

        2.  Strings

        3.  Boolean: true or false

    5.  Array: special variable that stores more than one value

        1.  Creating array literal: var colors = [“blue” , “black”, “red”];

        2.  Each item is given and index number, 0 is blue, 2 is red

        3.  Colors[1] is black

        4.  Colors.length is 2

    6.  An expressions evaluates into a single value

    7.  Expressions rely on operators, such as +, %

    8.  Arithmetic operations

        1.  Addition +

        2.  Subtraction-

        3.  Division /

        4.  Multiplication \*

        5.  Increment ++

        6.  Decrement –

        7.  Modulus %

4.  **Decisions and loops**

    1.  Often a decision has to made to determine which line of code is used

    2.  Two parts to a decision

        1.  An expression is evaluated, returning a value

        2.  A conditional statements says what to do in given situation

    3.  If (condition) {conditional statement}

    4.  Comparison operators

        1.  Equal to ==

        2.  Not equal to !=

        3.  Strictly equal to === (compares values and data types)

        4.  Strictly not equal to !== (compares values and data types)

        5.  \> greater than, \< less than

        6.  \>= greater than or equal to, \<= less than or equal to

    5.  Logical operators: for comparing multiple comparisons

        1.  And && returns true if both are true

        2.  Or \|\| returns true if either one is true

        3.  Not !, !true is false
