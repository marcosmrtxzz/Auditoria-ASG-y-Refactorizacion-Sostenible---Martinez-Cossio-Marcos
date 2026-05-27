# Auditoria-ASG-y-Refactorizacion-Sostenible---Martinez-Cossio-Marcos

## Fase 1: Inventario y Dimensión Ambiental (A)
Medición inicial. 
Utiliza herramientas gratuitas como Website Carbon Calculator o Lighthouse (pestaña de rendimiento en Chrome/Edge) para obtener la huella de carbono estimada por visita.

<img width="1333" height="723" alt="image" src="https://github.com/user-attachments/assets/7764daf3-2f41-4912-9e3b-f461737ae615" />

Identificación de Bloatware. Inspecciona la red (Network) en las herramientas de desarrollador del navegador. Identifica los 3 recursos más pesados que se descargan al abrir la web (imágenes sin comprimir, vídeos de fondo, librerías JavaScript pesadas, etc.).

| Numero | Recurso | Tipo | Tamaño |
| :---- | :---- | :---- | :---- |
| **1** | 512\_face2\_0\_0.jpg  | imagen | 1.2 MB  |
| **2** | background-video.mp4 | Vídeo  | \~5 a 10 MB  |
| **3** | showcase.js  | JavaScript  | JavaScript  |


Análisis. ¿Crees que la web sufre de "inflación de software"? Justifica tu respuesta.

Si, la web tiene una inflacion de sofware porque carga demasiados recursos que son mucho mas pesado de lo que es necesario, con el Network he visto que las imagenes sin comprimir pesan mas de 1MB , los JS y las fuentes son demasiadas pesadas tambien y es un tamaña grande, mas tiempo en cargar la web, para el consumo energetivo, muchos recursos que para una web que es para una taberna podria funcionar mejor que archivos muchos mas ligeros.

## Fase 2: Dimensión Social y Equidad (S)

La web debe ser utilizable por todos. Evalúa la accesibilidad (Sostenibilidad Social): 
Test de Accesibilidad. Pasa una herramienta como WAVE Web Accessibility Evaluation Tool o el propio Lighthouse (pestaña Accessibility).

   - Se ha evaluado la web con Lighthouse y wave y he visto que hay varios problemas que afectan a la sostenibilidad ya que hacen mas dificil el acceso


Identificación de barreras. Documenta al menos 2 problemas graves que impidan a personas con diversidad funcional usar la web correctamente (ej. falta de atributos alt en imágenes clave, bajo contraste de colores en botones, formularios sin etiquetas).

- Identificación de barreras de accesibilidad
    - Hay imagenes que no tienen el atributo alt.
    - Hay muchas imagenes que no tiene el texto, eso hace que las personas que no pueden leer, comprendan el contenido visual.

- El conrtraste de colores:
    - Hay textos y botonoes que tienen un contraste insuficientes comprado con el fondo y no cumple con las pautas, esto hace que las personas que tienen problemas de vision puedan no ver o dificultar la vision de las webs
## Fase 3: Dimensión de Gobernanza y Ética (G)
Revisa cómo trata la empresa a sus usuarios y sus datos:
Transparencia. ¿Es fácil rechazar las cookies no esenciales o utilizan "patrones oscuros" (Dark Patterns) para forzar al usuario a aceptarlas?
    - No da, la posibilidad de rechazarlas ademas de personalizarlas con Configuracion Perzonalizada para poder elegir cual si acepto y cual no.
    <img width="543" height="123" alt="image" src="https://github.com/user-attachments/assets/6e7b69d4-ee53-47d6-97cc-bab65ff5b644" />

    
Datos innecesarios. ¿Pide la web datos personales excesivos en su formulario de contacto o registro?   
   - Pide yo creo lo necesario para poder contactar conmigo, como es Nombre, para saber como llamarme al contactar, el telefono para ponerse en contacto conmigo, y correo para datos mas extensos, ademas de poder elegir donde quiero trabjar tanto en cocina como en sala, y un mensaje por si quiero puntuar algo en especifico.
      
<img width="897" height="793" alt="image" src="https://github.com/user-attachments/assets/4a883f33-0677-4e10-8572-80376aa55af4" />

## Fase 4: Propuesta de Refactorización (Green Coding)

Como desarrollador/a, no basta con encontrar los fallos; debes proponer soluciones. Redacta una propuesta de mejora técnica detallando:

Optimización de activos

¿Qué formatos usarías para sustituir las imágenes actuales (ej. WebP, AVIF)?

- WebP:

   * Porque es bueno como primera idea, ya que reduce entre 25 y 35% de peso.  
   * Soporta la transparencia del png y además con menos tamaño.  
   * Tiene una compatibilidad para casi todos los navegadores.

- AVIF:

   * Para mi ahora mismo es la que más eficiente es ya que cuenta con un 50% menos del peso que WebP y deja la misma calidad.  
   * Para las web donde tengamos que poner imágenes grandes, ya sea en un slider o de fondo es muy bueno.  
   * Tiene lo único malo que es que soporta el HDR (tecnología que mejora la calidad visual de las imágenes al ampliar el rango de luces, sombras y colores) pero va más lento.

- SVG:

   * Es lo mejor para fotografías pequeñas, como puede ser un logo o iconos.  
   * No tiene pérdida y tiene un peso mínimo.  
   * Puede tener CSS y animaciones.

¿Implementarías Lazy Loading?

   * Pues sí, ya que así consigo que solo se carguen cuando vayan a ser vistas, así reduce el consumo al abrir una web. Es como el Linux y el Windows: Windows tarda más en arrancar porque carga todo uses o no uses todo, y Linux carga solo lo que vayas a utilizar, por eso tarda menos en cargar el Linux.

Reducción de peticiones

¿Qué librerías o scripts externos eliminarías o aplazarías para mejorar la eficiencia del código y reducir el procesamiento en el dispositivo del cliente?

   * Cambiaría las imágenes a WebP.  
   * Reemplazo las imágenes grandes por AVIF.  
   * Quito imágenes que no dan un valor a la web.

## 3. Refactorización. Propuesta.

Debes plantear una mejora técnica estructurada de la web.

3.1. Posibles mejoras ambientales (A)

   * Optimización de imágenes (WebP, compresión)
     <img width="605" height="128" alt="image" src="https://github.com/user-attachments/assets/eb49feeb-3b4b-44bc-bb5b-beefa2676968" />

   * Reducción de peticiones HTTP
     <img width="770" height="132" alt="image" src="https://github.com/user-attachments/assets/4413e300-36c0-4ac3-a2c2-eae49333d15f" />

   * Lazy loading
     <img width="771" height="78" alt="image" src="https://github.com/user-attachments/assets/8152ceb2-b005-46b7-a936-7372ee7a03e7" />

   * Eliminación de código no utilizado
     - He borrado muchas cosas que no tenian que estar al estar vacias o no utilizadas:
     <img width="496" height="859" alt="image" src="https://github.com/user-attachments/assets/1f2715e4-3499-49ab-89d0-7485ebf42687" />


3.2. Posibles mejoras sociales (S)

   * Uso de HTML semántico (header, nav, main, etc.)
Línea 13: Inicio del <header class="site-header">

Línea 26: Inicio de la etiqueta de navegación <nav class="header-navigation"...>

Línea 39: Apertura del contenedor principal <main id="tm-main">

Línea 40: Uso de la división por bloques <section class="taberna-detail">

Línea 48: Etiqueta de datos de contacto <address class="contact-info">

Líneas 74 y 79: División de bloques de contenido independiente <article class="schedule-block">

Líneas 76, 77, 81, 82: Formateo de horas estructuradas con <time datetime="...">

   * Inclusión de atributos alt
     <img width="612" height="607" alt="image" src="https://github.com/user-attachments/assets/b1a4a865-0725-4b38-97fe-c02abd88267e" />

   * Mejora del contraste
      <img width="527" height="176" alt="image" src="https://github.com/user-attachments/assets/e589bdea-ce27-4347-a31a-60b724aa8143" />

   * Navegación accesible
     <img width="774" height="64" alt="image" src="https://github.com/user-attachments/assets/db647ffc-b33a-46a7-b78a-0d048bd24756" />


3.3. Posibles mejoras de gobernanza (G)

   * Implementación de consentimiento de cookies transparente  
   * Simplificación de textos legales  
   * Eliminación de prácticas engañosas  
   * Mejora de la privacidad

3.4. Propuesta técnica
Debes incluir:
   
   * Ejemplos de código mejorado  
   * Comparativa “antes vs después”  
   * Herramientas utilizadas (Lighthouse, PageSpeed, WAVE…)
