# Drawing-Deleting-lines-on-tkinter-Canvas
we try to develop a program that allow us to draw lines on tkinter canvas and than be able to delete those linesand the vent going to be attached to buttom clicks
from random import *
from tkinter import*

def generate_colors():
        x1 = randint(0, 400)
        y1 = randint(0, 400)
        x2 = randint(0, 400)
        y2 = randint(0, 400)
        my_canvas.create_line(x1,y1,x2, y2, fill=f'#{randint(0,0xffffff):06x}', width=20)

def delete_colors():
    my_canvas.delete("all")
my_window = Tk()
my_canvas=Canvas(my_window,height=400,width=400,background="white")
random_button_colors=Button(my_window,height=2,width=20,text="click to generate colors",command=generate_colors)
delete_button_colors=Button(my_window,height=2,width=20,text="click to delete colors",command=delete_colors)
my_canvas.grid(row=0,column=0)
random_button_colors.grid(row=1,column=0)
delete_button_colors.grid(row=2,column=0)
random_width=randint(1,25)

my_window.mainloop()

