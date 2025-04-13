# Detalles de lo implementado en el EXAMEN FINAL (Proyecto STR) - CHAT EN TIEMPO REAL

# Descripcion General
Este proyecto es el resultado de la aplicación práctica de los conocimientos adquiridos durante el desarrollo del curso Software en Tiempo Real. A continuación setallan los conociminetos y cómo fueron implementados los conceptos en el proyecto final desarrollado:

# Selección del Proyecto
Se eligió desarrollar una sala de chat en tiempo real, donde múltiples usuarios pueden enviar y recibir mensajes simultáneamente. Este proyecto permite simular escenarios reales donde se requiere concurrencia, sincronización, y consistencia de datos.

# Creación del Proyecto en Tiempo Real
Se construyó el sistema utilizando tecnologías modernas y adecuadas para el desarrollo en tiempo real:
- JavaScript (Node.js) para el backend.
- Socket.IO para la comunicación en tiempo real entre cliente y servidor.
- MongoDB Atlas como base de datos en la nube para persistencia.
- Express.js para la construcción del servidor web.

# Implementación de Semáforos
Se aplicaron semáforos utilizando la librería async-mutex para evitar condiciones de carrera y garantizar el acceso exclusivo a la base de datos al guardar nuevos mensajes. Esto asegura que múltiples usuarios no interfieran al escribir simultáneamente.

#  Manejo de Excepciones
Se implementó un control robusto de errores mediante bloques try/catch en todas las operaciones críticas, como la conexión a la base de datos, el envío de mensajes y el manejo de eventos de sockets.

# Concurrencia
Se desarrolló un método recursivo para consultar mensajes desde la base de datos en bloques, permitiendo manejar múltiples consultas sin bloquear el sistema, y asegurando la eficiencia y escalabilidad del chat.

# Sincronización
Se garantizó que los mensajes enviados por un usuario sean emitidos en tiempo real a todos los demás usuarios conectados utilizando eventos sincronizados por Socket.IO. Esto permite mantener todos los clientes actualizados al instante.

# Manejo de Eventos
Se emplearon eventos personalizados para controlar la conexión, desconexión, recepción y envío de mensajes. Esto permite una arquitectura basada en eventos eficiente y reactiva.

# Monitores
Se aplicaron principios de monitores para encapsular la lógica crítica del acceso a la base de datos, combinando el uso de semáforos, validaciones y control de estado en los métodos principales.

# Base de Datos
Se integró MongoDB Atlas como base de datos remota, almacenando los mensajes de forma persistente y segura. La base de datos soporta operaciones concurrentes y consultas eficientes para garantizar la disponibilidad y coherencia de la información.

# Conclusiones
El desarrollo de este proyecto ha permitido integrar todos los conceptos fundamentales del curso, demostrando su aplicabilidad en un caso real de software que requiere sincronización, concurrencia y tiempo real. El sistema desarrollado es escalable, robusto y funcional.



