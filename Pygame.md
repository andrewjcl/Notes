
```python



""" How to diplay an image """
# Initialise main window (surface)
screen = pygame.display.set_mode((800, 400))            
# Load from directory and save to surface. Convert changes to fastest format for blitting
sky_surface = pygame.image.load('graphics/Sky.png').convert_alpha()     

screen.blit(sky_surface,(0,0))   # Blit means to draw or render

""" 
Limitting the fps
Very important if our game logic loop is also render loop (which it is atm)
"""

clock = pygame.time.Clock()     # Initialise clock
clock.tick(60)                  # Sets fps

""" Event types """

if event.type == pygame.MOUSEBUTTONDOWN:    # Mouse clicked
            print("mouse up")
if event.type == pygame.MOUSEMOTION:    # Mouse moved, prints mouse position
            print(event.pos)

""" Rectangle collision """

if player_rect.colliderect(snail_rect):     # Collision of two rectangles
    print('COLLISION!')

if player_rect.collidepoint(mouse_pos):     # Collision of rectangle and point (ie mouse)
    print(pygame.mouse.get_pos())


```
