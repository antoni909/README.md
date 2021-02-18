# Reading-12

## If you wish to exit to the homepage click on the following link to head back to the [homepage](../README.md)

## Basic Usage of Canvas - How to set up a canvas 2d context

1. \<canvas> element syntax
  1. canvas only suppotys two shapes: rectangles and paths
  1. \<canvas id="content" width="123" heigth="123>\</canvas>
1. has only 2 optional attributes whose default is 300 by 150 px, try to define explicitly in canvas if distorted in css
1. getContext() used to obtain rendering context and its drawing functions. Has one parameter, type of context
      From MDN example on rendering:
        var canvas = document.getElementById('tutorial');
        var ctx = canvas.getContext('2d');

## Basic Usage of Canvas - Drawing Shapes with canvas

1. The Grid/coordinate space
  1. all elements are placed relative to the origin at (0,0) top left corner
      FROM MDN 3 functions that draw rectangles:
        fillRect(x, y, width, height)
          Draws a filled rectangle.
        strokeRect(x, y, width, height)
          Draws a rectangular outline.
        clearRect(x, y, width, height)
          Clears the specified rectangular area, making it fully transparent.

1. Drawing Paths
  1. paths are lists of points connected by segments
  1. steps to creating a path:
    create a path
    use drawing commands
    stroke/fill path to render
    FROM MDN functions used:
      beginPath()
          Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.
          Path methods
          Methods to set different paths for objects.
      closePath()
          Adds a straight line to the path, going to the start of the current sub-path.
      stroke()
          Draws the shape by stroking its outline.
      fill()
          Draws a solid shape by filling the path's content area.
1. Move to - is like lifting the pen and moves path to other coordinate specified
1. Straight Lines - use the lineTo(x,y) method
1. Arcs - or circles, use arc() or arcTo() method
      From MDN
      arc(x, y, radius, startAngle, endAngle, anticlockwise)
          Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by anticlockwise (defaulting to clockwise).
      arcTo(x1, y1, x2, y2, radius)
          Draws an arc with the given control points and radius, connected to the previous point by a straight line.

1. Applying Styles and Colors
  1. use the fillStyle and strokeStyle properties
  1. Transparency using globalAlpha
  1. lineCap - determines how the endpoints of lines are drawn
  1. lineJoin - determines how two connecting segments join
  1. Gradients - fill stroke shapes using gradients

1. Patterns using the createPattern(image, 'type') method
    creates and returns a new canvas pattern object

1. Shadows - involves 4 properties
      FROM MDN
        shadowOffsetX = float
          Indicates the horizontal distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.
        shadowOffsetY = float
          Indicates the vertical distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.
        shadowBlur = float
          Indicates the size of the blurring effect; this value doesn't correspond to a number of pixels and is not affected by the current transformation matrix. The default value is 0.
        shadowColor = color
          A standard CSS color value indicating the color of the shadow effect; by default, it is fully-transparent black.

## Drawing Text

1. Canvas provides 2 rendering methods

    FROM MDN
    fillText(text, x, y [, maxWidth])
        Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
    strokeText(text, x, y [, maxWidth])
        Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.