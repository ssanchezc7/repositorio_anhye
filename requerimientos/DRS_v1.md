# DRS_v1 - Sistema de Gestión de Biblioteca

## 1. Introducción
Versión inicial de requerimientos para el Sistema de Gestión de Biblioteca.

## 2. Alcance
- Registro y gestión de libros.
- Registro y gestión de usuarios (estudiantes, profesores, personal).
- Préstamos y devoluciones con control de fechas.
- Búsqueda y filtrado de catálogo.

## 3. Requerimientos funcionales (v1)
- RF1: El sistema permitirá registrar nuevos libros con: ISBN, título, autor(es), editorial, año, categoría, copias.
- RF2: El sistema permitirá registrar usuarios con: ID, nombre completo, correo electrónico, tipo de usuario.
- RF3: El sistema permitirá realizar préstamos registrando libro, usuario, fecha préstamo y fecha prevista de devolución.
- RF4: El sistema permitirá registrar devoluciones y calcular multas si aplica.
- RF5: El sistema ofrecerá búsqueda por título, autor, ISBN y categoría.

## 4. Requerimientos no funcionales (v1)
- RNF1: La interfaz será accesible por navegador web moderno (Chrome, Edge, Firefox).
- RNF2: Tiempo de respuesta < 3s para búsquedas en catálogo de hasta 10k registros.
- RNF3: Autenticación mediante usuario/contraseña.
- RNF4: Copias de seguridad diarias de la base de datos.

## 5. Suposiciones y restricciones
- Uso inicial por una biblioteca universitaria mediana (5k-20k ítems).

## 6. Criterios de aceptación
- Los usuarios pueden agregar, modificar y eliminar libros.
- Se puede ejecutar un préstamo y luego su correspondiente devolución.

(Archivo versión DOCX: `DRS_v1.docx` (marcador))

**Nota:** revisi�n 1 - a�adida l�nea para commit 2
