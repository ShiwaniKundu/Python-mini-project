## Python-mini-project
##Chess Board
import turtle
import chess
sc = turtle.Screen()
pen = turtle.Turtle()
def draw():

  for i in range(4):
    pen.forward(30)
    pen.left(90)

  pen.forward(30)
if __name__ == "__main__" :
    sc.setup(500, 500)
    pen.speed(100)
    for i in range(8):
      pen.up()
      pen.setpos(0, 30 * i)
      pen.down()

      for j in range(8):
        if (i + j)% 2 == 0:
          col ='black'

        else:
          col ='white'

        pen.fillcolor(col)


        pen.begin_fill()
        draw()
        pen.end_fill()
pen.hideturtle()

c=input("Enter colomn name:")
r=int(input("Enter row number:"))
d=['A','B','C','D','E','F','G','H','a','b','c','d','e','f','g','h']
m=[1,2,3,4,5,6,7,8]

while (c not in d) or (r not in m):
    c=input("Re enter colomn name:")
    r=int(input("Re enter row number:"))

if (c in d) and (r in m):
    x=d.index(c)
    s=x+r
    if s%2==0:
        print("WHITE")
    else:
        print("BLACK")
