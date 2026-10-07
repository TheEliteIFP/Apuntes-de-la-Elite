# ⚡ Resumen Exprés: Bases de Datos (Unidad 0 - Sesión 1)

## 📁 1. Organización de Ficheros
* **Secuencial:** Se busca del principio al final, registro a registro[cite: 16]. Ideal para leerlo todo de golpe (como una nómina), pero muy lento para buscar un dato suelto[cite: 16].
* **Indexada:** Se consulta un índice que indica la posición exacta[cite: 16]. Búsqueda rápida y ordenada, aunque el índice ocupa espacio y hay que actualizarlo en cada alta/baja[cite: 16].
* **Directa (Hash):** Una función calcula la posición a partir de la clave[cite: 16]. Es la más rápida para un registro concreto, pero no sirve para leer en orden ni por rangos y sufre colisiones[cite: 16].

---

## ⚠️ 2. Los 7 Problemas de los Sistemas de Ficheros (Caso Gimnasio Atlas)
1. **Redundancia:** El mismo dato repetido sin necesidad (ej. el teléfono de Marta en 4 filas)[cite: 17].
2. **Inconsistencia:** Copias del mismo dato que no coinciden (ej. teléfonos distintos en esas filas)[cite: 17].
3. **Anomalía de Inserción:** No puedes guardar un dato porque falta otro obligatorio no relacionado (ej. no dar de alta una actividad sin socios)[cite: 17].
4. **Anomalía de Borrado:** Al borrar una fila pierdes info extra sin querer (ej. si se va el último socio de una clase, se borra el horario y monitor)[cite: 17].
5. **Anomalía de Modificación:** Un cambio obliga a editar mil filas (ej. cambiar la hora de una clase socio por socio)[cite: 17].
6. **Dependencia Física:** Si cambia el formato del fichero, rompes los programas y macros[cite: 17].
7. **Concurrencia:** Dos personas abren el fichero a la vez y una pisa el trabajo de la otra[cite: 17].

---

## 💡 3. Base de Datos vs SGBD
* **Base de Datos:** El conjunto de datos relacionados y estructurados (los datos en sí)[cite: 18].
* **SGBD:** El software que gestiona, protege y da acceso a esos datos (el programa, ej. Oracle, MySQL)[cite: 18].
> *Frase clave:* **Una base de datos son los datos; un SGBD es el programa que los gestiona[cite: 18].**

---

## 📖 4. Vocabulario Clave
* **Tabla:** Colección de datos sobre un mismo tipo de cosa[cite: 19].
* **Fila / Tupla / Registro:** Un elemento concreto[cite: 19].
* **Columna / Campo / Atributo:** Una característica guardada de todos[cite: 19].
* **Clave Primaria:** Columna que identifica cada fila de forma única y sin repetirse[cite: 19].
* **Clave Foránea:** Columna que apunta a la clave primaria de otra tabla[cite: 19].

---
