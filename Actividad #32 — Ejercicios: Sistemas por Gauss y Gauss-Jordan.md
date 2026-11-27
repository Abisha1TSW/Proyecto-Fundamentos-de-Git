# Actividad #32 — Ejercicios: Sistemas por Gauss y Gauss-Jordan

## Resumen de resultados

| # | Método | Resultado |
|---|--------|-----------|
| 37 | Gauss | x = −4, y = 4, z = 2 |
| 38 | Gauss | a = 1, b = 0, c = 2 |
| 39 | Gauss | a = −1, b = −1, c = 2 |
| 40 | Gauss | x = −1, y = 2, z = 2 |
| 41 | Gauss | a = −3, b = 5, c = 1 |
| 42 | Gauss | a = 4, b = 1, c = 1 |
| 43 | Gauss | a = −2, b = 4, c = −2 |
| 44 | Gauss | a = −6, b = −1, c = 5 |
| 45 | Gauss-Jordan | Sin solución |
| 46 | Gauss-Jordan | a = 3, b = −6, c = −1 |
| 47 | Gauss-Jordan | Sin solución |
| 48 | Gauss-Jordan | r = 4, s = 3, t = 4 |
| 49 | Gauss-Jordan | x = 7 - z, 2y = z - 5 (z libre) (Infinitas soluciones) |
| 50 | Gauss-Jordan | r = −4, s = −1, t = 0 |
| 51 | Gauss-Jordan | r = 3, s = 0, t = −1 |
| 52 | Gauss-Jordan | x = 3, y = −2, z = −2 |

---

## Ejercicio 37 (Gauss)

- `6x + y - z = -22`
- `-x + 3y + 3z = 22`
- `-6x - 6z = 12`

**Matriz aumentada:**
```
[   6    1   -1 | -22 ]
[  -1    3    3 |  22 ]
[  -6    0   -6 |  12 ]
```

1. **R1 ↔ R2** (se intercambian filas para tener un pivote cómodo en la columna 1).
```
[  -1    3    3 |  22 ]
[   6    1   -1 | -22 ]
[  -6    0   -6 |  12 ]
```

2. **R2 → −R2 − 6R1** (elimina la columna 1 en la fila 2).
```
[   -1     3     3 |   22 ]
[    0   -19   -17 | -110 ]
[   -6     0    -6 |   12 ]
```

3. **R3 → −R3 + 6R1** (elimina la columna 1 en la fila 3). Se simplifica dividiendo la fila 3 entre 6.
```
[   -1     3     3 |   22 ]
[    0   -19   -17 | -110 ]
[    0     3     4 |   20 ]
```

4. **R2 ↔ R3** (se intercambian filas para tener un pivote cómodo en la columna 2).
```
[   -1     3     3 |   22 ]
[    0     3     4 |   20 ]
[    0   -19   -17 | -110 ]
```

5. **R3 → 3R3 + 19R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 25.
```
[ -1   3   3 | 22 ]
[  0   3   4 | 20 ]
[  0   0   1 |  2 ]
```

**Sustitución hacia atrás:**

- Fila 3: `z = 2` → **z = 2**
- Fila 2: `3y + 4z = 20` → **y = 4**
- Fila 1: `-x + 3y + 3z = 22` → **x = -4**

**Solución:** x = -4, y = 4, z = 2

**Comprobación:** ✓ cumple las 3 ecuaciones originales

---

## Ejercicio 38 (Gauss)

- `-4a - 3b - 2c = -8`
- `a - 4b - 2c = -3`
- `4a - 2b + c = 6`

**Matriz aumentada:**
```
[ -4  -3  -2 | -8 ]
[  1  -4  -2 | -3 ]
[  4  -2   1 |  6 ]
```

1. **R1 ↔ R2** (se intercambian filas para tener un pivote cómodo en la columna 1).
```
[  1  -4  -2 | -3 ]
[ -4  -3  -2 | -8 ]
[  4  -2   1 |  6 ]
```

2. **R2 → R2 + 4R1** (elimina la columna 1 en la fila 2).
```
[   1   -4   -2 |  -3 ]
[   0  -19  -10 | -20 ]
[   4   -2    1 |   6 ]
```

3. **R3 → R3 − 4R1** (elimina la columna 1 en la fila 3).
```
[   1   -4   -2 |  -3 ]
[   0  -19  -10 | -20 ]
[   0   14    9 |  18 ]
```

4. **R2 ↔ R3** (se intercambian filas para tener un pivote cómodo en la columna 2).
```
[   1   -4   -2 |  -3 ]
[   0   14    9 |  18 ]
[   0  -19  -10 | -20 ]
```

5. **R3 → 14R3 + 19R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 31.
```
[  1  -4  -2 | -3 ]
[  0  14   9 | 18 ]
[  0   0   1 |  2 ]
```

**Sustitución hacia atrás:**

- Fila 3: `c = 2` → **c = 2**
- Fila 2: `14b + 9c = 18` → **b = 0**
- Fila 1: `a - 4b - 2c = -3` → **a = 1**

**Solución:** a = 1, b = 0, c = 2

**Comprobación:** ✓ cumple las 3 ecuaciones originales

---

## Ejercicio 39 (Gauss)

- `a + 5b - 4c = -14`
- `2a - 5b - 5c = -7`
- `3a + 3b + 2c = -2`

**Matriz aumentada:**
```
[   1    5   -4 | -14 ]
[   2   -5   -5 |  -7 ]
[   3    3    2 |  -2 ]
```

1. **R2 → R2 − 2R1** (elimina la columna 1 en la fila 2). Se simplifica dividiendo la fila 2 entre 3.
```
[   1    5   -4 | -14 ]
[   0   -5    1 |   7 ]
[   3    3    2 |  -2 ]
```

2. **R3 → R3 − 3R1** (elimina la columna 1 en la fila 3). Se simplifica dividiendo la fila 3 entre 2.
```
[   1    5   -4 | -14 ]
[   0   -5    1 |   7 ]
[   0   -6    7 |  20 ]
```

3. **R3 → −5R3 + 6R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 29.
```
[   1    5   -4 | -14 ]
[   0   -5    1 |   7 ]
[   0    0   -1 |  -2 ]
```

**Sustitución hacia atrás:**

- Fila 3: `-c = -2` → **c = 2**
- Fila 2: `-5b + c = 7` → **b = -1**
- Fila 1: `a + 5b - 4c = -14` → **a = -1**

**Solución:** a = -1, b = -1, c = 2

**Comprobación:** ✓ cumple las 3 ecuaciones originales

---

## Ejercicio 40 (Gauss)

- `6x + 6y + 5z = 16`
- `-6x + 6y + z = 20`
- `2x - 2y + 3z = 0`

**Matriz aumentada:**
```
[  6   6   5 | 16 ]
[ -6   6   1 | 20 ]
[  2  -2   3 |  0 ]
```

1. **R1 ↔ R3** (se intercambian filas para tener un pivote cómodo en la columna 1).
```
[  2  -2   3 |  0 ]
[ -6   6   1 | 20 ]
[  6   6   5 | 16 ]
```

2. **R2 → 2R2 + 6R1** (elimina la columna 1 en la fila 2). Se simplifica dividiendo la fila 2 entre 20.
```
[  2  -2   3 |  0 ]
[  0   0   1 |  2 ]
[  6   6   5 | 16 ]
```

3. **R3 → 2R3 − 6R1** (elimina la columna 1 en la fila 3). Se simplifica dividiendo la fila 3 entre 8.
```
[  2  -2   3 |  0 ]
[  0   0   1 |  2 ]
[  0   3  -1 |  4 ]
```

4. **R2 ↔ R3** (se intercambian filas para tener un pivote cómodo en la columna 2).
```
[  2  -2   3 |  0 ]
[  0   3  -1 |  4 ]
[  0   0   1 |  2 ]
```

**Sustitución hacia atrás:**

- Fila 3: `z = 2` → **z = 2**
- Fila 2: `3y - z = 4` → **y = 2**
- Fila 1: `2x - 2y + 3z = 0` → **x = -1**

**Solución:** x = -1, y = 2, z = 2

**Comprobación:** ✓ cumple las 3 ecuaciones originales

---

## Ejercicio 41 (Gauss)

- `-2a + b - 4c = 7`
- `4a + 6b + c = 19`
- `-6a - 6b - 5c = -17`

**Matriz aumentada:**
```
[  -2    1   -4 |   7 ]
[   4    6    1 |  19 ]
[  -6   -6   -5 | -17 ]
```

1. **R2 → −2R2 − 4R1** (elimina la columna 1 en la fila 2). Se simplifica dividiendo la fila 2 entre 2.
```
[  -2    1   -4 |   7 ]
[   0   -8    7 | -33 ]
[  -6   -6   -5 | -17 ]
```

2. **R3 → −2R3 + 6R1** (elimina la columna 1 en la fila 3). Se simplifica dividiendo la fila 3 entre 2.
```
[  -2    1   -4 |   7 ]
[   0   -8    7 | -33 ]
[   0    9   -7 |  38 ]
```

3. **R3 → −8R3 − 9R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 7.
```
[  -2    1   -4 |   7 ]
[   0   -8    7 | -33 ]
[   0    0   -1 |  -1 ]
```

**Sustitución hacia atrás:**

- Fila 3: `-c = -1` → **c = 1**
- Fila 2: `-8b + 7c = -33` → **b = 5**
- Fila 1: `-2a + b - 4c = 7` → **a = -3**

**Solución:** a = -3, b = 5, c = 1

**Comprobación:** ✓ cumple las 3 ecuaciones originales

---

## Ejercicio 42 (Gauss)

- `5a - 3b + 5c = 22`
- `-4a - b + c = -16`
- `2a + 4b - c = 11`

**Matriz aumentada:**
```
[   5   -3    5 |  22 ]
[  -4   -1    1 | -16 ]
[   2    4   -1 |  11 ]
```

1. **R1 ↔ R3** (se intercambian filas para tener un pivote cómodo en la columna 1).
```
[   2    4   -1 |  11 ]
[  -4   -1    1 | -16 ]
[   5   -3    5 |  22 ]
```

2. **R2 → 2R2 + 4R1** (elimina la columna 1 en la fila 2). Se simplifica dividiendo la fila 2 entre 2.
```
[  2   4  -1 | 11 ]
[  0   7  -1 |  6 ]
[  5  -3   5 | 22 ]
```

3. **R3 → 2R3 − 5R1** (elimina la columna 1 en la fila 3).
```
[   2    4   -1 |  11 ]
[   0    7   -1 |   6 ]
[   0  -26   15 | -11 ]
```

4. **R3 → 7R3 + 26R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 79.
```
[  2   4  -1 | 11 ]
[  0   7  -1 |  6 ]
[  0   0   1 |  1 ]
```

**Sustitución hacia atrás:**

- Fila 3: `c = 1` → **c = 1**
- Fila 2: `7b - c = 6` → **b = 1**
- Fila 1: `2a + 4b - c = 11` → **a = 4**

**Solución:** a = 4, b = 1, c = 1

**Comprobación:** ✓ cumple las 3 ecuaciones originales

---

## Ejercicio 43 (Gauss)

- `-3a + 5b = 26`
- `-6a + 4b + c = 26`
- `3a + 5b + 3c = 8`

**Matriz aumentada:**
```
[ -3   5   0 | 26 ]
[ -6   4   1 | 26 ]
[  3   5   3 |  8 ]
```

1. **R2 → −3R2 + 6R1** (elimina la columna 1 en la fila 2). Se simplifica dividiendo la fila 2 entre 3.
```
[ -3   5   0 | 26 ]
[  0   6  -1 | 26 ]
[  3   5   3 |  8 ]
```

2. **R3 → −3R3 − 3R1** (elimina la columna 1 en la fila 3). Se simplifica dividiendo la fila 3 entre 3.
```
[  -3    5    0 |  26 ]
[   0    6   -1 |  26 ]
[   0  -10   -3 | -34 ]
```

3. **R3 → 6R3 + 10R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 28.
```
[ -3   5   0 | 26 ]
[  0   6  -1 | 26 ]
[  0   0  -1 |  2 ]
```

**Sustitución hacia atrás:**

- Fila 3: `-c = 2` → **c = -2**
- Fila 2: `6b - c = 26` → **b = 4**
- Fila 1: `-3a + 5b = 26` → **a = -2**

**Solución:** a = -2, b = 4, c = -2

**Comprobación:** ✓ cumple las 3 ecuaciones originales

---

## Ejercicio 44 (Gauss)

- `5a - 5b - c = -30`
- `5a - 6b - c = -29`
- `-5a + 4b - 4c = 6`

**Matriz aumentada:**
```
[   5   -5   -1 | -30 ]
[   5   -6   -1 | -29 ]
[  -5    4   -4 |   6 ]
```

1. **R2 → 5R2 − 5R1** (elimina la columna 1 en la fila 2). Se simplifica dividiendo la fila 2 entre 5.
```
[   5   -5   -1 | -30 ]
[   0   -1    0 |   1 ]
[  -5    4   -4 |   6 ]
```

2. **R3 → 5R3 + 5R1** (elimina la columna 1 en la fila 3). Se simplifica dividiendo la fila 3 entre 5.
```
[   5   -5   -1 | -30 ]
[   0   -1    0 |   1 ]
[   0   -1   -5 | -24 ]
```

3. **R3 → −R3 + R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 5.
```
[   5   -5   -1 | -30 ]
[   0   -1    0 |   1 ]
[   0    0    1 |   5 ]
```

**Sustitución hacia atrás:**

- Fila 3: `c = 5` → **c = 5**
- Fila 2: `-b = 1` → **b = -1**
- Fila 1: `5a - 5b - c = -30` → **a = -6**

**Solución:** a = -6, b = -1, c = 5

**Comprobación:** ✓ cumple las 3 ecuaciones originales

---

## Ejercicio 45 (Gauss-Jordan)

- `4r - 5s - t = -20`
- `-r + 2s + t = -1`
- `-r + s = -4`

**Matriz aumentada:**
```
[   4   -5   -1 | -20 ]
[  -1    2    1 |  -1 ]
[  -1    1    0 |  -4 ]
```

1. **R1 ↔ R2** (se intercambian filas para tener un pivote cómodo en la columna 1).
```
[  -1    2    1 |  -1 ]
[   4   -5   -1 | -20 ]
[  -1    1    0 |  -4 ]
```

2. **R2 → −R2 − 4R1** (elimina la columna 1 en la fila 2). Se simplifica dividiendo la fila 2 entre 3.
```
[ -1   2   1 | -1 ]
[  0  -1  -1 |  8 ]
[ -1   1   0 | -4 ]
```

3. **R3 → −R3 + R1** (elimina la columna 1 en la fila 3).
```
[ -1   2   1 | -1 ]
[  0  -1  -1 |  8 ]
[  0   1   1 |  3 ]
```

4. **R3 → −R3 − R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 11.
```
[ -1   2   1 | -1 ]
[  0  -1  -1 |  8 ]
[  0   0   0 | -1 ]
```

La fila `0 0 0 | -1` dice 0 = -1, imposible. **El sistema es inconsistente: no tiene solución.**

---

## Ejercicio 46 (Gauss-Jordan)

- `-5a - 5b + 5c = 10`
- `-6a - 2c = -16`
- `-6a + c = -19`

**Matriz aumentada:**
```
[  -5   -5    5 |  10 ]
[  -6    0   -2 | -16 ]
[  -6    0    1 | -19 ]
```

1. **R2 → −5R2 + 6R1** (elimina la columna 1 en la fila 2). Se simplifica dividiendo la fila 2 entre 10.
```
[  -5   -5    5 |  10 ]
[   0   -3    4 |  14 ]
[  -6    0    1 | -19 ]
```

2. **R3 → −5R3 + 6R1** (elimina la columna 1 en la fila 3). Se simplifica dividiendo la fila 3 entre 5.
```
[ -5  -5   5 | 10 ]
[  0  -3   4 | 14 ]
[  0  -6   5 | 31 ]
```

3. **R3 → −3R3 + 6R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 9.
```
[ -5  -5   5 | 10 ]
[  0  -3   4 | 14 ]
[  0   0   1 | -1 ]
```

4. **R1 → R1 − 5R3** (elimina la columna 3 en la fila 1). Se simplifica dividiendo la fila 1 entre 5.
```
[ -1  -1   0 |  3 ]
[  0  -3   4 | 14 ]
[  0   0   1 | -1 ]
```

5. **R2 → R2 − 4R3** (elimina la columna 3 en la fila 2). Se simplifica dividiendo la fila 2 entre 3.
```
[ -1  -1   0 |  3 ]
[  0  -1   0 |  6 ]
[  0   0   1 | -1 ]
```

6. **R1 → −R1 + R2** (elimina la columna 2 en la fila 1).
```
[  1   0   0 |  3 ]
[  0  -1   0 |  6 ]
[  0   0   1 | -1 ]
```

7. **R2 → (−1)R2** (convierte el pivote en 1).
```
[  1   0   0 |  3 ]
[  0   1   0 | -6 ]
[  0   0   1 | -1 ]
```

**Solución:** a = 3, b = -6, c = -1

**Comprobación:** ✓ cumple las 3 ecuaciones originales

---

## Ejercicio 47 (Gauss-Jordan)

- `-3b - 2c = -26`
- `a + 2c = 1`
- `2a - 3b + 2c = 3`

**Matriz aumentada:**
```
[   0   -3   -2 | -26 ]
[   1    0    2 |   1 ]
[   2   -3    2 |   3 ]
```

1. **R1 ↔ R2** (se intercambian filas para tener un pivote cómodo en la columna 1).
```
[   1    0    2 |   1 ]
[   0   -3   -2 | -26 ]
[   2   -3    2 |   3 ]
```

2. **R3 → R3 − 2R1** (elimina la columna 1 en la fila 3).
```
[   1    0    2 |   1 ]
[   0   -3   -2 | -26 ]
[   0   -3   -2 |   1 ]
```

3. **R3 → −3R3 + 3R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 81.
```
[   1    0    2 |   1 ]
[   0   -3   -2 | -26 ]
[   0    0    0 |  -1 ]
```

La fila `0 0 0 | -1` dice 0 = -1, imposible. **El sistema es inconsistente: no tiene solución.**

---

## Ejercicio 48 (Gauss-Jordan)

- `3r - t = 8`
- `-2r + s = -5`
- `-3r - 3s + 5t = -1`

**Matriz aumentada:**
```
[  3   0  -1 |  8 ]
[ -2   1   0 | -5 ]
[ -3  -3   5 | -1 ]
```

1. **R1 ↔ R2** (se intercambian filas para tener un pivote cómodo en la columna 1).
```
[ -2   1   0 | -5 ]
[  3   0  -1 |  8 ]
[ -3  -3   5 | -1 ]
```

2. **R2 → −2R2 − 3R1** (elimina la columna 1 en la fila 2).
```
[ -2   1   0 | -5 ]
[  0  -3   2 | -1 ]
[ -3  -3   5 | -1 ]
```

3. **R3 → −2R3 + 3R1** (elimina la columna 1 en la fila 3).
```
[  -2    1    0 |  -5 ]
[   0   -3    2 |  -1 ]
[   0    9  -10 | -13 ]
```

4. **R3 → −3R3 − 9R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 12.
```
[ -2   1   0 | -5 ]
[  0  -3   2 | -1 ]
[  0   0   1 |  4 ]
```

5. **R2 → R2 − 2R3** (elimina la columna 3 en la fila 2). Se simplifica dividiendo la fila 2 entre 3.
```
[ -2   1   0 | -5 ]
[  0  -1   0 | -3 ]
[  0   0   1 |  4 ]
```

6. **R1 → −R1 − R2** (elimina la columna 2 en la fila 1). Se simplifica dividiendo la fila 1 entre 2.
```
[  1   0   0 |  4 ]
[  0  -1   0 | -3 ]
[  0   0   1 |  4 ]
```

7. **R2 → (−1)R2** (convierte el pivote en 1).
```
[ 1  0  0 | 4 ]
[ 0  1  0 | 3 ]
[ 0  0  1 | 4 ]
```

**Solución:** r = 4, s = 3, t = 4

**Comprobación:** ✓ cumple las 3 ecuaciones originales

---
## Ejercicio 49 (Gauss-Jordan)

- `-6y + 3z = 15`
- `-3x - 6y = -6`
- `x - 6y + 4z = 22`

**Matriz aumentada:**
```
[  0  -6   3 | 15 ]
[ -3  -6   0 | -6 ]
[  1  -6   4 | 22 ]
```

1. **R1 ↔ R3** (se intercambian filas para tener un pivote cómodo en la columna 1).
```
[  1  -6   4 | 22 ]
[ -3  -6   0 | -6 ]
[  0  -6   3 | 15 ]
```

2. **R2 → R2 + 3·R1** (se elimina el −3 de la columna 1).
```
[  1  -6   4 | 22 ]
[  0 -24  12 | 60 ]
[  0  -6   3 | 15 ]
```

3. **R2 → R2 ÷ (−12)** y **R3 → R3 ÷ (−3)** (se simplifican las filas sin fracciones).
```
[  1  -6   4 | 22 ]
[  0   2  -1 | -5 ]
[  0   2  -1 | -5 ]
```

4. **R3 → R3 − R2** (la fila 3 queda en ceros).
```
[  1  -6   4 | 22 ]
[  0   2  -1 | -5 ]
[  0   0   0 |  0 ]
```

5. **R1 → R1 + 3·R2** (se elimina el −6 de la columna 2).
```
[  1   0   1 |  7 ]
[  0   2  -1 | -5 ]
[  0   0   0 |  0 ]
```

**Respuesta:** la última fila es `0 = 0`, así que hay **infinitas soluciones** (z es libre).

- `x + z = 7`
- `2y - z = -5`

Con `z = 2k + 1` (k entero): `x = 6 - 2k`, `y = k - 2`, `z = 2k + 1`
---

## Ejercicio 50 (Gauss-Jordan)

- `-3s = 3`
- `2r - 2s - 6t = -6`
- `5r + s + 4t = -21`

**Matriz aumentada:**
```
[   0   -3    0 |   3 ]
[   2   -2   -6 |  -6 ]
[   5    1    4 | -21 ]
```

1. **R1 ↔ R2** (se intercambian filas para tener un pivote cómodo en la columna 1).
```
[   2   -2   -6 |  -6 ]
[   0   -3    0 |   3 ]
[   5    1    4 | -21 ]
```

2. **R3 → 2R3 − 5R1** (elimina la columna 1 en la fila 3). Se simplifica dividiendo la fila 3 entre 2.
```
[  2  -2  -6 | -6 ]
[  0  -3   0 |  3 ]
[  0   6  19 | -6 ]
```

3. **R3 → −3R3 − 6R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 57.
```
[  2  -2  -6 | -6 ]
[  0  -3   0 |  3 ]
[  0   0  -1 |  0 ]
```

4. **R1 → −R1 + 6R3** (elimina la columna 3 en la fila 1). Se simplifica dividiendo la fila 1 entre 2.
```
[ -1   1   0 |  3 ]
[  0  -3   0 |  3 ]
[  0   0  -1 |  0 ]
```

5. **R1 → −3R1 − R2** (elimina la columna 2 en la fila 1). Se simplifica dividiendo la fila 1 entre 3.
```
[  1   0   0 | -4 ]
[  0  -3   0 |  3 ]
[  0   0  -1 |  0 ]
```

6. **R2 → (−1/3)R2** (convierte el pivote en 1).
```
[  1   0   0 | -4 ]
[  0   1   0 | -1 ]
[  0   0  -1 |  0 ]
```

7. **R3 → (−1)R3** (convierte el pivote en 1).
```
[  1   0   0 | -4 ]
[  0   1   0 | -1 ]
[  0   0   1 |  0 ]
```

**Solución:** r = -4, s = -1, t = 0

**Comprobación:** ✓ cumple las 3 ecuaciones originales

---

## Ejercicio 51 (Gauss-Jordan)

- `-5r + t = -16`
- `-2r + 2s + t = -7`
- `5r + 2s + 4t = 11`

**Matriz aumentada:**
```
[  -5    0    1 | -16 ]
[  -2    2    1 |  -7 ]
[   5    2    4 |  11 ]
```

1. **R1 ↔ R2** (se intercambian filas para tener un pivote cómodo en la columna 1).
```
[  -2    2    1 |  -7 ]
[  -5    0    1 | -16 ]
[   5    2    4 |  11 ]
```

2. **R2 → −2R2 + 5R1** (elimina la columna 1 en la fila 2).
```
[ -2   2   1 | -7 ]
[  0  10   3 | -3 ]
[  5   2   4 | 11 ]
```

3. **R3 → −2R3 − 5R1** (elimina la columna 1 en la fila 3).
```
[  -2    2    1 |  -7 ]
[   0   10    3 |  -3 ]
[   0  -14  -13 |  13 ]
```

4. **R3 → 10R3 + 14R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 88.
```
[ -2   2   1 | -7 ]
[  0  10   3 | -3 ]
[  0   0  -1 |  1 ]
```

5. **R1 → −R1 − R3** (elimina la columna 3 en la fila 1). Se simplifica dividiendo la fila 1 entre 2.
```
[  1  -1   0 |  3 ]
[  0  10   3 | -3 ]
[  0   0  -1 |  1 ]
```

6. **R2 → −R2 − 3R3** (elimina la columna 3 en la fila 2). Se simplifica dividiendo la fila 2 entre 10.
```
[  1  -1   0 |  3 ]
[  0  -1   0 |  0 ]
[  0   0  -1 |  1 ]
```

7. **R1 → −R1 + R2** (elimina la columna 2 en la fila 1).
```
[ -1   0   0 | -3 ]
[  0  -1   0 |  0 ]
[  0   0  -1 |  1 ]
```

8. **R1 → (−1)R1** (convierte el pivote en 1).
```
[  1   0   0 |  3 ]
[  0  -1   0 |  0 ]
[  0   0  -1 |  1 ]
```

9. **R2 → (−1)R2** (convierte el pivote en 1).
```
[  1   0   0 |  3 ]
[  0   1   0 |  0 ]
[  0   0  -1 |  1 ]
```

10. **R3 → (−1)R3** (convierte el pivote en 1).
```
[  1   0   0 |  3 ]
[  0   1   0 |  0 ]
[  0   0   1 | -1 ]
```

**Solución:** r = 3, s = 0, t = -1

**Comprobación:** ✓ cumple las 3 ecuaciones originales

---

## Ejercicio 52 (Gauss-Jordan)

- `x + y - 5z = 11`
- `-x - 2y - 3z = 7`
- `6x - 5y = 28`

**Matriz aumentada:**
```
[  1   1  -5 | 11 ]
[ -1  -2  -3 |  7 ]
[  6  -5   0 | 28 ]
```

1. **R2 → R2 + R1** (elimina la columna 1 en la fila 2).
```
[  1   1  -5 | 11 ]
[  0  -1  -8 | 18 ]
[  6  -5   0 | 28 ]
```

2. **R3 → R3 − 6R1** (elimina la columna 1 en la fila 3).
```
[   1    1   -5 |  11 ]
[   0   -1   -8 |  18 ]
[   0  -11   30 | -38 ]
```

3. **R3 → −R3 + 11R2** (elimina la columna 2 en la fila 3). Se simplifica dividiendo la fila 3 entre 118.
```
[  1   1  -5 | 11 ]
[  0  -1  -8 | 18 ]
[  0   0  -1 |  2 ]
```

4. **R1 → −R1 + 5R3** (elimina la columna 3 en la fila 1).
```
[ -1  -1   0 | -1 ]
[  0  -1  -8 | 18 ]
[  0   0  -1 |  2 ]
```

5. **R2 → −R2 + 8R3** (elimina la columna 3 en la fila 2).
```
[ -1  -1   0 | -1 ]
[  0   1   0 | -2 ]
[  0   0  -1 |  2 ]
```

6. **R1 → R1 + R2** (elimina la columna 2 en la fila 1).
```
[ -1   0   0 | -3 ]
[  0   1   0 | -2 ]
[  0   0  -1 |  2 ]
```

7. **R1 → (−1)R1** (convierte el pivote en 1).
```
[  1   0   0 |  3 ]
[  0   1   0 | -2 ]
[  0   0  -1 |  2 ]
```

8. **R3 → (−1)R3** (convierte el pivote en 1).
```
[  1   0   0 |  3 ]
[  0   1   0 | -2 ]
[  0   0   1 | -2 ]
```

**Solución:** x = 3, y = -2, z = -2

**Comprobación:** ✓ cumple las 3 ecuaciones originales

---
