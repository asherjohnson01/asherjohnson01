
#import the turtle module and give it a shorter name
import turtle as trtl
import random #allow the computer to pick random numbers
trtl.speed(100000)

#sky
trtl.penup()
trtl.goto(-510,430)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("lightblue")
for step in range(4):
   trtl.forward(1012)
   trtl.right(90)
trtl.end_fill()

#ground line
trtl.penup()
trtl.setheading(0)
trtl.goto(-510, -50)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("green")
for step in range(4):
   trtl.forward(1020)
   trtl.right(90)
trtl.end_fill()

#mountain 1
trtl.penup()
trtl.goto(-300, -50)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("dimgray")
trtl.setheading(45)
trtl.forward(350)
trtl.right(90)
trtl.forward(350)
trtl.right(135)
trtl.forward(550)
trtl.end_fill()

#mountain 1 snow cap
trtl.penup()
trtl.goto(-125, 127)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("white")
trtl.setheading(45)
trtl.forward(100)
trtl.right(90)
trtl.forward(100)
trtl.right(135)
trtl.forward(140)
trtl.end_fill()
trtl.setheading(0)

#mountain 2
trtl.penup()
trtl.goto(-500, -50)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("darkgray")
trtl.setheading(45)
trtl.forward(400)
trtl.right(90)
trtl.forward(400)
trtl.right(135)
trtl.forward(600)
trtl.end_fill()

#mountain 2 snow cap
trtl.penup()
trtl.goto(-288, 162)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("white")
trtl.setheading(45)
trtl.forward(100)
trtl.right(90)
trtl.forward(100)
trtl.right(135)
trtl.forward(140)
trtl.end_fill()
trtl.setheading(0)

#mountain 3
trtl.penup()
trtl.goto(-200, -50)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("gray")
trtl.setheading(45)
trtl.forward(500)
trtl.right(90)
trtl.forward(500)
trtl.right(135)
trtl.forward(700)
trtl.end_fill()

#mountain 3 snow cap
trtl.penup()
trtl.goto(83, 233)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("white")
trtl.setheading(45)
trtl.forward(100)
trtl.right(90)
trtl.forward(100)
trtl.right(135)
trtl.forward(140)
trtl.end_fill()
trtl.setheading(0)

#make the sun
trtl.penup()
trtl.goto(-430,300)
trtl.pendown()
trtl.fillcolor("yellow")
trtl.begin_fill()
trtl.circle(50)
trtl.end_fill()

#make the lines of the sun
num_rays = 12
ray_length = 30
radius = 50

#trtl.penup()
trtl.penup()
trtl.goto(-430,350)
trtl.pendown()

for i in range(num_rays):
   trtl.setheading(i * (360/num_rays)) # calculate angle 
   trtl.penup()
   trtl.forward(radius)
   trtl.pendown()
   trtl.forward(ray_length)
   trtl.penup()
   trtl.backward(radius + ray_length)

trtl.setheading(0)
trtl.pensize(1) 

           
#center the house in the middle of the screen
trtl.penup()
trtl.goto(-50, -50)
trtl.pendown()

#make the walls of the house
trtl.begin_fill()
trtl.fillcolor("sienna")
for step in range(4):
  trtl.forward(100)
  trtl.left(90)
trtl.end_fill()
trtl.penup()

#retrace the roof to add color
trtl.penup()
trtl.goto(-50,50)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("sienna")
trtl.left(45)
trtl.forward(70)
trtl.right(90)
trtl.forward(70)
trtl.right(135)
trtl.forward(100)
trtl.end_fill()

#make the roof of the house
trtl.setheading(0)
trtl.penup()
trtl.goto(-50, 50)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("red")
trtl.left(45)
trtl.forward(70)
trtl.right(90)
trtl.forward(90)
trtl.left(90)
trtl.forward(10)
trtl.left(90)
trtl.forward(100)
trtl.left(90)
trtl.forward(110)
trtl.left(90)
trtl.forward(10)
trtl.left(90)
trtl.forward(45)
trtl.end_fill()

#make the door of the house
trtl.setheading(45)
trtl.penup()
trtl.goto(-20, -50)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("red")
trtl.left(45)
trtl.forward(50)
trtl.circle(-20, 180)
trtl.forward(50)
trtl.end_fill()
trtl.penup()

#variables for the house
#walls
wall_left_x = -50
wall_right_x = 50
wall_top_y = 50
wall_bottom_y = -50

#door
door_left_x = -20
door_right_x = 20
door_top_y = 20
door_bottom_y = -50

#door knob
trtl.begin_fill()
trtl.fillcolor("black")
trtl.penup()
trtl.goto(door_right_x - 10, door_bottom_y + 25)
trtl.pendown()
trtl.circle(5)
trtl.end_fill()

#lines in the house
for y_pos in range(-50, 50, 20):
  if y_pos < door_top_y:
      trtl.penup()
      trtl.goto(wall_left_x, y_pos)
      trtl.setheading(0)
      trtl.pendown()
      trtl.forward(door_left_x - wall_left_x)
      trtl.penup()
      trtl.goto(door_right_x, y_pos)
      trtl.pendown()
      trtl.forward(wall_right_x - door_right_x)

  else:
      trtl.penup()
      trtl.goto(wall_left_x, y_pos)
      trtl.setheading(0)
      trtl.pendown()
      trtl.forward(wall_right_x - wall_left_x)

#roof line
trtl.penup()
trtl.goto(-30, 70)
trtl.pendown()
trtl.forward(58)
trtl.penup()

#chimney
trtl.penup()
trtl.goto(20, 95)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("red")
trtl.setheading(90)
trtl.forward(30)
trtl.right(90)
trtl.forward(20)
trtl.right(90)
trtl.forward(50)
trtl.end_fill()
trtl.penup()
trtl.setheading(0)

# draw house trail
trtl.penup()
trtl.goto(1, -69)
trtl.pendown()
trtl.setheading(270)
trtl.pensize(40)
trtl.pencolor("sienna")
trtl.forward(20)
trtl.circle(60, 90)
trtl.forward(20)
trtl.circle(-60, 90)
trtl.forward(20)
trtl.circle(-60, 90)
trtl.forward(20)
trtl.circle(60, 90)
trtl.forward(100)
trtl.pensize(1)

#draw sky clouds
def sky_clouds(x,y,size):
   trtl.penup()
   trtl.color("white")

   for i in range(20):
       cloud_x = random.randint(-size, size) #tells computer to pick whole number at random (start,stop)
       cloud_y = random.randint(-size, size) #based on the parameters
   
       trtl.goto(x + cloud_x, y + cloud_y) #moves it to random spot
       trtl.begin_fill()
       trtl.circle(random.randint(15, 21)) #random radius between 5 and 15 for the smoke puff
       trtl.end_fill()

#draw the clouds
sky_clouds(-200,300,25) #(x coordinate, y coordinate, size)
sky_clouds(-350,275,25)
sky_clouds(350,230,25)
sky_clouds(300,380,25)
sky_clouds(-25,300,25)
sky_clouds(-270,375,25)
sky_clouds(150,350,25)

#trees base
trtl.penup()
trtl.goto(-300, -100)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("brown")
trtl.setheading(90)
trtl.forward(100)
trtl.right(90)
trtl.forward(20)
trtl.right(90)
trtl.forward(100)
trtl.end_fill()

trtl.penup()
trtl.goto(280, -120)
trtl.pendown()
trtl.begin_fill()
trtl.fillcolor("brown")
trtl.setheading(90)
trtl.forward(100)
trtl.right(90)
trtl.forward(20)
trtl.right(90)
trtl.forward(100)
trtl.end_fill()

#tree top
trtl.penup()
trtl.goto(-290, 5)
trtl.pendown()

def tree_top(x,y,size):
   trtl.penup()
   trtl.color("green")

   for i in range(20):
       tree_x = random.randint(-size, size) #tells computer to pick whole number at random (start,stop)
       tree_y = random.randint(-size, size) #based on the parameters
   
       trtl.goto(x + tree_x, y + tree_y) #moves it to random spot
       trtl.begin_fill()
       trtl.circle(random.randint(20, 25)) #random radius between 5 and 15 for the smoke puff
       trtl.end_fill()

#draw the tree top
tree_top(-310, 5, 25) #(x coordinate, y coordinate, size)
tree_top(270, -12, 25)

#bushes
def bush(x,y,size):
   trtl.penup()
   trtl.color("lightgreen")


   for i in range(20):
       bush_x = random.randint(-size, size) #tells computer to pick whole number at random (start,stop)
       bush_y = random.randint(-size, size) #based on the parameters
   
       trtl.goto(x + bush_x, y + bush_y) #moves it to random spot
       trtl.begin_fill()
       trtl.circle(random.randint(10, 15)) #random radius between 5 and 15 for the smoke puff
       trtl.end_fill()

#draw bush
bush(-200, -250, 15) #(x coordinate, y coordinate, size)
bush(200, -100, 15)
bush(60, -350, 15)
bush(-100, -289, 15)
bush(-75, -173, 15)
bush(-300, -381, 15)
bush(300, -234, 15)
bush(-300, -175, 15)
bush(-150, -100, 15)
bush(100, -85, 15)

#chimney smoke
trtl.speed(50)

def draw_smoke_cloud(x, y, size): #x,y, and z are the parameters for the function
  trtl.penup() #never draw lines before smoke puffs
  trtl.color("darkgray") #light gray color

  for i in range(20): #20 smoke puffs for one big puff of smoke
      #picking one random spot near the (x,y) center
      off_x = random.randint(-size, size) #tells computer to pick whole number at random (start,stop)
      off_y = random.randint(-size, size) #based on the parameters
   
      trtl.goto(x + off_x, y + off_y) #moves it to random spot
      trtl.begin_fill()
      trtl.circle(random.randint(5, 10)) #random radius between 5 and 15 for the smoke puff
      trtl.end_fill()

draw_smoke_cloud(50, 150, 10) #(x coordinate, y coordinate, size of smoke cloud)
draw_smoke_cloud(65, 200, 10)
draw_smoke_cloud(55, 250, 10)
draw_smoke_cloud(63, 300, 10)
draw_smoke_cloud(60, 350, 10)
draw_smoke_cloud(70, 400, 10)

#keep it on screen until the user clicks
wn = trtl.Screen()
wn.mainloop()

