# Project-2
#Artistic Turtle Drawing

import turtle

drawing_bg = turtle.Turtle()

drawing_bg.hideturtle()
drawing_bg.speed(20)

for i in range(450):
  drawing_bg.forward(i)
  drawing_bg.right(80)
  drawing_bg.color("red")
  
def draw_circle(t, radius, color):
    t.fillcolor(color)
    t.begin_fill()
    t.circle(radius)
    t.end_fill()
  
def draw_skull():
    screen = turtle.Screen()
    screen.bgcolor("blue")

    skull_turtle = turtle.Turtle()
    skull_turtle.speed(0)

# head circle
    draw_circle(skull_turtle, 100, "white")
  
 # Left eye ball
    skull_turtle.penup()
    skull_turtle.goto(-50,50)
    skull_turtle.pendown()
    draw_circle(skull_turtle,30,"black")

# left eye socket
    skull_turtle.penup()
    skull_turtle.goto(-40, 60)
    skull_turtle.pendown()
    draw_circle(skull_turtle, 15, "white")

# right eye ball
    skull_turtle.penup()
    skull_turtle.goto(50, 50)
    skull_turtle.pendown()
    draw_circle(skull_turtle, 30, "black")
  
  # right eye socket
    skull_turtle.penup()
    skull_turtle.goto(40, 60)
    skull_turtle.pendown()
    draw_circle(skull_turtle, 15, "white")

# nose hole 1
    skull_turtle.penup()
    skull_turtle.goto(10, 15)
    skull_turtle.pendown()
    draw_circle(skull_turtle, 5, "black")

  #nose hole 2

    skull_turtle.penup()
    skull_turtle.goto(-10, 15)
    skull_turtle.pendown()
    draw_circle(skull_turtle, 5, "black")

#jaw
    skull_turtle.penup()
    skull_turtle.goto(-40,9)
    skull_turtle.pendown()
    skull_turtle.fillcolor("white")
    skull_turtle.begin_fill()

    skull_turtle.penup()
    skull_turtle.forward(80)
    skull_turtle.pendown() 
    skull_turtle.left(90)
    skull_turtle.forward(-50)
    skull_turtle.left(90)

    skull_turtle.forward(80)
    skull_turtle.left(90)
    skull_turtle.forward(-50)
    skull_turtle.left(90)
    skull_turtle.end_fill()

    skull_turtle.penup()
    skull_turtle.goto(-30, -20)
    skull_turtle.pendown()
    skull_turtle.fillcolor("black")
    skull_turtle.begin_fill()

  #mouth
    for _ in range(2):
        skull_turtle.forward(55) 
        skull_turtle.left(90)
        skull_turtle.forward(10)  
        skull_turtle.left(90)
    skull_turtle.end_fill()
    
                    
    skull_turtle.hideturtle()


draw_skull()
turtle.done()
