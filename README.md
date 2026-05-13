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

