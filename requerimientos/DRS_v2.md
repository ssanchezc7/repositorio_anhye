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

## 4. Escenarios de uso adicionales
- Reserva automática: cuando un libro no tiene copias disponibles, un usuario puede reservar; al devolver una copia, el primer usuario en cola recibe notificación y tiene 48h para retirar.
- Exportación de reportes: los administradores pueden programar reportes mensuales en formato CSV.

## 5. Requisitos de seguridad
- Todas las contraseñas almacenadas con hashing fuerte (bcrypt) y sal.
- HTTPS obligatorio en producción.

(Archivo versión DOCX: `DRS_v2.docx` (marcador))

## Requerimientos no funcionales (v2)
- RNF5: Auditoría de acciones clave (registro de quién ejecutó cada acción y cuándo).
- RNF6: Encriptación de contraseñas (bcrypt o similar).
- RNF7: Documentación de la API (si aplica) en OpenAPI/Swagger.

## Criterios de aceptación adicionales
- Las reservas se gestionan en cola FIFO y generan notificaciones.

(Archivo versión DOCX: `DRS_v2.docx` (marcador))
