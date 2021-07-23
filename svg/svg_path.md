# Paths

- Paths are the most advanced and powerful shapes in SVG and are challenging to master because you’re dealing with commands

## Creating a path

- To create a path, you add the <path> element.

<path fill="none" stroke="#000" stroke-width="10"></path>

- The <path> element is regarded as the most powerful shape because it can be conformed to draw any shape. Paths can create shapes with straight or curved edges. They can also have an unlimited number of sides. It is powerful, but it is the most difficult shape to master.

- In the example above, we applied the fill, stroke, and stroke-width attributes. We are starting with these attributes first so that we can get them out of the way. They are not new to us.

- Paths are built using coordinates and lines. You input the coordinates, and SVG will take care of connecting them all. It goes by the order you input them. The only difference is the command you have to input for each coordinate. Here’s how you would create a shape using the <path> element.


- <path
        d="M 100, 100 L 300, 150"
        fill="none"
        stroke="#000"
        stroke-width="10">
    </path>

To begin inputting your coordinates, you have to create the d attribute, which is short for data. The value for the d attribute must be a list of commands and coordinates.

What exactly does that mean? Imagine we have a digital pen. This pen can be moved around to different coordinates. While it is moving around, we can tell the pen whether it should draw a line or not. Based on the coordinates and commands, SVG will draw the coordinates while connecting them.

There are about ten commands in total. The very first command you will always use is the M command. The M command is short for move.

The M command instructs SVG to move the pen to a specific coordinate. By default, our virtual pen always starts at the 0 0 coordinate, which is the top left corner of the <svg> element. If we want to draw a shape somewhere else, we can use the M command to move the pen to a different starting point. This command will not draw anything. It simply moves the pen tool for you.

Right after this command, we need to provide the coordinates. The format for a coordinate is the x coordinate, followed by a comma, and then the y coordinate. In this example, the coordinates are being set to 100, 100.

Once you have input the first coordinate, you can proceed to the next one.

The next command is quite simple. It is the L command. L is short for the line. This command will tell SVG to draw a line to a coordinate. Like the previous command, you provide it with the x and y coordinates.

As you can see, we are following a pattern. It is the command followed by the coordinate. We can separate each pair of commands and coordinates with spaces. We can add as many commands as we want.

If you look at the output, you will find a simple line drawn in the image.

It is important to note that these are just random coordinates with no intended outcome. It is perfectly fine if you want to input your own custom coordinates.

That is the basics of paths in SVG. We have explored only two commands so far. For the sake of simplicity, we will not explore the other commands. We do not have to because when we get to D3, it will take care of working with the <path> element. All you need to understand is that the <path> element is meant for creating complex shapes. It uses commands and coordinates to determine how the shape is drawn.