# Flying-Comet
# A comet flying across the sky, as viewed from earth. Created using Python Graphics.
from graphics import Canvas
import random
import time
    
CANVAS_WIDTH = 400
CANVAS_HEIGHT = 300
SIDE = 10
CIRCLE_SIZE = 7
STAR_SIZE = 4
DELAY = 0.03

def main():
    canvas = Canvas(CANVAS_WIDTH, CANVAS_HEIGHT)
    # TODO: your code here!
    
    lake = canvas.create_rectangle(0, 0, CANVAS_WIDTH, CANVAS_HEIGHT, "navy")
    sky = canvas.create_rectangle(0, 0, CANVAS_WIDTH, CANVAS_HEIGHT*0.6, "midnightblue")
    road = canvas.create_rectangle(0, CANVAS_HEIGHT*0.8, CANVAS_WIDTH, CANVAS_HEIGHT)
    
    
    
    
    # bridge
    
    line = canvas.create_line(0, CANVAS_HEIGHT*0.69, CANVAS_WIDTH, CANVAS_HEIGHT*0.69)
    x=CANVAS_WIDTH/4
    for i in range (3):
        line = canvas.create_line(x, CANVAS_HEIGHT*0.69, x, CANVAS_HEIGHT*0.8)
        x=x+CANVAS_WIDTH/4
        
    # buildings
    
    l1=0
    r1=10
    l2=11
    r2=25
    l3=26
    r3=45
    l4=46
    r4=64
    shore=CANVAS_HEIGHT*0.6
    t1=128
    b1=130
    x1=4
    y1=7
    
    for i in range (7):
        h1 = canvas.create_rectangle(l1, CANVAS_HEIGHT*0.4, r1, shore)
        l1=l1+65
        r1=r1+65
        #while b1<shore:
         #   light=canvas.create_rectangle(x1, t1, y1, b1, 'tomato')
          #  t1=t1+15
           # b1=b1+15
        #t1=128
        #b1=130
        
        h2 = canvas.create_rectangle(l2, CANVAS_HEIGHT*0.5, r2, shore)
        l2=l2+65
        r2=r2+65
        
        h3 = canvas.create_rectangle(l3, CANVAS_HEIGHT*0.47, r3, shore)
        l3=l3+65
        r3=r3+65
        
        h4 = canvas.create_rectangle(l4, CANVAS_HEIGHT*0.53, r4, shore)
        l4=l4+65
        r4=r4+65
        
        
    #stars
    sl1=25.5
    sl2=24
    st1=30
    st2=31
    sr1=26.5
    sr2=28
    sb1=34
    sb2=32
    for i in range (3):
        rect1=canvas.create_rectangle(sl1, 30, sr1, 34, 'cornsilk')
        rect2=canvas.create_rectangle(sl2, 31, sr2, 32, 'cornsilk')
        sl1=sl1+150
        sr1=sr1+150
        sl2=sl2+150
        sr2=sr2+150
        
    sl1=90.5
    sl2=89
    st1=55
    st2=56
    sr1=91.5
    sr2=93
    sb1=59
    sb2=57
    for i in range (3):
        rect1=canvas.create_rectangle(sl1, 49, sr1, 53, 'cornsilk')
        rect2=canvas.create_rectangle(sl2, 50, sr2, 51, 'cornsilk')
        sl1=sl1+150
        sr1=sr1+150
        sl2=sl2+150
        sr2=sr2+150


    # comet
    
    star = canvas.create_oval(0, 0, STAR_SIZE, STAR_SIZE, 'azure')    
    trail1 = canvas.create_line(-40, -3, STAR_SIZE, STAR_SIZE-2,'paleturquoise')
    trail2 = canvas.create_line(-43, -3, STAR_SIZE, STAR_SIZE+1,'paleturquoise')
    trail3 = canvas.create_line(-46, -3, STAR_SIZE, STAR_SIZE,'paleturquoise')
    change_x = 6
    change_y = 1
    
    # animation loop
    while(True): 
        # update the ball
        canvas.move(star, change_x, change_y)
        canvas.move(trail1, change_x, change_y)
        canvas.move(trail2, change_x, change_y)
        canvas.move(trail3, change_x, change_y)
        # pause
        time.sleep(DELAY)
        
        
    # comet
    
    
        

if _name_ == '_main_':
    main()
