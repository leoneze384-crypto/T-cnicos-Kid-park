Inventario de Máquinas · v17

Roles:
- admin_tecnico: administrador general + técnico. Control total de la app y funciones normales de técnico.
- supervisor: administra técnicos, zonas, sectores y delegaciones de su equipo.
- tecnico: se incorpora únicamente mediante código de equipo y trabaja con sus máquinas asignadas.

Reglas de equipo:
- Solo admin_tecnico o supervisor pueden crear equipos.
- Los técnicos no pueden crear equipos ni zonas.
- Un técnico se une mediante código y registra su zona; la zona queda visible para administración.
- Sus máquinas personales, observaciones, mantenimientos, movimientos y catálogo se vinculan al equipo al incorporarse.
- Las delegaciones pueden hacerse por zona, sector o máquinas seleccionadas.
- El historial no se borra al cambiar de responsable.
- Las notificaciones futuras serán unidireccionales: administración/supervisor -> técnico.

IMPORTANTE:
La primera cuenta que será admin_tecnico debe quedar marcada como tal en Firestore mediante una operación administrativa segura antes de crear el primer equipo. No se permite que un usuario se autoproclame administrador desde la app.
