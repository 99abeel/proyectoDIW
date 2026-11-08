# Registro de Cambios y Uso de IA

---
## 1. Ayuda en el diseño y lógica de los User Flows
Basicamente como organizar bien los userflows del proyecto.
### Que le dije:
Le envie el userflow que yo habia planteado y el me lo corrigió y mejoro con algunas cosas que me faltaban
### Con que me quede:
Quité el bucle cerrado del login y uní el menú inicial directamente con la partida activa y creación de personaje.
### Criterio propio:
Me soltó muchas cosas que tampoco venian al caso o eran muy complejas de implementar.


## 2. Ayuda con el manejo de figma
Sobretodo lo principal que le pregunte es como hacer el prototipo, porque se me ponia en modo movil cuando lo queria ver en modo escritorio.
### Que le dije: 
Como podia visualizar mis wireframe de figma design en formato escritorio, ya que se me ponia solo en version de movil y no sabia como cambiarlo
### Con que me quede:
No me lo supo arreglar muy bien, asi que directamente borre todos los enlaces del prototipo y los hice de nuevo. Funcionó.

### 3. Retricciones del proyecto
Despues de contarle todo el proyecto, le pedi ayuda para que me dijera las herramientas que me iban a hacer falta para llevarlo a cabo.
### Que le dije:
Le envie de que trataba mi proyecto junto con los userflows, etc. Le pregunté que herramientas necesitaba para hacerlo.
### Con que me quede:
Usar HTML, CSS y JavaScript para el frontend, Node.js con base de datos para el Backend conectando las APIs de IA mediante peticiones asincronas.
### Criterio propio:
Descarté algunas cosas que me dijo para implementar debido a la complejidad.

## 3. Stitch
Mandandole el png de mi landing page: "hazlo siguiendo el Wireframe, no me hagas ya el mockup. Simplemente mejoralo con algo para que sea mas atractivo"
### Con que me quedé:
Mejoras aplicadas manteniendo el espíritu Wireframe, Retícula y Fondo de Diseño (Grid Blueprint), Tipografía y Jerarquía Visual.
### Criterio propio:
Quité algunos botones que me dió y no me gustaba como quedaba. 


---

# Órbita 2
## Entrada 1: Definición de paleta de color y verificación de contraste WCAG

* **Herramienta:** Gemini
* **Qué pedí (Prompt / Entrada):**
   * Necesito una paleta de color accesible para una web de rol D&D con tono morado, con escala de primitivos del 50 al 900 y tokens semánticos en dos modos (claro y oscuro). Calcula las parejas con peor contraste para comprobar que pasan WCAG AA (4.5:1).
* **Qué devolvió la IA:**
  * Una propuesta de escala primitiva para púrpura (`purple-50` a `purple-900`), ámbar (`amber-50` a `amber-900`) y grises neutrales (`neutral-50` a `neutral-900`).
  * La correspondencia semántica para `color/primary`, `color/surface`, `color/surface-container`, `color/on-surface` y `color/on-surface-variant` en ambos modos.
  * Los cálculos matemáticos de ratio de luminancia:
    * Modo claro (`#6B7280` sobre `#FFFFFF`): ~4.6:1.
    * Modo oscuro (`#9CA3AF` sobre `#1F2937`): ~4.8:1.
* **Qué conservé:**
  * Los valores hexadecimales base para los tonos clave (`#7C3AED` para primario, `#D97706` para secundario) y la separación arquitectónica en dos colecciones en Figma (`primitives` y `semantics`).
  * Las justificaciones de contraste para la tabla obligatoria de la Guía de Estilo.
* **Qué cambié / descarté:**
  * Se simplificó la lista de tokens semánticos eliminando estados intermedios que no se iban a usar en el Happy Path para no sobrecargar el panel de variables de Figma antes de la entrega.

---

## Entrada 2: Escala tipográfica y vinculación con etiquetas HTML 

* **Herramienta:** Gemini
* **Qué pedí (Prompt / Entrada):**
  * Cómo puedo estructurar una escala tipográfica de 8 niveles con Plus Jakarta Sans en Figma.
* **Qué devolvió la IA:**
  * Una tabla completa con 8 estilos de texto (`display-lg`, `heading-1`, `heading-2`, `heading-3`, `body-lg`, `body-md`, `body-sm`, `label-md`).
* **Qué conservé:**
  * La jerarquía completa, nombres de estilo con sintaxis de código (`heading-1`, `body-md`).
* **Qué cambié / descarté:**
  * Se descartaron los pesos secundarios extremos (Light 300 y ExtraBold 800) para limitarse a Regular (400), Medium (500) y Bold (700), garantizando que las fuentes en Google Fonts no superen el límite técnico de 500 KB fijado en los requisitos.

---

## Entrada 3: Construcción de componentes atómicos con Auto Layout 

* **Herramienta:** Gemini
* **Qué pedí (Prompt / Entrada):**
  * Indícame los pasos exactos para crear un componente de botón accesible con Auto Layout (mínimo 44 px de altura), esquinas redondeadas con variable, y variante Hover con elevación en Figma en español.
* **Qué devolvió la IA:**
  * Instrucciones paso a paso sobre el atajo `Shift + A`, configuración de padding vertical (12 px) y horizontal (20/24 px), asignación de variable `radius/button`, adición de variante `State = Hover` con `color/primary-hover` y estilo de sombra `elevation/md`.
* **Qué conservé:**
  * Toda la configuración de padding y variables para asegurar los 44 px táctiles exigidos por la rúbrica.
  * La estructura del componente maestro `Button` y del organismo `Card / Action`.
* **Qué cambié / descarté:**
  * Se omitió la creación de variantes adicionales de botones terciarios o estados de carga por falta de tiempo para la entrega de esta fase, priorizando los estados `Default` y `Hover`.

---

## Entrada 4: Redacción de la memoria de entrega (ORBITA2.md)

* **Herramienta:** Gemini
* **Qué pedí (Prompt / Entrada):**
  * Analiza todo la informacion sobre el proyecto que tengo hecha y redacta la plantilla oficial de ORBITA2.md, indicando de forma honesta lo que está completado (variables, estilos, componentes maestros) y lo que queda pendiente (mockups responsive completos y prototipo).
* **Qué devolvió la IA:**
  * El borrador íntegro en Markdown adaptado a la rúbrica, justificando las decisiones con las personas (Hugo y Rafael) y el estado real de la lista de comprobación.
* **Qué conservé:**
  * La redacción íntegra de las justificaciones técnicas y la honestidad en los campos no terminados de la checklist para evitar discrepancias con la corrección del profesor.
* **Qué cambié / descarté:**
  * Se sustituyeron los enlaces genéricos por los marcadores correspondientes para pegar las URLs reales del repositorio y del archivo de Figma, ademas de retocar unas cuantas cosas que sobraban. 
