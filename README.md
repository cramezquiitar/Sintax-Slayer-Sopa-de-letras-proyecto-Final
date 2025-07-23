
# 🧩 Sopa de Letras: Ingeniería Civil

Este proyecto es un juego interactivo de **sopa de letras en Python**, con palabras relacionadas a la **ingeniería civil**. El jugador elige una dificultad y debe encontrar palabras escondidas en una matriz que puede ir de 10x10 a 30x30. Las palabras pueden estar ubicadas **horizontal, vertical o diagonalmente**.

---

## 🛠️ Tecnologías Usadas

- `Python`
- `random` (para posiciones y letras aleatorias)
- `pandas` (para mostrar la sopa como una tabla)
- `numpy` (no se usa realmente en este código, puede eliminarse)

---

## 📚 Lista de Palabras

Las palabras seleccionadas están relacionadas con conceptos de ingeniería civil, como:

```
"PUENTE", "VIGA", "CIMENTACION", "CONCRETO", "ASFALTO",
"TOPOGRAFIA", "DRENAJE", "SUELO", "ESTRUCTURA", "HORMIGON",
"PLANOS", "MECANICA", "TRABAJO", "EDIFICIO", "LADRILLO", "COLUMNA"
```

---

## 🧱 ¿Cómo funciona el código?

### 1. **Crear la sopa vacía**
Se genera una matriz de tamaño `n x n` llena de espacios en blanco (`' '`).

### 2. **Insertar palabras**
Cada palabra se coloca aleatoriamente en la sopa:
- Horizontalmente (→)
- Verticalmente (↓)
- Diagonalmente (↘)

Antes de insertarse, se verifica que no se cruce con otra palabra.

### 3. **Rellenar espacios vacíos**
Una vez insertadas las palabras, los espacios en blanco se llenan con letras aleatorias del alfabeto (`A-Z`, `Ñ`).

### 4. **Mostrar la sopa**
Se usa `pandas.DataFrame` para visualizar la sopa con coordenadas, facilitando la interacción del jugador.

### 5. **Juego interactivo**
- El jugador elige dificultad:  
  `1 = 10x10`, `2 = 20x20`, `3 = 30x30`
- Se muestran 10 palabras aleatorias por encontrar.
- El jugador intenta adivinar:
  - La **palabra**
  - La **fila** y **columna inicial**
  - La **dirección** (`H`, `V`, `D`)
- El programa verifica si es correcta.

### 6. **Verificación**
El sistema compara letra por letra en la dirección indicada para confirmar si la palabra fue correctamente ubicada.

---

## 🧪 Ejecución del juego

Asegúrate de corregir el siguiente error antes de ejecutar:

```python
# ❌ Incorrecto:
if _name_ == "_main_":

# ✅ Correcto:
if __name__ == "__main__":
    jugar_sopa_letras()
```

Para ejecutar el juego:

```bash
python sopa_letras.py
```

---

## 🎮 Captura del juego (opcional)

Puedes añadir aquí una imagen de cómo se ve la sopa en consola usando `pandas`:

```
   0  1  2  3  4  5  6 ...
0  P  Q  L  A  N  O  S ...
1  U  T  R  B  E  H  G ...
...
```

---

## ✅ Estado del proyecto

- [x] Generación aleatoria de sopa
- [x] Inserción segura de palabras
- [x] Interacción por consola
- [x] Verificación de palabras encontradas
- [ ] Interfaz gráfica (pendiente)

---

## 📌 Notas adicionales

- Puedes modificar la lista de palabras según tu área de interés.
- Ideal para proyectos educativos o demostraciones en clase.
- Si vas a usar este código en presentaciones, recuerda explicar el uso de `pandas` y cómo se maneja la verificación de palabras por coordenadas.

---

## 📄 Licencia

Este proyecto está bajo la licencia [MIT](LICENSE).
