# ⚙️ Bloque 1: Programación Estructurada, Compilación y Números Aleatorios

Evolución histórica de los paradigmas de programación:
**Ensamblador** ➡️ **Programación estructurada** ➡️ **Programación orientada a objetos**

---

## 🛠️ 1. Ensamblador (Años 60)
- **Poco expresivo:** Tienes que escribir mucho código para crear una función sencilla.
- **Difícil de interpretar:** Cuesta identificar abstracciones fácilmente.
- **Muy flexible:** Permite múltiples formas de implementar bucles o condicionales.
- **Ventajas principales:** Control absoluto del hardware y alta eficiencia.

---

## 💻 2. Programación Estructurada (Años 70 - "C")
- **Uso de expresiones:** `(a * 2 + 2 * (1 - b))` o `3 + 5 * 2 - (edad / 2)`.
- **Asignación de valores:** `x = 3 + 5;`
- **Declaración de variables:** `int edad;` (el tipo de variable determina cuánto ocupa en memoria, cuál es su naturaleza —número, carácter, etc.— y cómo se codifica).
  - **Ejemplo `int`:**
    1. Ocupa **4 bytes** en memoria.
    2. Guarda datos de tipo entero.
    3. Su codificación suele ser en **complemento a 2**.
- **Estructuras de control:** `if`, `else`, `while`.
- **Operador de desigualdad (`!=`):** El símbolo `!` significa **diferente de**.

---

## 📂 3. Ejemplos de Código en Programación Estructurada

### 🔹 Condicionales y Bucles Básicos

**Ejemplo de Condicional (`if` / `else`)**
```c
int edad = 16;
int pedirtel;

if (edad < 18) {
    pedirtel = 1;
} else {
    pedirtel = 0;
}
```

**Ejemplo de Bucle (`while`) - Cálculo de Ahorro**
```c
int meses = 4;
int ahorro = 200;
int total = 0;

while (meses > 0) {
    total = total + ahorro;
    meses = meses - 1;
}
```

**Ejemplo de Bucle (`while`) - Sistema de Combate Simple**
```c
int gana = 0;
int vidaj = 100;
int vidae = 50;
int ataquej = 10;
int ataquee = 25;
int numataques = 4;

while (numataques > 0) {
    vidaj = vidaj - ataquee;
    vidae = vidae - ataquej;
    numataques = numataques - 1;
}

if (vidaj > 0) {
    gana = 1;
} else {
    gana = 0;
}
```

**Ejemplo de Bucle (`while`) - Adivinar Número Secreto**
```c
while (secreto != propuesta) {
    if (secreto > propuesta) {
        propuesta = propuesta + 1;
    } else {
        propuesta = propuesta - 1;
    }
}
```

---

## ⚙️ 4. Compilación de Programas

La **compilación** es el proceso de traducir instrucciones escritas en un lenguaje de alto nivel (C, C++, C#, Java) a un lenguaje ejecutable por el procesador (**lenguaje máquina**). El programa que realiza esta tarea es el **compilador** (por ejemplo, `cl.exe` de Microsoft en Visual Studio).

**Flujo de ejecución:**
`Código fuente` ➡️ `Compilador` ➡️ `Lenguaje máquina (.exe)` ➡️ `Procesador`

---

## 🔄 5. Lenguajes Compilados vs. Interpretados

### 🔹 Lenguaje Compilado
- Se traduce en su conjunto (**de golpe**).
- **Ejemplos:** C, C++, Rust, Go.
- **Características:** Más rápido y eficiente, pero más difícil de desarrollar/depurar.

### 🔹 Lenguaje Interpretado
- Se traduce e interpreta **línea a línea** durante la ejecución.
- **Ejemplos:** Python, JavaScript, PHP.
- **Características:** Más lento en ejecución, pero más fácil de programar.

---

## 🐞 6. Modos de Compilación

### 1. Modo Depuración (`Debug`)
- Produce un código **no optimizado**.
- Incluye información extra sobre el código fuente original (nombres de variables, números de línea, archivo `.pdb` en Windows).
- **Objetivo:** Facilita la detección y corrección de errores.

### 2. Modo Publicación (`Release`)
- Produce un código totalmente **optimizado**.
- Simplifica instrucciones redundantes y reordena el código.
- No incluye datos extra para reducir el tamaño y lograr el máximo rendimiento.

---

## 🎲 7. Números Aleatorios

Mecanismo para generar secuencias de números al azar. Útil para lanzar dados o simular condiciones cambiantes (como el clima en videojuegos).

- **Números Pseudoaleatorios (`rand()`):**
  - Genera un entero positivo al azar: `x = rand();`.
  - Si se vuelve a ejecutar el programa, la secuencia siempre es idéntica.
- **Uso de Semilla (`srand()`):**
  - Permite cambiar la secuencia inicializando el generador: `srand(2152);`.
- **Imprevisibilidad Total (`time()`):**
  - Para lograr imprevisto total en cada ejecución, se usa como semilla el tiempo actual en segundos o milisegundos:
  ```c
  t = time(NULL);
  srand(t);
  ```

---

## 📝 8. Código de generación de números "randoms"

```cpp
#include <iostream>
#include <cstdlib> // Para rand() y srand()
#include <ctime>   // Para time()

int main() {
    // --- 1. Programación Estructurada Básica ---
    int edad = 16;
    int pedirtel;

    if (edad < 18) {
        pedirtel = 1;
    } else {
        pedirtel = 0;
    }

    std::cout << "Resultado condicional (pedirtel): " << pedirtel << std::endl;

    // --- 2. Bucle de Ahorro ---
    int meses = 4;
    int ahorro = 200;
    int total = 0;

    while (meses > 0) {
        total = total + ahorro;
        meses = meses - 1;
    }

    std::cout << "Ahorro total tras 4 meses: " << total << std::endl;

    // --- 3. Generación de Números Aleatorios con Semilla de Tiempo ---
    time_t t = time(NULL);
    srand(t);

    int numero_azar = rand();
    int dado = (rand() % 6) + 1; // Rango de 1 a 6

    std::cout << "Semilla (tiempo actual): " << t << std::endl;
    std::cout << "Numero aleatorio generado: " << numero_azar << std::endl;
    std::cout << "Tirada de dado (1-6): " << dado << std::endl;

    return 0;
}
```
