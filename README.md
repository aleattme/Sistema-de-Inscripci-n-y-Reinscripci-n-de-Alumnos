# Sistema de Inscripción y Reinscripción de Alumnos

## Integrantes

* Alejandro Attme
* Andres Carisimo


**Versión:** 1.0
**Materia:** Práctica Profesionalizante II
**Docente:** Pablo Pedernera
**Fecha:** 03 / 06 / 2026

---

# 1. Descripción del sistema y contexto real

La Escuela Superior N.º 49 realiza anualmente procesos de inscripción para ingresantes y reinscripción para alumnos de segundo y tercer año.

Actualmente gran parte del proceso requiere intervención manual, generando problemas como:

* Errores en la carga de datos.
* Duplicación de información.
* Confusión en la selección de materias.
* Problemas con alumnos recursantes.
* Dificultades en la comunicación entre alumnos y Bedelía.

El objetivo del proyecto es desarrollar una aplicación web que permita automatizar y centralizar el proceso de inscripción y reinscripción, mejorando la experiencia de los alumnos y optimizando el trabajo administrativo.

---

# 2. Identificación de Stakeholders

## Stakeholders Primarios

### Alumnos

Utilizan el sistema para realizar inscripciones y reinscripciones.

### Personal de Bedelía

Gestiona, valida y supervisa la información académica.

### Equipo Directivo

Recibe reportes y estadísticas para la toma de decisiones.

## Stakeholders Secundarios

### Docentes

Acceden indirectamente a información actualizada de alumnos.

### Equipo de Desarrollo

Diseña, implementa y mantiene el sistema.

### Institución Educativa

Obtiene mejoras organizativas y administrativas.

---

# 3. Requisitos Funcionales y No Funcionales

## Requisitos Funcionales

RF01: Permitir acceso web al sistema.

RF02: Identificar alumnos mediante DNI.

RF03: Determinar si el alumno es ingresante o reinscripto.

RF04: Permitir seleccionar una carrera para alumnos nuevos.

RF05: Reconocer automáticamente la carrera de alumnos existentes.

RF06: Mostrar materias habilitadas según correlatividades.

RF07: Deshabilitar materias aprobadas.

RF08: Guardar la información en la base de datos.

RF09: Enviar correo de confirmación al alumno.

RF10: Enviar reportes diarios al equipo directivo.

RF11: Controlar fechas de apertura y cierre de inscripción.

---

## Requisitos No Funcionales

RNF01: Disponibilidad 24/7 durante el período de inscripción.

RNF02: Interfaz responsiva para dispositivos móviles.

RNF03: Seguridad y protección de datos personales.

RNF04: Tiempo de respuesta menor a 3 segundos.

RNF05: Escalabilidad para futuras ampliaciones.

RNF06: Compatibilidad con navegadores modernos.

---

# 4. Historias de Usuario

## HU01

Como alumno ingresante

Quiero seleccionar una carrera

Para realizar mi inscripción correctamente.

---

## HU02

Como alumno reinscripto

Quiero visualizar únicamente las materias habilitadas

Para evitar errores en la inscripción.

---

## HU03

Como personal de Bedelía

Quiero acceder a la información de los alumnos

Para gestionar correctamente las inscripciones.

---

## HU04

Como directivo

Quiero recibir reportes automáticos

Para monitorear la cantidad de inscriptos.

---

# 5. Casos de Uso

## CU01 - Inscripción de Alumno Nuevo

Actor: Alumno

Flujo principal:

1. Ingresa al sistema.
2. Introduce DNI.
3. El sistema verifica que no exista.
4. Selecciona carrera.
5. Selecciona materias.
6. Confirma inscripción.
7. El sistema guarda los datos.
8. Se envía correo de confirmación.

---

## CU02 - Reinscripción

Actor: Alumno

Flujo principal:

1. Ingresa DNI.
2. El sistema identifica al alumno.
3. Muestra materias disponibles.
4. El alumno selecciona materias.
5. Confirma reinscripción.
6. El sistema registra la información.

---

# 6. Modelo Entidad Relación

## Entidades principales

### Alumno

* id_alumno
* dni
* nombre
* apellido
* email

### Carrera

* id_carrera
* nombre

### Materia

* id_materia
* nombre
* año

### Inscripción

* id_inscripcion
* fecha
* estado

---

## Relaciones

Alumno 1:N Inscripción

Carrera 1:N Alumno

Carrera 1:N Materia

Inscripción N:M Materia

---

# 7. Referencias y Fuentes

* Documento de requerimientos institucionales.
* Entrevista realizada al personal de Bedelía.
* Relevamiento interno de la Escuela Superior N.º 49.
* Material de Ingeniería Web y Análisis Funcional.
* Ley N.º 25.326 de Protección de Datos Personales.
