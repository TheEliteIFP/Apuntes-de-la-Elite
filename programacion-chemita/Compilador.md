# ⚙️ Compilación y Números Aleatorios

## ⚙️ 1. Compilación de Programas

La **compilación** es el proceso de traducir instrucciones escritas en un lenguaje de alto nivel (C, C++, C#, Java) a un lenguaje ejecutable por el procesador (**lenguaje máquina**). El programa que realiza esta tarea es el **compilador** (por ejemplo, `cl.exe` de Microsoft en Visual Studio).

**Flujo de ejecución:**
`Código fuente` ➡️ `Compilador` ➡️ `Lenguaje máquina (.exe)` ➡️ `Procesador`

---

## 🔄 2. Lenguajes Compilados vs. Interpretados

### 🔹 Lenguaje Compilado
- Se traduce en su conjunto (**de golpe**).
- **Ejemplos:** C, C++, Rust, Go.
- **Características:** Más rápido y eficiente, pero más difícil de desarrollar/depurar.

### 🔹 Lenguaje Interpretado
- Se traduce e interpreta **línea a línea** durante la ejecución.
- **Ejemplos:** Python, JavaScript, PHP.
- **Características:** Más lento en ejecución, pero más fácil de programar.

---

## 🐞 3. Modos de Compilación

### 1. Modo Depuración (`Debug`)
- Produce un código **no optimizado**.
- Incluye información extra sobre el código fuente original (nombres de variables, números de línea, archivo `.pdb` en Windows).
- **Objetivo:** Facilita la detección y corrección de errores.

### 2. Modo Publicación (`Release`)
- Produce un código totalmente **optimizado**.
- Simplifica instrucciones redundantes y reordena el código.
- No incluye datos extra para reducir el tamaño y lograr el máximo rendimiento.

---

## 🎲 4. Números Aleatorios

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

