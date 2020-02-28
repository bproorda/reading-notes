[Home](README.md)

# HTML Images
- Good practice to create an image folder and store images there
- add images using the img tag, it is self closing
  - `<img src="images/dogpic.jpg" alt="picture of a dog" title="picture of a dog">`
  - source is where the image is from, either url or file path to folder
  - alt gives a description of picture if the picture doesn't load, or for screen readers
  - title gives more info, often appears as a tooltip when hovering
  - you can set the height and with of img in the tag
  `<img src="images/dogpic.jpg" width="400" height="400">`
  - where to place image, where you put effects how it is displayed
    - before a paragraph: paragraph starts on new line after image
    - inside start of paragraph: first row of text aligns with bottom of image
    - in the middle of paragraph: image is displayed between the words where it is listed.
  - save images in the right format
  - save images as the same size as you set it in the webpage
  - use correct resolution
  - vector images: are resolution independent
  - transparency: what it sounds like.
  - images often need captions
  - ``` 
        <figure> <img>
        <figcaption>Caption</figcaption>
        </figure>
        ```

# CSS Colors
- setting color of text, foreground
  - `color: value`
  - value can be in rgba, hsl, hex codes, names
- background-color
- color on screen is a combination of red green and blue
- opacity

# CSS Text
- Typeface Terminology
- serif: extra details on the ends on main strokes
- san-serif: straight ends to letters
- monospaced, fixed width, every letter has same width
- weight: light, bold, bolder, black
- style: normal, italic, oblique
- stretch
- specifying typefaces
  - font-family: fonts
  - size of font, font-size
- `@font-face`
    - allows developer to store font on page, so all users can see it
    - need to include font-family: name, and src: file path
- use font-weight to make bold text
- use font-style to make italic or oblique text
- text-transform, for all lower case, all upper case, or capitalize
- text-decoration, underline, or strike
- line-height, sizes the leading, the gap between lines of text
- letter-spacing, word-spacing
- text-align
- text-indent, indents first line of text
- text-shadow, creates a shadow for the text
- you can specify :first-letter or : first-line
- styling links, (anchor tags)
  - :link sets styles links that have not been visited
  - :visited sets styles links that have been visited
  - :hover sets styles for when mouse hovers over link
  - :active sets style for link is actived by user, such as being clicked
  - :focus