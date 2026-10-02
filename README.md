# Pygame

## Instrukce

- Spustit program main.py
- Využívat tlačítka A, D pro pohyb doleva a do prava
- Tlačítko Space pro jump

*Poznámka: program musí být spouštěn ze složky pygame*

**super duper duleziata vec**

### Ukázka kódu

`Code`

```python
class Main:
    def __init__(self):
        pygame.init()

        self.screen = pygame.display.set_mode((800, 600))
        self.screen.set_alpha(255)
        self.clock = pygame.Clock()
        self.space = pymunk.Space()
        self.space.gravity = (0, 700)

        self.player = PhysicsEntity(self, (50, 50), (23, 19))

        self.movement = [False, False]
        self.jump = False

        self.font = pygame.font.SysFont("Arial", 24)
        self.font_img = self.font.render("Kraaa", antialias=False, color=(15, 15, 15))
        self.say_kraa = False

        floor_body = pymunk.Body(body_type=pymunk.Body.STATIC)
        floor_shape = pymunk.Segment(floor_body, (-50, 300), (850, 300), 10)
        floor_shape.friction = 0.99
        floor_shape.collision_type = 2
        self.space.add(floor_shape, floor_body)
```



### TODO:

- [x] Dodělat dokumentaci
- [ ] Vylepšit webovou stranků