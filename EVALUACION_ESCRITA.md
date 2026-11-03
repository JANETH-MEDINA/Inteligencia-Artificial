           ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
            EXAMEN TEÓRICO — PERCEPTRÓN, MLP Y CNN (GRUPO B)

                            Eduardo Alcaraz
           ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━


1 Datos del alumno
══════════════════

  ━━━━━━━━━━━
   Nombre    Morelia Janeth Medina MOntes
   Grupo   B 
   Fecha    03/11/2026 
  ━━━━━━━━━━━


2 Pregunta 1 — Por qué no basta “una sola neurona”
══════════════════════════════════════════════════

  1. Resume el funcionamiento de un perceptrón como “regla de decisión”.
  2. Explica la noción de *frontera lineal* sin escribir fórmulas.
  3. Da un ejemplo (aunque sea inventado) donde esa frontera *no*
     alcanza.


2.0.1 Respuesta
╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌

1.- Un perceptón funciona recibiendo datos de entrada y apartir de ello toma una decision para poder clasificar los datos en su respectiva categoria.
2.-Una frontera lineal es una linea recta la cual puede separar los datos en distintas categorias.
3.-Una compuerta logica como la XOR podria ser un ejemplo en donde la frontera no alcanza ya que con una sola linea no se pueden separar los datos y para poder separarlos se necesita hacer uso de las redes neuronales como en el caso de la flor iris .


3 Pregunta 2 — CNN: de píxeles a mapas
══════════════════════════════════════

  1. ¿Qué problema de *estructura espacial* ignora un MLP si aplana la
     foto?
  2. ¿Qué significa que un mismo filtro se aplique en toda la imagen?
  3. Además de clasificación de objetos, cita *dos* usos donde la CNN
     encaja bien.


3.0.1 Respuesta
╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌

1.- Al aplanar una foto un MLP puede perder la informacion de la posicion de los pixeles.
2.- Que un mismo filtro se aplique a la imagen significa que se buscan las mismas caracteristicas en toda la imagen.
3.-En un programa de reconocuimiento facial y en un analisis de imagenes de distintos deportes.


4 Pregunta 3 — Softmax, clases y decisiones
═══════════════════════════════════════════

  1. Diferencia un problema *binario* de uno *multiclase* en términos de
     salida de la red.
  2. ¿Qué lectura le das a las probabilidades que produce un softmax?
  3. Imagina tres carpetas de imágenes (tres riesgos o tres animales):
     ¿qué arquitectura de *salida* usarías y por qué?


4.0.1 Respuesta
╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌

1.- Cuando existe un problema binario hay solamente 2 clases y cuando es multiclase hay 3 o más clases.
2.- Se indican las probabilidades de que la entrada permanezca en su respectiva clase.
3.-  Yo utilizaria 3 neuronas con uns salida Softmax para que se pueda elegir la clase dependiendo la probabilidad.


5 Pregunta 4 — MLP: profundidad con sentido
═══════════════════════════════════════════

  1. ¿Qué ganas al apilar capas densas con activaciones no lineales?
  2. ¿Qué riesgo aparece si la red es *demasiado* grande para tus datos?
  3. Relaciona “capa oculta” con la idea de aprender representaciones
     intermedias (en palabras simples).


5.0.1 Respuesta
╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌

1.-
2.- Pudiera ocurrir un overfigting
3.- La capa oculta aprende de las caracteristicas intermedias antes de dar la respuesta.


6 Pregunta 5 — Entrenamiento sin magia
══════════════════════════════════════

  1. Explica qué es una *época* a nivel intuitivo.
  2. ¿Hacia qué “objetivo” se mueven los pesos cuando hablamos de
     minimizar el error?
  3. Si el learning rate es absurdo (muy grande o muy chico), ¿qué
     síntomas conceptuales esperarías?


6.0.1 Respuesta
╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌
1.- Una epoca es cuando se recorren completamente todos los datos de un entrenamiento que se haya realizado anteriormente.
2.-Los pesos se mueven para reducir el error que dan las predicciones dadas 
3.-Si es muy grande podria ser inestable, y por el contrario si es muy pequeño podria aprender muy lento.

7 Pregunta 6 — Bloques de una CNN
═════════════════════════════════

  Sin matemáticas, di el papel de cada pieza:
  1. Kernel / filtro convolucional
  2. Función de activación después de conv
  3. Max pooling
  4. Capa densa + softmax al final de un clasificador


7.0.1 Respuesta
╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌

1.-EL kernel es aquel que nos ayuda a detectar poatrones
2.-La funciónd e activacion  nos añade linealidad 
3.-El max pooling nos ayuda a reducir las dimenciones
4.- La capa densa + softmax nos ayuda a realizar la ultima clasificacion

8 Pregunta 7 — XOR y la historia del aprendizaje
════════════════════════════════════════════════

  1. ¿Por qué XOR se volvió un “contraejemplo” famoso?
  2. ¿Qué elemento de un MLP permite patrones que no son una sola línea?
  3. ¿En qué tipo de tabla/problema del mundo real seguirías usando algo
     tan simple como un perceptrón o un modelo lineal?


8.0.1 Respuesta
╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌

1.- XOR nos demuestra el limite que tiene un percepton
2.- Las activaciones son las que nos permiten  que los patrones no sean de una sola linea.
3.-

9 Pregunta 8 — De lo simple a lo abstracto en visión
════════════════════════════════════════════════════

  1. Contrasta lo que buscan capas tempranas vs capas profundas en una
     CNN.
  2. ¿Qué intuición da eso para *transfer learning* (aunque no lo hayas
     programado)?
  3. ¿Cuándo sospecharías que tu CNN es “profunda de más” para el
     dataset del curso?


9.0.1 Respuesta
╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌
1.- Las primeras capas ayudan a detectar los bordes y las capas más profundas nos ayudan a detectar las formas
2.- 
3.- Cuando funciona bien con los datos que ya se tenian pero con los datos nuevos no


10 Pregunta 9 — Análisis: matching problema → modelo
════════════════════════════════════════════════════

  Elige *Perceptrón/lineal* / *MLP* / *CNN* (una opción) y justifica en
  una frase:

  1. Predecir “compra / no compra” con edad, ingreso y visitas a la web
     (columnas numéricas).
  2. Detectar si hay un gato en una foto.
  3. Aproximar una frontera “curva” o a trozos en datos 2D tabulares.
  4. ¿CNN es la herramienta natural para predecir la siguiente palabra
     de un párrafo? Justifica y nombra una familia del curso más
     adecuada (RNN/Transformer a nivel nombre).


10.0.1 Respuesta
╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌

1.-Percepton lienal ya que puede trabajar bien con tabulares
2.- CNN por que normalmente trabaj con imagenes
3.-MLP por que puede llegar a funcionar con las frontera que no son lineales 
4.- 


11 Pregunta 10 — Análisis: auditoría de un equipo
═════════════════════════════════════════════════

  Un equipo entrega un modelo “muy preciso” en su laptop y falla con
  datos nuevos.

  1. ¿Qué diagnósticos conceptuales harías *antes* de tocar
     hiperparámetros al azar?
  2. Pide *dos* evidencias que deberían mostrar en la defensa (curvas,
     separación train/val, ejemplos de error, etc.).
  3. Redacta *tres* preguntas tuyas para comprobar si saben cuándo usar
     perceptrón, MLP o CNN (distintas a las del Grupo A si las conoces).


11.0.1 Respuesta
╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌

1.-
2.-
3.-¿Cuando es mas conveniente usar una CNN que una MLP?,¿Qué limitación tiene un percepton simple?,¿Por que un MLP puede resolver problemas no lineales ?
3.1.- Es más conveniente usar una CNN cuando se usan imagenes y una MLPM cuando 
