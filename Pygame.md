
```python



""" How to diplay an image """
# Initialise main window (surface)
screen = pygame.display.set_mode((800, 400)) 

# Create a filled surface
test_surf = pygame.Surface((100, 200))
test_surf.fill('WHITE')

# Load from directory and save to surface. Convert changes to fastest format for blitting
sky_surface = pygame.image.load('graphics/Sky.png').convert_alpha()     
screen.blit(sky_surface,(0,0))   # Blit means to draw or render BLock Image Transfer

# Displaying text
score_surf = test_font.render(f'Score: {current_time}', False, (64, 64, 64))
score_rect = score_surf.get_rect(center = (400, 50))
screen.blit(score_surf, score_rect)

# Update the display
display.flip()      # Updates entire display
display.update()    # Updates parameters, if none updates entire display


""" Drawing things """

# Gold line from point to cursor
pygame.draw.line(screen, 'Gold', (400, 150), pygame.mouse.get_pos(), 2)

# Brown circle


""" 
Limitting the render/game loop
"""

clock = pygame.time.Clock()     # Initialise clock
clock.tick(60)                  # Sets fps

""" Event types """

if event.type == pygame.MOUSEBUTTONDOWN:    # Mouse clicked
            print("mouse up")
if event.type == pygame.MOUSEMOTION:    # Mouse moved, prints mouse position
            print(event.pos)
keys = pygame.key.get_pressed()         # Held down
        if keys[pygame.K_q]:

""" Rectangle collision """

if player_rect.colliderect(snail_rect):     # Collision of two rectangles
    print('COLLISION!')

if player_rect.collidepoint(mouse_pos):     # Collision of rectangle and point (ie mouse)
    print(pygame.mouse.get_pos())




pygame.draw.ellipse(screen, 'Brown', pygame.Rect(50, 200, 100, 100))



```
