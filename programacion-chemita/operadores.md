# Conceptos Básicos de Programación

Este repositorio recopila apuntes y conceptos fundamentales de programación, incluyendo sistemas numéricos, operadores y prioridades.

---

## Sistemas Numéricos
* **Binarios:** $0 + 0$
* **Unarios:** $\rightarrow -0$

---

## Operadores
Los operadores aparecen en expresiones y se dividen en diferentes categorías:

### Instrucciones de Asignación y Control
* `$X = 0;$`: Instrucción de asignación.
* `if (0)`
* `while (0)`

### Operadores de Comparación
* `<`: Mayor que
* `>`: Menor que
* `=<`: Igual o mayor que
* `=>`: Igual o menos que
* `==`: Comparación de igualdad (se utiliza exclusivamente para verificar un valor exacto).
* `!=`: Distinto de

### Operadores Aritméticos
* **Suma:** `+`
* **Resta:** `-`
* **División:** `/` *(Nota: La división puede ser real para números `int` o entera para números `float`)*
* **Multiplicación:** `*`
* **Operador Módulo (Exclusivo de Programación):** `%`
  * Da como resultado el **resto** de una división entera.

#### Estructura de la División
Basado en el esquema de división:

```text
  A  | B
-----|---
  R  | C
```

* **$A$:** Número a dividir (dividendo)
* **$B$:** Número entre el que divides (divisor)
* **$C$:** Total de la división (cociente)
* **$R$:** Resto de la división (Resultado de la operación módulo `%`)

---

## Prioridad de Operadores (Precedencia)
Orden de evaluación de los operadores de mayor a menor prioridad:

1. Parentésis: `()`
2. Unarios
3. Multiplicación, División y Módulo: `* / %`
4. Suma y Resta: `+ -`
5. Comparaciones de igualdad/desigualdad: `== !=`
