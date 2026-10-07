# 🗄️ Bases de Datos - Unidad 0: ¿Qué es un SGBD?

---

## 1. Base de Datos vs SGBD
* **Base de Datos:** La biblioteca. Los datos en sí, ya organizados[cite: 32].
* **SGBD (Sistema de Gestión de Bases de Datos):** El bibliotecario. El programa que la guarda, busca, protege y decide quién entra[cite: 32].
> *Nota:* Lo que **no** hace un SGBD es la interfaz gráfica de la aplicación (eso lo programa quien hace la app)[cite: 32].
* **Sus 7 funciones principales:** Definición, Manipulación, Recuperación, Control de acceso, Integridad, Concurrencia y Seguridad[cite: 32].
* **Ejemplos:** Oracle (el más usado en banca/empresa grande), MySQL, PostgreSQL, SQL Server, MongoDB[cite: 32].

---

## 2. Tipos de Bases de Datos

### 🏛️ Modelos Clásicos e Históricos
* **Jerárquico (IMS, años 60-70):** Árbol de un padre y varios hijos. Rígido, hoy casi no se usa[cite: 32].
* **En Red (CODASYL, años 70):** Como el jerárquico pero un dato puede tener varios padres mediante punteros. Muy complejo de programar a mano[cite: 33].
* **Relacional (Codd, 1970 - Oracle):** Tablas con filas y columnas relacionadas por un valor compartido. Separaba el "qué quieres" del "cómo está guardado". Es la estrella del curso[cite: 33].
* **Orientado a Objetos (años 90):** Guarda objetos directamente sin traducirlos a tablas[cite: 33].
* **Objeto-relacional (Oracle, PostgreSQL):** Relacional pero admite tipos complejos (listas, objetos) dentro de tablas. Lo que usa Oracle por debajo[cite: 33].

### 🚀 Las Familias NoSQL
* **Clave-Valor (Redis):** Acceso directo por etiqueta sin buscar. Extremadamente rápida (para sesiones de usuario o carritos de compra)[cite: 33].
* **Documental (MongoDB):** Cada registro es un documento independiente con campos distintos (para catálogos o datos sin forma fija)[cite: 33].
* **Columnar (Cassandra):** Datos agrupados por columna. Ideal para análisis masivo de series temporales o sensores[cite: 33].
* **Grafo (Neo4j):** Centrada en guardar relaciones (redes sociales, recomendaciones de compras)[cite: 33].

---

## 🌍 3. Tipos según dónde viven
* **Centralizada:** Todo en un único servidor (sencilla, pero si cae, cae todo)[cite: 33].
* **Distribuida:** Datos repartidos entre varios equipos en red, pero se ve como una sola[cite: 33].
* **Paralela:** Varios procesadores trabajando a la vez sobre los mismos datos en un único sistema (ej. *Oracle RAC*)[cite: 34].
* **En la nube (DBaaS):** Gestionada por un proveedor externo; crece y decrece según haga falta[cite: 34].
* **Embebida:** Vive dentro de la app, sin red ni servidor (ej. *SQLite* en móviles)[cite: 34].

---

## 🔗 4. Relación por valor
Las tablas se relacionan porque una columna de una tabla repite exactamente el mismo valor que la clave de otra (ej. el número de departamento `30`). **No usan flechas físicas**, solo la coincidencia del dato[cite: 34].

---

## ⚙️ 5. Cuatro familias de órdenes SQL
* **DDL (Construir):** `CREATE`, `ALTER`, `DROP`[cite: 34].
* **DML (Usar los datos):** `SELECT`, `INSERT`, `UPDATE` (la que más usaremos)[cite: 34].
* **DCL (Dar permisos):** `GRANT`, `REVOKE`[cite: 34].
* **TCL (Confirmar / Deshacer):** `COMMIT`, `ROLLBACK`[cite: 34].

---

## 🏗️ 6. Organización interna de un SGBD
* **Nivel externo:** Lo que ve cada usuario (vistas personalizadas)[cite: 35].
* **Nivel conceptual:** El diseño global con todas las tablas y relaciones[cite: 35].
* **Nivel interno:** Cómo se almacena físicamente en el disco[cite: 35].

> *Piezas clave por dentro:*
> * **Diccionario de datos:** Metadatos (el SGBD consultándose a sí mismo)[cite: 35].
> * **Optimizador:** Elige el mejor camino para ejecutar tu consulta[cite: 35].
> * **Gestor de memoria intermedia:** Mantiene los datos frecuentes en RAM para evitar accesos lentos al disco[cite: 35].
> * **Diario de transacciones:** Anota cambios previos (permite hacer `ROLLBACK` y salva los datos ante un apagón)[cite: 35].

---
[⬅️ Volver al Índice](./00-indice.md)
