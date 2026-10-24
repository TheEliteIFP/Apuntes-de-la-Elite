# Operadores Booleanos

## Álgebra
Se pueden definir unas matemáticas que solo tengan 2 valores: **Falso** y **Cierto**[cite: 1].
Por ejemplo: operaciones aritméticas como $3 + 4 * 1251$[cite: 1].

---

## Operador Y (AND)
* **Ejemplo:** "Hace sol y tengo menos de mil euros" $\rightarrow$ `dinero < 1000`[cite: 1].
* **Tabla de la Y:**
  * `True ^ True = True`[cite: 1]
  * `False ^ False = False`[cite: 1]
  * `False ^ True = False`[cite: 1]
  * `True ^ False = False`[cite: 1]

---

## Operador O (OR)
* **Ejemplo:** `Sol v dinero < 1000`[cite: 1].
* **Tabla de la O:**
  * `True v False = True`[cite: 1]
  * `False v False = False`[cite: 1]
  * `True v True = True`[cite: 1]
  * `False v True = True`[cite: 1]

---

## Traducción a C
* `&&` $\rightarrow$ And en C[cite: 1]
* `||` $\rightarrow$ Or en C[cite: 1]
* `!` $\rightarrow$ Not en C[cite: 1]

---

## Ejemplos Prácticos

### Ejemplo 1
* **Enunciado:** Estamos por la mañana y o bien hay más de 30 alumnos en clase o hoy es viernes y mañana hay examen[cite: 2].
* **Expresión:** `manana && (Alumnos > 30 || viernes && examen)`[cite: 2]
* **Valores y evaluación:**
  * `manana` $\rightarrow$ True[cite: 2]
  * `Alumnos` $\rightarrow$ False[cite: 2]
  * `Viernes` $\rightarrow$ True[cite: 2]
  * `Examen` $\rightarrow$ False[cite: 2]
  * **Final:** False[cite: 2]

### Ejemplo 2
* **Enunciado:** El asesino usa sombrero y llegó antes de las 10 AM o no llegó antes de las 8 AM y llevaba gabardina[cite: 2].
* **Expresión:** `Sombrero && hora < 10 || ! (hora < 8 && Gabardina)`[cite: 2]
* **Valores y evaluación:**
  * `Sombrero` $\rightarrow$ T[cite: 2]
  * `hora` $\rightarrow$ 9[cite: 2]
  * `Gabardina` $\rightarrow$ F[cite: 2]
  * **Resultado:** True[cite: 2]

---

## Prioridades de Operadores
1. `()`[cite: 2]
2. `- (unario) / +-`[cite: 2]
3. `* / %`[cite: 2]
4. `!= < > <= >= ==`[cite: 2]
5. `!`[cite: 2]
6. `&&`[cite: 2]
7. `||`[cite: 2]
