# DRS_v2 - Sistema de Gestión de Biblioteca

Versión refinada de requerimientos con mejoras y ajustes después de revisión.

## Cambios respecto a v1
- Agregado control de roles y permisos (administrador, bibliotecario, usuario).
- Se define gestión de reservas (reservar libro cuando todas las copias estén prestadas).
- Reportes programados (mensuales) exportables a CSV.
- Mejora en RNF: soportar concurrencia de hasta 50 usuarios simultáneos.

## Requerimientos funcionales (v2)
- RF6: Gestión de roles y permisos para operaciones sensibles (borrado masivo, backups manuales).
- RF7: Sistema de reservas con cola por libro.
- RF8: Generación de reportes (libros más prestados, préstamos por usuario, libros atrasados).
- RF9: Notificaciones por correo para reservas y recordatorios de devolución.

## Requerimientos no funcionales (v2)
- RNF5: Auditoría de acciones clave (registro de quién ejecutó cada acción y cuándo).
- RNF6: Encriptación de contraseñas (bcrypt o similar).
- RNF7: Documentación de la API (si aplica) en OpenAPI/Swagger.

## Criterios de aceptación adicionales
- Las reservas se gestionan en cola FIFO y generan notificaciones.

(Archivo versión DOCX: `DRS_v2.docx` (marcador))
