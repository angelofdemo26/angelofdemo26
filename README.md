EXECUTE

CODE = """
import pygame
import random

# Inicializar Pygame
pygame.init()

# Dimensiones de la pantalla
ANCHO = 800
ALTO = 600
TAMAÑO_CELDA = 30
COLUMNAS = ANCHO // TAMAÑO_CELDA
FILAS = ALTO // TAMAÑO_CELDA

# Colores
NEGRO = (0, 0, 0)
BLANCO = (255, 255, 255)
ROJO = (255, 0, 0)
VERDE = (0, 255, 0)
AZUL = (0, 0, 255)

# Crear la pantalla
pantalla = pygame.display.set_mode((ANCHO, ALTO))
pygame.display.set_caption("Tetris")

# Definir las formas de las piezas
FORMAS = [
    [[1, 1, 1, 1]],  # I
    [[1, 1], [1, 1]],  # O
    [[1, 1, 0], [0, 1, 1]],  # S
    [[0, 1, 1], [1, 1, 0]],  # Z
    [[1, 1, 1], [0, 1, 0]],  # T
    [[1, 1, 1], [1, 0, 0]],  # L
    [[1, 1, 1], [0, 0, 1]]  # J
]

# Clase para las piezas
class Pieza:
    def __init__(self, x, y, forma):
        self.x = x
        self.y = y
        self.forma = forma
        self.color = random.choice([ROJO, VERDE, AZUL])
        self.rotacion = 0

# Función principal del juego
def juego():
    reloj = pygame.time.Clock()
    corriendo = True
    while corriendo:
        for evento in pygame.event.get():
            if evento.type == pygame.QUIT:
                corriendo = False

        pantalla.fill(NEGRO)
        pygame.display.flip()
        reloj.tick(30)

    pygame.quit()

if __name__ == "__main__":
    juego()
"""
create_file('tetris.py', CODE)

STDOUT/STDERR

[File tetris.py created.]
[File: /home/user/tetris.py (62 lines total after edit)]
1|
2|import pygame
3|import random
4|
5|# Inicializar Pygame
6|pygame.init()
7|
8|# Dimensiones de la pantalla
9|ANCHO = 800
10|ALTO = 600
11|TAMAÑO_CELDA = 30
12|COLUMNAS = ANCHO // TAMAÑO_CELDA
13|FILAS = ALTO // TAMAÑO_CELDA
14|
15|# Colores
16|NEGRO = (0, 0, 0)
17|BLANCO = (255, 255, 255)
18|ROJO = (255, 0, 0)
19|VERDE = (0, 255, 0)
20|AZUL = (0, 0, 255)
21|
22|# Crear la pantalla
23|pantalla = pygame.display.set_mode((ANCHO, ALTO))
24|pygame.display.set_caption("Tetris")
25|
26|# Definir las formas de las piezas
27|FORMAS = [
28|    [[1, 1, 1, 1]],  # I
29|    [[1, 1], [1, 1]],  # O
30|    [[1, 1, 0], [0, 1, 1]],  # S
31|    [[0, 1, 1], [1, 1, 0]],  # Z
32|    [[1, 1, 1], [0, 1, 0]],  # T
33|    [[1, 1, 1], [1, 0, 0]],  # L
34|    [[1, 1, 1], [0, 0, 1]]  # J
35|]
36|
37|# Clase para las piezas
38|class Pieza:
39|    def __init__(self, x, y, forma):
40|        self.x = x
41|        self.y = y
42|        self.forma = forma
43|        self.color = random.choice([ROJO, VERDE, AZUL])
44|        self.rotacion = 0
45|
46|# Función principal del juego
47|def juego():
48|    reloj = pygame.time.Clock()
49|    corriendo = True
50|    while corriendo:
51|        for evento in pygame.event.get():
52|            if evento.type == pygame.QUIT:
53|                corriendo = False
54|
55|        pantalla.fill(NEGRO)
56|        pygame.display.flip()
57|        reloj.tick(30)
58|
59|    pygame.quit()
60|
61|if __name__ == "__main__":
62|    juego()
[File updated. Please review the changes carefully and make sure they are correct (correct indentation, no duplicate or redundant lines etc). Edit the file again if necessary.]



