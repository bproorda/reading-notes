1.  **Structure**

    -   html is broken up into sections using *elements*, consisting of tags in
        angled brackets

        1.  requires an opening and closing tag

        2.  \<h1\> content \</h1\>

    -   The first/last are the html tags, they tell the browser that everything
        between these tags are html code.

    -   Next, are the body tags, everything between these tags will be displayed
        on the webpage.

    -   use of headings and subheadings to create a hierarchy of information

        1.  headings are made using h1, h2, h3 tags, h1 is biggest

    -   paragraphs are between p tags

    -   attributes provide additional information about the contents of the
        element

        1.  \<p lang=”en-us”\>

        2.  lang is the attribute name, en-us is the attribute value

    -   Often before the body you will see the head element

        1.  Content here, will not display on the webpage, but is metadata for
            the page.

        2.  Includes the title of the page, which shows in the tab

2.  **Extra Markup**

    -   Programming must specify which version of HTML, current HTML5

        1.  Opens file with \<!DOCTYPE html\> for HTML5

    -   Comments: \<!--comment --\>

    -   All elements can include an id tag specifically identify that particular
        element

        1.  **\<**p id=’id’\>

    -   You can also use a class identifier, for multiple elements to be treated
        as the same

        1.  \<p class=’class’\>

    -   Block elements: some elements always start on a new line

        1.  H1, p, ul, li

    -   Inline elements: elements that continue on the same line

        1.  A, b, em, img

    -   Use div element to contain several elements to together into one block
        element

    -   Span is the inline equivalent of div

    -   Iframe: creates a window in the webpage to another, often used for maps.

        1.  **\<**iframe width, height, src=”url”\>\</iframe\>

    -   Escape characters: several characters are reserved to be used as html
        code, to be seen as content on the webpage, one must use escape
        characters.

3.  **HTML5 Layout**

    -   Html5 includes several new elements to help define and organize the
        page.

    -   Allows programmer to use less div tags, and new tags specific for those
        elements.

    -   Header: section at the top of the page, usually containing the site name
        and navigation links.

    -   Footer: section at bottom page, usually contains copyright information
        and related information

    -   Nav: links for navigation to the other pages of the website

    -   Article: contains elements that can stand alone as one independent
        section

    -   Aside: can be related but not required information, or other links, or
        info

        1.  Normally presented to the side of the other content

    -   Section: related elements tied together, normally with their own heading

    -   Figure/figcaption: creates captions for elements such as images and
        charts

    -   HTML5 allows web page authors to place an \<a\> element around a block
        level element that contains child elements. This allows you to turn an
        entire block into a link.

4.  **JS: ABC’s of programming**

    -   *What is a script and how to write one?*

        1.  A script is a series of instructions a computer can follow to
            achieve a goal.

        2.  First, define the goal

        3.  Split the goal into individual tasks, then the steps to achieve the
            tasks

        4.  Code the steps, put together as the script

        5.  Process can be helped by creating a flow chart, lays out how the
            script travels from one step/task to another.

    -   *How do computers fit in the world around them*

        1.  Every physical thing can be described as an *object*

        2.  The characteristics of the object/physical item are the properties

        3.  Event: the computers way of saying something happened, often used to
            trigger functions or other programs

        4.  A *method* interacts with object, either retrieving or updating a
            value of a property

        5.  All of these tie together to create model of the object

        6.  The current webpage is modeled as the document object, representing
            the html page

        7.  One can use methods, properties, and events, to access and change
            content of document

    -   *How do browsers see a webpage?*

        1.  Interprets page as one object, the document object, broken down into
            other objects, result looks like a family tree.

        2.  The first *node* on the tree is the document object, what affects
            this node, affects all nodes beneath it.

        3.  If there is a link to a CSS style sheet, the browser then receives
            those rules and applies them to the webpage.

        4.  If there is javascript, the browser interpreter converts the js
            instructions into something the browser can use to follow the steps
            described.

    -   How Do I write script for a webpage

        1.  First you must under how the three layers work together

            1.  Html: the content layer

            2.  CSS: the presentation layer

            3.  Javascript: the behavior layer

        2.  The three layers work together to create the *progressive
            enhancement* approach to web development.

        3.  Link JS to HTML using \<script src=’url’\>

            1.  You can also use script tags to write JS in the HTML file, not
                recommended

        4.  JS runs where it is found on the HTML page, often good to have it at
            the bottom of the page, so it is the last thing that runs
