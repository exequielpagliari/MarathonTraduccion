# Lineamiento del proyecto de traducción de Marathon

El proceso de traducción comprende múltiples aristas a tratar, no solo el medio que involucra la traducción, también los procesos en que los traductores se van a relacionar con el material a traducir, así como la integración de la traducción dentro del medio a traducir.

Marathon, siendo un juego que ha iniciado su desarrollo desde 1994, son múltiples instancias a tratar. Su primera versión comprende alteraciones en los recursos internos de la aplicación que debían ser modificados por aplicaciones especiales, mientras que las nuevas versiones aceptaban recursos externos con facilidad de edición, junto con las herramientas oficiales de Bungie.

Actualmente, AlephOne, el port multiplataforma, acepta hasta la edición por medio de scripts de todas las líneas de textos que hay en el juego, ayudando a la traducción total del juego, con posibles limitaciones.

Más allá de cuestiones tecnológicas, el texto que se presenta en las terminales de cada uno de los juegos involucra elementos de la literatura universal, pasando por diferentes estilos y géneros, así como citas de científicos y teorías científicas. La complejidad que representan estos elementos denota la necesidad de un especial cuidado en el tratar del contenido, con la necesidad de investigación bibliográfica en dichos detalles para una correcta interpretación.
En la ausencia de un proyecto de esta índole para toda la saga, damos por hecho la necesidad de iniciarlo y dar los lineamientos que se usaran para poder generar una traducción hecha por fanáticos, para los fanáticos de habla hispana, aun sabiendo de la existencia de versiones traducidas oficiales, pero que solo responden a un solo juego de la saga y de difícil acceso al material oficial.

### Proceso de traducción

El proceso de traducción se compone de partes delimitadas que trabajaran en conjunto. Cada una tendrá una finalidad específica y una metodología. El proceso, a grandes rasgos será el siguiente:
 

Iniciará en la carga del contenido base a una Plataforma de Traducción, en nuestro caso se aceptará Zanata (https://translate.zanata.org/). Se cargaran en el formato aceptado por la plataforma el contenido del Split del Escenario en cuestión, y se generará un proceso de traducción y mantenimiento de la misma, una vez terminada la traducción.

El siguiente paso en el proceso de traducción será el paso de cada uno de los elementos textuales de la traducción transcribirlo al contenido del Split del Escenario en cuestión, por medio de la aplicación HuxQT (https://github.com/janos-ijgyarto/HuxQt).
El proceso se generará en una rama llamada HuxQt, con la cual se copiaran los texto modificados, se generará un Merge del Mapa, haciéndose las pruebas de funcionamiento con ese archivo.

Posterior a ello, se generará un Merge de la rama HuxQt con la Main, usando el archivo Mapa como Release del repositorio.

