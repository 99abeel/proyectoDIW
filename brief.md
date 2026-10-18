# Brief de Proyecto: D&D con IA

Aplicación web para jugar a rol (Dungeons & Dragons) en solitario usando una Inteligencia Artificial como narrador y director de juego (Dungeon Master).

---

## 1. El problema que resuelve mi aplicación

Al hacer las entrevistas para el proyecto me di cuenta de dos problemas reales que tiene la gente que quiere jugar a rol:

1. **Es casi imposible cuadrar horarios con amigos:** El 100% de la gente con la que hablé me dijo lo mismo: entre los estudios, los trabajos y las cosas de cada uno, organizar una partida de 4 o 5 personas es una odisea. Al final las campañas se quedan a medias y nadie vuelve a jugar.
2. **Los manuales son infumables y jugar solo da pereza:** La gente que quiere empezar por su cuenta se encuentra con tochos de 300 páginas de reglas y hojas llenas de números. Las opciones que hay en internet para jugar solo suelen ser bloques de texto aburridos sin imágenes ni nada interactivo.

**D&D con IA(aun no se me ocurre un nombre bueno)** resuelve esto permitiendo que cualquiera pueda echarse una partida solo cuando le apetezca: una IA te cuenta la historia y maneja las reglas, para que puedas jugar turnos rápidos de 15 minutos sin tener que esperar a nadie.

---

## 2. Alcance del proyecto (MVP)

### Lo que entra en esta primera versión:
* **Registro y login:** Para que cada jugador tenga su cuenta y no pierda sus personajes ni el progreso de la historia.
* **Creación rápida de personaje:** Repartir los puntos de las estadísticas clásicas (fuerza, destreza, etc.) y elegir nombre de forma sencilla.
* **Generación de avatar con IA:** Escribir una pequeña descripción y que la IA dibuje la imagen del personaje (con un tope de 3 intentos para no gastar saldo de la API sin querer).
* **Partida interactiva (Chat con el Dungeon Master):** Una pantalla donde la IA te narra la aventura, tú escribes qué quieres hacer, ves tu barra de vida y tu inventario actualizados.
* **Guardado automático y aviso si se va internet:** La partida se guarda sola en la base de datos, y si se corta la conexión, la web avisa al usuario y guarda la última acción para que no se pierda nada.
* **Modo noche:** Un botón para poner la web oscura, que viene genial para jugar de noche y para que el móvil gaste menos batería.

### Lo que se queda fuera para más adelante (y por qué):
* **Modo multijugador:** Es muy complicado de programar para esta entrega y contradice la idea principal, que es poder jugar cuando tus amigos no están disponibles.
* **Voz para el narrador:** Pasaría demasiado audio por la red, haría la web más lenta y gastaría muchos datos a quien juegue con el móvil.
* **Tablero con miniaturas y mapas:** Meter un mapa interactivo complicaría mucho la pantalla; para empezar, lo divertido es centrarse en la historia y la imaginación.
* **Música de fondo:** Hace que la web tarde más en cargar y chupe batería del móvil innecesariamente.

---

## 3. Personas del proyecto

* **Persona Principal:** [Hugo Cisneros Flor (Ver ficha en FigJam)](https://www.figma.com/board/JU5khbn1JiyOxVHxUXTHKZ/Proyecto-DIW?t=Irm66x6CWXeL0B5y-0)  
  Tiene 23 años y estudia. Quiere probar el rol pero sus amigos no se animan y le da pereza leerse las reglas. Me he centrado en él para que la web sea rápida, visual y se entienda a la primera sin tutoriales.
* **Persona Secundaria:** [Rafael Suazo Periñán (Ver ficha en FigJam)](https://www.figma.com/board/JU5khbn1JiyOxVHxUXTHKZ/Proyecto-DIW?t=Irm66x6CWXeL0B5y-0)  
  Tiene 51 años, trabaja como frigorista y jugaba a rol de joven. Ahora no tiene tiempo libre y tiene vista cansada. Gracias a él he diseñado los botones más grandes, las letras con buen contraste y he pensado qué pasa cuando juegas con mala cobertura 4G.

---

## 4. Criterios de éxito

Sabré que el diseño funciona si en las pruebas se cumple esto:

1. Hugo es capaz de registrarse, hacerse su personaje, sacarse un avatar con la IA y empezar su primera partida en menos de 2 minutos y sin pedir ayuda.
2. Rafael puede leer los textos de la historia en el móvil sin dejarse los ojos y pulsar todos los botones con una sola mano sin equivocarse.
3. Si a Rafael se le corta la cobertura mientras envía una acción, la pantalla le avisa claramente de lo que pasa sin borrarse lo que había escrito, y le permite reintentar en cuanto vuelva la señal.
4. Cualquiera de los dos puede encontrar sus estadísticas o el panel de su cuenta desde la partida en dos clics como mucho.

---

## 5. Restricciones del proyecto

* **Técnicas:** Tengo que usar HTML, CSS y JavaScript para el frontend, y Node.js con base de datos para el backend, conectando todo con las APIs de IA (OpenAI / OpenRouter) mediante peticiones asíncronas seguras.
* **De usuario y accesibilidad:** La web tiene que verse bien tanto en pantalla de ordenador (16:9) como en móvil vertical (412 × 917 px). Las letras en móvil no pueden medir menos de 16 px y los botones deben tener un tamaño cómodo para tocarlos con el dedo.
* **Ambiental y sostenibilidad (WSG 2.4):** Para no saturar el móvil de quien tenga peor conexión ni gastar energía a lo tonto, la web no pesará más de 500 KB al cargar. Además, el modo oscuro con fondo negro real ayudará a ahorrar batería en pantallas de móvil.

---

## 6. Enlaces del entregable

**Investigación, Personas, MVP y Sitemap:** [Tablero en FigJam](https://www.figma.com/board/JU5khbn1JiyOxVHxUXTHKZ/Proyecto-DIW?node-id=45-1389&p=f&t=Irm66x6CWXeL0B5y-0)

**Wireframes y Prototipo Navegable:** [Archivo en Figma Design](https://www.figma.com/board/JU5khbn1JiyOxVHxUXTHKZ/Proyecto-DIW?node-id=45-1389&p=f&t=Irm66x6CWXeL0B5y-0)
