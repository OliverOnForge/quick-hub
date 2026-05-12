
# Machine Learning

## Indice

- [Machine Learning](#machine-learning)
  - [Indice](#indice)
  - [Que es machine learning](#que-es-machine-learning)
  - [aplicaciones de machine learning](#aplicaciones-de-machine-learning)
  - [programa tradicional:](#programa-tradicional)
  - [Arepndizaje automatico](#arepndizaje-automatico)
  - [que es aprender](#que-es-aprender)
  - [porque usar machine learning](#porque-usar-machine-learning)
  - [en dnde si](#en-dnde-si)
  - [donde no usr ML](#donde-no-usr-ml)
  - [Featura engeineng](#featura-engeineng)
  - [Conjuntos de entrenamiento](#conjuntos-de-entrenamiento)
    - [validacion y prueba](#validacion-y-prueba)
    - [conjunto de entrenamiento](#conjunto-de-entrenamiento)
    - [### conjunto de validacion](#-conjunto-de-validacion)
    - [Conjunto de pruebas](#conjunto-de-pruebas)
    - [omitir el conjunto de validacion](#omitir-el-conjunto-de-validacion)
  - [cualdiades de un buen data set](#cualdiades-de-un-buen-data-set)
  - [Tipos de aprenidzaje automatico](#tipos-de-aprenidzaje-automatico)
    - [supervisado](#supervisado)
    - [No supervisado](#no-supervisado)
    - [aprendizajes hibridos](#aprendizajes-hibridos)
    - [batch](#batch)
    - [Online](#online)
    - [basado en modelos](#basado-en-modelos)
    - [basado en instancias](#basado-en-instancias)
    - [superficial](#superficial)
  - [profuncdo](#profuncdo)
  - [Tareas que se afreontan con machine learning](#tareas-que-se-afreontan-con-machine-learning)
  - [Diss](#diss)
  - [hiperparametros](#hiperparametros)
  - [parametros](#parametros)
  - [Scikt Lean](#scikt-lean)
    - [entrenado prediciendo](#entrenado-prediciendo)
    - [entrenando y trasformando](#entrenando-y-trasformando)
  - [regresion lineal](#regresion-lineal)
    - [modelo lineal](#modelo-lineal)
    - [regresion multiple](#regresion-multiple)
    - [reescribiendo la ecuacion](#reescribiendo-la-ecuacion)
    - [funcion de costo](#funcion-de-costo)
    - [MAs de una variable](#mas-de-una-variable)
  - [regresion logistoca](#regresion-logistoca)
    - [resolviendo la regrecion logistica](#resolviendo-la-regrecion-logistica)
  - [arboles de desicion](#arboles-de-desicion)
    - [como se crean](#como-se-crean)
    - [Regularmente en ML](#regularmente-en-ml)
  - [k-vecions cercanos](#k-vecions-cercanos)
  - [Mauinas de soporte de vectore](#mauinas-de-soporte-de-vectore)
    - [ecuacion del hiper plano](#ecuacion-del-hiper-plano)
    - [kernel](#kernel)
  - [K Means](#k-means)
    - [se necesita](#se-necesita)
  - [como funciona](#como-funciona)
  - [el baseline](#el-baseline)
  - [Metricas de la clasificaion](#metricas-de-la-clasificaion)
    - [elegir el meor modelo](#elegir-el-meor-modelo)
    - [Metricas de clasificaon binaria](#metricas-de-clasificaon-binaria)
    - [Accuracy](#accuracy)
    - [Recall](#recall)
    - [recision](#recision)
    - [F1 Score](#f1-score)
  - [Metricas de regresion](#metricas-de-regresion)
    - [Mean absolute error](#mean-absolute-error)
    - [Root mean squared error](#root-mean-squared-error)
  - [REtos de ML](#retos-de-ml)
    - [los datos](#los-datos)
    - [Pocos datos](#pocos-datos)
    - [soluciones generales](#soluciones-generales)
    - [cuantos datos son suficientes?](#cuantos-datos-son-suficientes)
    - [underfiting](#underfiting)
    - [overfitting](#overfitting)

---

## Que es machine learning

Es una rama de la ciencia de la computacion que se encarga de dota a las computadoreas de la capacidad de aprender de un conjunto de datos sin la necesidas de haber progrado explicitamente.

es una evolucion del software tradicional lo que busca es crear un programa que genera otro programa

## aplicaciones de machine learning

## programa tradicional:

1. entrada
  - Datos
  - Programa
2. Proceso
  - computo
3. reultados

## Arepndizaje automatico

1. entrada
  - Datos
  - Programa

3. programa

ejecutamos el programa

1. nuevos datos
2. Proceso
  - computo
3. resultado

## que es aprender

Se dice que un programa de computadorea aprende con un **experiencia E** con respecto a una **Tarea T** y una **medida de desempeño P** si su desempeño en **T** medido usando **P** mejora dada **E**

las maquinas no aprenden como los humanos, aprenden numeros e instruccinoes para generar prediciones

## porque usar machine learning

## en dnde si

- problemas donde no existe un buena solucion

- problemas para los que no existe un algoritmo tradicional

- problemas cuyas soluciones cambien constantemente

- para encontrar y explorar mas informacion relacionada a los datos

## donde no usr ML

- Tareas que ya tengas una solucion ques epueda ajustar al caso de uso

- Tareas dificiles para un humano

- cuyas soluciones deban ser explicadas de forma clara

- si no existe una relacion direacta y consitente entre la entrada y la salida

## Featura engeineng

Datos crudos

- Mediciones del clima
- Imagenes de una camara
- Audio de grabadoreas
- Fechas del calendario 

> los algoritmos funcionan con datos numericos

por ello se traducen los datos categorios y no estructurados a valores numericos

## Conjuntos de entrenamiento

-set de entrenamieto
-set de validacion
-set de prueba

### validacion y prueba 

-conjuntos ocultos

- esperamos que su desempeño sea bueno en datos que no conoce, no ha ahalizado o no ha visto antes.

### conjunto de entrenamiento

- El conjunto mas grande

- usado por el algotimo para entrenar y produceir el modelo

### ### conjunto de validacion

- Coonjunto de desarollo

- uado por el desaroollador para decidir que modelo usar

### Conjunto de pruebas

- Usado apra medir que tanbueno es el modelo entrnado

- este se usa para la toma de desicones

- el conjutno de entrenamiento debe ser los suicientemente representativo de lo ue vamos a encontrar en prdociion

algunos valores iniciales son

80%,. 10%, 10%
70%,. 15%, 15%
60%,. 20%, 20%

### omitir el conjunto de validacion

- cuando no existen suficientes datos

- usa validacion cruzada

## cualdiades de un buen data set

La calidad es subjetiva, depende del problema

los 7 aspecto principales

- Correctitud

los datos deben ser consitentes entre si, representar cantidades similares y reflejar el fenomeno medido

- competitud

los datos deben representar enteramente el fenomeno

- confaiblidad

tu darta set es coherente con otros sobre el mismo evento

- relevancia

tu data set debe contener solo la inforacoin necesario
no tener dupicados

- temporalidad

la informacion fue recolectda o representa le epoca adecuada
fue recolectada con la frecuencua adecuada

- Granularidad

es el nivel de detalle excato para el problema
los datos existen agregados o resumidos

- diponibilidad

que los datos no sean acccesibles

que tenas el permiso de usar los datos para tu proposito

> la calidad varia de dominio a domion 
>requiere comprender el problema que se va a resolver
> puede ir evolicionando con form avanza el desarollo

- data-cerntric

comienza con un data set limintado y mejoralo conforme pasa el timepo

## Tipos de aprenidzaje automatico

### supervisado

la informacion consta de variables de entrada y de salida
- solucion esperada (etiquetas)

- Las soluciones ""supervisan el aprendizaje"

se asume que existe una relacion entre cada entrada y la etiqueta correspondiente

### No supervisado

solamente tenemos informacion de entrada - no hay salidas o etiquetas

las computadora trata de encontrar/ descubrir patrones en los datos

### aprendizajes hibridos

semi supervisados
multitarea
reforzado

### batch

tambien llado offline

el modelo es entrenado y puesto en produccion

el entremainto sucede cada semana, mes o año

### Online

- aprendeizaje oicremental

- hay modelos que entrenan en produccion

- el entrenamiento sucede en cuestoon de minutos u horas

es mas caro y no vale la pena en muchos escenarios

### basado en modelos

usa la informacion para crear un modelo amtematico que reporduzca el comportamiento exhibido en los datosde entrenamiento

### basado en instancias

memoriza el dataset de entrenameito apra realizar predciciones en nuevos datos

### superficial

el modelo aprende directamente de las caracteristicas de los datos de entrada

machine learnin tradicional

## profuncdo

el modelo aprended directamente de las caratersticas de los datos de entrada y de las capas interiores del mismo
- redes neuronales y deep learning

## Tareas que se afreontan con machine learning

- regresion

aprendizaje supervisado

predecir un valor continuo - un numero

tareas de regresion

- clasificaion

aprendizaje supervisado 

predecir un valor discreto - etiqueta

- Clusterizacion

apredizaje no supervisado

agrupar un conjunto de lementos en grupos con otros objetos similares

- deteccion de anomalias

aprendizaje no superrvisado

detectar elementos que resulten sospechosos dentro de un conjunto

- generacion de contenido

se una combinacin de tareas

crea conetinod similar a un data set existente

- reduccion de dimensiones

arpendizaje no supervisado

reducir la cantidad de varialbe en un dataset

## Diss

> el machine learning no es magia

es imnportante realiar un analisis exhustovo apra entender nuetro data sert yty las laciones que en este existen


justifica tus desiciones
 
analizar tus datos tambien te dara herrameintas para jsutificae la realziacoin de un proyecto

el machine laening no fuincaino con datos ctrudos

analizar tus datos ayudara ad decidier que tecnicas de feature engeering aplicar

## hiperparametros

argumentos y desciiones tomadas por los desarolladores 

establecidos anteds de comenzar el entrenamiento

se usa el conjunto de validacion

## parametros

valores establecidos por el algoritmo entrenador

establecidos durante el entrenamiento

## Scikt Lean

normalemnte nodebes escriibr uin entrenamiento desde cero

en la industria se usan bibliotecas y frameworks bien establecidos para entrenar modelos

 es un kit cientidoco de python

 pip install scikit-lean

 otros ejemplos: scikit-spatial, scikit-time, scikit-image

beuna para principiantes y para personas con expeiecncia

buena para experimentar y para produccion

- aprendizaje supervisado

- no supervisado

-seleccion 
evalicauion
inspeccion
persistencai
- interface unificada

- es opne source

### entrenado prediciendo

- estimadores o estimatoirs

- las clases estimadores rtequieren ser entrendas con el metodo fit

### entrenando y trasformando

- trasformadores o trasformes
- las clases transformadas requieren ser entrenadas con el metodo fit
- trasformamos nuevos valores con trasform

## regresion lineal

- Metodo estadistico

- modela la relacion esntre dos variables

- una variable dependiente y una independiente

y = a + b*x

### modelo lineal

toma una suma poidnerada de las caracteristicas de entrada, mas un valor extra llaamdo sesgo (Bias)

### regresion multiple

y = b_0 + b_1x_0 + b_2x_1 + b_3x_2 + ... + b_nx_(n-1)

### reescribiendo la ecuacion

pred_i = w_0 + w_1*x_i

bias = w_0
weights = w_1

El objetivo es encontrar los mejores valores para bias y waists

### funcion de costo

root mean squared error

J = (1/n) sumatoria { i=0 -> n } (pred_i - y_i)2

donde:

pred_i = w_0 + w_1*x_i

sustituyendo

J = (1/n) sumatoria { i=0 -> n } (w_0 + w_1*x_i - y_i)2

comom ecnontrar los mejores parametros: 

- para minimizar la funcion de costo

- implica derivar parcialmente la funcion de costo

dJ/dw_0 = (2/n) sumatoria { i=0 -> n } ((w_0 + w_1*x_i) - y_i)2

dJ/dw_1 = (2/n) sumatoria { i=0 -> n } ((w_0 + w_1*x_i) - y_i)2

calculando w_0 y w_1

elegimos un valor inical para w_0 y w_1 - valores aleatorios funcionan

- vamos actualizando estos valores, simultaneamente, con las ecuaciones de lso gradientes: 

w_0 := w_0 - a* (2/n) sumatoria { -> n } ((w_0 + w_1*x_i) - y_i)

w_1 := w_1 - a* (2/n) sumatoria { -> n } ((w_0 + w_1*x_i) - y_i)*x_i

donde:

a = learning rate (velocidad de aprendizaje)

iteramso hasta que los valores de w_0 y w_1 dejen de cambiar

hay mejores metodos

- el grafiente decendiente no es la mejor manera de resolver la regresion lineal: pero es un algoritmo que vale la pena cnocer

para predecir:

podermos usar los valores aprendidos w_0 y w_1, colocarlos en al ecuacion inicial y comenzar a predecir valores.

para predecir
podemos usar los valores aprendidos w_0 y w_1, colocarlos en la ecuacion inicial y omenzar a predecir valores

### MAs de una variable

existe la regresion lienal multivariable, es una extencion de una regresion variable multiple

## regresion logistoca

Usada para probleas de clasificacion binaria

el modelo es muy similar al de la regresion lineal y = a + b*x

modelo de regresion logistica

tomamos la regresion lineal 

z = w_0 + w_1 * x

la pasamos por una funcion sigmoide-trasforma cualquier valor a uno entre 0 y 1

{sigma} (Z) = 1 / (1+e^(-z))

sustituimos z en  {sigma}

{sigma} (Z) = 1 / (1+e^-(w_0 + w_1 * x))

con esto ya podemos definir etiquetas una etiqueta para valores de 1  y otra para valor 0 pudiendo segmentar los datos y haciendo que el modelo los calsifique

### resolviendo la regrecion logistica

gradiente descendiente - no tan efectiva

la regresion logistica es usada para realizar clasificacnion binaria

minimizara la distacion entre el resultado de la funcion sigmoide y el valor real (mapeado entre 1 y 0)

una vez entrenado el modelo

podemos tomar los aprametros W aprendidos y generar nuevas prediciones

pred_i = 1 / (1+e^-(w_0 + w_1 * x_i))

la direfrencia es que no vamos a obtener un valor contreto sino un valor en un rango entre 1 y 0

lo que debemos hacer es estableder un umbral a partir del cual el varo se conciderara como 1 o 0

es posible calibrar la regresion logistaca con el fin de obtener mejores resultados para cada problema individual

## arboles de desicion

Nos ayudan  visualizar posibles resultados de una serie de desiciones relacionadas

- determinan el mejor camino para obtener el maximo beneficio

- tabmien pueden ser usados para clasificar cosas, usualmente objetos.

### como se crean

tradiciionalmente son hechos a mano

revisando todos slos escenarios posibles

y si usamos machine learning?

se selecciona una varibale y un valore del dataa set para generar dos nodos, donde cada uno contiene una version reducida del data set y este proceso es iterativo y recursivo hasta llegar a un nodo del cual no se posible realizar una division de las observaciones

espues al ralizar una predicion tomamos la instancioa final de los datos y seguimos las deciciones validadas por el arbol.

Algoritmos

Cada algoritmo tendra la mejor forma de separar el dataset

- ID3
- C4.5
- CART
- CHAID
- MARS

prunning

podemos coratar algunas ramas del abol para reducir el over finting, y que el arbol pueda tomar las mejores desiciones

### Regularmente en ML

se crean varios arboles, cada uno con pequñas variaciones en las desiciones con el objetivo de tener varias opiniones para lograr predecir categorias de mejor forma

estos son llamados rendom forest (bosques aleatorios)

son de las mejores algoritmos de machine learning

- se concideran un buen comienzo para comenzar una tarea de clasificacion o de regresion en maechine learning.

- existen buenas implementaciones de random forest en los frameworks

- tambien pueden resolver problemas de regresion con un modelo similar

## k-vecions cercanos

modelo predictivo  para llevar a cabo al clasificacion 

se usa a su relativa simplicidad de implementacion

es una forma de medir la distancia entre observaciones

asumir que obejtos cercanos son similares

- no aprende los patrones escondidos en los patones en al informacion

- memoriza el data set

- esa es la "simpleza"

k es un hiperparametro

representa el valor de vecinos cercanos ej:

el valor de K-k= 1 tomamos el vecino mas cercano

el valor de K-k= 2 tomamos a los dos mas cercanos y asi sucesivamente hasta n donde n seria el numero total de elementos ene l dataset

K-k=n

hay fomras de seleccionar k

un valor pequeño o muy alto crea un mal modelo

experiemntacion es la mejor herramienta

la idea es entrenar y reentrenar el modelo para  lograr encontrar el mejor valor para nuestro modelo

##  Mauinas de soporte de vectore 

svm

modelo de clasificaion bianria

se usa cuando queremos clasificar usando las etiquetas 1 y -1 

se colocan las instancias en un espacio multidimencional

una vez colocadas vamos a intentar ubicar una divicion adecuada para los datos (hiperplane)

### ecuacion del hiper plano

b_0 + b_1*x_1  + b_2*x_2 + ... + b_m+x_n = 0

hiperplano en 2D

b_0 + b_1*x_1  + b_2*x_2 = 0

b+ mx = y

tomando esta linea como el valor '0 de referencia entoces podemos definir la psocion de las etiquetas en realcion al plano

la idea es encontrar el parametro b que permita aprender los parametros b del palo para encontar los valores que haga una separacion mas optima de los datos de entrenamiento

esto se logra maximisando un valor conocido como margen

asi como en la regresion lineal buscabamos, minimizar la cantida de perdidas, en este modelo maximisamos la cantidad de margin  que es la distancia ente los puntos mas cercanos al hiperplano con el margen {gama}

esto impone una restriccion muy dura al margen y es que este debe estar vacio en cuanto a que no debe haber ningun punto (valores del dataset) dentro de este

la tarea del algoritmo de svm es encontrar la mejor linea para separar las dos clases de objetos

en caso de no poder usar una linea para separar los datos se usa un

### kernel

trasforma los datos 

ejemplo con perros y gatos

caractersitica_nueva = orejas2 + bigotes^2

cambio de dimencionalidad den los gatos 

{numeros reales}2->{numeros reales}3

siendo asi mas facil encontrar una trasformacion lineal valida

este es otro hiperparametro del algoritmo

cambia la dimencionalidad de la informacion

la hace liealmente separable

tambien es posible relajar la resticcion del hiperplano, permitiendo que existan puntos dentro del margen este parametro es conocido como 'c'

si bien este parametro permite distinguir entre dos clases, tambien es posible extenderlo para ser multiclase.

## K Means

- aprendizaje no supervisado

- clusterizacion o agrupamiento

- agrupacion "natural"

requisitos:

ayuda a describir grupos sin necesidad de etiquetar cada obvservacion de forma individual

### se necesita

- un conjunto de observacoines y sus caracteristicas.

- una forma de medir la distacion entre observaciones

- la suposicion de que elementos similares estan cerca el uno del otro

muy pareceido al modelo de kNN, pero no supervisado

## como funciona

- observaciones don d caracteristicas

- representadas como un vector en el espacio de n dimenciones

una vez definiod los valores en el espacio podemos comenzar con el algoritmo de entrnamiento que es un algoritmo iterativo

1. seleccionamos k dentro del espacio

para ello existen diversas formas para encontrar la locaclizacion de estos puntos

pero al inicio se puede considerar una posicion aleatoria

estos puntos son conocidos como centroides, promedios o means

2. asignamos una etiqueta a cada uno de los puntos, deacuerdo a la media mas cercana qued escribe cada uno

se dice entonces que los puntos pertenecen a estos grupos

3. recalcular los centroides, basandose en la etiqueta que les fue asignada

4. revisar si existe diferencia con la posicion de los centriodes con los cuales se comenzo la iteracion y las nuevas posiciones

5. si existe diferencia entonces volvemos al punto 2 pero toamndo estos nuevos centrides como lso centriodes iniciales

6. si no existe diferencia se concidera el algoritmo como terminado

asi obtnemos un modelo entrenado

7. una vez que tenemos k grupos nos toca a nosotros darle una interpretacoin a cada uno de ellos

que es le valor k

un hiperparametro

siendo que el elegir un valor correcto para k sea una de las partes mas importantes al usar este algoritmo

- se puede usar la intuicion

- metodo de codo

## el baseline

antes de comenzar con ML

- trata de solucionar el problema por otros metodos

- intenta una solucion mas simple

- que es lo que pdoemos esperar de un modelo

es un modelo creado a aprtir de simples reglas de negocio

estadistica descriptiva

regresion lineal o logistica - simple

¿tengo que crear un sistema de machine learning mas sencillo antes de crear uno mas complejo?

si

el primer modelo debe ser sencillo

- la clave es no invertir muco tiempo en este primer intento

- nos da una idea de lo que es pisoble y lo que podemos espera de cualquier otro modleo

- responde a la pregunta: ¿es siquira posible resolver este problea con ML?

- un baseline puede ser usado como un peldaño hacia un mejor modelo

## Metricas de la clasificaion

### elegir el meor modelo

es neceasrio medir el desempeño del modelo de ML para saber cual es mejor.

- esto hace mas facil con modelos supervisados

- para decidir que tambueno es el modelo ya entrenado esusar una o varias matricas para medir su desempeño.

Ejemplo: si estas realizando ua prueba de si una persona tiene una enfermedad

independiente mente de la verdad

- si la prueba dice que el individuo tiene la enfermedad el resultado es positivo

- Si la prueba dice que el individuo no tiene la enfermedad es considerado negativo

### Metricas de clasificaon binaria

| valor | valor real positivo | valor real negativo |
| valor predecido positivo | verdadero positivo | Falso positivo |
| valor predecido negativo | falso noegativo | verdadero negativo |

resultados de estas metricas

0 es malo
1 es bueno

y estos se pueden convertir en porcenteges

### Accuracy

- Exactitud

- la metrica mas usada en clasificacion

- relacion de prediuciones correctas vs total de predicciones hechas

su fromula es

accuracy = (TP + TN) / (TP + TN + FP + FN)

TP - verdadero postivo
FP - faslo positivo
TN - Verdadero negativo
FN - falso negativo

### Recall

- exahustividad

- relacion de instancias correctamente clasificadas vs instancias que originalmente existian

RECALL = TP / (TP + FN)

TP - verdadero positivo
FP - Falso positivo
TN - verdadero negativo
FN - faslo negativo

### recision

- precision

precicion != de exactitud

- Relacion de las instancias clasificadas correctamente vs todas las que fueron clasificadas

Precision = TP / (TP + FP)

TP - verdadero positivo
FP - Falso positivo
TN - verdadero negativo
FN - faslo negativo

A veces bo es posible elegir

- ambas metricas son importantes o queremos darle valor a laso dos

### F1 Score

- combina recall y precision

- media armonica

- usala cuando ambas cifras son importantes

F1 = 2 * ( Precision * Recall / Precision + Reacall)

## Metricas de regresion

El error acumulado no es la mejor opcion, ya que existen opciones mas robustas

### Mean absolute error

MAE = (1/n) sumatorio { i = 1 -> n} ( | y_i - y_i' | )

y_i = valor verdadesro pra el ejemplo i

y_i' = valor predicho para el ejemplo

n = numero de ejemplos

### Root mean squared error

RMAE = ( (1/n) sumatorio { i = 1 -> n} ( y_i - y_i' )^2 )^(1/2)

y_i = valor verdadesro pra el ejemplo i

y_i' = valor predicho para el ejemplo

n = numero de ejemplos


cual metodo elegir?

- los dos entran orientadas negativamente: menos es mayor

- LAs dos van de 0 a infinito

no es necsacion elegir

Mean absolute error

- facil de entender
- facil de interpretar

Root mean squared error

- Recalca los grandes erores

- ayuda cuandlo los cassao extremos deben ser penalizados mas fuertemente

## REtos de ML

### los datos

- es el alimento pricnicpal del machine learnisng

- Necesitamos calidad

- Necesitamos canitdad

garbage in, garbage out

### Pocos datos

es un problema que limita las posibilidades de un equipo de ciencia de datos

- es un problema si vas a comenzar con algo nuevo, fuera de la linea de negocio de la organizacion

- Pocas etiquetas: puedes tener un monton de datos pero no las etiquetas correspondientes

- falta de generalizacion: el modelo se fija mucho en las caracterisitcas de nuestro data set de entrenamiento

- falta de reresentatividad

- desbalance: mas informacion de una sola clase o dsitribucion

- podemos tratar de mitigar este problema con un buen modelado

- falta de optimizacion: no hay suficiente informacion

- el modelo no aprende los patrones dentro de nuestro dataset

### soluciones generales

- tratar de conseguir mas datos:  podemos generalos usanto dataset sintetico, data augmentation.

- trabajar mas a detalle en el modelo y elegir uno que tome en cuenta el desbalance entre las clases del data set

- Usar transfer learning: usar un modelo ya entrenado y solamente personalizarlo con tu dataset pequeño

### cuantos datos son suficientes?

- usualmente los stakeholders quieren preveer costos

- se pueden usar para verificar la viabilidad de atacar un problema con machine learning

de que depende:

- de la complejidad del problema

- la cantidad de clases en las que hay que clasificar

- de las tecnicas que vas a usar

revisa la literatura:

- siempre es bueno revisar la opinion de otras personas

te da una idea de lo que se puede lograr

usa fatores:

- Clasificion: multiplica el numero de las classes esperadas por 10, 100, 1000...

- otros problemas: el numero de columnas diferentes x10, 100 o 1000

Siempre es un estimado

- debe quedar claro que el numero que des es suceptible a camvios conforme se avanza en la experimentacion

- mas datos es generalemente es mejor (hablando de cantidad de ejemplos)

- presta atencion a los rendimientos decrecientes

- tabien debemos cuidar del modeloy el algoritmo que usamos para entrenarlo

### underfiting 

subentrenamietno: sucede cuadno el modelo no logra capturar los patrones ocultos en el conjunto de entrenamiento y opbiente malos resultados

diagnostico

- tomar el modelo ya entrenado

- revisar el desempeño en el conjunto de datos de entrenamiento

- si nos da un resultado malo en entrenamiento, estamos sufriendo underfiting

- si estamos empleadno un algoritmo iterativo, podermos monitorearlo constantemente

ejemplo:

estas estudaiando para un examen

-tienes poco ejercicios para practicar
- no le entendiste bien a la clase
- no logras entender que es lo que se tiene que hacer

prevenir y evirat

- incremetnar la complejidad del modelo
  - uasr mas capas o neuronas
  - en soporte de vectores usa otro kernel
  - en caso de regresion podemos incrementar el grado de polinomio


- oteniendo mas infomracion
  - incrementar las variables independeintes
  - mas atos para que el modelo aprenda
  - usa feature engineering o extrae mas informacion

en algoritmos iterativos:

- dejar continuar el entrenamiento por mas tiempo
- solo funciona con algoritmos iterativos

### overfitting

sobreentrenamitno

sucede cuadno el modelo se "aprende" de memoria los datos en el conjunto de entrenamientoy no los patrones que existen en ellos

el aprendizaje automatico se trata de "aprender patrones" en el entrenamiento para generalizar a valores reales

Un modelo que no generaliza bien tendra problemas en produccion

diagnosticar:

- toma el modelo ya entrenado
- revisa el desempeño en el conjunto de datos de entrenamiento y de prueba
- si nos da un resultado bueno en entrenamiento, pero malo en la prueba, el modelo tiene opverfitting

ejemplo:

estas estudiando para un examen:

- te concentras mucho en aprender las respuesta  algunos ejercicios y los memorizas

-pero al final solo aprendite valores no eres capaz de resolver ejercicios nuevos

com evitar:

- incrementar la cantidad de informacion
  - sin descuidar la calidad de los datos

- reducir la complejidad del modelo
  - moidelo de bosques_ reducir la profundidad de los arboles
  - red neuronal: reducir la cantidad de neuronas o capas
  - regresion: reducir el grado del polinomio

  - deneter el entrenamiento de forma temprana
    - solo funciona para olgoritmos iterativos

Over fiting y underfitting

-ambas son condiciones "naturles" de un modelo de ML

- tienes que encontrar un balance etre estos dos conceptos

