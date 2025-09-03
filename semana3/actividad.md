### Guía de actividad Cliente-Servidor
Esta actividad introduce el modelo cliente-servidor en el contexto de APIs web (RESTful), usando Python para simular un cliente que interactúa con un servidor remoto. El objetivo es entender cómo un cliente envía peticiones HTTP, recibe respuestas en formato JSON y las procesa, mientras se contrasta con enfoques P2P (donde no hay un servidor central). La actividad se divide en fases para caber en ~30 minutos.

#### Preparación (5 minutos)
1. Asegúrate de tener Python y `requests` instalados. Abre un terminal y ejecuta `pip install requests` si es necesario.
2. Crea un nuevo archivo Python (e.g., `cliente_api.py`) en tu editor.

#### Implementación del Código (15 minutos)
Usaremos la API pública gratuita JSONPlaceholder (https://jsonplaceholder.typicode.com/), que simula datos como posts, usuarios, etc., sin necesidad de registro.

Pasos detallados:
1. Importa la biblioteca: En tu script, escribe:
   ```python
   import requests
   import json  # Para formatear la salida opcionalmente
   ```
   
2. Define la URL de la API: Por ejemplo, para obtener una lista de posts:
   ```python
   url = "https://jsonplaceholder.typicode.com/posts"
   ```

3. Envía una petición GET: Usa `requests.get()` para consultar el servidor.
   ```python
   response = requests.get(url)
   ```

4. Verifica la respuesta: Comprueba si la petición fue exitosa (código 200).
   ```python
   if response.status_code == 200:
       data = response.json()  # Convierte la respuesta a JSON
       print("Datos recibidos:")
       print(json.dumps(data[:5], indent=4))  # Muestra los primeros 5 elementos para no saturar la salida
   else:
       print(f"Error: {response.status_code}")
   ```

5. Experimenta con variaciones: Modifica la URL para otros endpoints, como `/users` o `/posts/1` (un post específico). Agrega parámetros, e.g., `url = "https://jsonplaceholder.typicode.com/posts?userId=1"` para filtrar por usuario.

6. Ejecuta el script: Corre el archivo con `python cliente_api.py` en la terminal. Observa la salida en consola.

#### Experimentación y Discusión (10 minutos)
- Prueba diferentes queries: Cambia la URL para endpoints como `/todos` (tareas) o agrega parámetros de consulta (e.g., `?id=1`).
- Discute en grupo: ¿Cómo escala este modelo cliente-servidor (e.g., el servidor maneja muchas peticiones)? ¿En qué difiere de P2P (e.g., en P2P, los peers comparten carga, pero hay más complejidad en descubrimiento)? Considera pros/contras: Servidor central es simple pero punto de fallo único; P2P es distribuido pero requiere manejo de conexiones peer-to-peer.
- Opcional: Maneja errores, como agregar try-except para conexiones fallidas.

Si hay tiempo, extiende a una petición POST (crear datos), pero manténlo simple para no exceder el tiempo.

### Entregables
Al final de la actividad, cada estudiante o grupo (sugerido: parejas para discutir) debe entregar lo siguiente para evaluación:

1. **Código Fuente**: El archivo `.py` con el script completo y comentado (e.g., explicar cada sección con # comentarios). Incluye al menos 2-3 variaciones de queries en el código.
2. **Capturas de Pantalla o Log de Salida**: Muestra la ejecución en consola (e.g., copia el output de al menos dos peticiones diferentes). Si usas Colab, comparte el enlace.
3. **Informe Breve (1-2 párrafos)**: Describe qué aprendiste sobre el modelo cliente-servidor, un ejemplo de la respuesta JSON procesada, y una comparación corta con P2P (e.g., "En cliente-servidor, el cliente depende del servidor para datos, mientras en P2P los peers se sirven mutuamente, reduciendo latencia en redes grandes pero aumentando complejidad").
4. **Demostración Opcional**: En clase, ejecuta el script en vivo y explica una query.

Entrega vía email, plataforma de aula (e.g., Moodle) o GitHub si aplica. Esto permite evaluar comprensión práctica y teórica en ~5 minutos por estudiante.
