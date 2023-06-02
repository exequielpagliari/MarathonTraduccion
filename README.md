# Marathon Traducción

### Introducción 

La trilogía de Marathon es una serie de videojuegos de ciencia ficción creado por Bungie, lanzada originalmente para el Macintosh. Marathon se refiere al nombre de una gigantesca nave interestelar que hace las veces de colonia, la cual proporciona el escenario para el primer juego y se convierte en referencia prominente en el argumento de las secuelas; la nave fue construida a partir de la que fuera la segunda luna de Marte, Deimos.

Ambientado en el año 2794, Marathon ubica al jugador como un oficial de seguridad, enviado a responder a una señal de socorro enviada desde una enorme nave espacial llamada U.E.S.C. Marathon, en órbita alrededor de una colonia en el planeta Tau Ceti IV. Durante el juego, el jugador intenta defender la nave (y su tripulación, además de los colonos) de una raza de extraterrestres esclavizadores llamados Pfhor. A medida que el jugador lucha contra los invasores, presencia interacciones entre las tres inteligencias artificiales de la nave (Leela, Durandal y Tycho), y descubre que no todo es lo que parece a bordo: entre otros problemas, Durandal se ha vuelto rampante y parece que está utilizando a los humanos contra los Pfhor para lograr un fin misterioso.

El primer juego de Marathon fue lanzado para el Macintosh en 1994, e introdujo a los videojuegos muchos de los conceptos que ahora son comunes. Características como la de blandir armas duales, personajes aliados no controlados por el jugador, y lo más notable, una intrincada historia. La secuela, Marathon 2: Durandal, fue lanzada en 1995 y amplió las tecnologías del motor gráfico y el Universo de la historia. A diferencia de su protosecuela más oscura, Marathon 2 se ha percibido a menudo por ser un juego más brillante, vivo y más atmosférico. Introdujo varios tipos de modos multijugador más allá del deathmatch y del juego cooperativo, tal como rey de la colina. En 1996, en un giro sorprendente, el juego fue lanzado para Windows 95, junto con Marathon Infinity, que incluía un nuevo panorama usando un motor modificado de Marathon 2, y lo más importante, las herramientas usadas para construirlo, Forge y Anvil. En el 2000, Bungie lanzó el código fuente del motor de Marathon 2, y el proyecto código libre de Marathon comenzó, dando como resultado el motor nuevo de Marathon llamado Aleph One. Finalmente, en 2005, Bungie lanzó la trilogía original completa para la distribución libre en línea, permitiendo que a través Aleph ONE funcionen los juegos de la trilogía en distintas plataformas (OS del Mac, Linux y Windows). 

### Mapas en Marathon

La herramienta Forge y Anvil fueron creadas para el desarrollo de contenido por parte de los fans. Ambas herramientas cuentan con la capacidad de la creación de Mapas o Escenarios con Terminales en Forge,  así como agregar Sprites, Animaciones, Sonidos o modificar el comportamiento del nivel con Anvil.
Los Mapas, además de creados, deben pasar por un proceso llamado merge (unión) para que el juego pueda detectar correctamente el contenido del mapa, así como darle forma a las Terminales del juego, si es que el mapa contiene alguna terminal.
Todo el proceso de creación está documentado en el Manual de Marathon Infinity.


### Funcionamiento del Terminal

En Marathon, un Terminal es un polígono que acciona la aparición de una pantalla con texto e imagen, utilizado normalmente para el desarrollo de la trama de la historia.
Esto se logra gracias al proceso del merge, donde debemos colocar cada archivo de mapa con su correspondiente archivo de terminal, con su propio sistema de etiquetado, así como los recursos de imagen y sonido que queramos que aparezca en el mapa final.

### Marcación Terminal en Marathon

Marathon tiene un sistema de marcación interno en la aplicación “Marathon”. Si ingresamos en los recursos de esta por medio de aplicaciones como ResEdit, encontraremos un conjunto de recursos llamados “Term”, donde se encuentra toda la marcación de los terminales, organizados según nivel.
Actualmente, desconocemos la marcación a nivel técnico de cada elemento así como herramienta específica para tratar la marcación, pero responde a la lógica de la marcación de Marathon 2 e Infinity.

### Marcación Terminal en Marathon 2 e Inf

La modificación del sistema de Marathon 2 trajo consigo la capacidad de unir mapas con sus respectivos recursos y así crear escenarios con sus terminales independientes, ya no modificando los recursos internos de la aplicación principal “Marathon”. Esto facilitó el proceso de generar contenido por fans y compartirlo sin problema. 

Las diferencias significativas entre Marathon 2 e Infinity son la capacidad de anexar a un escenario, los archivo de comportamiento (Enviroment) que pueden modificar las características, como físicas, comportamiento de armas, comportamiento de NPCs y demás.

En cuanto a la marcación:

El “;” es usado como comentario.

#Terminal n  inicia la terminal n, donde n es el número de ID (ID Number) del terminal. Siempre debe empezar en 0, al igual que los scripts para las terminales en el nivel.

#LOGON n representará un recurso número  n de la carpeta PICT. Este recurso PICT ocupará la mayor parte de la pantalla con solo un poco de contenido de texto debajo.

#UNFINISHED indica los comandos que se mostrarán mientras la misión del nivel no esté completa.

#FINISHED indica los comandos que se mostrarán cuando la misión del nivel esté completa.

#INFORMATION mostrará una página sin ninguna gráfica, solo texto y comandos que hayan ingresado.

#PICT n representará un recurso número  n de la carpeta PICT. Mostrará el recurso PICT en una mitad de la pantalla y la otra mitad será completada por el texto y comandos que agregues.

#CHECKPOINT n mostrará en la mitad de la pantalla, un mapa con el objeto n como objetivo, y la otra mitad será completada por el texto y comandos que agregues.

#INTERLEVEL TELEPORT n teletransporta al personaje al nivel n que se asigne en el escenario. Configura n a 256 y finaliza la partida y envía al jugador al menú principal del juego.

#LOGOFF n funciona exactamente cómo #LOGON, pero representa el mensaje saliente de la terminal.

#END da por terminada la sección de texto UNFINISHED  o FINISHED.

#ENDTERMINAL n da por terminada la marcación de la terminal n.

### Comandos de marcación de texto.

$Cn cambia el color del texto por el color n, donde n  puede ser un número del 0 al 7. Los colores responden a los siguientes números:

0- Verde Claro

1- Blanco

2- Rojo

3- Verde Oscuro

4- Azul Claro

5- Amarillo

6- Rojo Oscuro

7- Azul Oscuro

$B inicia el texto en negritas. Finaliza con $b

$I inicia el texto en itálica. Finaliza con $i
$U inicia el texto subrayado. Finaliza con $u

Una marcación de texto típica que podrías encontrar es:

#TERMINAL 0


;sample terminal

#UNFINISHED

#LOGON 1600

#PICT 10000

$C6You must kill $B$Ieverything$i$b you find and not return until your deed is done$c6

#LOGOFF 1601

#END

#FINISHED

#LOGON 1600

#PICT 10001

Good work. Onward we go.

#LOGOFF 1601

#INTERLEVEL TELEPORT 01

#END

#ENDTERMINAL 0

### Herramientas Terminal
[En Desarrollo]
