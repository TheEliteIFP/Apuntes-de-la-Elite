# Operadores Booleanos

## Álgebra
Se pueden definir unas matemáticas que solo tengan 2 valores: **Falso** y **Cierto**.
Por ejemplo: operaciones aritméticas como $3 + 4 * 1251$.

---

## Operador Y (AND)
* **Ejemplo:** "Hace sol y tengo menos de mil euros" $\rightarrow$ `dinero < 1000`.
* **Tabla de la Y:**
  * `True ^ True = True`.
  * `False ^ False = False`.
  * `False ^ True = False`.
  * `True ^ False = False`.

---

## Operador O (OR)
* **Ejemplo:** `Sol v dinero < 1000`.
* **Tabla de la O:**
  * `True v False = True`
  * `False v False = False`
  * `True v True = True`
  * `False v True = True`

---

## Traducción a C
* `&&` $\rightarrow$ And en C
* `||` $\rightarrow$ Or en C
* `!` $\rightarrow$ Not en C

---

## Ejemplos Prácticos

### Ejemplo 1
* **Enunciado:** Estamos por la mañana y o bien hay más de 30 alumnos en clase o hoy es viernes y mañana hay examen.
* **Expresión:** `manana && (Alumnos > 30 || viernes && examen)`
* **Valores y evaluación:**
  * `manana` $\rightarrow$ True
  * `Alumnos` $\rightarrow$ False
  * `Viernes` $\rightarrow$ True
  * `Examen` $\rightarrow$ False
  * **Final:** False

### Ejemplo 2
* **Enunciado:** El asesino usa sombrero y llegó antes de las 10 AM o no llegó antes de las 8 AM y llevaba gabardina.
* **Expresión:** `Sombrero && hora < 10 || ! (hora < 8 && Gabardina)`
* **Valores y evaluación:**
  * `Sombrero` $\rightarrow$ T
  * `hora` $\rightarrow$ 9
  * `Gabardina` $\rightarrow$ F
  * **Resultado:** True

---

## Prioridades de Operadores
1. `()`
2. `- (unario) / +-`
3. `* / %`
4. `!= < > <= >= ==`
5. `!`
6. `&&`[cite: 2]
7. `||`[cite: 2]
