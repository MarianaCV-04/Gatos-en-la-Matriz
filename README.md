# Gatos-en-la-Matriz
Progra II - Taller de programación. Juego de lógica en Python con matrices, validación de reglas, resolución por backtracking, generación de escenarios, persistencia en archivos e interfaz Tkinter.
Organización

- `logica.py`: matrices, movimientos, conflictos, victoria e historial de deshacer.
- `solucionador.py`: búsqueda de soluciones por backtracking (siguiente etapa).
- `generador.py`: creación de escenarios válidos (etapa posterior).
- `persistencia.py`: datos TXT/CSV/JSON, sin base de datos (etapa posterior).
- `interfaz.py`: menú y tablero interactivo en Tkinter.
- `main.py`: punto de entrada.

## Ejecutar

Desde la carpeta que contiene este README:

```bash
python -m gatos_en_la_matriz.main
```

Se usa únicamente la biblioteca estándar de Python, incluida Tkinter.

## Interfaz disponible

El menú permite iniciar una partida demostrativa en tamaños 4 × 4, 6 × 6, 8 × 8 y 10 × 10. El tablero muestra colores por región; haz clic para colocar o retirar gatos. Los conflictos se resaltan, y están disponibles el cronómetro, reinicio y deshacer.

La partida actual usa un escenario demostrativo con regiones verticales. Las demás opciones del menú aparecen deshabilitadas hasta que implementemos generación de escenarios, usuarios y persistencia.

## Reglas base

Cada gato debe ser el único en su fila, columna y región. Dos gatos no pueden tocarse, tampoco en diagonal. Se gana al colocar exactamente N gatos sin conflictos. Se permiten movimientos conflictivos durante el juego para poder mostrarlos y corregirlos.

Las coordenadas internas de las funciones comienzan en cero.
