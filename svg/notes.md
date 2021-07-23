- Creating an SVG image requires using the <svg> tag.
- The <svg> element is a container for all your graphics. 
- The browser will look at this and know that you want to create an inline SVG image.
- By default, the image will be empty. It is always good practice to set the dimensions of the image. 
- The <svg> element can be treated like a regular HTML element. 
- You can apply classes, IDs, and even bind JavaScript events. 
- It is one of the reasons why D3 recommends using SVG.

We are going to cover three shapes: rectangles, circles, and lines.

---------------------------------------------------------------------------------------------------------------------------------------

## Rectangles

- It is one of the most basic shapes in SVG.

- Rectangles are created using the <rect> element. We must add this element inside the <svg> element. The browser will not draw the shape unless it’s contained inside the <svg> element. This rule goes for the other shapes, too.


- <svg width="500" height="500">
    <rect 
        width="150" 
        height="150" 
        fill="#F44336" 
        stroke="#8BC34A" 
        stroke-width="10" 
        x="25" 
        y="25"
    >
    </rect>
</svg>

width - The width of the shape. Measurement in pixels.
height - The height of the shape. Measurement in pixels.
fill - Color of the shape. Supports any valid CSS color value. (Named, Hex RGB, RGBa, HSL, HSLa)
stroke - Color for the border of the shape, if any. Supports any valid CSS color value.
stroke-width - The width of the stroke. Measurement in pixels.
x - x coordinate
y - y coordinate

## Colors
- SVG shapes do not support the background-color and border CSS properties. If you want to apply a color, you’ll need to use the fill property.
- A stroke is the equivalent of a border in SVG. The width of the stroke can be set with the stroke-width property.
- SVG shapes can only be altered with a specific set of CSS properties.

## Coordinates
- With HTML and CSS, we have a variety of methods for moving elements. Such as margins, padding, grids, floats, etc. SVG takes a different approach to position shapes. It uses a coordinate system.

- There are two axes in SVG. The x-axis runs from left to right. The y-axis runs from top to bottom.

---------------------------------------------------------------------------------------------------------------------------------------

# Circles

- To create a circle, you need to use the <circle> element.

 - <svg width="500" height="500">
      <!-- Circle -->
      <circle
        r="100"
        cx="150"
        cy="150"
        fill="#9C27B0"
        stroke="#E91E63"
        stroke-width="10"
      ></circle>
    </svg>

- This element will create a perfect circle for you. We will introduce three new attributes. The only property required is r which is short for radius. The radius is used to calculate the width and height of the circle. In our example, we’re setting the radius to 100, which will give the circle a width and height of 200.

- Circles are moved from their center point. Unlike the <rect> element, configuring the coordinates for a circle can be set by adding the cx and cy properties.

---------------------------------------------------------------------------------------------------------------------------------------

# Lines

- To create a line, you use the <line> element. While lines are simple, the line element has quite a few properties we need to define. The first 4 are the coordinates.

- <svg width="500" height="500">
      <!-- Line -->
      <line
        x1="50"
        y1="50"
        x2="200"
        y2="200"
        stroke-width="10"
        stroke="blue"
      ></line>
  </svg>

- Basically, you need to set the start and end coordinates. The first set of properties you need to set are the x1 and y1 properties. These will be used as the starting point for the line.

- Then, you need to set the x2 and y2 properties. These are coordinates used to set the endpoint of the line. SVG will use these coordinates to draw the line.



- You will also need to provide stroke and stroke-width properties to have the line appear. There is no fill for lines. In the above example above, the line to a red color with a thickness of 10 pixels.

---------------------------------------------------------------------------------------------------------------------------------------

# Layering shapes

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>SVG Example</title>
  </head>
  <body>
    <svg width="500" height="500">
      <!-- Rectangle -->
      <rect
        width="150"
        height="150"
        fill="#F44336"
        stroke="#8BC34A"
        stroke-width="10"
        x="25"
        y="25"
      ></rect>

      <!-- Circle -->
      <circle
        r="100"
        cx="250"
        cy="150"
        fill="#9C27B0"
        stroke="#E91E63"
        stroke-width="10"
      ></circle>

      <!-- Line -->
      <line
        x1="50"
        y1="50"
        x2="200"
        y2="200"
        stroke-width="10"
        stroke="blue"
      ></line>
    </svg>
  </body>
</html>
