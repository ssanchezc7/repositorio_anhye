# Propuesta de Mantenimiento - Sistema de Gestión de Biblioteca

## Tipo propuesto
- Principal: Perfectivo — Mejoras continuas para optimizar búsquedas, UX y nuevos reports.
- Secundario: Correctivo — Corrección de errores detectados en producción.

## Actividades propuestas
- M1: Ciclo de versiones trimestral para mejoras funcionales.
- M2: Monitorización y alertas para caídas del sistema.
- M3: Plan de pruebas automáticas (unitarias e integración) para deploys.
- M4: Procedimiento de rollback y backups antes de cambios mayores.

## Plan de mantenimiento detallado
- Frecuencia: mantenimiento menor cada 2 semanas; releases mayores cada 3 meses.
- Tareas recurrentes: aplicar parches de seguridad, revisar logs semanales, ejecutar backups diarios.
- Gestión de incidencias: usar un sistema de tickets (ej. GitHub Issues) con SLA de 72h para bugs críticos.

## Métricas de control
- Tiempo medio de resolución (MTTR)
- Número de incidencias por release
- Cobertura de pruebas automatizadas

## Prioridades
- Seguridad (parches), integridad de datos (backups), luego mejoras UX y nuevas funciones.

## Recursos y tiempos estimados
- Equipo: 1 desarrollador backend, 1 frontend, 1 QA — sprints de 2 semanas.

## Entregables
- Registro de incidencias, plan de versiones, changelogs y pruebas automatizadas.
