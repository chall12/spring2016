---
layout: post
author: wookiemage
title: "Colin's Game"
---
### Here\'s the game:
<iframe src="https://trinket.io/embed/python/75f65f8d0c" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

### Here are my updated milestones:

- [x] Make a function that spawns turtles in random locations

- [x] Make a custom turtle class that has a default color and shape

- [x] Make a function that checks if two turtles are touching

- [x] Make a function that turns a turtle when it collides with a boundary or another turtle (didn't end up bouncing turtles off each other)

- [x] Make a function that governs turtle movement such that: turtle move as a function of time, and they bounce off walls

- [x] Make a function that sets up the play space with walls (visible to the player)

- [x] Make a function that allows user to reset and start over

- [x] Make a function that sets a score as a function of time and number of turtles

- [x] Make a function that displays a message when player turtle collides with other turtle (and it changes the sprite for that turtle too)

- [ ] Make a function that allows the user to move the turtle using keys - Ended up moving the turtle with the mouse

- [x] Make a function that explains goals and only runs once

- [x] Make a function that randomly changes the background color as a function of time (or a function of turn number anyway)

- [x] Make a function that generates turtles as a function of time (or a function of turn number anyway)

- [x] Make a function that changes the player turtles sprite when they collide with another turtle

- [x] Make a turtle counter

- [ ] Find and use 6 different enemy sprites. (I only ended up using one)

Stretch Goals: Turns out I didn't have time for these.
- [ ] Make a mode of this game that creates a turtle that has to be caught

- [ ] Make a function that generates turtles on click

Most of the changes I made to my milestones were design decisions, but a few were scope related. Turns out I don't have time for everything. For example, I determined that having six different sprites was a nice idea, but took more time than it was worth. If I were going to continue to flesh out this game, I would definitely find more sprites to use.

### Process
I started off by listing out my milestones. They were somewhat useful and most of them were accomplishable tasks, but some of them were much larger than the others. I ended up breaking everything down much further on whiteboards so that I could get a better idea of what each goal involved.  
Here are some photos of what that looked like:

![Whiteboards with code snippets and goals](http://i.imgur.com/VWzA5W3m.jpg) ![Whiteboards with code snippets and goals](http://i.imgur.com/uXuB3Srm.jpg) ![Whiteboards with code snippets and goals](http://i.imgur.com/AfQiXsXm.jpg)
![Whiteboards with code snippets and goals](http://i.imgur.com/T2lmA1gm.jpg) ![Whiteboards with code snippets and goals](http://i.imgur.com/IYmapzom.jpg) ![Whiteboards with code snippets and goals](http://i.imgur.com/NeJLpsvm.jpg)  

This was very very helpful. I was able to work on different sections and functions distinctly. I dedicated different sections of whiteboard to different goals which allowed me to keep things somewhere other than my head. I could easily work on a section until I got stuck and move to another. Being able to move back and forth between different sections turned out to be helpful for problem solving as well. I was able to move on whenever I needed.  

### Troubleshooting
This is by far the most complicated program I've written. It has a lot of functions that call other functions and some of the time they just didn't work the way they should. A few strategies really worked well for me here. Printing to the console variables was very helpful. Another strategy that I ended up using in the end was tracking down in which function the error occurred and rewriting the function in a completely different way.

#### An Example
This code block  
```
def collider(t1, t2, rad = 30):
  xOverlap = (t1.xcor()-rad, t1.xcor() + rad)
  yOverlap = (t1.ycor()-rad, t1.ycor() + rad)
  enemyX, enemyY = t2.pos()
  check_x = enemyX > min(xOverlap) and enemyX < max(xOverlap)
  check_y = enemyY > min(yOverlap) and enemyY < max(xOverlap)
  if (check_x and check_y):
    return True
  else:
    return False
```
Became this code block  
```
def collider(t1, t2, rad = 30):
  if (t1.distance(t2) < rad):
    return True
  else:
    return False
```
I knew there was some trouble with the logic but I just couldn't trace through all the possibilities. So instead I wrote it again using a different method to compare those values. Thank goodness .distance existed.

### Another Problem
I discovered another problem as I was getting ready to submit the game. The character could fly off the screen. Obviously I didn't want to allow this. I made a function to check if the player was inside the playing field. Then I called this function every turn and if the player was not inside the playing field, the player couldn't move. This, of course, was only a partial solution. This resulted in the character getting stuck at the edges of the playing field. I then needed to add a way for the player to move if and only if they are stuck on the edge. To solve this, I called the function that checks the player condition with the "not" operator because I only wanted this to work if the player was stuck. Then, if it wasn't true, the click function would move the player in the direction clicked. This still doens't quite solve the problem, because the player might not move the character back onto the playing field, but it's much better than before.
