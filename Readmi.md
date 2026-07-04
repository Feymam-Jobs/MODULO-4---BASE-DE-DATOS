# PROYECTO
# 🏥 Hospital Vida Sana - Diseño Conceptual y Lógico de la Base de Datos

## 📋 Descripción del Proyecto

Este proyecto corresponde al diseño conceptual y lógico de una base de datos relacional para el **Hospital Vida Sana**, cuyo propósito es gestionar la información de pacientes, médicos, citas y diagnósticos de manera organizada, consistente y libre de redundancias.

El desarrollo se realizó siguiendo las buenas prácticas del modelado de bases de datos, aplicando un **Diagrama Entidad-Relación (DER)**, su correspondiente **Modelo Relacional** y la **normalización hasta la Tercera Forma Normal (3FN)**.

> **Nota:** Este proyecto únicamente contempla el diseño de la base de datos. No incluye scripts SQL, carga de datos ni desarrollo de interfaces gráficas.

---

# 🎯 Objetivo

Diseñar una base de datos relacional que permita administrar la información del Hospital Vida Sana, garantizando:

- Integridad de los datos.
- Consistencia de la información.
- Eliminación de redundancias.
- Correcta implementación de claves primarias y foráneas.
- Normalización hasta la Tercera Forma Normal (3FN).

---

# 📌 Alcance del Proyecto

El sistema permite gestionar la siguiente información:

- Registro de pacientes.
- Registro de médicos.
- Gestión de citas médicas.
- Registro de diagnósticos médicos.

---

# 🗂️ Entidades del Sistema

## Paciente

Almacena la información personal de los pacientes.

**Atributos**

- id_paciente (PK)
- nombres
- apellidos
- fecha_nacimiento
- sexo
- telefono
- direccion

---

## Médico

Contiene la información de los profesionales de la salud.

**Atributos**

- id_medico (PK)
- nombres
- apellidos
- especialidad
- telefono
- correo

---

## Cita

Representa las consultas médicas programadas.

**Atributos**

- id_cita (PK)
- fecha
- hora
- estado
- motivo_consulta
- id_paciente (FK)
- id_medico (FK)

---

## Diagnóstico

Almacena el resultado de la atención médica realizada durante una cita.

**Atributos**

- id_diagnostico (PK)
- descripcion
- tratamiento
- observaciones
- id_cita (FK - UNIQUE)

---

# 🔗 Relaciones

Las relaciones entre las entidades son las siguientes:

- Un **Paciente** puede tener muchas **Citas** (1:N).
- Un **Médico** puede atender muchas **Citas** (1:N).
- Una **Cita** genera un único **Diagnóstico** (1:1).

---

# 🗃️ Modelo Relacional

```text
PACIENTE
---------
id_paciente (PK)
nombres
apellidos
fecha_nacimiento
sexo
telefono
direccion


MEDICO
---------
id_medico (PK)
nombres
apellidos
especialidad
telefono
correo


CITA
---------
id_cita (PK)
fecha
hora
estado
motivo_consulta
id_paciente (FK)
id_medico (FK)


DIAGNOSTICO
---------
id_diagnostico (PK)
descripcion
tratamiento
observaciones
id_cita (FK - UNIQUE)
```

---

# ✅ Normalización

## Primera Forma Normal (1FN)

- Todos los atributos contienen valores atómicos.
- No existen grupos repetitivos.
- Cada campo almacena un único valor.

---

## Segunda Forma Normal (2FN)

- Todas las tablas poseen una clave primaria.
- No existen dependencias parciales.
- Cada atributo depende completamente de su clave primaria.

---

## Tercera Forma Normal (3FN)

- No existen dependencias transitivas.
- Cada atributo depende únicamente de la clave primaria de su propia tabla.
- Se elimina la duplicidad de información.

---

# 📂 Archivos del Proyecto

El proyecto está conformado por los siguientes archivos:

- **DER.pdf** → Diagrama Entidad-Relación.
- **ModeloRelacional.pdf** → Modelo Relacional.
- **Hospital_Vida_Sana_DER_ModeloRelacional.drawio** → Archivo editable en Draw.io.
- **README.md** → Documentación del proyecto.

---

# 🛠️ Herramientas Utilizadas

- Draw.io (Diagrams.net)
- Modelo Entidad-Relación (DER)
- Modelo Relacional
- Normalización (1FN, 2FN y 3FN)

---

# ✔️ Cumplimiento de los Criterios de Aceptación

- Se diseñó un Diagrama Entidad-Relación (DER) con entidades, atributos, claves primarias y claves foráneas.
- Se construyó un Modelo Relacional equivalente al DER.
- Se definieron los tipos de datos de cada atributo.
- Se aplicó la normalización hasta la Tercera Forma Normal (3FN).
- Se verificó la correspondencia entre el modelo conceptual y el modelo lógico.

---

# 👨‍💻 Autor

**Isaias Cañate**

Proyecto académico  
**Diseño Conceptual y Lógico de Bases de Datos**  
Hospital **"Vida Sana"**