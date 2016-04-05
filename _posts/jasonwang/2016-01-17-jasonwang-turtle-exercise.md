---
layout: post
author: wagerpascal
title: "The Case of the Disappearing Turtles"
---

Custom input:
<iframe src="https://trinket.io/embed/python/c9a0e93b91" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

For ease of viewing, here's the code:

```
import turtle
mike = turtle.Turtle()

mike.forward(100)
mike.stamp()

mike_color = raw_input("What color should Mike be now?")
mike.color(mike_color)

mike.left(90)
mike.forward(100)

bg_color = raw_input("What color should we make the background?")
#print(dir(mike))

mike.getscreen().bgcolor(bg_color)

```

Thoughts:
It's nice to have the user have their own input into the program for a degree of control and customizibility. 
After all, different possibilities make the experience more interesting.

Since I was late, I never really got the whole turtle class explanation. So I had to use the dir() function in order to figure out how to use some of the functions, as well as figure out which are functions to start with.


Turtle Hacking:
<iframe src="https://trinket.io/embed/python/eb7273e016" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

For ease of viewing, here's the code:

```
import turtle

chair = turtle.Turtle()

chair_color = raw_input("What color should Chair be now?")
chair.color(chair_color)


side_number = int(raw_input("How many sides are in this polygon?"))
total_angle= 180*(side_number - 2)
#print(total_angle)
#print(total_angle/side_number)

side_number_1 = side_number

world_size = (side_number/2)*100
chair.getscreen().setworldcoordinates(-world_size,-world_size,world_size,world_size)

filledcol = raw_input("What color should the fill be?")
chair.fillcolor(filledcol)

while (side_number_1 > 0):
  chair.fill(True)
  chair.left(180-(total_angle/side_number))
  chair.forward(100)
  side_number_1 = side_number_1 - 1

chair.fill(False)
```

Thoughts:
The program asks for a number of sides that you wish the polygon to have. From this value, it determines the angles of which to form an equilateral polygon with the specified number of sides.

I ran into a number of issues/observations while working on this:
1. While raw_input calls a number, I could not use it as an integer (it was still stuck as a string) until I converted the data type.
2. I initially did not normalize the angle of which the arrow turned (I interpretated the direction in the wrong direction). This is why it's 180 degrees minus the value.
3. I wasn't sure if loops were explicitly allowed during this exercise, but it was the only way that I could reliably make a case for all possible polygons.
4. If the side number = 7 or more, the shape runs off the screen. Therefore, I had to change the size of the view to a value proportional to the polygon, which is the result of the formula in the line starting with "world_size".
By doing so, I could then redimension the viewpoint to something that always fits the shape no matter what the size.
5. Strangely enough, even if you set the cursor to a different shape in the beginning, it is forced back into an arrow. Still not sure why.
6. For filling the shape, the color of the cursor is overridden by the color of the fill. However, the cursor turns into a blend of both colors.

If given more time/opportunties, I'd like to figure out how to center the polygon, and maybe resize the worldview. Also, I'd like to look into the cursor behavior.

