# 🗄️ Bases de Datos - Unidad 0: BBDD Distribuidas, Protección de Datos y Big Data

---

## 1. Bases de Datos Distribuidas
* **Problema:** Si todo está en un servidor central, si se cae la conexión, esa sede no puede trabajar. Si cada sede tiene sus datos sueltos, nadie sabe el total de la empresa.
* **Solución:** Los datos están repartidos entre varios servidores, pero quien los usa los ve como si fuera una sola base de datos.
* **Transparencia:** El usuario no tiene que saber dónde está cada dato, ni si está repetido, ni cómo está partido (a mayor transparencia, más fácil de usar y más difícil de construir por dentro).

---

## 2. Fragmentación vs Replicación

### 🧩 Fragmentar (Repartir)
* **Horizontal:** Por filas. Cada sede se queda con las suyas. Se recompone con `UNION`.
* **Vertical:** Por columnas. Los datos sensibles se separan del resto. Se recompone con `JOIN` por la clave.
* **Mixta:** Ambas cosas a la vez.
* **Derivada:** Sigue la fragmentación de otra tabla relacionada (ej. los pedidos van donde esté su cliente).
> **Reglas:** Completitud (ningún dato queda fuera), Reconstrucción (debe poder montarse la original repitiendo la clave primaria) y Disyunción (un dato no debe estar en dos fragmentos a la vez, salvo la clave).

### 📑 Replicar (Copiar)
* No es repartir, es **copiar la misma tabla entera** en varios sitios. Se replica lo pequeño que consultan todos (ej. un catálogo de productos) y se fragmenta lo grande que usa cada sede por separado (ej. clientes o pedidos).

---

## 3. Protección de Datos (Ley y Normativa)

### 📜 Las Tres Normas Principales
* **RGPD:** Reglamento (UE) 2016/679 (marco europeo desde el 25 de mayo de 2018).
* **LOPDGDD:** Ley Orgánica 3/2018 (adapta el RGPD a España).
* **LSSI-CE:** Ley 34/2002 (comercio electrónico y cookies).

### 👥 Vocabulario Clave
* **Interesado:** La persona a quien se refieren los datos (cliente, empleado).
* **Responsable del tratamiento:** Quien decide para qué se usan (la empresa titular).
* **Encargado del tratamiento:** Quien trata los datos por cuenta del responsable (gestoría externa).
* **AEPD / DPD:** Autoridad de control española / Delegado de protección de datos (obligatorio solo en algunas organizaciones).

### ⏱️ Tres Cifras Clave para el Examen
* **72 horas:** Plazo máximo para notificar una brecha de seguridad.
* **1 mes:** Plazo máximo para responder a un derecho (acceso, rectificación, supresión...).
* **20 millones de € o 4% de la facturación mundial:** Sanciones máximas.

---

## 📊 4. Big Data (Las 6 V's)
Cuando los datos son demasiados para mirarlos a mano, se analizan bajo seis dimensiones:
1. **Volumen:** Cantidad masiva de datos.
2. **Velocidad:** A qué ritmo llegan.
3. **Variedad:** Formatos distintos.
4. **Valor:** Qué decisión permite tomar.
5. **Veracidad:** Fiabilidad de la información.

### 🔄 La Cadena de Inteligencia de Negocio
`Fuentes` ➡️ `ETL` ➡️ `Almacén de datos` ➡️ `OLAP` ➡️ `Cuadros de mando`

---
[⬅️ Volver al Índice](./00-indice.md)
