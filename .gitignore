import pygame
import time
import random





pygame.init()

display_width = 800
display_height = 700





 
black = (0,0,0)
white = (255,255,255)
limegreen=(50,205,50)
red1=(250,128,114)
red2=(255,160,122)
red = (255,0,0)
bright_red=(220,20,60)

bright_green = (0,255,0)
bright_green = (0,255,0)
green = (0,200,0)


yellow=(153,153,0)


black = (0,0,0)
light_brown=(218,165,32)

iii_brown=(184,134,11)
ll_brown=(238,221,130)

block_color =(210,105,30) #(53,115,255)













font = pygame.font.SysFont('SquareFont', 15)



 
car_width = 35.5


 
gameDisplay = pygame.display.set_mode((display_width,display_height))



clock = pygame.time.Clock()




 
shipimg = pygame.image.load('galgadaship.png')
bg=pygame.image.load('galgadab.png')

intros=pygame.image.load('introscreen.png')
intros1=pygame.image.load('introscreen1.png')
intros2=pygame.image.load('introscreen2.png')
intros3=pygame.image.load('introscreen3.png')

 
def things_dodged(count):
    font = pygame.font.SysFont('Insane hours 2', 20)
    text = font.render("avoided: "+str(count), True, bright_green)
    gameDisplay.blit(text,(150,3))


def lives_lived(lcount):
    font = pygame.font.SysFont('Insane hours 2', 20)
    text = font.render("lives: "+str(lcount), True, red)
    gameDisplay.blit(text,(0,3))

    
pygame.display.set_caption('space avoiders')    
 
def things(thingx, thingy, thingw, thingh, color):
    pygame.draw.rect(gameDisplay, color, [thingx, thingy, thingw, thingh])

def thingsa(thingxa, thingya, thingwa, thingha, color):
    pygame.draw.rect(gameDisplay, color, [thingxa, thingya, thingwa, thingha])



def button(msg,x,y,w,h,ic,ac,action=None):
    mouse = pygame.mouse.get_pos()
    click = pygame.mouse.get_pressed()
    print(click)
    if x+w > mouse[0] > x and y+h > mouse[1] > y:
        pygame.draw.rect(gameDisplay, ac,(x,y,w,h))

        if click[0] == 1 and action != None:
            action()         
    else:
        pygame.draw.rect(gameDisplay, ic,(x,y,w,h))

    smallText = pygame.font.SysFont('Insane hours 2',15)                               #"SquareFont",15)
    textSurf, textRect = text_objects(msg, smallText)
    textRect.center = ( (x+(w/2)), (y+(h/2)) )
    gameDisplay.blit(textSurf, textRect)


def introscreen():
    gameDisplay.blit(intros,(0,0))
    pygame.display.update()
    pygame.mixer.music.load('introsound2.mp3')
    pygame.mixer.music.play(0)
    time.sleep(1)
    gameDisplay.blit(intros1,(0,0))
    pygame.display.update()
    time.sleep(1)
    gameDisplay.blit(intros2,(0,0))
    pygame.display.update()
    time.sleep(1)
    gameDisplay.blit(intros3,(0,0))
    pygame.display.update()
    time.sleep(1)
    


def ship(x,y):
    gameDisplay.blit(shipimg,(x,y))


def BG():
    
    gameDisplay.fill(white)
    gameDisplay.blit(bg,(0,0))

    

 
def text_objects(text, font):
    textSurface = font.render(text, True, red)
    return textSurface, textSurface.get_rect()
 
def message_display(text):
    largeText = pygame.font.Font('freesansbold.ttf',115)
    TextSurf, TextRect = text_objects(text, largeText)
    TextRect.center = ((display_width/2),(display_height/2))
    gameDisplay.blit(TextSurf, TextRect)



    
 
    pygame.display.update()
 
    time.sleep(2)
 
    game_loop()
    
    
 
 
    
    
   
    
def quitgame():    
    quit()
    pyame.quit()

    
    

def game_intro():
     

     
     
     introscreen()


     pygame.mixer.music.load('spaceavoiders.mp3')
     pygame.mixer.music.play(-1)
     
   


     intro = True

     while intro:
         for event in pygame.event.get():
            #print(event)
             if event.type == pygame.QUIT:
                 pygame.quit()
                 quit()

                
                
        
         
         BG()
         largeText = pygame.font.SysFont('Insane hours 2',65)#"freesansbold.ttf")
         TextSurf, TextRect = text_objects("space avoiders", largeText)
         TextRect.center = ((400),(150))
         gameDisplay.blit(TextSurf, TextRect)


         largeText = pygame.font.SysFont('Insane hours 2',15)#"freesansbold.ttf")
         TextSurf, TextRect = text_objects("avoid as much pixels as possible", largeText)
         TextRect.center = ((400),(400))
         gameDisplay.blit(TextSurf, TextRect)
    
         button("start",150,450,100,50,green,bright_green,game_loop)
         button("quit",550,450,100,50,red1,bright_red,quitgame)
        

         pygame.display.update()
         clock.tick(15)
        
    
def crash():
    
    
    #shipimg=pygame.image.load('explosion image.png')
    
     pygame.mixer.music.load('explosion.mp3')
     pygame.mixer.music.play(0)
    
     time.sleep(2)
    




    
     pygame.mixer.music.load('spaceavoiders.mp3')
     pygame.mixer.music.play(-1)




     intro = True

     while intro:
         
         for event in pygame.event.get():
             if event.type == pygame.QUIT:
                 pygame.quit()
                 quit()

         
         BG()
        
         largeText = pygame.font.SysFont('Insane hours 2',55)#"freesansbold.ttf")
         TextSurf, TextRect = text_objects("game over", largeText)
         TextRect.center = ((400),(100))
         gameDisplay.blit(TextSurf, TextRect)


         largeText = pygame.font.SysFont('Insane hours 2',15)#"freesansbold.ttf")
         TextSurf, TextRect = text_objects("avoid as mutch pixels as you can ", largeText)
         TextRect.center = ((400),(400))
         gameDisplay.blit(TextSurf, TextRect)
    
         button("rematch",150,450,100,50,green,bright_green,game_loop)
         button("give up",550,450,100,50,red1,bright_red,quitgame)
        

         pygame.display.update()
         clock.tick(15)

    
        
    
    #message_display('game over')
    #game_intro()
  #lived-=1


                 
                

                
                
        
        

        
        

    
def game_loop():
    x = (display_width * 0.45)
    y = (display_height * 0.8)


    xa=400
    ya=400
    
    shipimg=pygame.image.load('galgadaship.png')

    pygame.mixer.music.load('spaceavoidersbg.mp3')
    pygame.mixer.music.play(-1)

    
    


 
    x_change = 0
 
    thing_startx = random.randrange(0, display_width)
    thing_starty = -600
    thing_speed = 15
    thing_width = 40
    thing_height = 40


    thing_startxa=random.randrange(0, display_width)
    thing_startya=-400
    thing_widtha=45
    thing_heighta=45
    thing_speed2=10



    
    
 
    thingCount = 1
 
    dodged = 0
    lived =3
 
    gameExit = False
 
    while not gameExit:
        #print(x)
        print (clock)

        
 
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                pygame.quit()
                quit()


            #if lived<=0:
           #     crash()
 
            if event.type == pygame.KEYDOWN:
                if event.key == pygame.K_LEFT:
                    x_change = -7
                if event.key == pygame.K_RIGHT:
                    x_change =7
                    
 
            if event.type == pygame.KEYUP:
                if event.key == pygame.K_LEFT or event.key == pygame.K_RIGHT:
                    x_change = 0
 
        x += x_change
        
        
        BG()
        things(thing_startx, thing_starty, thing_width, thing_height,block_color )
 
 
        
        thing_starty += thing_speed
        thing_startya +=thing_speed
        ship(x,y)
        
        things_dodged(dodged)
        lives_lived(lived)
 
        if x > display_width - car_width or x < 0:
            
            crash()
            
            
 
        if thing_starty > display_height:
            thing_starty = 0 - thing_height
            thing_startx = random.randrange(0,display_width)
            dodged += 0.5
            thing_speed += 0.2
            #thing_width += (dodged * 1.2)


        if thing_startya > display_height:
            thing_startya = 0 - thing_heighta
            thing_startxa = random.randrange(0,display_width)
            dodged += 0.5
            thing_speed2 += 0.2



        if dodged>=5:
            thingsa(thing_startxa, thing_startya, thing_widtha, thing_heighta, block_color)
             
             
             
   

            #print('higher')



            
 
       
 
        if y < thing_starty+thing_height:
            if x > thing_startx and x < thing_startx + thing_width or x+car_width > thing_startx and x + car_width < thing_startx+thing_width:
                   # print('x crossover')
                   crash()

                
        if y < thing_startya+thing_heighta:
            if x > thing_startxa and x < thing_startxa + thing_widtha or x+car_width > thing_startxa and x + car_width < thing_startxa+thing_widtha:
                   crash()






        #if thing_startya+thing_heighta:
            #if x> thing_startxa and x< thing_start_startxa+ thing_widtha or x+car_width> thing_startxa and x + car_widtha< thing_startxa+thing_widtha:
                #crash()
           



           
        
        pygame.display.update()
        fps=42.9
        clock.tick(fps)
       # if lived<=0:
            #lived=0
            #print ('dead')


           # if lived=0<:
             #   pygame.quit()
             #   quit()
        
        
game_intro()
game_loop()
pygame.quit()
quit()
