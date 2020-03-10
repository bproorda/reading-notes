[Home](README.md)

# Canvas API
- Basic Usage
  - canvas element looks a like img element without src and alt attribute
  - only has width and height
  - can be styled like any image
  - can define fallback content if browser doesnt support content
  - use closing canvas state after fallback
  - canvas creates a fixed size drawing surface that exposes rendering context
  - canvas uses getContext method to obtain the rendering context and and its drawing functions
  - draw function

- # Drawing Shapes
  - css canvas uses coordinate grid
  - origin of the grid 0,0 is the top left corner of canvas
  - canvas only supports rectangles and paths
  - three functions for drawing rectangles
    - fillrect(x,y, width, height) draws filled outline
    - strokerect(x,y,width,height) draws rectangle outline
    - clearrect(x,y,width,height) makes specified area transparent
  - drawing paths, list of points connected by segments
    - beginpath, closePath, stroke, fill
  - moving the pen moveTo(x,y)
  - lineTo
  - arc(x, y, radius, startAngle, endAngle, anticlockwise)
  - arcTo(x1, y1, x2, y2, radius)
  - quadraticCurveTo(cp1x, cp1y, x, y)
  - bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)
  - rect(x, y, width, height)
  - 