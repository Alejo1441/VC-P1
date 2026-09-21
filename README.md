## Práctica 1. 


### TAREA1 :Sin herramientas de IA, crea una imagen, p.e. de 800x800 píxeles, con la textura del tablero de ajedrez. Una vez resuelto de forma manual, resuelve la misma tarea usando un asistente de IA de tu elección (Claude, ChatGPT, Copilot, etc.). Compara ambas versiones en el informe de la práctica.

Para la primera tarea lo que se ha realizado es lo siguiente:

- se establecen los pixeles que van a ocupar, que en este caso son 800, y cuadra perfectamente ya que el tablero de ajedrez tiene 8 filas y columna, por lo que cada 
"cuadrado" del tablero ocuparan 100 pixeles

- luego creamos una imagen totalmente negra, del tamaño del tablero de ajedrez y asi nos permite solo tener que pintar los "cuadrados" blancos del tablero

- hacemos un bucle for de 8 y recorremos por filas, si el numero de la fila que esta es par, pintamos el primer cuadrado y luego de forma salteada, y si es impar,
 pues al contrario, el primero no lo pintamos, y pintamos de forma salteada a partir del segundo

- pintamos todo el tablero por ultimo


### TAREA 1 CON IA

la diferencia básicamente es que, lo que yo he realizado con un bucle for, Gemini en este caso, lo realiza directamente al crear un tablero y modifica las filas y 
columnas para pintar directamente ( no tengo captura de gemini para este ejercicio)

### TAREA 1 conclusión

Gemini, en este caso, lo realiza de forma más elegante y sin ningún bucle for, a esto se le conoce como indexación con saltos, según gemini, y con interpolation
'nearest' también hace que los bordes no se difuminen y se vean mas nítidos


### TAREA 2:  Crear una imagen estilo Mondrian (un ejemplo https://www3.gobiernodecanarias.org/medusa/ecoescuela/sa/2017/04/17/descubriendo-a-mondrian/) con las funciones de dibujo de OpenCV. No hagas uso de herramientas de IA, parte del ejemplo anterior.

en esta tarea, se ha realizado un cuadro estilo Mondrian, y siguiendo las instrucciones, seguí el ejemplo anterior y realize varios rectángulos de diferentes 
colores (blanco, rojo, azul y amarillo), aprovechando, que el fondo es negro, para no tener que dibujarlo y siempre dejando, en mi caso 25px de distancia entre 
rectángulos y el borde, lo mas complicado del ejercicio era saber donde estabas pintando y asegurarse de no pintar encima de otro rectángulo y dejar el espacio 
suficiente entre ellos



### TAREA 3 Pintar círculos en las posiciones del píxel más claro y oscuro de cada fotograma captado por la cámara. ¿Funciona de forma fluida o a saltos? En el segundo caso, ¿podrías acelerarlo? Si haces uso de herramientas de IA, incluye la conversación.

para este ejercicio, me he fijado en otros ejercicios que ya estaban y he reutilizado una parte, ya que lo que hago en este ejercicio es bastante simple, recorro 
todos los pixeles de la pantalla con un doble bucle for, y en cada pixel saco el numero de los colores que tienen en RGB, y luego los sumo en una variable brillo,
luego hago dos if, para saber si es mas grande o mas pequeño de todos los vistos y guardo su posición y por ultimo los pintos con un cv2.circle azul para el mas brillante y negro para el mas 
oscuro. Como no se me ocurría una forma de hacerlo que fuera sin dar tirones le pregunte directamente a gemini, para saber la 
 respuesta y básicamente, hay que convertir la imagen a escala de grises, y que también hay funciones que devuelven los valores máximos y mínimos de grises, el código propuesto por gemini es mucho mas compacto y mejor optimizado
https://share.gemini.google/fW6pMercBeAL
y no realizo ningún cambio al mio, ya que fue lo que se me ocurrió hacer a mi, y la otra respuesta esta dentro del enlace




### TAREA 4:TAREA: Llevar a cabo una propuesta propia de pop art. Incluye fuentes consultadas. Si haces uso de herramientas de IA, incluye la conversación.

Para esta tarea he partido del ejercicio anterior, donde se dividía la cámara en 4 y se hacia un pop art, y lo que he hecho, ya que no tengo mucha idea de arte, es preguntarle a gemini, que colores que debería quitar en RGB, para crear un arte pop estilo Andy Warhol, luego a partir de ahi, me puse a  experimentar por mi cuenta, y deje los que mas me llamaron la atención.
https://share.gemini.google/89cG0qgdAZgJ