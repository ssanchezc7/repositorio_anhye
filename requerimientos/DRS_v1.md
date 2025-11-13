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
### Criterios de aceptación (detallados)
- CA-01: Un usuario con rol `bibliotecario` puede crear/editar/eliminar un libro y los cambios se reflejan en el listado en menos de 5s.
- CA-02: Al registrar un préstamo, se crea un registro en `prestamos` con `usuario_id`, `libro_id`, `fecha_prestamo` y `fecha_devolucion_prevista`.
- CA-03: Al registrar una devolución tardía, el sistema calcula la multa aplicando la política configurada y la asocia al `usuario_id`.
- CA-04: Las búsquedas por título/autor/ISBN devuelven resultados relevantes y paginados.

## 7. Flujo básico de préstamo
1. El bibliotecario busca el libro por ISBN o título.
2. Selecciona la copia disponible y el usuario que solicita el préstamo.
3. Registra el préstamo indicando la fecha y la fecha prevista de devolución.
4. El sistema decrementa el stock disponible y crea el registro en `prestamos`.

## 8. Modelado de datos (resumen)
- `libros` (id, isbn, titulo, autores, editorial, año, categoria, total_copias, copias_disponibles)
- `usuarios` (id, nombre, correo, tipo_usuario, estado)
- `prestamos` (id, libro_id, usuario_id, fecha_prestamo, fecha_devolucion_prevista, fecha_devolucion_real, multa)

(Archivo versión DOCX: `DRS_v1.docx` (marcador))

**Nota:** revisi�n 1 - a�adida l�nea para commit 2
