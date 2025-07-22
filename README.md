A cristian le gustn los hombres



# Sintax-Slayer-Sopa-de-letras-proyecto-Final

## Objetivo: 📌
Desarrollar una aplicación en Python que genere y permita jugar una sopa de letras de tamaño mínimo 10x10 y máximo 30x30, utilizando palabras clave relacionadas con la carrera de Ingeniería Civil, aplicando los conocimientos adquiridos durante el curso de programación.

## Objetivos especificos 📎
- Implementar estructuras de datos adecuadas (listas, matrices) para representar el tablero de la sopa de letras y gestionar el contenido de forma dinámica.

- Aplicar algoritmos de inserción y búsqueda de palabras en distintas direcciones (horizontal, vertical y diagonal), asegurando que estas no se sobrepongan incorrectamente ni excedan los límites de la matriz.

- Automatizar el proceso de generación del tablero, incluyendo la inserción de letras aleatorias en los espacios vacíos para camuflar las palabras ocultas.

- Diseñar una interfaz simple en consola que permita al usuario interactuar con el juego, ingresar palabras, recibir retroalimentación y visualizar el tablero actualizado.

- Integrar un conjunto de palabras relacionadas con Ingeniería Civil, tales como: cimentación, hormigón, estructura, acero, plano, geotecnia, topografía, entre otras, promoviendo así la familiarización con el vocabulario técnico de la profesión.

- Fomentar la reutilización del código mediante el uso de funciones y/o módulos, favoreciendo el desarrollo estructurado, legible y mantenible.

- Incorporar elementos básicos de validación y control de errores, como verificar la validez de palabras ingresadas o el rango del tablero.


## Diagrama
```mermaid
flowchart TD
    A[Inicio] --> B[Definir lista de palabras]
    B --> C[Pedir al usuario escoger dificultad]
    C --> D{Dificultad}
    D -->|Fácil| E[Definir tablero 10x10]
    D -->|Medio| F[Definir tablero 20x20]
    D -->|Difícil| G[Definir tablero 30x30]
    E --> H[Crear tablero con guiones]
    F --> H
    G --> H

    H --> I[Para cada palabra en lista]
    I --> J[Repetir]
    J --> K[Elegir dirección y posición aleatoria]
    K --> L{¿Cabe la palabra sin conflicto?}
    L -->|Sí| M[Insertar palabra en tablero]
    M --> N[Fin Repetir]
    L -->|No| K
    N --> O{¿Quedan palabras?}
    O -->|Sí| I
    O -->|No| P[Recorrer tablero]

    P --> Q{¿Celda es -?}
    Q -->|Sí| R[Rellenar con letra aleatoria]
    Q -->|No| S[Siguiente celda]
    R --> S
    S --> T{¿Quedan celdas?}
    T -->|Sí| P
    T -->|No| U[Imprimir tablero en consola]

    U --> V[Iniciar puntuación = 0]
    V --> W{¿Quedan palabras por encontrar?}
    W -->|Sí| X[Pedir palabra al usuario]
    X --> Y{¿Está en lista y en tablero?}
    Y -->|Sí| Z[Mostrar Correcto\nAumentar puntuación\nMarcar como encontrada]
    Y -->|No| AA[Mostrar Incorrecto o ya encontrada]
    Z --> W
    AA --> W

    W -->|No| AB[Mostrar mensaje de fin de juego]
    AB --> AC[Mostrar puntuación final]
    AC --> AD[FIN]

```

## Codigo 


![image](https://github.com/user-attachments/assets/a1f9d695-79dd-4e52-945b-ddb1b0473f86)
