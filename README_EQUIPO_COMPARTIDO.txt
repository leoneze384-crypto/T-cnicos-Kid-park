INVENTARIO - EQUIPO COMPARTIDO

Esta versión agrega un equipo compartido. Dos cuentas que usen el mismo código trabajan sobre la misma base de inventario.

1) Publicar las reglas de Firestore
   - Copiar firestore.rules a Firebase/Firestore Rules, o desplegarlo con Firebase CLI.
   - El archivo firebase.json ya apunta a firestore.rules.

2) Primera cuenta (tu cuenta)
   - Entrar normalmente.
   - Ir a Cuenta.
   - Elegir "Crear equipo y compartir mi inventario".
   - La app migrará los registros actuales al equipo y mostrará un código EQ-XXXXXX.

3) Cuenta del supervisor
   - Crear/iniciar sesión con su propia cuenta.
   - Ir a Cuenta.
   - Elegir "Unirme con código de equipo".
   - Escribir el código EQ-XXXXXX.

4) Desde ese momento
   - Ambos consultan el mismo inventario.
   - Ambos pueden agregar/modificar registros.
   - Las observaciones, mantenimientos y movimientos quedan compartidos.
   - La app mantiene sincronización en vivo mientras haya conexión.

Importante:
   - El respaldo JSON sigue existiendo como respaldo de emergencia.
   - La transferencia por archivo NO es el mecanismo de colaboración. Para colaborar se usa el equipo compartido.
   - La seguridad depende de las reglas de Firestore incluidas en este paquete; deben estar publicadas en el proyecto Firebase ivdm-a03d4.
