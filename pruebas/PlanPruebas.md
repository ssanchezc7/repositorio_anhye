# Plan de Pruebas - Sistema de Gestión de Biblioteca

## Objetivo
Validar procesos críticos: registro de usuarios, préstamos y devoluciones, búsquedas y reservas.

## Casos de prueba (mínimo 3)

1) CP-01: Registrar usuario nuevo
- Precondición: Interfaz de registro accesible.
- Pasos: Completar formulario con datos válidos y enviar.
- Resultado esperado: Usuario creado y aparece en la lista con estado activo.
- Validación: Comprobar en la base de datos el nuevo registro (ID, correo).

2) CP-02: Realizar préstamo de libro disponible
- Precondición: Libro con al menos 1 copia disponible; usuario activo.
- Pasos: Seleccionar libro, seleccionar usuario, registrar préstamo.
- Resultado esperado: Estado de copia cambia a prestada; registro de préstamo con fecha y vencimiento.
- Validación: Verificar registro en tabla `prestamos` y que stock decrementó.

3) CP-03: Registrar devolución con multa
- Precondición: Préstamo vencido (fecha pasada) con política de multa establecida.
- Pasos: Registrar devolución del préstamo vencido.
- Resultado esperado: Multa calculada y asociada al usuario; estado de copia disponible.
- Validación: Verificar cálculo de multa y registro en `sanciones` o similar.

(Archivo versión DOCX: `PlanPruebas.docx` como marcador)