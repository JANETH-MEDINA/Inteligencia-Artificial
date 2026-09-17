# Operación Dino Crash (EDA conceptual)
## Bloque 1 - ¿Qué dataset necesitamos?
Necesitamos valores binarios los cuales nos indiquen el momento en el que el dinosaurio brinque, 
y para ello es necesario saber el momento exacto en el que el dinosaurio debe brincar.
Se pudiera ver con una compuerta lógica el si hay objeto brinca (1), y si no hay no brinca (0), ejemplo:

|Objeto 1|Objeto 2|=|Salto|
|1|1|= 1
|1|0|=1
|0|1|=1
|0|0|=0
Pero esto podría generar un problema al momento de que los 2 objetos estén presentes al mismo tiempo.
### Análisis del escenario 1 ¿Morirá en el siguiente frame?
#### Variable objetivo (Y): 
binario: 0 = no, 1 = si.
#### Variables de entrada (X): 
1.- ¿Hay muchos osbtaculos? - Preguntaría eso ya que entre más obstáculos se tengan más fácil es morir
2.- ¿Has jugado antes? - Es menos probable morir si tienes practica
3.-  
4.-
5.-
#### Granularidad: 
Para este análisis se necesitará un resumen por partida para saber si murió en el frame o no
#### Tamaño mínimo razonable: 
Para mi sería necesaria 1 partida, ya que lo que pregunta es en el siguiente, más no "siguientes"
#### Riesgo si el dataset está mal definido: 
Si hay algun error en especial de diseño (un caso en el que no se muestre el dibujo o imagen del objeto y mueras por causas que no sean visibles)
seria un problema muy grande en el dataset


### Análisis del escenario 2 ¿Cuántos puntos alcanzará esta partida al morir?
#### Variable objetivo (Y): 
Esta variable seria de tipo numérica ya que pide los puntos que se obtendran 
#### Variables de entrada (X): 
1.- ¿Cuántos puntos has realizado como máximo en tus ultimas partidas? - Esto ayuda a determinar una probabilidad de los puntos o bien, un aproximado
2.- 
3.-
4.-
5.-
#### Granularidad: 
Aquí tambien se necesita un análisis por partida para saber cuantos puntos se obtuvieron al finalizar la partida
#### Tamaño mínimo razonable: 
Solo bastaría con una única partida, para saber el puntaje que se obtuvo
#### Riesgo si el dataset está mal definido: 
Si el dataset presenta algún error de diseño en donde se muestran los puntajes, sería un riesgo, ya que no sería verídico el valor que muestre



### Análisis del escenario 3 ¿Qué tipo de obstáculo viene próximo?
#### Variable objetivo (Y): 
En este caso la variable sería una categoría, ya que estamos hablando del tipo de obstáculo que vendra
#### Variables de entrada (X): 
1.- ¿Cuáles fueron los últimos obstáculos que te aparecieron? - es importante saberlo ya que así podemos ver que opciones tendremos
2.- ¿Cuál obstáculo aparece más frecuentemente? - esto es más para un tema de probabilidad, para ver cuál es más probable que salga
3.- ¿Cuál obstáculo aparece con menos frecuencia? - nos ayuda a ver cuál es el menos probable que aparezca
4.-
5.-
#### Granularidad: 
Se necesita un frame por salto, para saber cuál es el objeto que se salto
#### Tamaño mínimo razonable: 
 Bastaría con una sola línea, ya que en esa línea se puede mostrar el obstáculo que deseamos saber
#### Riesgo si el dataset está mal definido: 
Si tenemos un error de diseño en el cual no se vean los obstáculos gráficamente no podremos observar el obstáculo siguiente



### Misión 2: Diccionario de datos (qué debe traer el CSV)
La Historia
Interceptaste un borrador de telemetría. 
En mi opinión si alcanza con esas columnas ya que tiene los apartados necesarios para mi precepción 

##### Columnas propuestas:
Columna	Tipo sugerido	Descripción breve
session_id	entero	ID de partida
frame	entero	Índice del frame en la partida
time_ms	entero	Tiempo desde que empezó la partida
score	entero	Puntuación en pantalla
speed	numérico	Velocidad del escenario
obstacle_type	categórica	none, cactus_small, cactus_large, bird
dist_obstacle	numérico	Distancia al próximo obstáculo (px)
jump	binaria 0/1	¿El dino está saltando?
died	binaria 0/1	1 solo en el último frame de la sesión
