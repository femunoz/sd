# Actividad: Monolito vs. Microservicios

**Objetivo**: Analizar y comparar las arquitecturas monolíticas y de microservicios aplicadas a un escenario práctico, basándose en el artículo de Martin Fowler ("Microservices").

## Contexto
Han leído el artículo de Martin Fowler sobre microservicios (disponible en https://martinfowler.com/articles/microservices.html). Ahora participarán en una actividad grupal para aplicar los conceptos del artículo a un caso práctico.

## Escenario
Deben diseñar un **sistema de gestión de reservas de restaurante** con los siguientes requisitos:  
- **Funcionales**: 
  - Registrar una reserva (nombre, fecha, hora, número de personas).  
  - Consultar disponibilidad de mesas.  
  - Enviar notificaciones al cliente (confirmación de reserva).  
- **No funcionales**: 
  - Escalable para manejar picos de reservas (por ejemplo, en fines de semana).  
  - Tolerante a fallos en caso de que un componente no responda.

## Instrucciones
1. **Formación de equipos (5 minutos)**:  
   - Se organizarán en grupos de 3-4 personas.  
   - Cada grupo recibirá una copia de este enunciado y acceso a una pizarra o herramienta digital (como Jamboard) para tomar notas.

2. **Análisis y diseño rápido (10 minutos)**:  
   - **Tarea 1: Diseño básico (5 minutos)**:  
     - Esbocen cómo implementarían el sistema en dos arquitecturas:  
       - **Monolítica**: Describan cómo organizarían el sistema como una sola aplicación (por ejemplo, módulos internos, base de datos compartida).  
       - **Microservicios**: Identifiquen 2-3 servicios clave (por ejemplo, servicio de reservas, servicio de notificaciones) y especifiquen cómo se comunicarían (por ejemplo, API REST, mensajería).  
   - **Tarea 2: Pros y contras (5 minutos)**:  
     - Listen 2 ventajas y 2 desventajas de cada arquitectura (monolítica y microservicios) para este escenario, basándose en conceptos del artículo (por ejemplo, despliegue, escalabilidad, tolerancia a fallos).

3. **Mini debate (10 minutos)**:  
   - Cada grupo elegirá un portavoz para presentar su análisis en **1 minuto** (ventajas/desventajas y cuál arquitectura prefieren).  
   - Participarán en un debate moderado, respondiendo preguntas como:  
     - ¿Qué arquitectura es más adecuada para este escenario y por qué?  
     - ¿Cómo aplican conceptos del artículo como "smart endpoints", "dumb pipes" o "diseño para fallos"?  
     - ¿Cómo manejarían un fallo en el servicio de notificaciones?

4. **Reflexión final (5 minutos)**:  
   - Cada estudiante responderá individualmente (en voz alta o por escrito):  
     - ¿Qué concepto del artículo les ayudó más a decidir entre monolito y microservicios?  
   - Entreguen sus notas grupales y respuestas individuales al profesor.

## Entregables
- Notas grupales (esquema de diseños y lista de pros/contras).  
- Respuesta individual a la pregunta de reflexión.
