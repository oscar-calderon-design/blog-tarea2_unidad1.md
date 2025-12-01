# blog-tarea2_unidad1.md
Tarea 2 - Ejercicios Unidad 1

2.Crea el rastro de una tortuga moviéndose hacia abajo usando únicamente print() e input().

Salida esperada: una línea vertical simulada con ↓.
# reto2.py

print("Simulación de tortuga bajando")
pasos = int(input("¿Cuántos pasos debe bajar la tortuga? "))

print("Tortuga bajando ↓")

for _ in range(pasos):
    print("↓")
cada iteración imprime una flecha hacia abajo simulando el desplazamiento vertical.

3.La tortuga ahora avanza, gira a la derecha y vuelve a avanzar, formando una “L”.

# reto3.py

print("Simulación de tortuga girando y avanzando")

pasos1 = int(input("Pasos hacia adelante: "))
giro = 90  # Simulación del giro
pasos2 = int(input("Pasos después del giro: "))

print("Movimiento:")
print("→" * pasos1)
for _ in range(pasos2):
    print("↓")

el programa reproduce el dibujo de una “L”: primero se imprime la línea horizontal → y luego la vertical ↓.

4. Reescribe los retos usando las funciones
   # reto4.py

def adelante(n):
    print("→" * n)

def abajo(n):
    for _ in range(n):
        print("↓")

print("Simulación con funciones")

adelante(5)
abajo(3)

Se modulariza el comportamiento creando funciones para cada movimiento.

5. Ajusta las funciones para que la tortuga pueda bajar escalones, manteniendo la posición horizontal acumulada.

Cada escalón tiene un tramo horizontal seguido de uno vertical.

# reto5.py

posicion_horizontal = 0

def adelante(n):
    global posicion_horizontal
    print(" " * posicion_horizontal + "→" * n)
    posicion_horizontal += n

def abajo(n):
    global posicion_horizontal
    for _ in range(n):
        print(" " * posicion_horizontal + "↓")

# Ejemplo de escalera
adelante(5)
abajo(2)

adelante(5)
abajo(2)

adelante(5)
abajo(2)

La variable posicion_horizontal conserva el desplazamiento acumulado, permitiendo dibujar escalones correctamente alineados.

referencia bibliografica: https://chatgpt.com/s/t_692d0b7e18f88191806aa1f1e8e36e
