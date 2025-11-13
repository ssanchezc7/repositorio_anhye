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
4) CP-04: Reserva y notificación
- Precondición: Libro sin copias disponibles y usuario registrado.
- Pasos: Usuario solicita reserva; se añade a la cola.
- Resultado esperado: Reserva creada en cola; cuando se libera una copia, primer usuario en cola recibe notificación.
- Validación: Verificar entrada en tabla `reservas` y registro de notificación enviada.

## Procedimiento de ejecución de pruebas
- Preparar datos: crear 2 usuarios de prueba, 3 libros (1 con 0 copias, 2 con copias disponibles).
- Ejecutar pruebas en ambiente de pruebas o base de datos de prueba.
- Registrar evidencia: capturas de pantalla y registros de la base de datos.

(Archivo versión DOCX: `PlanPruebas.docx` como marcador)
**Evidencia:** pasos de validaci�n ampliados
