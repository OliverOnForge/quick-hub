
# Css Flex y Grid

## Indice

- [Css Flex y Grid](#css-flex-y-grid)
  - [Indice](#indice)
  - [Flexbox](#flexbox)
  - [Grid](#grid)

---

## Flexbox

Hoy es el curso de css y lo dejamos si os habéis perdido la primera parte pues
0:05
lo que sea pues queréis echarle un vistazo que sepáis que lo tenemos aquí 1 hora 45 buenas tardes Mira esto con mi
0:11
peinado de aquí qué teníamos Pues aprende css gratis curso de css de css desde cero para principiantes vamos a
0:17
ver otra vez Vamos a repasar Cómo dejamos lo del box icing el modelo de la caja porque eso es muy importante que lo
0:22
entendamos Y a partir de ahí vamos a ver también lo que es el overflow vamos a ver que el tema de desbordamiento una
0:28
cosa que da muchos problemas a mucha gente y de hecho el chiste más mítico de css viene por culpa del overflow luego
0:35
vamos a ver los diferentes position porque la gente se hace un lío con los position qué es esto de position static
0:42
absolute sticky fix Cuál es la diferencia de cada uno y vas a ver la diferencia y te juro que hoy los
0:47
entiendes hoy los vas a entender de una vez por todas y vas a decir pues n er tan difícil lo que pasa es que te lo
0:53
estaban explicando mal luego qué más Vamos a ver también el Z Index una cosa que es muy compleja pero lo vamos a
0:59
simplif explicar al máximo y también lo vas a entender y finalmente Flex vale Flex es el modelo de la caja flexible
1:06
que muchas veces a muchas gente le vuelve loco y también lo vas a entender superfácil porque con ejemplos prácticos
1:12
todo se se entiende se aprende y se se valora Así que vamos a ver todos esos
1:17
temas hoy aquí y vamos a empezar con el modelo de la caja que lo dejamos al final pero lo vamos a repasar rápidamente solo para ver si ha quedado
Modelo de la Caja
1:24
claro vale la semana pasada dejamos el modelo de la caja el modelo de la caja de de css es básicamente Cómo se
1:31
calculan el ancho y el alto de una caja no cómo tenemos el contenido de una caja y aunque Nosotros le decimos 100 píxeles
1:37
por 100 píxeles de ancho y de alto esto en realidad no mide Exactamente eso y lo
1:43
vas a ver y lo cual esto es uno de los grandes problemas que mucha gente tiene en css si miramos Cuánto mide Esto vale
1:49
vamos a poner Cuánto mide fíjate aquí verás aquí que sale la la pone el altura y anchura pone 120 por 120 pero fíjate
1:57
que aquí pone alto y ancho 100 píxeles Qué pasa que por defecto la caja en css
2:03
es el alto y el ancho más el padding y el borde Qué significa esto que si tú
2:09
pones un alto y un ancho de 100 píxeles y le dices que tiene que rodear un
2:15
padding de 10 píxeles esto ya va a ser 120 porque son 10 píxeles arriba abajo
2:21
izquierda derecha Aquí tienes un ejemplo super bueno no ves que tenemos el ancho y el alto de 100 píxeles y luego el
2:28
padding pero si le ponemos un borde además borde de 10 píxeles esto lo que
2:33
va a ocurrir es que va a hacer que nuestra caja pues ahora ocupe 140 píxeles vale 140 píxeles el modelo de la
2:41
caja por defecto se calcula Así es el alto y el ancho más el padding más el
2:47
borde y esto por qué es un rollo porque te viene tu ux tu amigo ux o amiga ux y te dice yo quiero que este botón sean
2:54
150 píxeles y claro Qué haces pues tú dices vale pues 150 píxeles dice vale
3:00
150 píxeles vale Y esto Esto es un botón vale dices vale genial he hecho un botón
3:06
aquí maravilloso y te dice y tiene que ser de 24 píxeles Claro tú haces esto
3:11
pero luego te viene la persona de ux y te dice a ver a ver dice pero esto está mal esto está mal y es que resulta que
3:18
aunque tú lo has puesto aquí 150 píxeles resulta que la sección ocupa 190 y es
3:24
por este problema no el problema es que la medida que tú le estás poniendo hay que sumarle el padding el borde Cómo se
3:30
arregla esto Esto es como funciona por defecto y muchas veces este problema igual no lo encontráis porque por arte
3:37
de magia y por algo todo poderoso resulta que se ha utilizado algún tipo de reseteo de css o alguna propiedad que
3:44
hace que esto funcione de una forma distinta y cómo funciona esto pues utilizando Box sizing Border Box vale Y
3:51
fíjate que ya cambia aquí bastante la cosa por defecto Cuál es es content box el box sizing lo que mide la caja viene
4:00
por el content box que quiere decir que vamos a sumar el contenido más el padding más el borde vale Y eso va a ser
4:07
el el el ancho y el alto va a venir por esa fórmula pero si le ponemos Border
4:13
Box vamos a ver que nos cambia totalmente y el Border Box Qué quiere decir pues que si tú aquí le pones que
4:19
mide 150 píxeles va a ser 150 píxeles y si el ancho le dice que son 24 el ancho
4:25
van a ser 40 aquí 40 bueno por qué pasa esto mira es super interesante esto pasa
4:31
justamente por el tema del overflow No aquí podemos ver que pone 40 porque en realidad lo que está haciendo es que el
4:36
texto ocupe un poquito más pero aún así podríamos llegar a un momento en el que ahora realmente sí que no vamos a ver
4:41
ningún ves si ponemos 64 cuando ya el texto ocupa menos pues vamos a ver que sí que son 64 vale Esto del texto está
4:48
bastante interesante porque por defecto veis que esto funciona así O sea el texto se sigue viendo y por lo tanto la
4:54
altura se ve Se ve que tiene un efecto en en en justamente esto también tener
4:59
en cuenta una cosa si se cuenta el padding y el borde claro el padding son 10 + 10 porque es arriba y abajo más 10
5:07
del borde más 10 arriba y abajo serían 40 o sea que si vosotros le ponéis 14
5:13
píxeles 24 tal como mínimo tienen que ser 40 porque ya el padding y el borde
5:18
son 40 Aunque vosotros pongáis una altura e intentéis forzarla de que sea un píxel si el padding y el borde ya es
5:24
más pues ya va a ser esa altura vale eso utilizando el Border boox tened en cuenta Esto vale Ya la ura mínima va a
5:30
tener que ser la que tenga el pading el Border y vas a ver que en cuanto yo suba esto Fíjate que ya sí que va empujando
5:35
esto Okay entonces ahí ya lo tenemos y ya teníamos este problema solucionado Así que ya sabes cómo funciona el box
5:42
sizing Border boox y es el que Por qué mucha gente y Esta es una pregunta que muy poca gente sabe la respuesta o la
5:49
entiende Porque alguien dirá si todo el mundo carga esto sabes todo el mundo pone el box icing todo el mundo carga
5:55
esto sabes todo el mundo el box icing Border Box Box iing Border Box Vais a ver que en todos los sitios Mira qué es
6:02
y para qué sirve Mira está midu dep pero este este fue el artículo que en 2012 en
6:08
2012 popularizó el tener que utilizar Box sizing Border boox Y entonces la
6:13
pregunta del millón que muchas veces mucha gente se hace sobre todo gente que no es que no sabe mucho css es Oye o o
6:20
no sabe cómo funciona el mundo del desarrollo web es Oye y por qué tenemos que aplicar esto a todas nuestras páginas web si lo hacemos constantemente
6:27
esto Oye por qué no por qué no lo cargamos por defecto Por qué los navegadores no lo cargan por defecto y
6:34
La respuesta es la retrocompatibilidad esto es una cosa que apareció en 2012 tú
6:40
Imagínate que de repente por lo que sea vale Imagínate que aquí cambiamos por
6:46
defecto es esto y de repente los navegadores dicen no ahora el el alto y el ancho se calcula así pum pues
6:53
imaginad la de páginas web que se iban a romper de golpe millones y millones de páginas web entonces entonces Muchas
6:59
veces aunque ahora queramos trabajar así lo cierto es que por por defecto no trabaja así se lo tenemos que Añadir ya
7:06
sea de forma indirecta si utilizas telwin ya añade esto sin que tú te des cuenta pero ya sea de forma directa que
7:12
tú lo tengas que Añadir y la razón por la que no lo añade los navegadores es retrocompatibilidad que amigos y amigas
7:18
Esta es una de las razones por las que muchas veces tanto javascript como css como html tienen que evolucionar
7:24
teniendo en cuenta todo lo que tienen detrás algo que no hay ningún lenguaje ahí fuera que tenga que ocurrir Porque
7:31
pueden trabajar con mayors cosas que cosa que con estos tres lenguajes es un poquito más complicado también trabajan
7:37
con Mayos pero normalmente son 100% retrocompatibles porque si no romperían
7:42
muchas páginas web vale solo para que lo sepáis ahora que ya tenemos esto vamos a ver un caso muy típico imaginad que
Desbordamiento: Overflow
7:48
teníamos Este ejemplo aquí con esto es una caja 100 pixels y todo esto vamos a poner el borde el vamos a utilizar el
7:54
Border Box vale Vamos a ponerle que sea un poquito más grande y un error muy típico que tenemos aquí es el tema del
8:01
desbordamiento Y esto es uno de los memes de css por ejemplo este de css is
8:08
awesome no seguro estoy seguro que esto lo has visto alguna vez en alguna camiseta o lo que sea imaginad que
8:13
tenemos el font size y lo hacemos muy grande vale pum qué pasa con esto que
8:19
fíjate que el texto está saliendo de la caja está desbordando esto ocurre cuando
8:25
nosotros tenemos un tamaño fijo de una caja Pues nos podemos encontrar que el contenido No cabe en esta caja esto os
8:32
habréis pasado un montón seguro que habéis visto alguna taza eh alguna camiseta y tal vale es el el chiste
8:38
típico cs6 awesome y aquí sale el awesome no Bueno hay que entender que
8:44
este meme que la verdad que está bastante divertido en realidad ocurre por no saber css porque css sí que
8:51
soluciona esto y hay diferentes formas de de solucionarlo el tema es que si tú le estás forzando el alto y el ancho es
8:58
normal Claro si pasase al revés también le harían memes si pasase al revés haría otro meme porque imagínate que tú le
9:04
pones un texto tú le has dicho esto tiene que ser de 150 por 150 y le pones
9:09
un contenido y se lo salta verdad pues el tema es que también sería al revés un problema al final tiene que tomar
9:15
prioridad sobre uno de los dos y la prioridad se la da a la altura y la anchura que tú le has dicho esto es lo
9:20
que se le llama un desbordamiento y hay diferentes formas de solucionarlo Vale entonces cómo se se soluciona esto por
9:28
defecto cuando cuando un contenido desborda qué se hace cómo está funcionando está funcionando como un
9:34
overflow visible que es lo que justamente está pasando este sería el valor por defecto está haciendo que el
9:40
overflow o sea lo que está desbordando es visible esto es por defecto porque si no podríamos tener un montón de
9:47
problemas pero obviamente tenemos otros valores también este es que el contenido
9:52
no es recortado y se dibuja fuera de la caja contenedora pero tenemos otros por ejemplo tendríamos el de hidden El el
9:59
deiden directamente lo que hace es Oye el contenido lo vamos a recortar y no lo puedes no lo puedes ver De ninguna forma
10:05
está ahí porque está ahí pero no lo vamos a mostrar y esto muchas veces se utiliza justamente para eso para evitar
10:11
que una vez que sale y se desborda el contenido pues Que aparezca mal por ahí en medio okay Ahora hay veces que pese a
10:19
todo nos gustaría poder acceder a ese contenido Fíjate que aquí no podemos acceder a ese contenido no podemos ver
10:24
qué es lo que hay debajo de esto no no sabemos noy No hay forma de ver ese contenido del debajo de esto no lo
10:30
podemos ver entonces qué podemos hacer otra solución es el de scroll scroll lo
10:36
que hace es recortar el contenido y el navegador web va va a utilizar unas
10:41
barras de desplazamiento donde se haya recortado el contenido si es que se ha recortado o no vale Y esto lo que va a
10:47
hacer es prevenir que se Que aparezca fuera pero vas a poder moverte por dentro gracias a las barras fíjate que
10:54
tenemos unas barras tanto horizontales porque el contenido Sale tanto de derecha de izquierda a derecha de forma
10:59
horizontal como vertical vale Así que así sería con el workflow scroll pero imagínate si tú tienes el visible sale
11:06
así si le pones el hidden está ahí el contenido pero no puedes acceder no puedes scrollear y entonces tendrías el
11:12
scroll que recorta Exactamente igual pero ahora sí que te pone unas barras para poder moverte y además de esto
11:19
teníamos uno más que sería el auto que si vas a utilizar scroll normalmente es el recomendado por auto Qué quiere decir
11:26
pues que dependiendo del navegador lo que van a hacer es poner las barras de desplazamiento pero igual en otro
11:31
dispositivo no pone barras lo pone de otra forma o sea lo va a hacer por de forma automática Depende como sea el
11:37
desplazamiento en ese sitio normalmente son barras vale pero lo digo por si ves el auto que sepas que se trata de esto y
11:44
lo interesante del auto es que si por lo que sea si tú pones el scroll le estás forzando Ya que siempre salgan las
11:49
barras y en Windows es posible que si por lo que sea esto sí que cabe aquí Imagínate que solo pones esto puede ser
11:57
que en otros navegadores veas aquí la barra pero la veas desactivada entonces hay veces que te interesa más el auto
12:03
porque va a determinar automáticamente si tiene que Mostrar las barras o no Si es que hay desbordamiento o no por eso
12:09
te recomiendo que siempre que quieras que salgan las barras utilices el auto porque va a determinar si tienen que salir las barras o no tienen que salir
12:15
las barras vale Y el tema de que desaparezcan las barras eso también tiene que ver con el navegador yo porque estoy utilizando macos y por eso ni
12:21
siquiera Aparecen las barras solo aparece cuando te están moviendo Vale cuando te mueves Entonces sí que aparece pero en el caso de de otros igual
12:29
siempre salen las barras aquí a la derecha pegadas depende del sistema operativo y depende del dispositivo incluso vale solo para que lo sepas y
12:36
qué más se puede hacer Pues pensad que una vez que tenéis este tipo de cosas por ejemplo si ponéis el overflow hidden
text-overflow
12:41
vale también se pueden llegar a hacer otras cosas por ejemplo está el text overflow que lo que te permite es
12:47
indicarle cómo se tiene que intentar eh evitar Que aparezca la información claro
12:53
aquí no se ve casi voy a hacerlo un poquito más pequeño para que lo veáis pero ves Si no cabe lo que hace ese
12:58
overflow Es que le puedes decir vale Voy a ocultar el contenido que desborda la
13:03
caja pero si es texto quiero que el desbordamiento termine con un elipsis y
13:09
por eso me pone estos tres puntos suspensivos fíjate la diferencia si pones esto te lo corta así a saco Pero
13:15
puedes utilizar para el texto el text overflow elipsis que lo que hace es vale he detectado que este texto va a
13:20
desbordar y lo que voy a hacer por lo tanto es ponerle puntos suspensivos para que ese contenido quede claro que no
13:26
cabe pero no lo voy a recortar de golpes que voy a poner puntos suspensivos y ya está no por defecto el text overflow
13:32
también tiene un valor que es clip que es este que vemos aquí el text overflow clip lo que quiere decir es simplemente
13:37
recortar donde sea ya está y luego tendríamos el de elipsis por desgracia que lo sepas esto te lo comento para que
13:43
sepas sobre el futuro de css pero que sepáis que en el futuro La idea es que esto puedas poner aquí un puedas poner
13:51
un símbolo esto no funciona todavía vale esto todavía por desgracia no funciona Pero la idea ves que pones sintaxis clip
13:57
elipsis y pone aquí String es porque en el futuro La idea es que tú puedas poner un text overflow y aquí poner lo que
14:03
quieras vale puedas poner un símbolo puedes poner lo que quieras pero como ves todavía no funciona por desgracia
14:09
Así que hay que tener un poquito de paciencia Pero con esto ya sabes al menos Cómo puedes tratar los
14:15
desbordamientos en css algo que ocurre cuando el ancho y alto que tiene tu caja
14:21
no es capaz de contener todo el contenido que le has puesto Ya sea imágenes texto texto o lo que sea no Se
14:27
podría poner un leer Se podría poner cuando se pueda podrías hacer esto pero el problema es que con css a día de hoy
14:34
no se puede tienes que utilizar solo elipsis y lo tendrías que hacer más con con con javascript Entonces se puede
14:41
estilar la barra se puede estilar la barra la barra se puede estilar con css scroll bar css playground lo podéis
14:48
Buscar por aquí Ahí playgrounds ves esta por ejemplo y aquí podéis ver que se puede estilar por ejemplo podéis decir
14:53
que sea más finita que no tenga que no tenga borde que yo que sé le podéis
14:59
cambiar los colores podéis cambiarle el borde radius vale su más borde radius puedes hacer que tenga más altura ves
15:05
que sea más ancha más lo que queráis le podéis hacer lo que queráis ahora bien Yo no es una cosa que os recomiende
15:12
mucho vale porque el problema de estilar lo Es que mira también esta que pone
15:17
feral esta también está muy chula dónde os recomiendo estilar la barra yo la barra solo la estilar en cajas internas
15:25
o sea en esta tiene sentido porque está dentro pero una barra a nivel de página web yo no la
15:32
estilar En mi opinión eh para que lo sepáis para que lo sepáis se puede tentar con javascript un texto es
15:37
completamente visible creo que no se puede no se puede creo que no se puede
15:42
con css hacerlo creo que no lo tendría que mirar pero que yo recuerde no se puede no te no te devuelve ya css algo
15:49
para decirte sí estoy utilizando esto sería increíble Pero por desgracia no habría que hacer alguna magia negra por desgracia vamos con otro tema
La magia del position
15:56
interesantísimo del css esto muchas veces da problemas porque mucha gente se vuelve loca y hoy lo vas a aprender ya
16:03
has aprendido el desbordamiento que está muy interesante pero te voy a explicar hoy en la magia del position voy a poner
16:10
una cajita por aquí me voy a copiar este este html que tengo por aquí vale pum y
16:15
voy a poner Este css vale css que ya más más o menos desparecido pero es solo más
16:21
que nada Para que veamos una cosita vale Imagínate que tenemos este css lo voy a hacer un poquito más pequeño para que lo
16:27
veáis bien bien Vamos a hacer esto Aquí y ahora te explico Cómo es esto vale vamos a hacer esto un poquito más
16:33
pequeño vale vale imagínate Tenemos aquí voy a poner en el body vamos a poner un color así a ver esto tiene sí qué bien
16:42
qué maravilla Pues algo así vale esto qué es lo que tenemos lo que tenemos
16:47
aquí es una section vale que tenemos un borde de cinco píxeles de color negro y
16:53
una altura y una anchura de 250 píxeles le vamos a poner el box sizing a Border box vale Y fíjate que ha cambiado un
16:59
poco porque así nos aseguramos que son 250 píxeles y dentro tenemos un dip con la clase container que ahora Aquí voy a
17:07
ponerle container para que veamos que es un container y que básicamente tiene el fondo de color azul la el eh la caja de
17:15
100 píxeles 100% y ya está no Cómo funcionan las posiciones en css vale Y
17:20
esto es superimportante los elementos de css se posicionan por por defecto de
17:26
forma estática Y qué decir pues lo que quiere decir simplemente es que se quedan donde están definidos en el html
17:34
y se van apilando dependiendo de diferentes cosas pero se van apilando O sea no hay ninguna historia aquí como
17:39
tenemos un section y dentro tenemos un dip pues como puedes ver dentro de El section este tenemos el dip no hay
17:46
ningún tipo de magia está está directamente directamente está puesto
17:51
donde le corresponde de forma estática ya ha determinado que hay una etiqueta dentro de otra etiqueta y ya está no se
17:57
ha posicionado de una forma mágica no ha hecho nada es como lo pondríamos de forma totalmente normal esto es como funciona por defecto y a esto se le
18:04
llama position static vale toma su sitio y ya está si pondríamos otro dip pues
18:10
esto lo que haría Es simplemente ponerlo justo debajo justo después y seguiría
18:15
estando dentro del section vale perfecto esto es como funciona por defecto que está muy bien es muy divertido Pero hay
18:22
diferentes formas de indicar que nuestros elementos se tienen que posicionar con css uno de los más
Absolute y relative
18:27
importantes por defecto tenemos el position static Pero uno de los más importantes es absolute y qué quiere decir que sea
18:34
absoluto absoluto A qué no bueno si ponemos el position absolute Fíjate que parece parece que no ha ocurrido nada no
18:42
ha pasado no ha pasado nada no ha cambiado nada Y es que por defecto su posición donde Tendría que ir este
18:47
elemento section es ese aunque tengamos la posición absoluta pero cuando ponemos que la posición es absoluta nosotros lo
18:54
que vamos a poder hacer es determinar sus coordenadas en el documento le vamos a poder decir Oye pues ahora quiero que
19:00
el top esté en la posición cero vale posición cero y el left Ah es que Perdón
19:05
perdón Es que además lo estoy poniendo donde eses lo quiero lo voy a poner en el container vale para que lo veamos mejor ahí está Vale en el container y
19:12
ahora el container es la la caja azul y ahora le vamos a decir que el top le vamos a poner cero ojo qué ha pasado
19:19
aquí qué ha pasado aquí se ha salido de la caja y ahora decimos left cero vale
19:24
fíjate dónde me lo ha llevado si le digo no la posición right cer0 Qué quiere decir esto cuando decimos top cero lo
19:30
que quiere decir es que del punto de mása arriba en el punto cero píxeles el punto de mása arriba de cero píxeles
19:37
obviamente es aquí ahora cuando decimos derecha cero lo que queremos decir empezando de la derecha empezaríamos en
19:44
la posición cer0 y Cuanto más le digamos vale por ejemplo 10 píxeles sería 10
19:50
píxeles desde la posición más a la derecha 50 píxeles más de la desde la posición más a la derecha y lo que estás
19:57
viendo es que está empujando y este espacio que ves aquí son los 50 píxeles incluso podrías utilizar porcentajes
20:04
claro un 50% se supone que debería ser un 50% lo que pasa es que aquí hay que tener en cuenta que el ancho de la caja
20:10
también determina esto O sea el punto que ves aquí este punto que ves aquí es el que se ha quedado en mitad o sea lo
20:16
está posicionando bien pero visualmente igual tú no lo ves así Igualmente lo que está haciendo el position absolute Es
20:23
que de forma absoluta saltándose totalmente cualquier control que tu emos
20:28
de Cuál eran los elementos html que estaban conteniendo esto lo está posicionando Vale qué pasa aquí bueno
20:34
Que obviamente este position absolute se está posicionando respecto a qué pues respecto al documento como puedes ver si
20:41
le ponemos right 0 eh top cero ves se está pegando arriba a la derecha o sea
20:48
lo está posicionando relativo a todo el documento Okay qué pasa que nosotros
20:54
muchas veces vamos a querer que esto se posicione respecto a otras cosas Por ejemplo yo me gustaría que este esta
21:01
caja Yo moverla dentro pero no la quiero mover de todo el documento la quiero mover dentro de esta cajita Pues
21:08
imagínate que lo queremos poner abajo a la izquierda vale abajo a la izquierda veis se ha quedado a No aquí [ __ ] Aquí
21:17
no aquí aquí se ha quedado aquí no la veis aquí aquí está la cajita pero imaginad que la quiero poner realmente
21:22
aquí dentro Cómo podríamos conseguir esto Pues para eso tenemos otro position que se llama rela Qué hace el position
21:30
relative lo que ocurre con el position relative es que estamos creando un punto
21:35
relativo para que cualquiera de nuestros hijos pueda tomarlo como referencia
21:41
cuando tiene tenemos un position absolute va a estar buscando a todos los padres no a su primer padre al abuelo y
21:49
si no al documento no va a estar buscando en todos los elementos html cuál de ellos es el elemento relativo
21:56
cuando no encuentra ningún elemento relativo lo que va a pasar es que va a utilizar el documento como referencia
22:02
Pero qué pasa que hay muchas veces que vas a querer utilizar esto vas a querer
22:07
moverlo dentro de esta caja por lo tanto necesitas un punto de referencia relativo Así que al padre vale este
22:14
section que sería el padre de hecho Vamos a ponerle aquí eh parent vale Vamos a ponerle parent para que lo vean
22:20
más claro Vale pues vamos a ponerle el position relative y esto nos va a permitir que cualquiera de nuestros
22:26
hijos ahora se puedan se puedan posicionar de forma relativa ese Así que
22:31
el container ahora por ejemplo Imagínate que lo quiero poner aquí arriba a la derecha pues le ponemos W 0 y top cer
22:37
pero fíjate que ahora esas coordenadas siempre son relativas al padre que está
22:43
envolviendo Este container vale Así que por eso es super importante el relative el relative en realidad tiene mucha
22:49
importancia porque si vosotros siempre intentáis utilizar el position absolute Vais a ver que no tiene ningún tipo de
22:55
sentido Vais a estar viendo que que ent Entonces no funciona correctamente va a ser muy difícil que de forma absoluta
23:01
siempre estéis constantemente moviendo cosas en el documento necesitáis pues este tipo de referencias relativas para
23:07
poder posicionar correctamente vale Así que aquí tendríamos el relative funcionando para que veáis que tenéis su
Centrar ‘algo’ con absolute
23:14
sentido una cosa muy interesante de justamente el position absolute es que también podríais llegar a a centrar un
23:20
dip Y esto es una cosa que se puede utilizar mucho para modales vale muchas veces me dice cómo cómo centrar un dip y
23:26
tal Pues mira aquí tendríamos una forma correcta vale mira fíjate Imagínate que tenemos este position absolute aquí con
23:32
el right 0 top c pero qué pasa Imagínate que dices vale quiero que sea que esté
23:38
lo más arriba a la derecha posible y lo más abajo Lo más abajo a la izquierda
23:43
posible vale fíjate dónde se ha puesto ahora se ha puesto aquí y dices ostras
23:48
si yo le he dicho que tiene que estar a la derecha del todo arriba del todo abajo del too y a la izquierda del todo
23:53
por qué lo pone arriba a la izquierda no Bueno lo que está pasando Es que en realidad necesita haríamos decirle que los márgenes tienen que estar
24:00
automáticos Y fíjate dónde te ha dejado el dip te lo ha dejado en el centro porque ha detectado que si tiene que
24:06
tener la misma distancia por todos los sitios y le dices que el margen que tiene que utilizar es automático lo que
24:12
va a pasar justamente aquí es centrarlo ahora bien esta es la forma que tendrías que centrar un dip no Esta es una forma
24:20
que puede ser interesante A veces por ejemplo para modales para modales para diálogos y cosas así pero vas a ver que
24:27
hay otra formas mucho más sencillas y más recomendadas para centrar contenido en este caso si es un si es un contenido
24:34
que va a quedar por encima de toda la página web esto puede tener sentido Pero te recomiendo que no lo hagas De hecho
24:39
hay una forma todavía más corta de hacer esto y es que tienes la posibilidad de utilizar la propiedad inset cer que es
24:46
una forma corta de decirle tanto arriba abajo izquierda derecha vale inset cer Y
24:51
así estarías haciendo Exactamente lo mismo y con el margin auto ya lo tendrías vale Así que ahí lo tienes no
24:57
es la mejor forma pero es una forma de lograrlo que siempre es importante saber todas las formas posibles y ya os digo
25:03
que esta puede ser interesante en algunos en algunos casos vale ya hemos visto tanto la de position absolute y
fixed
25:09
hemos visto position relative que ya veis que tiene bastante sentido vamos a ver la tercera que también es bastante
25:15
interesante que es position fixed que esta es muy chula Mirad imaginad que
25:22
vamos a tener más contenido para que aquí pues tengamos un un scroll típico qué es lo que hace el position fix el
25:28
position fix lo que hace es parecido al absolute lo vamos a poner aquí en el container Vamos a ponerle el fix Qué
25:35
pasa pum Fíjate lo que ha pasado que me lo ha dejado aquí vale me lo ha dejado Aquí vamos a quitar esto del inset vamos
25:40
a poner que se quede arriba y a la derecha vale Y qué pasa a ver el fix es
25:46
parecido al absolute pero como puedes ver no se mueve al hacer scroll ya que
25:52
se queda fijo en pantalla Así que las coordenadas que le vamos a poner aquí en el top y el el right van a ser relativas
26:00
no al padre que ponga relative no al documento sino a la pantalla vale a la
26:05
pantalla se va a quedar fija en el viewport si le pones top 0 right 0 lo
26:10
que va a ocurrir es que se va a quedar fija en el viewport en esa posición vale Así que este position relative que
26:17
tenemos aquí en realidad no sirve ahora mismo para nada porque conforme vas a tener esto aquí fíjate que se queda
26:23
Aunque tú scroll se queda siempre en la misma posición y aquí ten en cuenta una cosa que aquí tenemos tres elementos
26:29
tenemos este de aquí este de aquí y este de aquí para que lo vean más claro fíjate ahí tienes el container pero si
26:36
le doy a inspeccionar vas a ver que en la misma posición tenemos estos tres elementos este container tiene claro
26:43
como tiene el fix y tiene que quedarse ahí tenemos tres elementos ahora mismo que están ahí y fíjate con el scroll se
26:48
queda exactamente igual o sea el position fix es fijo en el viewport las
26:54
coordenadas que le vas a poner son las coordenadas como de la la pantalla no de la ventana no no se ve ni aplicado no no
27:02
le afecta ni el scroll ni si tiene un padre que sea position relative nada de esto vale Así que position fix significa
27:09
este elemento quiero que quede fijo y que no importa el scroll que haga que siempre se queda ahí para qué puede ser
27:15
útil este el fix puede ser útil por ejemplo habrás visto muchas veces abajo a la derecha que ponen una ayuda de chat
27:22
eh Para hacer el soporte técnico de chat y lo ponen abajo a la derecha Pues para eso puede ser interesante Mira te voy a
27:28
poner un ejemplo de para qué se puede utilizar el fix en mi página de midudev cuando tú entras Fíjate que aquí abajo
27:34
ves aquí abajo hay como mf no dispone de conexión que es mentira pues sí que estoy conectado pero ves cuando tú haces
27:40
scroll aunque esto se queda aquí fijo se queda siempre aquí no así que esto por ejemplo sería con un position fix
27:47
también dónde puede ser interesante con los menús estos que tienes o también seguro que has entrado a alguna página
27:53
web que abajo del todo te aparece un menú y está fijo por ejemplo en el advengers Ay advengers no perdón en
27:59
aprende javascript.edu en modo móvil tienes fijo
28:05
un menú abajo en la pantalla vale aquí a ver Ah ostras no sale Ay me ha dejado
28:11
fatal a ver pensaba que salía [ __ ] no sale el menú no sé si es porque en modo
28:18
pensaba que debería salir un menú juraría que en móvil salió menú igual lo he roto eh igual lo he roto pero Debería
28:24
Debería salir el debería salir un nabar no sé por qué no sé si es que dice la el que lo detecte de una forma distinta
28:30
pero debería saber si no lo arreglaré Pero bueno el nbar ese típico que ponen también sería fijo vale Hay uno muy chulo muy chulo que Vais a ver que es la
sticky
28:37
leche y Vais a entender por fin Vais a entender cuál es la diferencia entre fix
28:43
y sticky vale porque sticky es una cosa que mucha gente se confunde con el fix
28:49
Pero son muy diferentes y cada uno muy interesante Vale qué hemos dicho el fix
28:55
se queda fijo en pantalla y no le afecta el position relative Pero qué pasa que
29:00
tenemos otro que se llama se llama sticky vale fíjate el sticky que es
29:05
diferente Fíjate que ya solo cambiarlo ya cambia por qué Porque el sticky no se
29:11
va a quedar siempre fijo en pantalla sino que va a ser y va a depender se va a quedar pegado al contenedor Vale y va
29:18
a tener va a tener en cuenta lo relative iba a decir vale Yo voy a voy a dejar mi
29:23
posición siempre que pueda dentro del contenedor en el que esty y vas a ver ahora la la diferencia vale Imagínate
29:30
este po sticky fíjate fíjate que sco y mira lo que le pasa a este container
29:35
fíjate qué está pasando lo que está pasando Es que lo está empujando Fíjate
29:40
que lo hago así y lo empuja si fuésemos a a más vamos a hacer que esto sean como más vamos a hacer que tenga más altura
29:47
para que lo veamos bien vale pero fíjate vamos a poner 100 no igual deberíamos Sí
29:53
vamos a poner 100 vale Imagínate yo voy esando Y fíjate que esto lo que está haciendo es que quedarse ahí pegado hasta donde puede hasta donde puede del
30:00
contenedor en el que se encuentra fíjate ves que no sale no sale esto es super
30:06
chulo porque muchas veces lo que puedes poner aquí por ejemplo esto lo habrás visto en un montón de sitios y esto Solo con css lo que significa sticky es que
30:13
se está quedando pegado al contenedor en el que está por lo tanto no es que sea
30:19
fijo como lo hemos visto antes no el fix lo que estaba pasando era esto no que se estaba quedando donde no era pero ahora
30:25
lo que está haciendo es quedarse fijo donde debe ser en el contenedor también Es verdad que claro aquí hay un hay un
30:31
tema y es que te habrás dado cuenta que debería ser position relative porque si no no debería funcionar pero lo que ves
30:37
es que se queda hasta aquí se queda hasta aquí y ahí como ve dice Ah Ya no
30:42
puedo más pues ahí me quedo vale No no continúo y aquí igual aquí se queda aquí y entonces empuja empuja empuja hasta
30:48
que llegue al siguiente y ahí Lo tendríamos O sea que este sí que es importante que entiendas que tiene que
30:54
ver con el contenedor en el que se encuentra O sea no tiene nada que ver con el fix puede ser que visualmente en
31:00
algún momento tenga alguna cosa que digas ostras esto sí que sí que le
31:05
afecta de alguna forma pero que tengas en cuenta que no no tiene ningún tipo de sentido no se parece absolutamente en
31:10
nada vale Así que no tiene absolutamente nada que ver ese sería el position sticky así que ya tenemos el fix el
31:17
absolute el relative y el sticky Ya teníamos todos los diferentes el static es el que es por defecto o sea el static
31:22
no tiene ningún tipo de misterio el absolute ya lo habéis visto que sería relativo al primer contenedor que fuese
31:30
relative que si no encuentra ninguno sería el documento tendríamos el relative que no solo el relative puede
31:35
ser importante en cuanto a posición sino también de Z Index que Eso lo veremos más adelante y luego también teníamos el
31:41
fix que puede ser interesante para dejar fijo algo en pantalla respecto al scroll Y luego el sticky para que se quede ahí
31:48
enganchado ahora lo que vamos a ver es el Z Index porque vamos a ver vamos a ver el el el vamos a hacer una cosa con
z-index
31:55
el con el fix aquí teníamos el fix no el fix el fix y vamos a quitar todo No sé
32:02
si quitar o poner aquí 500 vale vale aquí en el fix vamos a poner no sé si
32:10
había puesto bottom vale vale Fíjate en el fix que pasa una cosa muy curiosa
32:15
fíjate aquí en el fix pasa una cosa bastante curiosa Fíjate que aquí podemos
32:21
ver que queda por encima de uno pero por por debajo del otro queda por debajo del
32:26
primero pero queda por no queda por debajo del segundo pero por encima del otro Qué está pasando con este container
32:32
que cuando le hemos puesto este fix vamos a poner solo uno vale Este fix que
32:37
se queda ahí fijo que parece justamente el sticky pero fíjate que se queda así
32:42
el fix lo que hacía era quedarse pegado a pantalla lo voy a poner a la derecha para que lo veáis bien vale pero fíjate
32:47
que se queda ahí y lo tenemos aquí justamente que queda por encima de uno pero por debajo del otro Qué es lo que
32:53
está pasando aquí esto lo que está pasando Es otra de las cosas más complicadas que ocurren en el mundo de
32:59
css vale Y es básicamente el contexto de apilamiento Qué quiere decir esto a ver
33:04
nosotros en realidad vemos las páginas web que parece que son 2D parece que es
33:09
una caja eh que la tienes ahí y dices bueno Esto es un plano que está como si fuese un papel y estás dibujando encima
33:16
Pero no es exactamente así te tienes que imaginar que nosotros cuando vemos los elementos puede estar uno por encima del
33:23
otro y en realidad si fuésemos capaces de la pantalla deberíamos ver en realidad
33:30
que tenemos elementos que están por encima de otros y que realmente sí que hay como profundidad en estos elementos
33:37
tenemos una capa encima de otra Así que digamos que el apilamiento cuando
33:43
decimos de contexto de apilamiento lo que quiere decir es el concepto de que en realidad los elementos html que vemos
33:49
dibujados son en 3D por lo tanto hay un eje Z un eje de de profundidad es un eje
33:56
imaginario porque no lo vemos cuando vemos las páginas web pero aunque el usuario lo ve todo plano en realidad
34:02
tenemos que pensar que realmente sí que hay una profundidad no y que en ese esa profundidad los elementos están ocupando
34:07
un espacio en html porque aquí lo podemos ver claramente aquí podemos ver que este container está pasando por
34:14
encima de uno pero por debajo del otro o sea no Cómo podría pasar esto pues justamente por el contexto de
34:20
apilamiento no el contexto de apilamiento Cómo se forma es bastante complicado pensar de Cómo se forma pero
34:27
voy a intentar hacer un poquito un un resumen el elemento raíz crea un contexto de apilamiento cuando un
34:33
elemento tiene una posición relativa con un valor de Z Index distinto al auto que
34:38
ahora lo veremos crea un contexto de apilamiento cuando tiene un elemento Flex cuando tienen elementos de transf
34:46
opacity que sean diferentes a los por defecto por lo tanto cuando pasan este
34:51
tipo de cosas crea un nuevo contexto y por lo tanto puede tener un elemento encima encima de é vale Hay un montón de
34:58
casos y como no lo voy a saber de memoria os voy a decir una lista muy buena donde lo Vais a encontrar que es esta en el contexto de apilamiento mira
35:05
aquí tenéis elementos con opacity transform mix Blend filter perspective isolation position fix Hay un montón
35:12
vale un montón de de formas de crear contextos de apilamiento aquí justamente
35:17
estamos creando uno porque fíjate que lo pone aquí pone position fix ves position fix qué está pasando aquí pues aquí
35:24
tenemos el position fix Ahora cuando esto ocurre cuando se están apilando una capa encima de la otra Lo bueno es que
35:30
tenemos una forma de nosotros determinar qué capa es la que tiene que quedar por delante de la otra vale o sea no es que
35:37
esto lo hacemos así ya decimos Bueno pues ya está no hay nada que hacer qué le vamos a hacer No no no se puede
35:43
arreglar no realmente sí que lo podemos arreglar de una forma y para eso podemos utilizar la propiedad Z Index lo que
35:50
está pasando aquí Qué es lo que está pasando aquí por qué en uno queda por debajo y el otro queda por encima lo que
35:55
está pasando Es que el primero fíjate que en el primero la caja azul queda por encima del borde en la primera lo que
36:01
está pasando Es que este container es el que corresponde con este con este container de aquí este de aquí y este
36:08
container de aquí está dentro de este section este section es el primer borde que podéis ver el primero que se queda
36:13
por encima y ahí Obviamente el elemento que está dentro sí que por defecto los
36:19
elementos que están dentro de otro elemento quedan por delante de ese elemento porque obviamente es importante
36:25
que el contenido sieme quede por encima del contenedor esto es típico Imagínate
36:30
que tienes una caja con un fondo blanco vale Y le pones un texto qué esperarías que el texto quedase por detrás o por
36:36
delante Obviamente esperarías que el texto quedase por delante así que por defecto siempre Y esto es muy importante
36:42
cuando lo lo lo entiendas de Por qué quedan por encima o por detrás no es el hecho de que siempre vas a querer que el
36:49
contenido tenga una Z mucho mayor para que esté como más cerca del usuario y lo
36:55
pueda ver El ejemplo del texto es el más típico Pero puede ser una imagen puede ser más contenido puede ser lo que sea
37:01
vale porque en el segundo queda por detrás porque en este fíjate ves en el segundo queda por detrás lo que está
37:07
pasando en el segundo es que ya estamos viendo aquí el segundo section y el segundo section está separado de este
37:15
contenido es como que este dip está quedando por detrás de este section Y es
37:20
que tiene sentido porque no es su hijo no es su hijo por lo tanto ya tiene un nivel de Z
37:27
que sería mayor pero nosotros podríamos forzar que quedase por delante podríamos decirle que los contenedores el índice
37:34
de Z sea 10 por ejemplo no vale 10 Qué quiere decir este 10 Qué quiere decir
37:39
este 10 a ver lo que estamos dando aquí es un número como para decirle la prioridad no la posición que tendría que
37:46
tener en ese eje de profundidad que decimos si le quitamos el Z por defecto
37:51
vemos que ya ha hecho un cálculo en el que ha dicho Vale cuando es mi hijo es normal que quede por delante pero en el
37:57
siguiente Pues voy a hacer que quede por detrás de hecho podría quedar incluso totalmente eh tapado si aquí le ponemos
38:03
background fff vamos a ver que esto todavía es peor no veis está quedando por detrás Y ya desaparece pero lo
38:10
podríamos decir es bueno aunque tú tengas un Z Index por defecto Lo cierto es que este container quiero que tenga
38:16
como más más importancia en el Z índex y quiero que quede por delante Entonces
38:22
por defecto lo que le estamos diciendo es que este tendría que tener un Z índex de dos pero por defecto el otro tiene
38:28
uno menor por lo tanto lo que vamos a hacer con esto es conseguir que quede por delante este de Z Index muchas veces
38:35
el problema es que nos ponemos y nos volvemos locos y ponemos unos números así no que la gente dice Ah pues voy a hacer un nu nu y este tipo de cosas lo
38:42
que hay que intentar muchas veces es utilizar solo y simplemente los los
38:47
números que necesitas de forma controlada incluso eso lo podrías hacer con custom properties con variables no
38:53
para decir Bueno voy a tener como voy a estudiar como mi diseño y voy a tener en cuenta esa capa 3D Cuáles cuáles son los
39:00
elementos que tienen que quedar más adelante normalmente eh suele pasar que las modales y todo este tipo de cosas
39:06
tengan que tener un número mucho más grande pero no tiene mucho sentido que algunas cosas empecemos ahí a tener un Z
39:13
Index ahí muy bestia porque si no al final lo que te cuesta es pensar Cuál es el nivel que tiene que tener vale Así
39:19
que esto sería un poco como funcionar Z Index lo que os recomiendo porque Z Index lo mejor es practicarlo y aquí
39:25
tenéis de de web dep que está super chulo esto porque tiene algún Además de
39:30
que tiene algunos croquis que os van a ayudar un montón tiene un montón de ejemplos que están superb esto es un
39:36
ejemplo muy típico y muy importante porque y os lo voy a enseñar esto un tema que tenéis que tener en cuenta con
A tener en cuenta con el z-index
39:41
el Z Index Mirad vamos a cambiar Este section vale vamos a poner otro estilo aquí para que lo veamos y vamos a poner
39:49
tres cajas aquí Ay me he copiado lo que no era sí me he copiado lo que no era vamos a poner estas tres cajas vale que
39:54
es un ejemplo similar a este una cosa bastante importante del Z Index aquí lo único que he hecho es un section
40:01
que tenemos una caja con un dip un un un dos un tres Y fíjate que lo que hemos hecho aquí es que el dip cada una de las
40:08
cajas tiene un margin top menos 100 qué pasa con esto claro cuando tú le ponen margin top -1 -150 lo que está pasando
40:16
es que por arriba va a tomar espacio y fíjate que va a quedar por encima o por debajo dependiendo de cada uno claro
40:22
aquí lo que podemos ver Es que está funcionando más o menos como se le espera cuanto más abajo también está el
40:27
contenido Es normal que tenga que tener un Z Index mayor es normal que el contenido que está más abajo nuestro
40:33
html queramos que quede por encima del otro por eso está pasando esto de forma por defecto vale lo podríamos cambiar
40:39
pero podemos ver que por defecto el tres que sería el contenido que tenemos aquí aquí podemos ver que queda por encima
40:45
del dos porque está un poquito más arriba y el dos queda por encima del uno porque está un poco más arriba o sea lo que está haciendo por aquí es justamente
40:51
como machacarlo no esto sería un poco lo del Z Index pero ahora no estamos utilizando
40:56
alguien puede decir ostras vamos a utilizar el Z Index para arreglarlo quiero que el amarillo este de aquí
41:02
quiero que el amarillo quede por encima de todos lo que estamos utilizando aquí es un selector vale Deep First Child y
41:09
aquí lo que estamos haciendo Es que esto quede queremos que quede por encima de todos Vale pues le pondríamos un Z Index
41:14
999 y no funciona por qué no funciona porque a ver el Z Index por defecto
41:21
tiene que tener algún tipo de relación claro yo le estoy diciendo Z index 9999 pero hemos dicho que hay que crear como
41:29
eh contextos de apilamiento no le estamos diciendo Oye pero tienes que apilarse Y cómo hemos dicho que se crean
41:35
claro no estamos creando ninguno tendríamos que crearlo nosotros Entonces si queremos que el uno sea el que quede
41:41
por encima que lo puedes hacer así tendríamos que asegurarnos que todos tienen un position relative vale
41:46
position relative Y ves ahora sí que ha detectado ha dicho Vale ahora que sé a
41:52
qué son relativos e los dip tienen el position relative ahora voy a crear ar una un nuevo stack de de apilamiento y
42:00
ahora sé que este 999 Es mayor que el que va a tener por ejemplo el rojo y el
42:05
azul pero podríamos hacer decir Bueno vamos a hacerlo de otra forma vamos a decir Mira vamos a hacer un selector que
42:11
quede el segundo vale el segundo lo hacemos así NC Child y vamos a hacer que tenga el background de calor 09f y así
42:19
lo tenemos todos Imagínate que queremos ahora que sea el segundo que quede por encima de todos pues tendríamos que
42:24
hacer un Z index todavía mayor al que lo habíamos puesto antes ves y ahora quedamos tendríamos que el dos está por
42:31
encima de todos el segundo sería el amarillo porque le hemos puesto un valor más bajo y finalmente teníamos el Last
42:38
Child porque es el que tiene el valor por defecto y es el que tenemos el más bajo tenemos que entender que en ese stack de apilamiento tendría que tener
42:45
un Z Index de cero vale Pero esto lo podríamos cambiar fijaos que no hace falta poner números muy grandes una vez
42:50
que tienes claro cómo quieres que quede cada uno Z Index 2 Z Index 1 y así nos aseguramos esto a este le ponemos Z
42:57
Index 3 y ya quedaría por encima del otro vale al final lo importante es que entendamos Cómo funciona el stat de
43:04
apilamiento Cuando se activa realmente que si le quitas el position relative Entonces no lo tiene y cuando se crean
43:11
también se pueden crear con el position fix que lo hemos visto antes Y con diferentes cosas vale Hay que practicar el Z Index a ver el Z Index Lo
Recurso para z-index
43:17
importante es no abusar de él porque el problema no es del Z Index en sí que de hecho también se pueden poner valores
43:22
por en negativo sino es cuando se abusa y no se entiende entonces claro cuando abusas y no lo entiendes Entonces te
43:29
empiezas a poner un montón de Z Index por todos los sitios Y eso lo que hace es que sea complejo trabajar con z Index
43:35
no está genial no entendía el contexto contexto de apilamiento os recomiendo mucho mucho mucho el de mdn el tema del
43:42
apilamiento porque ahí lo explican muy bien y os dicen todas las veces que se crean vale Y aquí los tenéis todas las
43:49
propiedades y en qué qué situaciones se se hacen No yo leí que es ponerlo mejor de 100 en 100 no no O sea no es verdad O
preguntas de la comunidad
43:56
sea quiero decir puede ser una forma de hacerlo hacerlo de 100 en 100 pero no es tan importante Cuál es el número sino
44:03
más el control y además Hay a veces incluso eh funciones de Sas o custom
44:09
properties que podéis hacer para controlarlo No yo con mi 999 para el mayor de todos es que a ver utilizar el
44:15
99999 es lo típico Pero no es lo que os recomiendo os recomiendo de Mira a mí si lo queres hacer cada 100 puede ser no
44:22
mala puede no ser una mala idea pero lo importante es que lo tengáis controlado ya explicaste los float No porque yo
44:29
Considero que los float a día de hoy no son necesarios Entonces yo no explicaría ni siquiera los float porque no me
44:35
parecen ni importantes ni interesantes a día de hoy y por eso vamos a explicar flexbox ahora el contexto de apilamiento
44:41
es el mismo para todos o se quedan por cada elemento cuando lo desbloqueas el contexto de apilamiento es compartido
44:46
desde la raíz para todos pero se va creando uno nuevo dentro de cada
44:51
elemento claro va siendo un nuevo contexto de apilamiento que es justo lo que hemos visto aquí Aquí no aquí Fíjate
44:57
que aquí con este position relative no está afectando y hasta que no hemos hecho position relative y crea el
45:02
contexto de apilamiento Entonces es que sí que lo hemos tenido no si sticky no se puso en right a pesar que lo tenía o
45:08
vi mal ostia pues no me fijé pero Pero puede ser Pero puede ser también porque
45:13
en realidad no sé si llegué a poner el position relative no no no me fijé no eh
45:19
los flot me sirvi para un aspecto muy particular de una maqueta muy específica que requería que la imagen desbordara su contenedor claro es muy Espe vamos a
Flexbox
45:26
hablar de Flex que al final muchas veces lo que pasa con con Flex hay muchas preguntas de cuándo utilizar Flex y
45:33
cuandoo utilizar grid y no sé qué hoy vamos a hablar de Flex que me parece como uno de los más interesantes e
45:39
importantes Flex porque con Flex puedes hacer el 95 por incluso lo que haces con
45:46
grid muchas veces lo puedes hacer con Flex te puede solucionar mucho la vida te puede quitar un montón de problemas y
45:52
al final lo importante es que menos sepas Flex grit es genial para muchas
45:58
cosas pero vamos a ver sobre todo cuándo puede ser interesante grid os lo comentaré después de grid pero vamos con
46:05
Flex que Flex es muy especial os conté de display que había diferentes displays
46:10
no vamos a ver vamos a vamos a quitar todo esto voy a dejar el 1 do TR OK Vamos a poner un section por ahora vamos
46:17
a poner que el section que es el padre vamos a poner aquí el parent vale vamos
46:23
a poner parent y vamos a poner aquí un item Entonces vamos a poner tanto aquí
46:28
aquí y aquí Class item vale Y con esto ya tendríamos nuestros items esto por
46:35
aquí esto por aquí vale qué hacemos con el item voy a hacer que sean cajitas vamos a hacer que sean cajitas con un
46:41
Pixel eh vamos a hacer que tenga una opacidad pun nu más que nada lo mismo no algo parecido pero vamos a hacerlo solo
46:48
con cajitas para que lo veamos muy claro vamos a hacer que tengan un color así luego le cambiamos Mira vamos a hacer
46:54
algo similar Pero que sea como lo que teníamos pero desde cero vale el item el
46:59
primer Child vamos a hacer que tenga el color que sea Yellow y el qu he hecho aquí First Child lo he
47:07
hecho bien No item claro que igual no
47:13
punto item vale es que he puesto algo mal me parece no antes Last Child venga ponemos
47:19
otra vez el color rojo y t vale Entonces hasta aquí habíamos visto el display el display block block lo que hacía era
47:27
crear y Mostrar ese contenido Como si fuese una caja Y en lugar de hacer que
47:32
el contenido se leyese de forma en línea lo que hacemos Es tener un bloque y el
47:38
siguiente elemento aparece después del Salto de línea no entonces aquí podemos ver que este contenedor este dip que es
47:45
lo que le está afectando este bloque este de aquí display block este es donde tenemos el display block lo tenemos aquí
47:51
por defecto dip tiene display block por eso si le quitamos esto y le quitamos esto vas a ver que se comporta
47:58
Exactamente igual no pero qué pasa que eh También podríamos decirle el item le podemos decir que se mostrase en línea
48:05
no si se muestra en línea qué es lo que pasa bueno como puedes ver que se muestre en línea significa que se va a
48:11
comportar Exactamente igual que como si fuese texto o sea que va a ir uno en
48:16
línea con el otro en dirección a como le iríamos el texto en nuestro caso es de izquierda derecha pero en otro sitio
48:23
vale en otro país esto que estamos viendo nosotros de izquierda a derecha en otro sitio lo podrían ver de derecha
48:28
a izquierda vale para que lo tengas claro cuando decimos que sea en línea es siguiendo siguiendo la línea del texto y
48:36
se pone uno detrás del otro como funciona el texto una palabra detrás de la otra es en línea vale Y lo que está
48:42
ocurriendo aquí es que después cada elemento va uno seguido del otro no hay un salto de línea y el problema igual
48:48
que le pasa al texto es que tanto el Alto Como el ancho no le afecta lo que estamos teniendo aquí es que si yo le
48:54
digo que cada item son 100% 100 píxeles o sea 100 de ancho y 100 de alto Fíjate
48:59
que no está ocurriendo este no está pasando aquí que sean 100 píxeles lo
49:04
está ignorando porque el cuando mostramos la la caja en línea lo que
49:10
está haciendo es lo que sea el contenido y después el siguiente contenido siguiente contenido sin salto de línea y
49:15
nada vale ahora si ponemos el block qué es lo que va a pasar el blog sí que va a
49:21
hacer esto le va a afectar el ancho y alto y después cada contenido lo que que va a ocurrir es que va a ser el sentido
49:27
de la lectura general que es de arriba a abajo no lo está pilando de arriba a abajo cada contenido no lo pone en línea
49:34
sino de arriba a abajo que sería también la dirección en la que leemos los textos de arriba a abajo y finalmente hace un
49:40
salto de línea para poner el siguiente contenido por eso aunque este dos Aunque este dos realmente cabe aquí lo que
49:47
estamos viendo Es que le está dando ahí un salto de línea para poner el siguiente vale muy bien ahora tenemos
display: flex
49:54
más displays tenemos diferentes displays y uno de ellos es display Flex display
50:00
Flex Qué es es una propiedad de css que establece cómo tienen que funcionar
50:05
realmente el contenedor respecto a sus hijos o sea que el Flex no lo tenemos que utilizar directamente en el hijo
50:11
sino que tenemos que utilizar en el contenedor esto Lo tendríamos que poner aquí display Flex y esto directamente lo
50:18
que va a ocurrir es que vamos a tener un contenedor que es flexible y que nos va a permitir a nuestro a todo los hijos
50:26
ser alineados de otra manera mucho más eficiente tanto horizontal como vertical
50:31
incluso cuando tenemos tamaños desconocidos o dinámicos vale Y fíjate Ya la diferencia del display Flex que lo
50:38
que ha ocurrido es uno a los hijos le está afectando el alto y el ancho Pero
50:43
ha detectado que sí que tiene espacio suficiente para ponerlos a los lados y
50:48
lo ha puesto al lado por qué Porque ha determinado que tiene una dirección en
50:53
la que puede este contenido estar y por defecto el el la dirección en la que nosotros estamos trabajando es como
51:00
filas Así que como una fila ya ha dicho vale la dirección del contenido de esta este contenido flexible va a ser una
51:07
fila y por lo tanto voy a poner el contenido en fila en nuestro caso en
51:12
nuestro caso de lectura es de izquierda a derecha pero luego veréis Por qué es importante entender esto O sea no es
51:17
correcto no es correcto y tenlo muy en cuenta pensar y decir siempre que es de izquierda derecha o sea decir en fila es
51:24
de izquierda derecha no es así correcto y luego vas a ver por qué y lo vas a ver clarísimo vale aquí qué le podemos poner
flex-direction
51:29
el Flex Direction El flex Direction por defecto es Row vale es en filas pero
51:35
también le podríamos indicar cuál es la dirección en que nosotros queremos que funcione que realmente no sea así le podemos decir que sea por columnas Y qué
51:42
va a pasar con las columnas que aunque tú ahora estés viendo que sea muy parecido visualmente a lo de dip lo que
51:48
está pasando realmente no es tanto que está haciendo un salto de línea sino que está apilando todos sus hijos como si
51:54
fuese una columna y cómo es una columna pues arriba uno abajo el otro y abajo el otro vale pero si tuviésemos otro ancho
52:01
podríamos tener algo al lado lo podríamos llegar a hacer podríamos apilarlos de formas totalmente distintas si quisiéramos pero una cosa que ya te
52:07
estarás dando cuenta si podemos tener la dirección que sea columnas o filas es
52:13
que Flex es unidireccional Es de un solo eje siempre
52:19
siempre siempre Flex vamos a estar trabajando de un solo eje ya sea filas o
52:25
columnas Y esta es la diferencia clave con grid porque grid justamente es una
52:32
cuadrícula sera correcto cuadrícula que no me salía una cuadrícula entonces en Flex Siempre vamos a estar trabajando en
52:38
un eje ya sea un eje en filas o en columnas pero la en grit al final es es
52:44
una cuadrícula Entonces al ser una cuadrícula Qué pasa que Vais a poder trabajar bidimensionalmente vas a poder
52:50
trabajar tanto en filas y en columnas a la vez y es una de las cosas más más interesantes que tiene ahora bien si
52:56
solo necesitáis un eje podéis utilizar también grid porque os permite trabajar en dos ejes a la vez pero también
53:02
podríais utilizarlo solo para uno pero para Flex solo podéis trabajar en una filas o columnas ya veis que no podéis
53:08
decirle ni ni diagonales ni cosas raras Flex Direction no flex Direction o column o Row ahora bien Ahora bien tened
53:16
en cuenta que también hay otros eh algunos valores un poco especiales por ejemplo tenemos Row reverse que Fíjate
53:22
lo que hace es darle la vuelta le estaría haciendo el sentido contrario estaría poniendo el último al final y
53:29
sería en filas pero al revés sin necesidad de hacer ninguna cosa Esto
53:34
está bastante interesante porque hay veces que hay mucha gente que para hacer el reverse utiliza javascript y hay
53:39
veces que con esto te lo puedes ahorrar porque en lugar de hacer un reverse del ar Rey lo puedes hacer visualmente en el
53:45
caso de que sea un ar Rey conocido que no sea Dinámico y que al final Pues a lo mejor Imagínate que son 15 opciones Y
53:52
dices reverse hay gente que lo hace con javascript pero pero es muy fácil hacerlo muchas veces con esto y así te
53:57
quitas un montón de complejidad y lo mismo con la columna también le puedes dar la vuelta a la columna vale Y ahora
54:03
Vais a ver más cositas que tienen cosas muy chulas pero imaginemos que seguimos aquí con el Flex vale Esta es la
54:08
dirección por defecto por defecto es display Flex La dirección es por filas Fíjate que la dirección de escritura es
54:14
importante si tú le pones Direction que la el Direction es justamente lo que indica es la dirección de escritura No
direction
54:21
pues tú en la dirección le podrías poner rtl rtl qu quiere decir right to left o
54:26
sea escribes de derecha a izquierda entonces Fíjate que solo poniendo Flex Direction Flex ya le ha dado la vuelta
54:33
al contenido entiendes ya le ha dado la vuelta al contenido porque el contenido ahora se muestra correctamente porque la
54:40
gente que escribe de derecha a izquierda lo que está pasando Es que le es de derecha a izquierda y entonces ya
54:45
tenemos aquí que lo primero que leerán es el uno luego el dos y luego el tres no O sea que ahí ya tenemos la
54:51
diferencia que es clave y lo mismo pasaría un poco con el writing Mode eh podemos poner writing Mode y le decimos
writing-mode
54:56
que es vertical de izquierda a derecha vale Y fíjate qué pasa no que está cambiando totalmente Fíjate que Flex lo
55:03
interesante que tiene Es que aquí ya podemos ver cómo está Ajustando nuestro contenido a esto no estamos viendo aquí
55:10
que tenemos aquí el el primero vale el primero lo tenemos aquí y como estamos haciendo que la escritura es vertical de
55:16
izquierda a derecha pues está Ajustando el contenido esto es espectacular porque aunque vosotros en el 95 por % del
55:26
trabajo que hacéis solo pensáis en español y es está bien no pasa nada pero
55:31
es importante que entendáis esto porque esta es la implicación importante que tiene de Flex cuando hablamos de de
55:37
filas y de columnas Y es que se se adecúa también a la escritura a los
55:43
diferentes idiomas y es clave porque creáis o no internet eh es mundial no
55:48
solo en español no es solo occidental es de un montón de sitios entonces tenéis que tener en cuenta también esto no de
55:54
que tamb bien tanto el Row como el column se afecta dependiendo de la dirección de escritura tendríamos el
flex-wrap
55:59
tema del Flex grap vale tenemos el Flex Direction y tenemos otra cosa que por defecto sería el Flex grap que por
56:06
defecto es No grap ahora si no hay suficiente espacio en el contenedor los
56:11
elementos se van a desbordar vamos a vamos a hacer aquí un borde un vamos a poner cuatro píxel solid y el negro vale
56:18
vamos a a forzar que tenga 300 pixels y o o menos no sé 200 200 150 200 píxeles
56:26
Vale qué está pasando aquí lo que está pasando aquí fíjate yo le he puesto que sea de 200 píxeles si miramos a ver aquí
56:33
vamos a ver de Cuánto ha dejado esto y cuánto está haciendo que ocupe cada cosa Vale vamos a poner esto por aquí
56:39
quitamos al 100% y esto lo ponemos abajo para que veamos bien vale Y aquí tenemos
56:46
el section bueno es 208 por el borde vale Pero bueno Ay [ __ ] le he puesto
56:51
Flex aquí le he puesto Flex Direction Flex Pero bueno era Row y como por defecto era Row pues ya funcionaba no sé
56:56
por qué he puesto Flex pero me he equivocado eh era Row entonces dicho esto fijaos que yo le he puesto aquí que
57:02
el padre son 200 pixels y cada item tiene que ser de 100 pixels pero claro
57:08
si cada item es de 100 pixels el tema es que no debería caber no debería caber
57:14
pero por defecto tenemos este Flex grap que le decimos no grap lo que está pasando por aquí es que ya está
57:20
Ajustando claramente el contenido que tenemos para decir bueno como no me no cabe lo que voy a hacer es hacer más
57:27
pequeño cada uno de los elementos vale lo que estamos teniendo aquí es esto fíjate Se ve se ve un poquito que hay
57:34
como una flecha ahí y es bastante curiosa lo que está pasando ahí es que está diciendo Mira debería haber sido
57:39
esta anchura pero lo he ajustado hecho un sprink vale que sería como lo he
57:45
encogido a esta a este ancho para que realmente quepa perfectamente porque si
57:50
no lo que iba a pasar Es que no iba a caber y claro si no cabe pues al final se ve mal y la hemos liado parda Por qué
57:56
está pasando esto Esto está pasando por magia este no grap no este no grap qué
58:01
es lo que quiere decir lo que quiere decir es que por defecto no va a hacer si no hay suficiente espacio en el
58:07
contenedor lo que va a hacer es decir bueno no quiero que me lo pongas en una línea más Hazlo como tú quieras intenta
58:15
lo que tú quieras pero tiene que caber aquí vale esto no quiero que me lo me lo cambies por nada del mundo tiene que
58:20
caber aquí de alguna forma hay veces que se puede hacer con desbordamiento depende unas cuantas cosas que ahora
58:25
veremos pero lo que sí que tiene claro es que no está haciendo un salto de línea para hacer que quepa el contenido
58:31
Bueno qué es lo que vamos a hacer aquí en este en este caso pues fíjate Qué pasa si le pones grap pum qué está
58:38
pasando cuando le decimos el grap Es que le estamos diciendo Oye te doy la posibilidad de que si no cabe hagas un
58:45
salto de línea qué es lo que ocurre que no cabe porque cada item es de 100
58:50
píxeles tenemos 200 disponibles por lo tanto lo que dice es vale como no cabe
58:56
porque tenemos 100 píxeles pues lo que hago es otro salto de línea mira y aquí tenemos algo interesante porque ves que
59:02
pone 200 píxeles y no cabe no cabe porque dos items deberían ser 200
59:08
píxeles pero no cabe Y esto no sé si con el box I lo arreglaremos vamos a ver Border Box no no no no solucionamos
59:16
porque no sé si aquí también lo deberíamos poner no pensaba que a lo mejor a lo mejor iba a caber pero no
59:22
cabe porque va justo no no cabe pensaba que no iba a caber por el borde pero lo cierto Es que no cabe porque no cabe no
59:28
cabe Por poco no cabe Por poco ves así sí que cabe y le sería justamente por el borde pero pensaba que con el Border Box
59:35
igual conseguíamos que que cupiera pero no cabe Pues eso pero es por el borde por lo que no cabe dicho esto el tema es
59:42
que como no cabe pues lo que está haciendo básicamente es
59:47
saltáis que es importante que sepas que por defectos este valor porque muchas veces la gente lo que le pasa es que se
59:53
vuelve loca de Por qué me está cambiando el tamaño por qué me lo pone todo una fila Por qué no sé qué no sé cuánto O
59:59
sea que ya está lo que no cabe es otra cosa ya sabes dónde [ __ ] savitar Cómo estás atento Y estás aquí encima en una
1:00:06
clase de css madre mía estás más perdido más perdido que el día que te
1:00:11
encontraste eso en la boca que que te puse tío trozo de carne sí el trozo de carne Ya sabes cuando fuimos al asador
1:00:17
aquel que fue buenísimo en fin el grap lo que va a hacer es si no cabe te permito que hagas un salto de línea si
1:00:24
pones No wrap es que no tienes que tener el Salto de línea vale tienes que saber que hay una forma abreviada de utilizar
Atajo de flex-direction/wrap (flex-flow)
1:00:30
los dos puedes utilizar Flex Flow y le puedes indicar por un lado la dirección Row y luego decirle si quieres no wrap O
1:00:36
grap Vale entonces aquí lo puedes decir en una muy poco usado la verdad El flex Flow lo he visto muy poco pero que sepas
1:00:43
que es una forma abreviada de hacer exactamente lo mismo por si te interesa vamos a poner el espacio controlar el
Controlar el espacio de los elementos
1:00:49
espacio de los elementos flexibles que tenemos dentro vamos a poner con el no wrap que queda un poquito mejor vale
1:00:54
bueno suponemos Esto no que tenemos este contenido 200 píxeles e y cuál es el
1:01:00
problema El Imagínate si le ponemos un poquito más 350 Bueno claro 350 no lo
1:01:06
vamos a ver vamos a hacerlo más pequeño vamos a poner 300 y vamos a hacer que los items sean solo de 50 no vale Fíjate
1:01:13
lo que pasa aquí que son de 50 píxeles y tenemos aquí más más espacio disponible
1:01:18
podríamos rellenar ese espacio ahora vemos cómo lo lo podemos rellenar no cómo cómo realmente hacemos que aunque
1:01:25
sea 50 píxeles le digamos Oye quiero que estos elementos se adecúen a ese eje y
1:01:30
que pueda pueda crecer todo lo que yo quiera a ver el contenedor tiene más espacio para mostrar los elementos se
1:01:36
están alineando ahora mismo al principio pero yo lo que me gustaría es que se
1:01:43
ocupasen todo el espacio Por qué está haciendo esto por defecto por defecto lo que está ocurriendo Es que aquí tenemos
1:01:48
diferentes propiedades voy a poner esto por aquí en css tenemos diferentes propiedades una es Flex gr que por
1:01:55
defecto es cero Qué quiere decir los elementos no crecen vale No crecen luego
1:02:00
tendríamos Flex ring que por defecto es uno que quiere decir los elementos
1:02:06
pueden reducir su tamaño a un tamaño más pequeño que su Flex basis Vale y su Flex
1:02:13
basis por defecto es auto vale que los elementos tienen un tamaño base en auto
1:02:20
en automático que por automático en este caso va a tener en cuenta sobre todo todo el Wiz que le hemos puesto aquí
1:02:25
claro le hemos puesto un Wiz de 50 píxeles pues va a esperar que sean 50 píxeles Entonces ya podemos ver que lo
1:02:31
que está ocurriendo es uno le estamos diciendo que los elementos que tenemos en Flex no pueden crecer O sea que no
1:02:37
pueden crecer no le no podemos hacer que crezcan si le ponemos un uno podrían crecer pero en este caso no va a hacer
1:02:43
nada por el Flex basis Flex Spring le estamos diciendo que los elementos pueden reducir su tamaño y de hecho
1:02:49
antes hemos visto que lo han hecho si nosotros le ponemos aquí un 100 Fíjate que aquí qué ha pasado que el no wp que
1:02:56
hacía que evitase un salto de línea y el ancho a un 100 a 100 píxeles junto con
1:03:01
el Flex ring 1 que este es el valor por defecto estos son los valores por defecto vale que esto valores por
1:03:08
defecto lo que está ocurriendo aquí es que como sí que le estamos permitiendo que puedan reducir su tamaño gracias a
1:03:16
esto Realmente está haciendo esto de de que se queda así si no claro lo que pasa es que tiene el auto que el auto ya no
1:03:22
está salvando eh si no lo que podríamos hacer es se redujese su espacio para también ajustarse al tamaño vale Así que
1:03:28
este sería por el defecto ahora cambiaremos el auto porque el auto es el que tiene el tamaño base que nos está engañando y tal Y que sepáis que todo
1:03:34
esto sería como el Flex initial sería como la forma inicial de tratar el Flex Vale ahora la clave está en el Flex
1:03:40
basis porque imagínate que en Flex basis le decimos Oye el tamaño es 200 píxeles OK le decimos que el Ah es que claro
1:03:48
tengo el grab aquí y le decimos aquí que no puedes ni ser más pequeño ni más grande ni lo que sea el FX basis va a
1:03:55
ser el tamaño base que vamos a tener por lo tanto vamos a tener ahí un tamaño que sea 200 píxeles por por defecto y le
1:04:03
podemos decir que crezcan o que no crezcan y todo esto vale Bueno yo estoy viendo Y por qué no está cambiando nada
1:04:09
de esto a ver a ver a ver si es que la ha liado ahora porque me estoy volviendo un poco loco ahora con el Flex a ver a
1:04:16
ver qué está pasando esto cuánto ocupa que me lo me lo diga Flex vale est 100
1:04:22
100 50 50 No claro es que ostia Pero por qué no ha dicho nadie nada que le
1:04:28
estamos poniendo donde no es claro es que le estamos poniendo todo esto todo esto Flex y tal todo esto se lo hemos
1:04:34
puesto donde no es claro es que todo esto que se lo he puesto aquí no va Aquí tío madre mía ya estaba flipando Y es
1:04:40
que esto va Aquí tío es que va en el item y a lo mejor me lo habéis dicho y no me había enterado eh igual Es sabit
1:04:47
que me ha puesto nervioso sí sabit me lo dijo sí sí sabit me va a decir lo que yo sé no es verdad nosotros lo sabíamos per
1:04:52
no queer decir sí sí sí porque estamos en un curso de css Bueno pero se me ha se me ha ido se me ha ido eh se me ha
1:04:58
ido claro es que claro como tengo que estar arriba abajo y tal claro Es que esto no va en el padre Esto va en el
1:05:03
hijo Esto va en los hijos Vale ahora ahora ahora ya tiene sentido ahora ya tiene sentido Ay Ay Ay Ay Ay claro claro
1:05:10
claro Vale ahora ya lo tenemos vale vale aquí por ejemplo claro es que si no no tenía sentido ya estaba flipando el tema
1:05:17
es que estos Flex grow Flex ring y Flex basis Esto va en los hijos vale Y por
1:05:22
defecto ya hemos dicho que es el Flex de hecho estos son los valores por defecto el Flex grow a cer El flex ring
1:05:29
a un y el Flex basis a auto Vale ahora sí Ahora sí Entonces los elementos no
1:05:35
crecen pero sí que pueden reducir su tamaño ahora sí que le podemos decir esto de los 200 píxeles Vale ahora sí
1:05:40
que podemos ver esto que ahora sí que estamos ocupando 200 píxeles 100 píxeles lo que sea no Claro en este caso no no
1:05:46
ocupa más pero fijaos que aquí este ocupa un poquito más y los otros ocupan un poquito menos ahora sí que podemos
1:05:52
ver eh que le está afectando perfectamente Vale entonces el padre cuánto ocupaba 100 píxeles perfecto lo
1:05:59
que podemos hacer es por ejemplo que Ajustando el tamaño esto sería Ajustando a 100 píxeles y que sí que se puedan
1:06:06
hacer un poquito más pequeño pero podemos hacer que se ajuste automáticamente a Su contenido vale si
1:06:11
le ponemos un Flex no grap y le decimos que se ajuste automáticamente a Su
1:06:17
contenido y que se pueda hacer tan grande también se pueda reducir O hacer más grande fijaos que ahora
1:06:23
independientemente de cuál sea Oy hecho esto independientemente de cuál sea el ancho del padre le hemos puesto 200 pxs
1:06:30
imagínate ahora 100 pero si ahora lo hacemos más grande lo que estamos haciendo con esto es Oye los elementos
1:06:35
pueden crecer los elementos se pueden reducir y el tamaño es automático esto
1:06:40
lo que estamos haciendo es del espacio que tiene va va a ajustarse a todo lo
1:06:46
que tenga disponible independientemente va a tener en cuenta el contenido Fíjate que el primero este ocupa más
1:06:52
automáticamente pero lo que estamos haciendo aquí es que estos 200 píxeles los está rellenando completamente porque
1:06:58
le hemos permitido que se hagan más grandes y que además se hagan más pequeños que se ajusten automáticamente vale Y esta sería la forma del Flex auto
1:07:06
que es como la más popular porque es como el contenido se va a ajustar el
1:07:11
automáticamente al contenedor y ya está no otra cosa que podríamos hacer es independientemente del contenido que
1:07:18
todos tuviesen el el mismo ancho o sea en lugar de utilizar el Flex basis le podríamos decir vale los elementos
1:07:24
pueden crecer los elementos se pueden hacer más pequeños pero vamos a hacer que la base sea cero y esto lo que vamos
1:07:31
a hacer es que todos tengan el mismo ancho fíjate que ahora independientemente del contenido ahora
1:07:36
todos tienen el mismo ancho si le pones un auto ves sí que se va a ajustar automáticamente según el tamaño base
1:07:42
según el contenido que tiene cada uno si le pones el cero independientemente del contenido los tres van a tener el mismo
1:07:48
el mismo espacio y la forma abreviada de hacer esto sería Flex 1 que esto también
Atajo de flex-grow-shrink-basis
1:07:54
lo habréis visto un montón de veces De dónde sale este Flex 1 pues Flex 1 lo que quiere decir es los elementos pueden
1:07:59
crecer los elementos pueden reducir su tamaño a un tamaño más pequeño que el Flex basis y el Flex basis si lo pones
1:08:05
cer0 que al final es el tamaño base Claro si es cero Si todos parten desde la misma base si cada uno se tiene que
1:08:11
distribuir el espacio va a ser el mismo espacio para todos pero si le pones auto lo que va a hacer es tener en cuenta el
1:08:17
contenido de cada uno para distribuir el espacio vale Así que ahí tendríais un poquito la diferencia y una cosa que es
1:08:24
super interesante de esto Una vez que por ejemplo ponemos Esto del Flex basis lo podemos a cero Eh bueno a cero vamos
1:08:31
a vamos a quitar todos estos hemos dicho que la forma corta sería esta Flex 1 pero una cosa muy interesante es que el
1:08:38
uno también puede servir como una medida relativa para indicar cuánto espacio
1:08:43
tiene que tomar cada uno de los elementos vale por ejemplo cuando decimos Flex 1 Vamos a poner los tres
Ejemplo de flex
1:08:49
Aquí vamos a poner el item nt Child 2 y este va a ser el background Blue y
1:08:55
quitamos esto aquí vale ya tenemos aquí el primero el segundo y el tercero una cosa bastante interesante es que cuando
1:09:02
le decimos Flex 1 le decimos Oye todos tienen que tomar el mismo espacio pero imagínate que por lo que sea queréis que
1:09:09
el primero tenga el doble de espacio que el resto pues lo que podes hacer es Vale
1:09:14
pues el primero quiero que tenga el doble de espacio que el resto por lo tanto el primero va a tener de ancho el
1:09:22
doble que los os elementos y aquí lo podéis ver por ejemplo este si lo
1:09:27
medimos Aquí vamos a ver que tiene unos 350 si vamos al otro pues deberían ser
1:09:33
unos Cent no A ver es que he mirado el que no es es Ah son 160 vale unos 160 y
1:09:40
mirando este pues vamos a ver que tiene 80 vale o sea que tiene el doble lo mismo podríais hacer Si en lugar de
1:09:46
tener dos vamos a decir que tenga cuatro veces Vale pues podemos decir el primer hijo tiene cuatro el el segundo tiene el
1:09:53
doble del que solo tiene uno y así lo podemos ver no podemos ver que el último hijo que por defecto pues ahí tendría El
1:09:59
flex un se ha quedado con uno el segundo hijo tiene el doble del que solo tiene
1:10:05
uno y el primer hijo tiene cuatro veces del que solo tiene uno y el doble del que solo tiene dos vale es una
1:10:11
referencia relativa de cuánto espacio tienen que tomar respecto al padre no le
1:10:17
estamos diciendo este tiene que tomar cuatro veces lo que ocuparía uno de los espacios es una forma cuando lo pensamos
1:10:24
muchas veces en proporciones como las columnas Es como decir mira si tengo eh
1:10:29
10 columnas Pues aquí quiero que se queden ocho aquí una y aquí una no es como la proporción que tiene que tomar
1:10:35
del espacio cada uno de ellos vale lo digo porque podéis poner el Flex un para que todos tengan el mismo espacio pero
1:10:42
imaginad que el del medio queréis que tenga el doble de espacio pues le pondréis un dos y tomará el doble del
1:10:48
espacio de lo que tienen cada uno de los elementos que tienen un Uno Vale si le ponéis un dos van a a tener el primero y
1:10:54
el segundo el doble del espacio que el que tiene el uno vale Así que es bastante importante esto porque al final
1:11:00
es una forma de distribuir el espacio de forma mucho más sencilla y de forma que
1:11:05
no tengas que preocuparte de pensar en píxeles en tantos por Cent ni cosas así
1:11:11
Porque además en tantos por Cent lo importante ahora es justamente el espacio que tienen disponible y punto
Cambiar el orden de cada elemento
1:11:17
una cosa también muy interesante de Flex es que podéis utilizar el orden para cambiar visualmente
1:11:23
Cómo se ven los elementos por ejemplo veis aquí que tengo primero segundo y tercero una cosa muy chula es que podes
1:11:29
utilizar la propiedad order para decir bueno el primero quiero que su orden sea tres vale Ay sea tres y el segundo
1:11:37
quiero que su orden sea uno y el tercero creo que su orden sea dos qué hemos hecho con esto Pues los hemos
1:11:43
desordenado con css lo que está pasando aquí es que le estamos dando como el
1:11:49
orden en el que los hijos se tienen que mostrar en nuestro contenedor flexible fijaos que el primer hijo ahora aparece
1:11:57
el último porque le hemos dicho que el orden es tres aquí Lo importante es un poquito como el Z Index le podéis poner
1:12:02
el valor que queráis y lo que va a hacer Es ordenarlo según el valor numérico que tenéis en el orden Así que si le ponéis
1:12:08
el número que sea lo va a dejar el último porque este número es mayor y van a empezar primero a poner el número
1:12:15
menor el primero y así Consecuentemente lo importante de esto muchas veces y lo
1:12:20
que está muy chulo Es que podéis cambiar ualmente el Cómo se ve algo cambiarle el
1:12:26
orden sin necesidad de hacer ningún tipo de javascript que a veces esto muchas veces puede ser bastante problemático No
1:12:31
pues podéis utilizar el orden solo para esto podéis decirle bueno eh Imagínate
1:12:37
que el usuario reordena con un drag and Drop podéis utilizar el orden para en lugar de cambiar el html simplemente
1:12:43
cambiar el order y ya está y cada uno le podríais dar una prioridad diferente para ponerlo en un sitio o en otro y ya
1:12:48
está aunque y aquí va mi recomendación es importante que tengas en cuenta cuenta que el html es lo importante O
1:12:55
sea si algo en orden tiene que estar arriba por tema de importancia porque es donde tiene que estar tienes que cambiar
1:13:02
el html y lo que tiene sentido Pero hay veces que por temas visuales o incluso responsive hay veces que algo que está
1:13:08
arriba Pues que es que esté abajo y tal puedes utilizar ya sea el order O puedes utilizar el Flex Direction para
1:13:14
cambiarlo y hacer y hacerlo que sea reverso y cosas así vale pero es importante que tengáis en cuenta que si
1:13:22
semánticamente tiene sentido que esté arriba hac que esté arriba el html si visualmente solo visualmente por un tema
1:13:29
de responsive porque en ese momento queda mejor ahí porque lo está ordenando el usuario y es algo Temporal y tal Pues
1:13:36
igual lo podéis utilizar que muchas veces tiene sentido Exacto en responsive de footer se suele utilizar mucho
1:13:41
totalmente Menos mal que no fue los colores de la bandera Rusia [ __ ] No hombre a ver no sé son tres colores
1:13:47
normales y corrientes no sé por qu estáis viendo banderas donde no las hay eh vamos a quitar los órdenes vamos a
Posicionar elementos: Jusitify-content
1:13:52
quitar los órdenes vamos a quitarle también los Flex porque ahora os voy a explicar una de las cosas Yo creo que lo
1:13:58
más importante de Flex seguramente de lo más importante de Flex es el tema de de
1:14:04
cómo cómo se queda cada una de las cajas vamos a poner que wid vamos a poner 50 píxeles y vamos a poner que sea 50
1:14:12
píxeles y esto le vamos a poner un poquito más Vamos a ponerle 1000 píxeles Lu 500 píxeles vale
1:14:19
No 400 píxeles vale aquí es donde viene el divertido amigos lo divertido y donde
1:14:26
justamente os voy a mandar de veres hay un juego muy interesante que hoy Espero que hagáis que es Flex froggy me parece
1:14:34
Flex froggy es este juego flexbox froggy es un juego que es totalmente gratuito que está en SP en español y que os
1:14:41
enseña flexbox y al final flexbox Vais a tener que pelear un montón Vais a tener que preparar y tal Y aquí tenéis 24
1:14:47
ejercicios que son totalmente interactivos para poner en práctica todo lo que aprendéis de de flexbox pero lo
1:14:53
más importante justamente que Vais a practicar ahí es el tema de cómo posicionar vuestros elementos y esto es
1:15:00
lo más difícil alinear los elementos en flexbox no es que sea difícil pero básicamente es lo más divertido no
1:15:07
Entonces os comentaba que en flexbox teníamos eh el eje no el eje principal
1:15:13
vamos a trabajar siempre en un eje que va a ser la distribución En la que queremos ya sea en filas o en columnas
1:15:18
pero también tenemos otro concepto que es el eje cruzado Porque si tú trabajas
1:15:24
en filas al final esos elementos que hay dentro También tienen sus propios ejes
1:15:29
tanto horizontales como verticales y también vas a querer centrar losos ya sea vertical o horizontalmente Entonces
1:15:35
vamos a ver cómo funciona esto exactamente a ver el más importante de todos el más importante obviamente
1:15:41
cuando trabajamos en Flex es la distribución del espacio en el eje principal el eje principal es el que le
1:15:48
hemos indicado o el que está utilizando por defecto o sea en línea el el eje principal sería el Flex Direction Row o
1:15:55
column en este caso column vale sería así y Row sería así esto Esto es el eje
1:16:02
principal sobre el que vamos a trabajar vale eje principal Entonces cómo distribuimos el contenido en el eje
1:16:08
principal lo podemos hacer con un justify content y aquí le podemos decir diferentes cosas le podemos decir que lo
1:16:15
justifique en el centro y fijaos que en el eje principal o sea en la fila lo
1:16:20
está centrando cuando Center en su eje principal lo está centrando le podemos
1:16:26
decir más cosas interesantes como el space around por ejemplo para que deje el espacio el mismo espacio alrededor o
1:16:33
sea el espacio que está dejando aquí vale es el mismo que tiene
1:16:39
aquí lo que pasa es que aquí es el mismo espacio que está dejando este aquí y este espacio que está dejando aquí es el
1:16:45
mismo que está dejando aquí así que por eso está llamando space Sound luego tendríamos el space between esto lo que
1:16:51
va a hacer es que a los laterales no deja espacio sino que simplemente entro los elementos es que lo va a separar
1:16:58
entonces space between es solo espacio entre los elementos y luego tendríamos
1:17:03
el space everly que es similar similar al bwin pero fíjate que la diferencia es
1:17:10
que el espacio que ves aquí es el mismo que hay aquí el mismo que hay aquí el mismo que hay aquí o sea tiene el mismo espacio entre cada elemento y los
1:17:18
laterales es un poco un poquito diferente al between porque el betweenin
1:17:23
el al ar Perdón perdón al alrededor porque el ar Fíjate que aquí hay el doble de espacio que el que hay aquí
1:17:29
vale Así que es una diferencia sutil pero importante hay más por ejemplo por
1:17:35
defecto lo que tenemos es un Flex Start O sea al inicio de la fila pero fíjate que el Flex n lo deja al final uno de
1:17:43
los más importantes obviamente es el Center que es el que hemos visto que lo centra y ya está pero imagínate que los
1:17:48
quieres centrar y por lo que sea no solo quieres centrar sino que también los quieres eh separar pero los quieres
1:17:55
separar un poquito tampoco los quieres separar tanto Y claro el space between space around space evenly como Que los
gap
1:18:01
separa demasiado pues lo que puedes decir es utilizar un Gap y en el Gap le podis decir cuál es la la separación que
1:18:08
queréis Entonces tenemos un Gap que este Gap lo que está afectando siempre va a ser entre elementos no entre los
1:18:14
laterales vale entre elementos aquí lo podemos poner 16 píxeles y podemos utilizar todos y cada uno de los valores
1:18:20
que hemos ido viendo vale tambén pod utilizar porcent podéis utilizar un montón pero aquí lo que está dejando son
1:18:25
16 píxeles vale Así tendríamos el Gap no tiene mucho sentido utilizar el ar con
1:18:31
el Gap porque entonces ya empiezan las cosas raras vale tenéis aquí una separación con un Gap de 16 Pero además
1:18:37
otra separación que le hemos puesto en SP around y en el Flex Star sí que funcionaría lo que pasa es que la separación la dejaría siempre entre los
1:18:44
elementos vale Así que nada le hacéis El flex Center y ya lo tenéis vale con esto tendríamos la justificación de la
1:18:49
distribución del espacio en el eje Ay perdón el Center lo dejamos así en el eje el eje principal pero qué pasa con
distribución en el eje cruzado
1:18:57
la distribución en el eje cruzado y el cruzado Digamos si el principal es el
1:19:02
Row el cruzado Cuál sería la columna Bueno pues podríamos decir align content
1:19:09
Center no pero qué pasa aquí aquí no no parece que haya que haya cambiado nada
1:19:14
no O sea este Por qué por qué no ha cambiado nada No no ha pasado nada
1:19:19
verdad el tema es que sí que están centrados ya o sea están centrados Porque todos están ocupando lo mismo en
1:19:26
su eje cruzado que sería la columna o sea el la caja esta de primero ya está centrada porque ocupa 50 píxeles y en
1:19:34
esa fila de 50 píxeles ya está centrada vamos a intentar una cosa para que veamos la diferencia vamos a hacer que
1:19:39
el primero ocupe 25 píxeles el segundo que sean 30 píxeles y el tercero que
1:19:46
sean 40 píxeles no vale entonces Ah me ha dejado fatal porque esperaba que me
1:19:51
lo me lo dejase ah qué ha pasado me esperaba que me lo dejase centrado pero no me ha dejado centrado en el en el eje
1:19:57
por qué no me lo ha dejado centrado en el eje pensaba que me los iba a centrar ahí por qué me lo has dejado centrar en el eje vale Line item Center no ves esto
1:20:06
no Yo pensaba que esto me lo iba a centrar por qué no me lo está centrando a ver si o sea esto esperaba que estos
1:20:14
en su eje cruzado me lo centrase el align items a ver si pones un Flex no
1:20:21
pensaba que me los iba a centrar en el eje en el eje en su mismo eje no el el align items es para otra cosa el align
1:20:27
items que lo vamos a hacer después eh es para centrarlo a nivel de todo el ves a
1:20:33
centrarlo de todo pero yo no quiero centrar eso sino quería al final el align self es solo para uno eh eh tiene
1:20:39
que ser Flex wp Ay [ __ ] de la madre es que he quitado el grab la madre que me
1:20:45
parió no pero Flex Ay Flex Flex grap
1:20:51
grab no no pero tampoco es justo lo que queríamos eh No es lo que queríamos no
1:20:58
me ha dejado ahí fatal Eh texaline texaline sí sí no me ha dejado fatal
1:21:03
porque esto lo tenía clarísimo eh Como de decir no esto seguro que funciona así no sé qué las alturas están bien o sea
1:21:09
que no no tiene mucha historia A ver el align content básicamente es la distribución del espacio en el eje
1:21:15
cruzado o sea eso no hay ningún tipo de duda el tema es que el eje cruzado Debería ser la columna seguro que es una
1:21:21
chorrada que ahora mismo lo veo no sé por qué pero el tema es que la idea es que una cosa es centrar a nivel de fila
1:21:29
no que sería el eje principal que para eso utilizamos el justify content y luego dentro de la fila lo que me
1:21:36
gustaría es alinear verticalmente dentro del espacio que tiene aquí y aquí lo que
1:21:42
esperaría con el Aline content Es que este Me lo despegase me lo dejase en medio que no me lo hace vale que no sé
1:21:48
por qué me lo hace debe ser una tontería como un piano pero que no no lo no lo termino de ver entonces el Flex
1:21:54
Direction Flex Flow esto tiene que ser Row y no grab O sea pero es que este es el por defecto y finalmente la altura y
1:22:03
tal o sea lo tenemos todo correctamente que te falta un High y usar align items
align-items
1:22:08
es que a ver el align items si es que ya sé lo que va a pasar el align items eh el al items te lo centra a nivel de todo
1:22:14
el contenedor y eso no es lo que queremos que está interesante también pero pero no queremos Aline items para
1:22:20
todo el contenedor Aline items que está Interesante pero es para otra cosa no es para para para Esto vale o sea la Line
1:22:28
items alinea los elementos flexibles en elemento en el lje cruzado Pero yo lo que quería era el contenido vale No era
1:22:35
todo el item Pero bueno no pasa nada Ya no pasa nada Sol que el box está muy grande el H A ver vamos a ver sí sí no
distribución en el eje cruzado 2
1:22:42
puede ser puede ser que a lo mejor es eso que está muy grande el H O sea que al final haciéndola así el tema es que
1:22:48
haciendo el align items vamos a ver correctamente que esto sí que lo está haciendo así o sea esto sería con el
1:22:53
multilínea O sea ya eso ya lo he tenido claro eh que lo hemos tenido así O sea el tema es que con esto estaríamos
1:22:59
centrando ahora vamos a decirlo bien desde el principio vale Y porque el problema Está que es cuando tenemos más de una línea Solo que utilizado el
1:23:06
content y ahí la hemos liado el justify content la distribución del espacio en el eje principal vale o sea que esto lo
1:23:12
que haría es centrar en el eje principal que es la fila justify content Center fíjate la diferencia y luego en el al
1:23:18
item Center lo que vamos a hacer es centrar los elementos flexibles en el en la dirección Cruzada que sería
1:23:25
en este caso las columnas pero también si le diésemos la vuelta lo veríamos al revés o sea veríamos que el primero el
1:23:32
primero el justify content vamos a hacer esto justify content lo está haciendo lo
1:23:38
está centrando claro en este caso no no se vería ninguna centrada y el Aline items lo estaríamos haciendo en el eje
1:23:44
cruzado que serían las filas o sea estaremos centrando a nivel de filas vale ese sería el tema vamos a dejarlo
1:23:50
en Row vale Y ya lo tenemos así Entonces ya tenemos el tema este de la align
1:23:55
claro es que el tema de align content es que tenéis razón que es que tendríamos que tener más de una filas o sea
1:24:00
tendríamos que ponerle aquí que fuese grab y aquí en el Aline content sí que podríamos ver una diferencia podríamos
1:24:08
ver una diferencia si le pudiéramos a ver 500 o algo así no Y a ver Flex end
1:24:14
Flex Start vale Aquí sí que lo tenemos el tema es que yo pensaba que con el Aline content con una sola línea lo
1:24:20
íbamos a poder ver el Aline content lo que como Vais a ver es por defecto lo está haciendo que ocupe todo el espacio
1:24:27
que puede pero le podríamos decir Oye ponlo solo al principio lo agrupas ahí lo podríamos poner al final Esto es lo
1:24:32
que estaba intentando y luego lo podríamos poner en el centro también vale Y entonces así en lugar de intentar
1:24:38
utilizar con el lo dejas vacío lo que va a intentar es dejar o utilizar el máximo
1:24:43
espacio disponible para el contenido para las dos líneas Yo pensaba que con una línea iba a funcionar no ha
1:24:49
funcionado Y eso es lo que me ha vuelto un poco loco vale pero aquí sí que podemos ver un poco la diferencia La diferencia entre alinear los items vale
1:24:58
alinear el contenido La diferencia La tenéis aquí porque si esto el align
1:25:04
items este es a nivel de cómo se alinean en el eje cruzado el centro si le ponemos Flex Start lo que vamos a ver
1:25:11
fíjate que este ha subido para arriba este para arriba y tal el align items items lo que vamos a hacer es en el eje
1:25:17
cruzado que en este caso son las columnas al ponerle el Center vamos a ver aquí que lo centra Pero dentro de la
1:25:24
fila está centrando la columna el align content sería a nivel de todo el contenedor Si queremos todo el contenido
1:25:30
lo queremos al principio si lo queremos al final o queremos en el centro y Cuál ha sido mi error que al principio me he
1:25:36
vuelto todo loco y por qué no me funcionaba mi error es porque pensaba que en una línea iba a funcionar igual
1:25:43
que en una línea esperaba que el contenido como solo era ese espacio también lo hiciese pero no lo correcto
1:25:48
era utilizar el align items que eso era justamente lo que quería hacer de que se
1:25:54
centrase esa línea dentro del eje de la línea cada una de las columnas y luego
1:25:59
dentro del contenido pero solo íbamos a poder ver cuando teníamos más de una línea todo el contenido si lo íbamos a
1:26:05
poder centrar al principio al final o en el centro así que por eso ya veis que es
1:26:11
super interesante y super importante y por eso hay que jugar al flexbox froggy porque hay que practicar este tipo de
los más usados
1:26:17
cosas también os digo que es verdad esto que muchas veces y es interesante este
1:26:23
tipo de cosas lo más importante que es importante sabér selo pero el align content no se suele utilizar tanto los
1:26:30
que se suele utilizar más son estos dos uno para el eje principal El justify será para el eje principal en este caso
1:26:36
para las filas porque estamos en Row Y luego el align items que sería para el
1:26:42
eje cruzado vale que en este caso sería cada una de las columnas dentro de las filas lo que me decíais mucho que es muy
1:26:49
interesante es el align self Y es que dentro de todo el orden que hemos hecho
1:26:54
podríamos detectar cada uno de los elementos imagínate vamos a poner que el elemento 2 y el elemento cuatro vale
1:27:03
vale lo vamos a poner de color bueno elemento cinco lo vamos a poner de color azul y queremos que los de color azul
1:27:10
ellos por lo que sea no se centren veis que ahora están centrados en el eje Dentro de este eje están centrados pues
1:27:17
podríamos decirle que se alinee el mismo le podemos cambiar el alineamiento le podemos deir decir que se alinea arriba
1:27:23
o que se alinea abajo y esto puede ser muy interesante para cuando Tenemos un montón de elementos que los hemos
1:27:29
centrado y por lo que sea ya sea una oferta especial o lo que sea podemos dentro de un elemento decirle Bueno
1:27:36
quiero que ese elemento él se alinee de forma diferente a como el padre está
1:27:42
diciendo que se tienen que alinear porque es el padre el que dice cómo se alinean los elementos Pero uno mismo
1:27:47
puede decidir y decir Bueno yo voy a ser una excepción y yo quiero centrarme al principio vale Yo me voy a alinear a la
1:27:53
parte más de arriba o al revés podéis hacer que todos se alinean arriba y algunos pues abajo en el centro y todo
1:28:00
esto y para eso es el la Line self para una excepción no para algo no para hacerlos o centrar losos todo vale Y
1:28:06
está bastante chulo la verdad una cosa que no he hecho y que os recomiendo mucho que está muy chula es que las
1:28:12
herramientas de desarrollo de Chrome están s super super bien las de Chrome y las de firefox las de Safari no tanto
1:28:19
pero están bastante bien justamente por esto fijaos que aquí tenéis esto que le podéis dar un clic y aquí tenéis con
1:28:25
unos iconit super chulos podéis ver Flex Direction veis y podéis incluso cambiar visualmente como lo podéis ver vale le
1:28:32
podéis dar a cada una de las de unas Vale y vais viendo cómo se va comportando si es flx grab o no grab Si
1:28:38
el contenido se tiene que centrar o no se tiene que centrar y vais poniendo en tiempo real cómo le afecta cada una de
1:28:44
estas cosas y se van a ir cambiando y modificando cada una de las propiedades es que esto está superb porque Vais a
1:28:50
entender muy fácilmente mente cómo funciona Cómo se ve qué es lo que pasa por qué esto no funciona qué es lo que
1:28:57
necesitas y tal Y es tan fácil como darle ha un iconito que es este iconito de aquí y veis aquí como un como una
1:29:05
previsualización un poco de cómo va a quedar y cuando le deis clic pues va a cambiar tanto el el valor en el css aquí
1:29:11
como la previsualización que tenéis aquí Así que si tenéis problemas como los que he tenido yo que debería haber tenido
1:29:16
que tenía Tendría que haber revisado pues ya sabéis que lo podéis verar aquí con las herramientas de desarrollo eh selecciona el del padre bueno el del
1:29:24
padre es el que he seleccionado no no seleccionado Ah no he seleccionado el del padre Yo diría que sí
1:29:30
no aquí Ah Es verdad Claro que no es seleccionado el del padre no es seleccionado el del padre tienes razón
1:29:36
es seleccionado el del hijo Que bueno que también le afectaba Igualmente pero bueno que está interesante pero sí es verdad que no seleccionado del padre s
1:29:43
del hijo pero aún así Esto es lo básico y css bueno a ver css yo lo dije un día css es un lenguaje que es bastante más
1:29:50
complejo de lo que parece Porque tiene un montón un montón de cositas y ahora nos queda justamente grid que grid es
1:29:57
bastante más importante la de cosa que se puede hacer y que es bastante complejo así que de
1:30:02
deberes lo que si no habéis hecho nunca yo creo que deberíais hacerlo css es un lenguaje de programación no lo hemos
1:30:08
dicho 80 veces me parece una chorrada el tema de de discutir si es de programación o no pero sí que es un
deberes
1:30:14
lenguaje y eso no hay ningún tipo de duda o sea discutir eso sí que es una chorrada porque ese es un lenguaje declarativo para el diseño de las
1:30:21
páginas web bueno os dejo como deberes que le dais cañita al fxw froggy que es
1:30:26
increíble y que al final tenéis 24 niveles y que estoy seguro que con todo lo que habéis aprendido No vais a tener
1:30:32
ningún problema para pasaros y que os va a ayudar un montón Así que muchas gracias gracias por la paciencia Por el
1:30:38
error ahí que hemos cometido de Flex la verdad es que no sé por qué lo he hecho ahí s Pero bueno es que es normal pensad
1:30:44
que está ahí dos horas que no me he preparado nada y que al final pues lo hemos hecho ahí a salto de mata Y tiene
1:30:50
estas complejidades que a veces pasa Pero gracias por vuestra paciencia que lo hemos hecho con todo el cariño del mundo y ya está

## Grid


hoy vas a aprender y vas a amar y te va a gustar y lo vas a entender y lo vas a abrazar y nunca más volverás a llorar en
0:06
la almohada por culpa de grit porque lo vas a entender hoy vas a entender grit te lo digo yo que lo vas a entender
0:12
porque está increíble la potencia la de cosas que puedes hacer con grit y no
0:17
puedes dejar la oportunidad de entenderlo de abrazarlo para que de esa forma puedas maquetar páginas web en
0:23
condiciones Así que la semana anterior hicimos flexbox que ya lo explicamos y hoy vamos con grido pero también te voy
0:30
a explicar las diferencias un poquito que hay entre uno y otro vale Bueno amigos kod va a empezar mañana porque
Codember
0:35
hoy no he tenido tiempo entonces mañana arrancamos cod vale arrancamos mañana cod y lo desbloquearemos en vivo y en
0:43
directo mientras estamos streame porque mañana vamos a abrir la plataforma de cod donde Vais a tener retos retos
0:50
secretos del mundo de la programación retos de programación que podréis resolver con cualquier lenguaje con el
0:56
que queráis y que va a tener un montón de sorpresas pero no lo perdáis porque Vais a a tener retos todo el mes de
1:01
noviembre nuevos retos cada semana he desarrollado páginas y nunca he utilizado grid siempre utilizo Flex así
Introducción a Grid
1:06
que sería bueno aprender un poco de grid haces bien es bueno aprender grid Y es que a ver Flex es genial está muy bien
1:13
Es maravilloso Es maravilloso Pero Vais a ver que hay cosas que no se pueden hacer fácil con Flex y que hoy Vais a
1:21
entender de ostras Pues con grid se puede hacer con esto mucho más fácil no una cosa que se suele hacer mucho en
1:26
maquetación web que es los resultados de una búsqueda y vais aprender hoy Cómo hacer resultados de una búsqueda
1:32
responsive superfácil en muy pocas líneas de código y lo Vais a entender que es lo mejor se pueden combinar por
1:38
supuesto se puede combinar grid con Flex sin ningún tipo de problema vale un elemento no puede tener los dos a la vez
1:43
el mismo elemento pero sí que se puede hacer que dentro de cada elemento uno utilice grid y dentro tengas Flex De
1:49
hecho si queréis lo miramos ahora en un momentito no hay uno que sea mejor que el otro Eh Esto es un error muy común
1:54
donde la gente se cree que git es más avanzado que Flex o que un uno es más
2:00
nuevo que el otro y entonces es mejor es más recomendable utilizar grid que Flex son diferentes literalmente son
2:06
diferentes y luego os lo comento Por qué son diferentes pero el resumen fácil y
2:12
rápido es que Flex es unidimensional o sea siempre estamos hablando de una dimensión filas o columnas y grid
2:19
estamos hablando de bidimensionalidad que son filas y columnas okay Así que
2:24
ahí tenéis la diferencia clave importantísima Claro si utilizáis Twin puedes utilizar grid calls 2 pero aún
2:31
así Eso sería para tener dos columnas pero es que Vais a ver que lo que Vais a aprender hoy lo Vais a poder utilizar
2:37
con tawin también porque al final tailwind fss y además hay cosas que tailwind no te soluciona porque eso que
2:43
dice nefes eso es muy simple el hecho de hacer dos columnas y ya está pero hay
2:49
veces que hoy lo vamos a ver por ejemplo este tipo este tipo de de diseño que son los ventos que están muy pero que muy
2:55
muy muy de de moda eh estos ventos hay algunos que no lo Vais a poder hacer tan
3:01
fácil como esperáis en en telwin porque justamente no os dan las herramientas
3:06
pero si sabéis cs sí que lo Vais a poder hacer con telwin sin ningún tipo de problema estos por ejemplo son los que
3:11
utiliza Apple esto esto que veis aquí esto se puede hacer bastante fácil con
3:17
grid y vamos a intentar daros las herramientas para que podáis crear el que os dé la gana para que no tengáis
3:23
ningún problema de hacer esto que esto lo podáis hacer con css facilísimo las
A mover las manitas
3:29
clases de la semana pasada del curso de css las tenéis en mi canal de YouTube secundario y vamos con nuestra
3:34
herramienta favorita que es cod link vale la semana pasada nos quedamos aquí utilizando Flex hicimos un montón de
3:41
cosas raras todo esto lo vamos a lo vamos a quitar vale porque no lo vamos a necesitar Entonces por ahora todo esto
3:47
lo quitamos pum y vamos a quitar también todo esto y por ahora vamos a dejar aquí
3:52
no sé si poner un container vale un container y ahora empezaremos por aquí
3:57
estas cosas antes de nada vamos a definir Qué es grid Para qué sirve grid cómo funciona grid y de qué estamos
Qué es Grid?
4:03
hablando con grid a ver grid básicamente voy a enseñaros una imagen que Ah Bueno
4:08
mira me sirve esta imagen por ejemplo Estoy seguro que habréis visto imágenes como esta como esta que tenéis un layout
4:15
donde queréis poner pues arriba queréis el header en un lado la navegación abajo queréis poner el footer pero aquí tenéis
4:22
una car aquí otra o tenéis los resultados de una búsqueda por ejemplo resultados de una búsqueda donde queréis
4:27
que están una al lado de la otra o lo que queréis es hacer un Vento un Vento
4:32
un Vento grid de esto Vento es esta maquetación nueva en la que tú puedes poner como columnas y cada columna tiene
4:39
una altura diferente por ejemplo Estos son tres columnas como podemos ver tres columnas Y tiene tres filas lo que pasa
4:46
es que este este cajón este cajón Fíjate que ocupa dos filas en cambio Tenemos
4:52
aquí algunas Cars que solo ocupan una así que ya queremos hacer una diferenciación de que algunas ocupen más
4:58
que otras y y esto lo vamos a poder lograr con grid esto de poder tener una
5:04
cuadrícula que podamos controlar en dos dimensiones Cómo se van a comportar las
5:09
cosas este sistema de maquetación bidimensional es lo que hablamos de grid
5:15
Okay una cuadrícula con un conjunto de líneas tanto horizontales como verticales que al final hacen
5:20
intersección y aquí podemos tener elementos y estos elementos pues pueden tomar una sola columna dos columnas tres
5:27
cuatro filas lo que sea y siempre pues Que respete el conjunto Cuál es el diseño de css Por qué es tan importante
5:35
grid Por qué le da miedo a la gente le da mido a la gente porque grit se enseña mal no hay muchos sitios donde se enseña
5:41
bastante bien De hecho os voy a recomendar como siempre os recomiendo eh un recurso que os va a encantar que está
5:47
muy chulo que es el de mi amigo manz vale que está muy bien explicado que podéis ir y le podéis dar cañita tiene
5:54
un montón de ejemplos y tal que lo explica superb y y eso vale Así que le podéis echar un vistazo que además tiene
6:01
un montón de de dibujitos y así lo podéis acompañar con todo este tipo de cosas y luego además además al final del
6:09
curso de hoy os voy a recomendar el juego típico que siempre se hace que es este el grid Garden el juego de grid
6:16
Garden es un juego que tiene 28 niveles donde Vais a poder poner en práctica todo lo que Vais a aprender en la clase
6:22
de hoy y así os
6:29
aseguraros Pues que las cosas estén en su sitio correcto por ejemplo las las zanahorias tienen que estar aquí y esto
6:36
no tiene que estar ahí tienes que mover las cosas está muy chula vale Y así que para aprender lo que necesitas yo te lo
Características de Grid
6:41
voy a explicar hoy aquí Entonces ya sabemos grid no pero uno de los problemas que tenemos con grid es Cuáles
6:47
son las características concretas No si que te he dicho que es una cuadrícula pero tienes que saber que los elementos
6:52
pueden tener tamaños fijos o flexibles que podemos posicionar elementos en
6:57
cualquier sitio de la cuadrícula esto quiere decir que un elemento no tiene
7:03
por qué seguir el orden estricto típico que siempre vemos de arriba abajo izquierda derecha sino que el primer
7:08
elemento lo puedes poner el último y todo lo demás vacío o el el que el último lo puedes poner el primero y que
7:14
ocupe la mitad vale lo puedes poner donde quieras además los elementos se van colocando en esta cuadrícula y
7:20
importante se pueden poner elementos superpuestos esto quiere decir que tú puedes poner un elemento encima de otro
7:27
que esto es algo que no normalmente no se puede hacer en todos y necesitas utilizar position absolute que lo vimos
7:34
en clases anteriores Bueno pues en grid esto es como una excepción porque sin
7:39
utilizar position absolute puedes poner un elemento encima de otro veremos un ejemplo después porque es muy interesante Porque mucha gente cree de
7:47
forma errónea que solo se puede lograr composition absolute y no es cierto también lo puedes utilizar con grid
7:54
totalmente fácil la diferencia clave vale la pregunta del millón que todo el mundo se hace siempre bueno Cuál es la
Grid vs Flex
8:00
diferencia entre Flex y grid por qué debería utilizar Uno cuál por qué debería utilizar otro Cuál es mejor
8:06
pregunta errónea porque no hay nada que sea mejor que lo otro todo depende del contexto A ver flexbox es un sistema de
8:14
maquetación unidimensional es decir que solo nos permite trabajar en un eje
8:20
filas o columnas y la diferencia básica Entonces es que grid como ya he dicho
8:25
nos permite trabajar en los dos ejes filas y columnas Así que en Flex vamos a
8:30
tener que elegir uno de los dos y en grid vamos a poder utilizar los dos es mejor uno que el otro no Simplemente si
8:36
tú tienes un diseño bidimensional que vas a tener que pensar tanto en filas como en columnas vas a querer
8:42
seguramente utilizar grid Vale y de hecho vas a ver que Flex y grid comparten muchas especificaciones a la
8:49
hora de alinear y justificar elementos contenedores contenido y todo esto Así
8:54
que si has aprendido Flex muchas de las cosas que ya sabes te van a servir para grid Así que simplemente es eso ahora me
9:00
diréis Bueno pero entonces pues para eso utilizo siempre grid tampoco hace falta porque hay veces que no hace falta que
9:07
tengas columnas por ejemplo Imagínate que tú lo único que quieres en este caso aquí claramente tenemos dos columnas
9:13
tenemos tres filas y Aquí vamos a querer utilizar grid porque te va a simplificar mucho hacer esto con Flex es mucho más
9:21
complicado porque el tener que poner esto luego que esto esté arriba y esto
9:26
se quede abajo que esto no sé qué y que esto además en Flex sea responsive va a ser mucho mucho más complicado vale si
9:33
lo intentas hacer con Flex en cambio con grid va a ser mucho más fácil ahora bien si fuese que tienes una sola línea ya
9:40
sea de filas o de columnas al final lo que tendríamos aquí directamente y será mucho más fácil sería hacerlo con Flex
9:46
entonces una sola dimensión Flex bidimensión grid Punto Pelota por eso Si
9:52
Solo tienes una dimensión no te va a valer la pena utilizar grid porque a lo mejor te lo complica sin necesidad
9:57
entonces no es que sea mejor o peor sino que simplemente cada uno está hecho para una cosa en concreto vamos a crear un
Grid en código
10:03
ejemplo básico Tenemos aquí un section con siete elementos que son dips porque sé que os encantan los dips vamos a
10:09
estilar un poco esto para que lo veamos un poquito mejor vamos a estilar el container le ponemos un background de yo
10:14
que color salmón le ponemos aquí un borde que sea negro y Esto será el
10:20
contenedor vale el contenedor Fíjate que tiene este borde color negro le voy a poner un B de radius vale que creo que
10:25
todavía no habis visto el borde radius Pero al menos para que teamos esto está funcionando de forma por defecto O sea
10:31
container ya sabéis que como es un section tanto section como dip por defecto tienen el display lo tienen como
10:39
si fuese block vale Este sería el valor por defecto Y esto es lo que vamos a
10:44
cambiar ahora ahora lo que vamos a hacer es que el container todos los containers que el dip que tenemos dentro del
10:50
container Vamos a ponerle un light Blue Vale y vas a ver que ahora mismo Está rellenando todo el espacio del
10:57
contenedor Tenemos también vamos a poner acá un un borde Así que sea de color 09f
11:03
y un borde radius vale de 6 píxeles vale Fíjate que cada uno de los elementos
11:09
está ocupando totalmente el espacio y esto por qué está pasando porque ya vimos vale Ya vimos Sí el salmón
11:15
desapareció pero ahí está ahí está veis que está ahí justo debajo Entonces qué es lo que está pasando que con display
11:21
block lo que está haciendo es ocupar todo el espacio y hace un salto de línea
11:26
esto sería el valor por defecto de lo que está ocurriendo no vamos a empezar a crear nuestra primera cuadrícula vale vamos a poner nuestra
Nuestra primer Grid
11:32
primera cuadrícula voy a poner para que esto no sea tan vamos a poner que esto tenga un background con un poquito así
11:41
para que no sea blanco puro que no moleste tanto vale muy bien Vamos a empezar con el grid voy a querer que mi
11:48
contenedor lo que tenemos de color negro sea una cuadrícula qué tenemos que hacer
11:53
pues tenemos que utilizar display y le ponemos que esto es un grid anda si no
11:59
cambiado sigue igual menudo timo menudo timo Ajá ha cambiado o no ha cambiado
12:04
parece igual vale parece igual pero vamos a ver una cosa Fíjate si tú abres Este ejemplo y le das a inspeccionar
12:11
vamos a ver aquí no sé por qué me lo he abierto en otra ventana pero vamos a ver aquí que fíjate que ahora al lado de
12:17
section tienes este botoncito de grid y aquí ya ojo cuidado que está trucazo
12:22
trucazo de las herramientas de desarrollo eh fíjate que tenemos aquí Este grid si le das un click ojo ya
12:29
pasan cosas vale le puedes dar un click aquí justamente que te indica si es un grid Y fíjate que le pone aquí como un
12:36
montón de numeritos y no sé qué no te preocupes que hoy vas a salir conociendo
12:41
entendiendo dominando estos numeritos vas a saber qué son estos numeritos y vas a alucinar
12:47
cómo de potentes son estos numeritos pero por ahora Quédate que al menos algo diferente tenemos Porque fíjate que si
12:52
le quitas el display grid esto desaparece no tenemos numeritos si ponemos el display grid tenemos numeritos vale Así que algo algo ha
13:00
cambiado no lo suficiente no pero tenemos numeritos Qué significa estos numeritos estos numeritos al final lo
13:06
que nos está indicando son las filas que tenemos en nuestra cuadrícula visualmente ahora qué podríamos decir
13:11
que esta cuadrícula tiene una sola columna una columna no porque puedes ver que solo tiene una columna y tenemos
13:19
siete filas una 2 3 4 5 6 7 por defecto
13:24
lo que está pasando aquí es que nos ha nos está fluyendo el contenido
13:29
poniendo el contenido uno cada uno de los elementos en cada fila No eso es lo que está haciendo está fluyendo el
13:35
contenido así está ocupando todo el espacio lo está poniendo cada uno pero yo lo que me gustaría Imagínate que quieres tener dos columnas en tu
13:41
cuadrícula no porque dices ostras es que una columna es un poco rollo yo lo que quiero es tener dos columnas bueno Cómo
13:47
definimos que queremos tener dos columnas ahora mucha gente diría pues git calls 2 porque esto es lo que hago
13:52
en telwin vale Pero qué es lo que está haciendo telwin por detrás lo vamos a entender y lo vamos a ver tenemos que
13:57
utilizar la propiedad grid template columns vale y le vamos a indicar Cuántas columnas queremos que tenga
14:04
nuestra cuadrícula y le tenemos que poner el espacio que tiene que utilizar cada columna Imagínate que queremos dos
14:10
columnas de 100 píxeles Vale pues le vamos a decir una columna de 100 píxeles Fíjate que ya solo con esto ha cambiado
14:16
porque qué es lo que está pasando le estamos diciendo que nuestra cuadrícula tiene una columna de 100 píxeles y ya
14:23
nos ha puesto que esto sean 100 píxeles y lo está agrupando así pero le podemos decir que tenga otra más de otro 100
14:28
píxeles y Fíjate lo que ha pasado ahora tenemos dos columnas de 100 píxeles y lo que está pasando Es que los elementos se
14:35
van a distribuir en esta cuadrícula de izquierda a derecha y de arriba a abajo Eso es porque nosotros leemos así vale
14:41
pero ya vimos la semana pasada vale que la dirección en la que se distribuyen los elementos es importante dependiendo
14:47
de cómo es eh la dirección de lectura para cada uno de nuestros usuarios para nosotros que somos latinos pues para
14:54
nosotros es así pero tened en cuenta esto que no todo el mundo no no está bien decir de arriba a abajo y izquierda derecha porque no en todos los sitios es
15:00
así es según la dirección de lectura ahora bien Imagínate que quieres Añadir un tercero pues no pasa nada otros 100
15:07
píxeles y ahora tenemos tres columnas y cada columna es de 100 píxeles y se
15:12
distribuye el contenido así vale también podemos utilizar otros valores por ejemplo podríamos utilizar el valor de
15:18
auto qué es lo que hace el valor de auto Fíjate que el de auto lo que ha hecho es ocupar un poquito más que que el otro y aquí Le podremos decir que ese solo sea
15:25
20 píxeles y el tercer la tercera columna sea de 100 así que tenemos que la primera columna son automático que
15:32
ahora te explicaré lo que es la segunda son 20 píxeles y la tercera son 100 píxeles vale el auto Qué quiere decir
15:39
auto es de automático pero auto lo que quiere decir exactamente Es que el
15:44
navegador es el que va a decidir Cuál es el espacio que tiene que utilizar y lo va a hacer dependiendo del espacio que
15:51
hay disponible y del contenido que esto es importante según el contenido del texto aquí lo que está ocurriendo es que
15:57
como tenemos dos fijos claro este seguro es de 100 este seguro es de 20 y ha dicho Bueno pues este como es auto
16:03
utilizo el resto y ya está mucho más fácil pero si tienes dos que son auto Aquí sí que va a ver va a ser un poquito
16:09
más más complejo no porque podemos decir vale Este es de 20 píxeles pero este es automático y este es automático pero
16:15
claro si son automáticos Fíjate que según el contenido que hay dentro Pues claro como tiene más contenido va a
16:21
decir el navegador Ah claro como este tiene más contenido me ha dicho es automático voy a hacer que sea más ancho
16:27
que ocupe más espa esta columna que la segunda que necesita menos vale entonces fíjate Y esto es importante porque mucha
16:33
gente se cree que el automático automáticamente siempre va a tener el mismo espacio y no es así vale no es así
16:41
entonces ya hemos visto que podemos ir combinando diferentes valores y tenemos el automático tenemos los píxeles Y
16:48
tenemos obviamente más eh tendríamos podríamos si lo ponemos todo en auto auto auto va a utilizar siempre según el
16:53
contenido esto perfecto y también podemos mezclar y hacer por ejemplo
16:58
vamos a hacer ahora cinco columnas vamos a quitar esto vamos a poner cinco columnas y le podemos decir que la
Creando más columnas
17:04
primera columna sea con porcentajes que la segunda sea con píxeles que la tercera sea automática y que la cuarta
17:10
sean 10 puntos del viewport vale o sea un 10% del viewport del ancho del
17:15
viewport y Lo tendríamos Así Fíjate ahora tenemos cuatro columnas donde cada columna esta primera columna tiene es un
17:21
50% del contenedor el dos este ocupa 100 píxeles el tercero es automático y el
17:27
cuarto son un 10% del ancho del viewport vale o sea que ya veis que podéis
17:33
mezclar unidades sin ningún tipo de problema no es lo lo normal lo habitual
17:38
ni lo aconsejable vale ni lo aconsejable porque al final aquí la podéis liar muy parda eh Pero bueno no os preocupéis que
17:45
esto lo iremos viendo de cómo lo podemos arreglar sobre todo porque ahora vamos a explicar una unidad especial y es que
Unidad especial
17:52
hay una unidad especial y específica que solo funciona con grid y es la de
17:59
fracción Qué significa fracción Bueno vamos a poner aquí en grid template columns fijaos que tantos valores como
18:05
ponéis son el número de columnas que vamos a tener aquí tenemos cuatro valores por lo tanto tenemos cuatro
18:11
columnas y automáticamente Fíjate que me ha generado otra fila o sea porque lo
18:16
que está intentando es es fluir los elementos y si no caben pues ya a la siguiente fila Vale ahora si yo quito
18:23
esto y le pongo 100 píxeles una sola columna de 100 píxeles pero vamos a
18:29
utilizar las fracciones Qué es una fracción es una unidad especial que nos permite indicar el tamaño de las
18:36
columnas de forma proporcional proporcional a qué bueno se llama FR No
18:42
si le ponemos una fracción Fíjate que ha ocupado todo el espacio Por qué Porque
18:47
una fracción por defecto si no tiene nada más va a ser el 100% del espacio no
18:52
una fracción si tiene que ocupar una fracción y no hay más columnas es el 100% del espacio Pero qué pasa que si
18:59
tenemos dos columnas y cada una tiene una fracción Qué significa esto Pues que
19:05
claro si el 100% lo divides entre dos vamos a tener que cada columna es una
19:10
fracción y por lo tanto cada fracción tiene que ser del 50% va a ser Mitad y Mitad si tenemos tres pues esto lo que
19:17
va a decir es que es un tercio una fracción como hay tres fracciones en total cada columna va a ser una fracción
19:24
por lo tanto va a ser un 33,33 por. y estas fracciones no son puedes utilizar una fracción Imagínate que solo quieres
19:31
dos columnas vale Pero quieres que la primera sea una fracción y la segunda columna sea el doble pues haces dos
19:38
fracciones y Fíjate lo que hemos hecho aquí la primera columna tenemos que es una fracción y la segunda columna es el
19:45
doble de la primera columna lo que estamos consiguiendo Ho aquí es que haya algún estilo de forma relativa de decir
19:53
que queremos que una columna sea el doble de la otra y ojo no tenéis que utilizar como forma base una fracción
19:59
podéis decir Estos son dos fracciones y estas son cuatro vamos a conseguir lo mismo pero fíjate que lo que estamos
20:05
diciendo es que estas son dos fracciones y estas son cuatro es el doble y podríamos Añadir otra que fuese una
20:11
fracción y lo que está pasando aquí es que tendríamos que dividir No aquí tenemos 2 4 y 6 son serían 100 entre 6 y
20:18
una fracción sería sería justamente Esta división y así sabríamos perfectamente A
20:23
qué se refiere cada una así que esto es la clave cuando trabajemos con grid el conocer las fracciones porque las
20:31
fracciones lo que significa es cómo tenemos que separar todo el espacio y va a depender de Cuántas columnas tengáis
20:37
vale fíjate Ah que lo he contado mal era siete perdón eh que he dicho seis era eh
20:42
100 / 7 perdón eh que me equivoqué entonces voy a volver a explicar lo de las fracciones porque es muy importante
20:48
vale una fracción si solo tenemos una columna y es una fracción Esto va a ser un 100% No si tenemos dos columnas y
20:56
cada columna es una fracción cada columna va a ser un 50% Fíjate en una
21:01
cosa si decimos que una columna es una fracción y la otra son 100 pixeles
21:06
Entonces cuánto va a ser cada una pues muy fácil hemos dicho que empezamos con
21:12
el 100% no empezamos con el 100% y tenemos que una columna esta columna la
21:19
segunda que es esta que tenemos aquí son 100 píxeles pues 100% menos 100 píxeles
21:25
lo que tengamos aquí va a ser el el el ancho que va a tener la fracción vale
21:30
porque va a ser el resto ya está así de fácil o sea lo que vamos a tener es esta columna que es una fracción va a ser el
21:37
resto del 100% menos los 100 píxeles vale Y ahí Lo tendríamos el texto no
21:42
influye Porque da igual lo que tengamos dentro al final es una fracción de las columnas que tenemos Punto Pelota no
21:48
importa ya el contenido que tengamos porque eso solo sería con el auto Así que básicamente lo que no esté ocupado
21:54
efectivamente Así que lo mismo si hacemos una tercera columna Así que una fracción será 100% men 100 píxeles menos
22:03
buen vamos a poner 50 píxeles para entendamos mejor vale Y esto sería una fracción OK Así Lo tendríamos es más
22:11
cómodo escribir la fracción con porcentaje porque así te evitas de calcularlo claro es mucho más fácil porque imaginad que lo queréis hacer así
22:17
esto sería lo mismo que escribir una fracción y una fracción sería lo mismo visualmente pero claro esto es un
22:23
cálculo bastante fácil y que lo tenéis bastante Claro pero imag que tenéis
22:29
cinco columnas y y tenéis que estar pensando y dividiendo mentalmente cómo tiene que ser cada cosa y tal Qué pasa
22:36
con una sola columna si son dos fracciones buena pregunta no no pasa absolutamente nada si yo le pongo aquí que tiene 100 millón de fracciones las
22:43
cuántas columnas hay solo hay una columna no solo hay una columna Entonces el 100% son estas fracciones ya está
22:52
porque solo tiene una columna el tema es cuando tiene más de una que entonces hay que empezar a calcular pero si solo hay
22:58
una columna da igual Cuántas fracciones pongas que son Porque si solo indicas que 1000 fracciones es una columna pues
23:04
ya lo tendrías ya lo tendrías hecho así que las fracciones Lo importante es cuando queremos dividir por ejemplo
23:11
entre tres No pues aquí el 100% dividimos entre tres fracciones 33,3 pensad en pizzas que muchas veces es
23:17
mucho más fácil y ya lo tendréis Pero lo importante es cómo podemos fraccionar nuestro contenido para básicamente así
23:24
de esta forma sin necesidad de poner porcentajes que funcione correctamente así tenemos una fracción una fracción y
23:30
una fracción Y de nuevo podemos decir 200 píxeles 200 píxeles y una fracción
23:36
veis aquí en este caso lo que pasa que está saliendo esto es normal eh Porque claro le estamos poniendo más espacio del que tiene estamos obligándole que
23:42
tenga como más espacio y justamente por esto también Vais a querer evitar muchas veces el poner anchos fijos que esto lo
23:50
vamos a ver después de cómo lo podemos arreglar para evitar este tipo de problema que hemos visto aquí claro le estoy diciendo tenemos tres columnas la
23:56
primera 200 píxeles las seg la tercera es 200 píxeles y luego el resto pero claro fíjase que el resto ya no le queda
24:02
nada así que está rompiendo el contenedor esto veremos cómo lo podemos arreglar y vas a ver que es muy sencillo Bueno vamos a poner dos fracciones o sea
grid template rows
24:09
tenemos dos columnas y al final pues 50% y 50% por ahora ponemos dos fracciones y ya está pero fijaos en una cosa
24:16
automáticamente lo que está ocurriendo aquí es que me está creando filas y las filas están tomando el alto que le da la
24:23
buena la le dé la gana no O sea me ha creado aquí filas me ha creado una dos tres cuatro filas me ha creado pero me
24:30
los está haciendo con el ancho que le ha dado la gana el ancho que está utilizando Fíjate que es que ha dividido
24:35
el número de filas por el espacio disponible y lo ha rellenado y ya está no podríamos decir que ahora mismo en
24:41
los rows tendríamos una fracción una fracción Ay me lo he cargado una fracción una fracción y una y una
24:47
fracción o sea tenemos cuatro fracciones cuatro filas y ya está pero vosotros podéis cambiar también cómo queréis que
24:52
sean las filas podéis hacer lo mismo grid template rows y decirle quiero que la primera fila sean 100 píxeles que la
24:59
segunda sean 50 píxeles que la tercera sean 25 píxeles o un poquito más 30
25:04
píxeles y que la última sea 100 píxeles vale Y fíjate lo que hemos conseguido ya y aquí es justamente Lo que empezamos a
25:11
hablar muchas veces con el tema de El que sea bidimensional y esto luego lo veremos cuando empecemos a crear un
25:17
layout real de una página para que veáis Cuál es la clave de todo esto fijaos que lo que estamos haciendo es decirle la
25:23
primera fila es de 100 píxeles por lo tanto esta fila de aquí de izquierda derecha tendría que ser de altura de 100
25:31
píxeles la segunda fila es de 50 píxeles Así que esta como puedes ver Es más
25:36
corta que la primera Y es de 50 píxeles la tercera de 30 Bueno pues aquí tenemos esta más más cortita y pone aquí que la
25:43
cuarta de 100 píxeles y la tendríamos aquí y Qué pasa si le ponemos aquí otra de 50 píxeles tan tan tan Pues que la
25:50
añade ojo con esto que es un error bastante común y es el hecho de que la
Cuadricula vacia
25:55
gente cree que la cuadrícula se crea a través de los elementos y no es así O
26:01
sea vosotros podéis tener una cuadrícula vacía fijaos en esto fijaos que he creado una fila aquí de 50 píxeles
26:07
podéis poner lo que os dé la gana veis Y qué va a ocurrir con esto pues lo podemos ver fácilmente en las herramientas de desarrollo Vais a ver
26:13
que está la cuadrícula aunque no haya un elemento vale si miráis aquí y le dais a
26:19
grid fijaos que cuando os ponéis encima vale Vais a ver cómo no se va a ver casi
26:24
en el en el streaming vale pero sí que se ven como unas rayitas un borde ahí que que no es sólido que te indica los
26:30
elementos que deberían ir dentro de la cuadrícula aunque no haya un elemento dentro vale importante tú puedes tener
26:36
una cuadrícula donde dentro no haya un elemento Y esto es un error muy común donde la gente dice Pero por qué este
26:41
está Porque qué está este espacio porque está bueno piensa en un Excel Cuando tenemos en Google docs un Excel piensa
26:48
en esto esto sería una cuadrícula vale una cuadrícula básicamente en la que tendríamos aquí el hecho de que está
26:55
totalmente vacía pero la cuadrícula ya la tienes hecha donde tendrías aquí cada una de las cosas y puedes poner donde tú
27:01
quieras vale Así que ten en cuenta esto ten en cuenta que la cuadrícula puede estar vacía pero puede estar creada
27:07
aunque tú no veas un elemento dentro no significa que no pueda haber una cuadrícula y aquí lo puedes ver
27:12
claramente que hemos hecho mira lo voy a hacer un poquito más pequeño para que lo veas este espacio de 10 pixels eso en
27:18
realidad ese espacio Fíjate que tiene la cuadrícula ya preparada vale Así que ahí
27:24
ahí lo teníamos ten en cuenta que puedes crear cuadrículas que no haya elementos dentro importantísimo vale Y ahora que
27:31
tienes esto ya clarísimo vamos a ver qué qué hacemos con lo siguiente porque antes te he comentado que vale podríamos
Filas automaticas
27:38
cambiar esto mira lo podemos cambiar aquí con el template Rose si lo quitamos genera filas de forma totalmente
27:44
automática Vale ahora ojo porque también tenemos una forma de indicar fácilmente
27:50
Cuál es el tamaño que tienen que tener las filas que automáticamente se generan fíjate que yo aquí solo estoy diciendo
27:57
Oye Quiero que mi plantilla de la cuadrícula tenga dos columnas no le digo las filas pero las está generando no
28:04
cuando no caben genera nuevas filas pues tenemos una propiedad que le podemos indicar Oye cuando esta grid
28:11
automáticamente me cree filas quiero que tengan una altura y quiero que la altura
28:17
de todas las que genera sea de 200 píxeles vale Y ves el cambio lo que estamos diciendo aquí de alguna forma es
28:23
Oye cada vez que tengas que generar una fila automáticamente quiero que tenga
28:29
esta esta altura que sea de 100 píxeles le puedes poner lo que tú quieras y Fíjate cómo está cambiando la diferencia
28:35
entre lo que tendríamos a nosotros indicarle las filas que automáticamente se pongan y ten en cuenta otra cosa
28:41
Aunque tú tengas un template de las filas y le digas la primera fila quiero
28:46
que sean 100 píxeles Vale y lo cierras Fíjate lo que va a hacer la primera fila
28:51
que es esta que tendríamos Aquí esta que tendríamos aquí la primera fila le hemos dicho que sea de 100 píxeles pero el
28:57
resto de filas las ha tenido que generar y por lo tanto las Ha generado automáticamente y ha dicho Bueno voy a
29:03
ver cuál es el tamaño que me has dicho de las filas que tengo que generar yo por lo tanto de la primera que le hemos
29:09
dicho ha utilizado la de 100 píxeles y como del resto No le hemos puesto ha utilizado esta vale Así que esto es
29:15
bastante importante a la hora de controlar cuando se generen nuevas filas
29:21
qué es lo que tenemos que utilizar o sea queremos que se vean de alguna forma queremos que tenga algún tipo de tamaño
29:26
lo podéis poner así vale superimportante se puede hacer igual en columnas se puede hacer lo mismo en columnas lo que
29:31
pasa es que para las columnas que lo veremos después es que a la hora de cómo se generan
29:37
El el autoflow cómo se genera por defecto ves por defecto se generan en
29:43
filas cuando algo no cabe se genera en filas este sería el valor por defecto vale el valor por defecto es que se
29:49
genera en filas Pero puedes ver que hay otras por ejemplo en columnas ves y en column Fíjate lo que hace en columnas al
29:55
final lo que hace es intentar meterlas todas en la columna O podría meterlo denso que esto lo veremos más adelante
30:00
que lo que hace es rellenar los huecos con aquellos que pueden pero por defecto lo hace por rows pero también lo podrías
30:07
hacer con columnas obviamente lo que pasa es que tienes que cambiarle la dirección que lo harías eh pongamos que voy a quitar esto pongamos que tenemos
Propiedad repeat()
30:13
aquí tres fracciones vale eh o mira mejor vamos a poner aquí 200 píxeles un
30:19
vamos a hacer algo así y lo vamos a hacer también vamos a tener tres columnas vale vamos a quitar aquí esto
30:27
que lo había puesto como un poco vamos a poner el uno el dos y el tres así normal vamos a tener tres columnas 100 píxeles
30:33
una fracción 50 píxeles eh vamos a poner ahora que la vamos a tener tres filas y
30:39
vamos a decir que sean 100 píxeles 100 píxeles y 100 píxeles no lo queremos hací bueno Esto normalmente es algo que
30:46
Vais a repetir mucho Cuando hacemos una cuadrícula un problema que vamos a tener constantemente es que vamos a querer
30:52
repetir lo mismo una y otra vez O sea por ejemplo Vais a querer las columnas que sea una fracción una fracción y una
30:58
fracción no tres veces estamos repitiendo lo mismo y las filas estamos repitiendo tres veces lo mismo no esto
31:04
lo Vais a ver repetido 10,000 millones de veces y hay una función un método que te permite simplificar esto que es el
31:10
método de repeat qué es lo que te permite imagínate aquí que en este grid template columns le dices en lugar de
31:16
tener que poner manualmente Cuántas veces tiene que ser lo que puedes decirle es Oye quiero que repitas tres
31:22
veces una fracción vale Y esto es exactamente lo mismo A lo que hemos hecho lo que estamos diciéndole aquí es
31:28
que queremos tres columnas de una fracción y aquí podríamos hacer exactamente lo mismo Oye repite tres
31:34
veces los 100 píxeles o incluso podríamos decirle Pues que sean cinco veces Entonces ahora me crearía cinco
31:40
columnas de una fracción Lo bueno que tiene el repeat es que nos va a permitir muy rápidamente sin necesidad de estar
31:46
todo el rato repitiendo lo mismo el hecho de escribir Cuántas columnas queremos siempre y cuando sea
31:52
exactamente el mismo valor pero también se puede utilizar solo para una parte y
31:57
mira y esto es una cosa que muy poca gente sabe vale el repeat Imagínate que
Nadie sabe esto sobre el REPEAT()
32:02
quiero hacer que el primero sean 25 píxeles una fracción una fracción
32:08
eh una fracción vale algo así O sea quieres que la primera columna esta de
32:14
aquí sea un poquito más cortita que solo sean 25 píxeles y esto sean tres veces
32:19
una fracción aquí hay mucha gente que se cree que Entonces ya no puede utilizar repeat y he visto incluso prs que la
32:25
gente a lo mejor había empezado con el repeat pero aquí como no se podía utilizar pues lo quitaba no pero sí que
32:31
se puede o sea hay que tener en cuenta que aquí como está repitiendo tres veces la fricción puedes hacer esto repeat 3 1
32:37
FR y lo que tienes que tener en cuenta es que al final lo puedes utilizar solo para una parte por ejemplo Imagínate que
32:43
al final queremos utilizar queremos crear una quinta columna aquí a la derecha que sea también de 25 píxeles
32:50
pues lo puedes poner Y fíjate la primera columna 25 píxeles que sea esta del uno
32:55
luego tres veces una fracción que sería la del dos la del tres y la del cuatro y finalmente la última columna 25 píxeles
33:03
incluso y a ver esto lo habéis pillado porque esto está bastante chulo y al final mucha gente se cree que que no se
33:09
puede hacer y el tema es que con esto tenemos cinco columnas la primera de 25 píxeles tres veces una fracción porque
33:16
estamos utilizando el repeat y luego una quinta columna de 25 píxeles sí esto entendido perfecto vale es como si fuera
33:23
una función que hace un splash es como es una función que básicamente te cambia esto por esto vale es como lo mismo esto
33:31
mira lo voy a hacer para que lo veáis más claro es básicamente que cuando ve esto esto lo cambia por esto vale es una
33:39
equivalencia Perfecto ahí está eh pero espérate porque hay otra una cosa todavía mejor a esto eh Y es el hecho de
33:46
imaginad que queréis que sea 25 píxeles 100 bueno 50 píxeles 25 píxeles 50
33:52
píxeles Vale y 25 píxeles y 50 píxeles algo así vale queréis que sea la primera
34:00
25 píxeles la segunda 50 la tercera 25 la cuarta 50 La Quinta Entonces ya veis
34:06
que se está repitiendo algo verdad veis que se está repitiendo un patrón tres veces se está repitiendo 2550 2550 2550
34:13
se está repitiendo tres veces pues esto también se puede hacer con el repeat otra cosa que muy poca gente sabe
34:18
entonces se puede hacer esto y le puedes decir quiero que esto lo hagas tres veces y veis está quedando Exactamente
34:24
igual está diciendo quiero que tres ve me pongas la primera y la segunda columna vale Así que ya veis que también
34:31
es mucho más potente de lo que parece que también podéis utilizar esto es normal poner tantas columnas es normal
34:37
Claro que sí claro que puede ser que tengas tantas columnas o sea por ejemplo eh en Google cuántas columnas ves aquí
34:44
claro es que vosotros muchas veces os os
34:57
un montón al final depende un montón de hecho os os voy a decir algo un
Ejercicio practico Excel (recomendado)
35:02
ejercicio muy chulo que podéis hacer con grid Y si queréis aprender un poquito de
35:07
javascript es el hecho de hacer un spreadsheet lo podéis hacer con grid esto podéis hacer que cambie Y fijaos
35:14
qué es lo que podéis hacer aquí que cuando solté el ratón le
35:25
cambiábamos 10 veces una fracción vale Y así lo lo podríais tener y así podéis
35:31
hacerlo la verdad podéis hacer un clone con display grid bastante fácil así que para que lo sepáis entonces tema de las
35:37
columnas son muchas o pocas es que depende de la ui No es que sea normal o no normal es que depende del diseño
35:43
Habrá más columnas o menos columnas y ya está y no no pasa absolutamente nada vamos a quitar todo esto una cosa muy
35:49
común que Vais a ver en grid es el hecho de que imaginad que tenemos unos resultados unos resultados Esto está
35:55
bastante chulo no que tenéis unos resultados eh tenéis unos resultados de búsqueda y queréis que como mínimo claro
36:02
normalmente decís Bueno pues quiero que sean tres columnas ya está quiero que sean tres columnas Pero qué pasa que no
36:08
queréis que pierda un valor mínimo O sea a lo mejor queréis que la primera columna como mínimo ocupe algo y claro
36:15
si así siempre lo hacéis Imagínate tú esto lo haces ahora más pequeño Ves lo haces más pequeño y siempre su ancho va
36:22
a ser en concordancia a los demás por porque es un tanto por cada fracción va a cambiar por lo tanto si ahora aquí
36:29
Pues imagínate tiene 100 píxeles cada columna Será 33.3 pero imagínate que por
36:35
lo que sea quieres que la primera columna siempre sea de un ancho mínimo
36:40
Pues eso lo puedes lograr cómo lo puedes lograr utilizando otro método una función que css grid tiene que te
36:47
permite definir un tamaño mínimo y Máximo para las filas o las columnas eso
36:53
lo puedes utilizar ahora lo vamos a utilizar para las columnas pero lo puedes utilizar también para filas Imagínate que esta primera columna de
36:58
aquí queremos que como mínimo queremos que como mínimo sea
37:06
de 100 píxeles vale Y que como máximo sea de un fragmento una fracción qué es
37:13
lo que vamos a hacer aquí lo que va a pasar aquí es que como mínimo siempre siempre la primera columna va a ocupar
37:19
100 píxeles nunca va a ser menos y lo que va a ocurrir es que en ese supuesto se va a comportar Como si fuese así y
37:26
por lo tanto el resto de fracciones van a dividir el espacio disponible pero cuando pueda ser de más de 100 píxeles
37:33
se va a comportar como si fuese una fracción más y por lo tanto va a conseguir el 33,3 por del espacio dicho
37:40
de otra forma cuando el 33,3 1% del espacio del espacio sea menor de 100
37:46
píxeles se va a quedar en 100 píxeles vale eso es lo que explicaría esto y este 33,3 viene porque como hemos dicho
37:54
que como máximo es una fracción cuando todo el espacio se divide en tres fracciones sería 33,33 vamos a verlo en funcionamiento si
38:02
nos vamos aquí a la preview vale fíjate que ahora si lo hacemos un poquito más pequeño si soy capaz de pillar de algún
38:08
sitio vale lo vamos haciendo pequeño pequeño pequeño Vale y tan pequeño lo puedo hacer que no no lo vemos
38:14
funcionando a ver lo voy a hacer aquí pero se me va a romper otra vez Esto vale Fíjate en la primera columna vale
38:19
fíjate la primera columna ves la primera columna ha llegado un momento que se
38:25
queda siempre siempre en 100 píxeles vale Pero cuando su tamaño puede ser mayor a 100 píxeles porque la fracción
38:32
ya tiene ese espacio Entonces sí que crece pero su tamaño mínimo va a ser de
38:37
100 píxeles y el resto se va a tener que adecuar al espacio que tiene disponible
38:42
como el primero toma 100 píxeles el resto va a tener que dividirse vale Y por eso estáis viendo que los otros sí
38:48
que se quedan un espacio igual pero el primero se queda fijo en 100 píxeles y esto lo estamos consiguiendo Gracias
38:54
básicamente a este mmax le estamos diciendo Oye la primera columna como mínimo tiene que ser de 100 píxeles y si
39:00
no tiene que tomar el espacio de una fracción Okay este método es super importante y super interesante y para
39:07
que veáis un caso super típico que va os va a acompañar toda vuestra vida vale
39:12
porque esto lo Vais a ver así de veces así de veces es el hecho de Mira voy a
39:17
hacer un voy a hacer un ejemplo rápido en un momento para que os deis cuenta mira tengo por aquí un html que os va a
39:24
sonar que sería así no el tener un dip y tenéis una barra lateral y un Main tenéis un Main al lado Entonces vamos a
39:32
poner esto así y quitamos el de javascript y ponemos el css imaginad
39:38
barra lateral contenido principal Bueno pues tenéis el dip le ponemos un display grid y le vamos a decir que vamos a
39:45
tener dos columnas grid template columns le decimos que el primero mi Max 100 píxeles y sin una fracción y el otro
39:51
pues que sean cinco fracciones ya tendríamos aquí una barra lateral no el aside con la barra lateral voy a tener
39:57
Border solo para que lo veamos un poquito vale Y luego podríamos poner que el Main pues tenga el borde de color
40:03
azul vale algo así pero fijaos en una cosa y esto lo podríamos hacer que sea
40:08
pues más grande vamos a poner Body margin cer y esto en en un momento lo lo
40:15
vamos a tener vale vamos a decer que ocupe todo el espacio para que lo tengamos aquí vale Ahí tendríamos la
40:21
barra lateral Vale y la barra lateral lo que va a ocurrir aquí es que como mínimo va a ser de una acción lo que pasa es
40:26
que claro Ahora aquí no tengo mucho espacio pero lo Vais a ver ahora vale vale fijaos que la barra lateral tiene
40:32
este espacio ahora se está viendo bastante bien Entonces lo vamos a ir haciendo cada vez más pequeño fijaos que
40:38
cada vez se va haciendo más pequeño hasta que llega un momento que ya no se hace más pequeño Por qué Porque lo que estamos evitando es decir Bueno yo la
40:44
barra lateral puedo ajustarla durante un tiempo pero no quiero romper nada esto seguro que te suena por ejemplo Spotify
40:51
eh Spotify Ay Spotify aquí no Ay sí lo puedo mirar fijaos en la barra lateral
40:57
Spotify es un claro ejemplo que está hecho con grid en la barra lateral seguramente vamos a ver que se va a
41:04
ajustar un no se ajustar Mira pasa al revés pasa al revés se ajusta se ajusta lo otro y eso tiene un tamaño fijo pero
41:11
es raro porque normalmente lo que se hace Es que se ajuste esta parte de aquí vale mientras se hace pequeño pero llega
41:17
un momento que no lo puedes hacer más pequeño porque no quieres que se rompa porque sabes que tienes un icono con el texto entonces dices vale quiero que la
41:24
barra lateral como mínimo 100 píxeles porque sé que es lo mínimo indispensable para que se vean
41:31
mis botones que tengo dentro Así esta barra lateral que tenemos aquí si tengo aquí todos mis botones imagínate pues
41:38
Play vamos a poner aquí eh buscar lo que sea Vale pues sé que este espacio es el
41:45
necesario para que no se me rompa pero si hay más espacio voy a darle más espacio y si hay un momento en que no
41:51
tengo suficiente espacio lo que voy a hacer es que sea el contenido principal El que pierda el espacio y la barra se queda ahí Y fíjate que esto lo vas a
41:58
lograr gracias al minmax esto es una cosa muy común muy típica muy muy muy
42:05
típica que va a ocurrir en todas y cada una de las páginas web de internet a la hora de maquetar vale utilizar un minid
42:12
Max para que una columna tenga el ancho mínimo que nunca va a tener que bajar de los 100 píxeles por lo tanto si el
42:19
espacio disponible llega un momento que iba a ser de menos de 100 píxeles se queda fijo ahí min Max es total ente
42:26
específico de grid vale No podéis utilizar en cualquier sitio o así como cualquier cosa eh y el y el ancho máximo
42:33
sería en este caso una fracción ahí tendrías el problema de una fracción o sea el máximo sería este una fracción lo
42:39
que pasa es podrías ponerle máximo 200 píxeles por ejemplo y ya está podrías
42:45
ponerle como máximo 200 píxeles y y lo podrías y ya está pero claro ves cuando no puede hacer más de 200 fíjate que se
42:53
hace pequeño pero Normalmente se utiliza el una fracción para que tome antes el el espacio vale esto os evita un montón
43:00
de media queries también por qué porque normalmente esto se hace con media queries eh aquí alguien diría no quiero
43:06
que ocupe 200 píxeles pero cuando el ancho que tenemos disponible sea mayor a
43:12
no sé qué entonces lo que hacemos Es sabes y Sería mucho más complejo Así que
43:18
esto es una forma bastante chula de evitar este tipo de cosas vamos a ver otra cosa Este sería un ejemplo para que
43:24
veáis una un layout vamos a a ver un otro ejemplo bastante típico Mira
Que no hacer
43:29
esto esto por ejemplo mira esto por ejemplo esto por ejemplo de la Kings leag la Kings League veis que tiene aquí
43:36
una cuadrícula que sería de con tres resultados que conforme se va haciendo más pequeño veis que llega un momento
43:42
que pasa dos y luego a una una dos y tres no O sea dependiendo del del punto
43:49
se van haciendo más o menos vale vamos a ver voy a ver si podemos robar este contenido un momento espero que no me
43:55
vuelvan a denunciar Mira esto es un ejemplo buenísimo esto es un ejemplo buenísimo de cómo no hacerlo Vale y os
44:00
voy a enseñar cómo hacerlo fijaos Que aquí tiene un montón de cálculos super chungos vale de wid cal no sé qué no sé
44:07
cuánto margin left - 30 bueno esto en realidad a ver si ves y tiene la primera
44:13
columna o sea primera columna segunda columna tercera columna cuarta columna o sea como que tiene aquí un sistema super
44:19
chungo en el que tiene un montón de dips que tiene dentro el item otra otra cosa
44:24
aquí eh a ver aquí aquí sí que los tiene todos y entiendo y está utilizando Flex
44:30
aquí es un caso concreto típico y seguro justamente de utilizar display grid
44:36
porque va a ser mucho más interesante para este caso sin necesidad de utilizar media queries veis que está utilizando
44:42
aquí media queries para hacer esto vamos a hacer un caso similar vale mira Avengers posters vamos a hacer Avengers
Ejercicio
44:50
posters vamos a hacerlo en un momento vamos a hacer este de aquí no un un
44:56
póster de Avengers este este póster de Avengers vale vamos a copiar la dirección de la imagen vamos a poner una
45:01
imagen source imaginar que esta imagen la tenemos unas cuantas veces okay Porque es que si no no no terminamos ahí
45:08
todo el día la tenemos unas cuantas veces y vamos a poner que las imágenes tengan un máximo de ancho de 300 y la
45:16
altura que sea automática vamos a hacerla más pequeñas básicamente para que se vean vale vamos a poner ahí un
45:22
montón imaginaos que son diferentes imágenes que si no no me no me da la pero imaginad que son diferentes
45:27
imágenes vamos a hacer que esto esté dentro de un dip Okay lo vamos a a envolver con un dip y vamos a poner que
45:34
el dip tenga un display grid vamos a hacer nuestra cuadrícula display grid
45:39
Okay ahora nosotros lo que queremos ahora mismo es que tenga el grid
45:44
templates podríamos decir si queremos que sea similar a lo que hemos visto en la Kings leag deberíamos decir que tiene
45:51
que tener tres columnas no tres columnas de una fracción una fracción y una fracción o sea ten tenos tres fracciones
45:56
Vale entonces aquí tendríamos las tres fracciones cada una Bueno aquí claro le he puesto esto eh En lugar de hacer esto
46:04
no sé Eh así vale para que ocupe todo el espacio de la cuadrícula porque si no
46:09
queda ahora una cosa que tendríamos en la Kings leag fijaos que hay una separación en cada uno de ellos no
46:16
entonces una cosa que podemos hacer para separar las columnas es indicarle que
46:22
las columnas tienen que tener un Gap un hueco no se utiliza el margin ni ni
46:28
paddings ni cosas raras vale lo que se utiliza es el Gap el Gap lo que vamos a hacer hacer es asegurarnos que vamos a
46:35
tener una separación entre las columnas en este caso le podemos decir Oye 16 píxeles entre cada columna ves que ahora
46:41
ha aparecido aquí una separación entre cada columna quiero que haya una separación de 16 píxeles ojo con esto
46:48
porque la última forma correcta de hacerlo en realidad es poniendo al principio grid gu colum Gap no pasa
46:57
absolutamente nada si utilizáis colum Gap porque como veis está totalmente soportado no hay ningún problema pero
47:03
pero esta es la forma antigua yo lo hago así porque estoy acostumbrado pero en realidad automáticamente va a utilizar
47:08
esta vale o sea que deberéis utilizar grid gu colum Gap Pero bueno si utilizáis esta o si la veis que sepáis que también funciona pero es por
47:15
retrocompatibilidad con los navegadores antiguos no la van a quitar Eh tampoco os preocupéis luego tendríamos esto no
47:20
colum Gap vale Y ahora también fijaos que entre filas entre la fila un la fila
47:26
uno y la fila dos que tenemos aquí también están pegados tendríamos que poner Row Gap y aquí también pues
47:32
podríamos poner 32 píxeles y fijaos que la separación que hay entre filas es el doble que la separación que hay entre
47:38
columnas porque le he puesto que la fila tenga 32 px o sea el doble de la separación de las columnas esto lo
47:45
podéis hacer en una sola línea también vale podéis poner Gap y podéis ponerle creo que la primera si no me equivoco la
47:51
primera son los las filas 32 píxeles y la segunda las columnas lo podéis hacer con una sola propiedad y si vais a
47:59
utilizar la misma separación entre filas y columnas podéis simplemente poner 16 y
48:04
ahora fijaos que ha quedado lo mismo tanto en columnas como en filas vale Así que ya sabemos separar ya estamos nos
48:11
estamos adjuntando bastante a esto de aquí también cada imagen veo que tiene un borde radius Pero bueno Esto tampoco
48:17
es tan importante pero lo vamos a hacer solo por porque quede más o menos igual Vale hasta aquí bien vale Hasta aquí
48:23
perfecto tenemos tres tres columnas parece que todo va bien pero qué pasa que es verdad que tenemos tres columnas
48:30
y es verdad que sí que se está Ajustando a su espacio no O sea no hay ningún problema se está Ajustando a su espacio
48:35
Pero qué pasa que llega un momento que me gustaría cuando llega aquí que pasase
48:40
a ser dos columnas verdad O sea hay un momento que ya se ve tan pequeñito que
48:46
realmente lo correcto Debería ser que se viese como en dos columnas porque si no no tendría mucho sentido qué podríamos
48:53
hacer pues podríamos decirle a ver vamos a hacer una cosa cuando por defecto vamos a hacer fíjate vamos a hacer algo
48:58
responsive lo voy a hacer en un momento por defecto quiero que sea una sola columna pero si el ancho que tenemos
49:05
disponible es mayor a 300 píxeles vamos a decirle que el el di Perdón vale el
49:12
template sea de dos vale queremos que sea de dos Entonces qué va a pasar que cuando sea de menos de 300 va a utilizar
49:19
una columna cuando es de mayor de dos vale Ya lo estamos haciendo ya lo estamos haciendo responsive vale vamos a
49:24
vamos a ir más allá cu el wid es mayor de 600 píxeles pues vamos a hacer que tenga tres columnas vale tres columnas
49:31
perfecto pues una fracción una fracción y una fracción Y ahora fíjate conforme va ganando espacio Vale ahora son tres
49:38
columnas menos de 600 dos columnas vale lo hemos hecho responsive pero se puede
49:45
hacer mejor se puede hacer mucho mejor y esto fijaos es es bastante código
49:50
bastante difícil de entender y que al final lo que está pasando Es que no estamos utilizando correctamente grid
49:56
vale No estamos utilizando correctamente porque esto al final es sería un rollo tener que estar constantemente Aquí
50:02
pensando en cada media query Cuánto tiene que utilizar y aquí amigos es donde está la magia de El mmax vale voy
50:10
a crear un nuevo codil link que con Exactamente lo mismo Okay Exactamente lo mismo pero aquí lo voy a hacer un poco
50:17
diferente vamos a quitar la media queries y en el grip template columns vamos a hacer una cosa vamos a decirle
50:22
Oye quiero que repitas vale quiero que repitas no sé cuántas veces todavía no
50:29
sé cuántas veces tienes que repetir las columnas pero lo que tengo claro es que como mínimo cada columna como mínimo
50:36
tiene que ocupar 200 píxeles y si no utiliza una fracción pero claro Cuántas
50:41
veces se tiene que repetir Cuántas veces Cuántas columnas tendrías que utilizar con el min Max no lo sabemos verdad pues
Auto-fill auto-fit
50:47
por suerte tenemos dos valores de grid que nos va a ayudar justamente con esto uno sería autofill vale autofill o o
50:55
auto podemos a autofill o autofit que ahora os explicaré la diferencia para que la veáis claramente qué es lo que
51:00
hace auto voy a utilizar autofill primero qué es lo que hace autofill lo que hace autofill es ubicar el número de
51:06
columnas que sean que ocupan el ancho mientras su ancho mínimo sea de 200
51:12
píxeles Qué quiere decir que si tenemos 400 píxeles me va a colocar dos columnas
51:17
pero si tenemos 500 píxeles me va a poner dos columnas Solo que me las va a hacer un poco más grande hasta que sea
51:23
capaz de poner una tercera columna que serán el punto de los 600 píxeles porque cabrán tres columnas de 200 píxeles
51:30
porque 200 píxeles es el tamaño mínimo que le hemos dicho que Tena que tener una columna vale Así que con Esto
51:36
justamente ahora lo que tendríamos que ver Es que fíjate que automáticamente en
51:42
cuanto tiene la posibilidad Qué pasa aquí aquí solo puede enseñar una columna porque no puede poner otra columna que
51:49
satisfaga el tamaño mínimo y hasta que no pasemos de 400 píxeles para que puedan caber dos columnas aunque sean
51:56
cada una de 200 píxeles que es el tamaño mínimo que hemos puesto aquí no la va no va a aparecer veis ahora han aparecido
52:02
por qué porque ya es de más de 400 píxeles dice Vale ahora soy capaz de con
52:07
el tamaño mínimo poner dos columnas qué es lo que tendría que que hacer para enseñar una tercera tener 600 píxeles
52:14
como mínimo porque hasta que no llegue a ese punto no va a ser capaz de poner como mínimo una tercera columna cuando
52:19
llegue a 600 píxeles Pondré la tercera pum y así constantemente fijaos constantemente Ahí lo vamos a tener
52:26
constantemente lo vamos a tener Así que esto sería la forma correcta y fijaos
52:31
fijaos por favor que son literalmente cinco líneas de código en cinco líneas
52:37
de código sin utilizar ni una media query sin utilizar absolutamente nada lo que hemos hecho es este sistema que veis
52:44
aquí este sistema que veis aquí bastante más complejo lo hemos hecho con
52:50
simplemente cinco líneas de código sabes o sea hemos hecho cinco líneas de código
52:55
No hemos tenido que utilizar hacks raros de menos 30 píxeles No hemos tenido que utilizar eh Por ejemplo aquí cálculos
53:03
suere extraños No hemos tenido que poner veis No hemos tenido que utilizar media queris No hemos tenido que utilizar
53:09
absolutamente nada la diferencia con Flex grap como o sea es que esto es muchísimo muchísimo más potente que Flex
53:16
graap Flex graap al final lo que va a hacer es separarlo tirarlo abajo y ya está Y esto es mucho más potente y al
53:22
final lo que estamos haciendo es que estamos controlando mucho mejor Cuál es el tamaño mínimo Cómo luego se tiene que
53:27
expandir es mucho mejor no pero Qué función tiene min Max bueno Ángel rojo seguramente es porque ha llegado tarde
53:32
pero es que lo hemos explicado antes hemos explicado el método de la función que tiene min Max hemos explicado que lo
53:38
que estamos diciéndole es cuál es el tamaño mínimo que tiene que tener la columna vale Y si ya llega al tamaño
53:45
mínimo Cómo se tiene que comportar por default digamos no Así que como máximo va a tener una un fragmento también
53:51
podríamos llegar a decir Oye si queremos limitar el el ancho máximo podemos decirle que como máximo sea de 400
53:57
píxeles Lo que pasa que en este caso ya va a ser un poco más rollo porque justamente lo que queremos es que se
54:03
puede ajustar constantemente y luego si queréis limitar el número de columnas lo que tendríais que hacer más bien Es
54:09
decir Bueno pues lo que podemos hacer es que esto el contenedor tenga un ancho
54:14
máximo por ejemplo podríamos decir 500 píxeles y esto lo podréis lo podemos Eh
54:21
centrar vale Y ahora lo que va a ocurrir es que ya no va a seguir cre podéis hacer el cálculo de cuánto sería lo que
54:27
queréis por ejemplo tres columnas y ya lo tendríais ahí y ya estaría Punto Pelota vamos a ver otra cosa que es
Diferencia entre auto-fill y auto-fit
54:33
bastante interesante sobre el autofill vamos a hacer esto un poco más pequeño vale que ahora las columnas sean de 100
54:38
vale fijaos que ahora como son de 100 Pues ahora salen más es normal y salen más fácilmente eh la diferencia entre
54:45
autofill y autofit hay una diferencia muy sutil muy pequeña vale que es un
54:51
poco que no es tan importante pero sí que que es interesante que sepas claro
54:56
aquí porque tenemos un montón de imágenes y al final cabe por todos los lados pero imaginad que solo tenemos
55:02
eh cuatro imágenes vale cuatro imágenes Esto es lo que muchas veces nosotros
55:07
esperamos el hecho de si tenemos una cuadrícula y solo tenemos tres elementos lo que esperaríamos es que ocupe cada
55:14
espacio y aquí debería ir otra pero como no lo hay pues queda así Esto es lo que normalmente se hacen los resultados de
55:20
búsqueda no tiene sentido que que ocupen todo el espacio sino tú lo que es siempre tener el mismo ancho para que no
55:27
se rompa el lallo no entonces lo que podríamos hacer aquí es decir bueno no me da igual quiero que hagas un autofit
55:34
y lo que va a pasar con el autofit es que va a ocupar todo el espacio va a decir Bueno aunque no haya e no hay si
55:41
no hay más elementos voy a ocupar todo el espacio y voy a hacer que sean más grandes Pero esto no es normalmente lo
55:48
que quieres hacer los resultados de búsqueda porque Quedaría muy raro que de repente no te diga ah si solo sale un
55:53
elemento sale enorme Si salen seis elementos salen chiquititos no Entonces diríamos que uno sería lo que está
56:00
rellenando el espacio y el otro lo está Ajustando fíjate la diferencia autofit es que está Ajustando está estirando el
56:07
contenido y lo está Ajustando hasta los límites Y autofil es que lo está rellenando está dejando Trozos de la
56:14
cuadrícula vacíos y solo está rellenando los huecos eso sería la diferencia pero el tema es que cuando tenéis muchos
56:21
resultados No vais a ver la diferencia vale no Vais a ver la diferencia va a ser exactamente lo mismo y Vais a pensar
56:28
pues no tiene diferencia pero cuando tenéis pocos elementos sí que Vais a notar Cuál es la diferencia no con
56:33
tailwind esto ocupa menos líneas de código o más con tailwind el problema es que hacer esto esto lo tenéis que hacer
56:39
con lo tenéis que hacer manualmente eh ocupa más o menos lo mismo o sea al final va a ocupar Esto va a ocupar
56:46
Exactamente lo mismo o sea tú igual lo haces en menos líneas tendrías pero tendrías que hacer cosas así como grid
56:52
eh calls eh repeat No sé qué lo tenías que hacer manualmente esto es clave amigos esto es clave aquí es donde se ve
56:58
justamente la potencia que tiene que tiene grid porque fijaos lo fácil que
57:04
hemos hecho un sistema de resultados en una cuadrícula que Vais a ver que un
57:09
montón de veces se hacen cosas muy raras como en este caso de la Kings leag con margin left con un montón de media
57:16
queries de decir Bueno cuando es uno o tres Incluso si utilizáis bootstrap seguro que os ha pasado que tenéis que
57:22
hacer un montón de cosas raras para tener que para tener que hacer justamente que sean responsive a la hora
57:29
en diferentes tamaños y aquí es superfácil el hecho de que se ajuste a la cuadrícula y automáticamente en cinco
57:36
líneas de código haces unos resultados de búsqueda buenísimos vale buenísimos sin ningún tipo de problema Entonces ya
margin o gap?
57:41
hemos visto la separación los Gap vamos a ver el tema de las líneas de la cuadrícula que esto está bastante
57:48
interesante también y que muy pocas veces la gente se para a ver Esto vale Mirad cuando nosotros otros voy a hacer
57:55
que sean más grandes las eh vamos a hacer auto rows vamos a poner que cada fila sea de 50 píxeles vale Vamos a
58:01
ponerle un Gap de 16 píxeles para que veáis antes me preguntaba alguien por qué utilizas Gap y no utilizas margin a
58:08
ver si utilizas margin aparte que el margen no lo puedes poner aquí el margen lo tienes que aplicar dentro de los
58:14
elementos pero claro el margen es bastante complicado de aplicar porque tú no puedes aplicar no se aplica
58:20
Exactamente igual la separación del margen a cada uno de los elementos O sea si tú dices que quieres que sea cuatro
58:26
píxeles Fíjate que el margen se está aplicando también aquí fuera que a veces a lo mejor es lo que quieres eh no
58:32
pasaría nada si es justamente lo que quieres no pasa nada eh pero muchas veces lo que quieres no es que haya una
58:37
separación aquí y por lo tanto ya Imagínate que te decir no Pero entonces y esto de hecho es lo que hace que es lo
58:45
que hemos visto aquí que es un hack vale lo que pasa justamente aquí Fíjate en equipos aquí qué es lo que pasa que hace
58:52
la separación con margin como hace la la separación con margin Fíjate lo que hace ves que hace margin left - 30 píxeles
59:00
por qué Porque lo que quiere es que este margen de la izquierda no esté y lo que dice es bueno pues lo que voy a hacer es
59:06
margin left eh menos le quito el margen que estoy aplicando Y así va a quedar
59:13
alineado como espero Pero eso no es la forma correcta cuando lo que quieres tener es la separación entre elementos
59:18
lo correcto en todo caso además es decirle Bueno quiero hacer el Gap de cuatro píxeles Y en todo caso dentro si
59:24
lo que quieres es empujar el contenido lo que puedes hacer es el padding Y entonces es mucho más fácil además de
59:30
pensar si lo estás aplicando directamente desde el contenedor en lugar de tener que aplicarlo en los elementos porque muchas veces además en
59:37
los elementos tienes el problema este de que si no quieres que haya ningún tipo de separación no lo vas a poder lograr a
59:43
no ser que utilices algún hack no es imposible utilizar margin no es no es algo siempre negativo ni está mal o sea
59:50
a veces puedes utilizar Marin y puede tener sentido Pero normalmente si hablamos de separación entre elementos
59:56
lo mejor es que lo hagas directamente en el contenedor oa sería un poco lo lo que es mucho más sencillo y te va a
1:00:02
simplificar a la hora de pensar cómo cómo los quieres separar vale dicho esto fijaos que habíamos dicho por aquí que
Líneas de la cuadricula
1:00:09
teníamos el grid no y que al darle aquí a grid vale hay un botoncito aquí fijaos que aquí aparecen unos botones uno uno
1:00:16
veis uno ahí sale un dos a ver aquí dos aquí un tres aquí un cuatro vale Y aquí
1:00:23
también hay uno 2 3 4 y luego -4 -3 men2 men1 vale esto es una de las cosas más
1:00:31
divertidas y con la que vas a hacer esto de los Vento grids vale esto de los Vento grds se hace con lo que te voy a
1:00:37
explicar ahora este este tipo de evento se hace con lo que te voy a explicar ahora fíjate tenemos estas líneas no
1:00:45
estos números aquí qué es lo que hace esto esto lo que está haciendo es las líneas de la cuadrícula es como que
1:00:52
estamos está nos da estas líneas numeradas para posicionar elementos por ejemplo el
1:00:59
elemento este de arriba a la izquierda está posicionado entre la columna un y
1:01:04
la columna dos no está ahí posicionado Así que tenemos aquí 1 2s 3 cu no ahí lo
1:01:12
que podríamos decir es que el primer elemento mira lo voy a lo voy a poner de otro color para que lo veas más bien
1:01:17
vale Voy a ponerle background Green y así lo vamos a ver mientras hablo vale
1:01:22
Ahí lo tenemos vale vamos a ponerle un light light Green y borde un pixxel
1:01:30
vamos a ponerlo Bueno no sé de dos pixels do pixels y ponemos que este sea
1:01:36
vale vale fijaos en este elemento este elemento si lo veis aquí si le damos a los numeritos está posicionado entre
1:01:42
esta esquinita entre este uno y este dos entonces lo que podríamos decir es que este elemento First Child lo podríamos
grid-column-start/end
1:01:50
mover y decirle dónde dónde está ahora mismo eh posicionado vale Vale pues está el grid column Start Dónde está
1:01:58
empezando pues está empezando desde el uno y dónde está terminando pues está terminando en el dos No fíjate que no ha
1:02:05
cambiado nada visualmente está terminando en el numerito uno del uno al
1:02:10
dos no ha cambiado absolutamente nada Pero lo bueno es que una vez que tenemos estas propiedades Nosotros le podemos
1:02:17
indicar Dónde tiene que terminar y dónde tiene que empezar Imagínate que este primer elemento quieres que vaya del uno
1:02:24
hasta el tres pues le diríamos Oye quiero que la columna empiece del uno pero que termine en el tres y Fíjate lo
1:02:31
que pasa lo que pasa es que de repente ese elemento dice vale empiezo desde la
1:02:36
línea eh vertical uno hasta la línea tres o sea estoy empezando desde aquí
1:02:42
hasta aquí y ojo lo más interesante es que lo puedes le puedes decir que empiece donde te dé la gana por ejemplo
1:02:48
Imagínate que quieres que el primer espacio quede quede vacío pues le vamos a decir que empiece desde la línea
1:02:54
vertical dos vale Fíjate lo tenemos aquí desde el dos al tres Pues le decimos
1:02:59
Esto del dos al tres Y fíjate dónde se coloca y lo mismo podríamos decirlo otra vez que vaya hasta el cuatro y entonces
1:03:05
empuja el resto con Esto justamente es que vamos a poder construir los ventos
1:03:10
porque los ventos lo mismo que le decimos de las columnas también se lo vamos a decir de los rows Mira Cuántos
1:03:16
elementos hay aquí 1 2 3 4 5 6 7 8 hay ocho elementos no vamos a hacer una cosa
1:03:24
eh lo he contado bien no 4 5 6 7 sí ocho vale vamos a hacer una cosa fijaos lo
1:03:31
fácil lo fácil que es aplicar esto lo fácil que es aplicar Esto imaginad vale
1:03:37
que tenemos esto y os digo venga Hay que hacer este evento este evento aquí pues
1:03:43
lo único que tenemos que hacer es fijarnos en las líneas aquí podemos ver que es si nos fijamos aquí sería la uno
1:03:49
el 1 2 3 cu no que lo tenemos aquí 1 dos bueno Tenemos aquí aquí los dibujos 1 2
1:03:55
3 4 Vale entonces Tendría que ir del uno al dos vale solo del uno pero tendría
grid-row-start/end
1:04:02
que hacer grid Row Start del uno grid Row Start y tendría que llegar hasta el
1:04:07
tres Ahí está al end Perdón n hasta el tres y ya está o sea con esto ya tendríamos esto de aquí obviamente me
1:04:14
faltaría todo el diseño Y tal Pero fíjate que lo que está pasando aquí es que está ocupando dos filas Así que aquí
1:04:20
lo que podemos decir es que vaya del uno al tres y así ocuparía dos filas esto muchas veces es un poco raro Por qué
1:04:26
Porque tienes que estar pensando constantemente dónde empieza dónde termina Dónde tenemos que estar
1:04:32
diciéndole eh Pero al final Aquí queda muy claro que si lo ves dices Bueno pero si me estás diciendo que ocupa dos filas
1:04:39
por qué no puedes directamente decirle que ocupe dos filas y te olvidas de tener que hacer que vaya de la línea de
1:04:45
la uno a la tres que es un poco rollo no de la línea uno a la tres es un poco rollo Bueno pues se puede hacer También
1:04:51
le puedes decir Oye quiero que empieces y que ocupes dos filas fíjate que ahora
1:04:57
ocupa dos filas y lo mismo le podríamos decir con las columnas quiero que ocupes dos columnas Y entonces Fíjate lo que
1:05:02
hacemos Ahora aquí lo que tenemos ahora es que ocupa dos filas y dos columnas y lo tenemos ahí así que lo que estamos
1:05:08
haciendo ahora es decirle lo que ocupa directamente no estamos diciendo De dónde empieza a dónde termina le decimos
1:05:14
lo que ocupa y podríamos hacer esto exactamente con otros o sea podríamos ir al dip NC NC Child 2 Creo que no sé si
1:05:24
Esto sí creo que esto lo hará bien vamos a poner aquí light Blue borde dos pixels
1:05:29
solid Blue y grow column Start span 3
1:05:35
vale Fíjate que aquí Bueno claro light red light red no existe light coral
1:05:41
ahora es que el coral es muy parecido al salmón eh canan
1:05:47
Pink sig Green vale Y aquí le vamos a poner esto y lo mismo podríamos decirle
1:05:52
con los con el Row y le podríamos decir Row Start y span 2 vale Y aquí le
1:05:59
podríamos decir a cada elemento Cuánto es lo que tiene que ocupar vale fijaos lo fácil que es Eh Esto también se puede
1:06:06
hacer de otras formas mucho más sencillas vale porque eh tienes que poner grid column Start no sé qué no sé
1:06:12
cuánto y puede ser un poco rollo pero también puedes utilizar la forma más corta por ejemplo grid column y le
Atajo más simple de grid-column/row
1:06:17
puedes decir aquí que vaya del dos al cuatro vale Y fíjate aquí va desde la línea dos a la cuatro y lo mismo con el
1:06:24
r Le puedes decir que vaya de la dos A la tres vale Y entonces ya lo estamos moviendo y una cosa que es muy
1:06:30
interesante con esto es que también puedes moverlos donde te dé la gana por ejemplo aquí puedes poner que este vaya
1:06:36
del uno al tres Y fíjate que aquí lo que vamos a hacer es independientemente de su posición en el html no que era 1 2 3
1:06:43
4 5 6 7 8 9 lo que estamos haciendo es bueno como este de aquí lo he puesto
1:06:49
aquí lo que voy a hacer con este es ponerlo aquí y esto muchas veces es
1:06:55
interesante con temas de responsive porque a lo mejor en una media query vas a querer que un elemento que a lo mejor
1:07:01
lo quieres centrado en algún sitio por lo que sea cuando cambia A lo mejor lo quieres poner arriba a la izquierda pues
1:07:07
esto lo puedes hacer cambiando esto y el tema de los números por eso es importante que lo tengas aquí en visibilidad que tienes los números de
1:07:14
las líneas tanto verticales que sería la de las columnas que sería la columna O sea la línea 1 dos 3 y cuat y la de las
1:07:21
filas una dos tres y cuatro y cinco porque tenemos al final cuatro filas cinco líneas vertical horizontales y ojo
1:07:30
también una cosa que es bastante interesante que también podéis utilizar números negativos Qué quiere decir esto
1:07:35
que podéis contar desde el final Por ejemplo si queréis que la columna o sea
1:07:40
este dos vaya desde bueno el dos será este no queréis que vaya desde la
1:07:46
primera hasta la penúltima No pues podéis hacer esto no el menos un vale Ah claro es que he hecho columna vale hecho
1:07:52
columna Vale pues sería así os2 Y entonces sería la penúltima la última sería esta y esta sería la penúltima
1:07:58
pues entonces lo estaríamos haciendo así lo estaríamos logrando de una forma diferente Pero lo podríais hacer o si
1:08:03
queréis que ocupen todas las filas pues podéis decirle Bueno quiero que vaya de la un a la os1 y grid Row Ay Por qué no
1:08:12
me ha hecho esto espérate Por qué no me ha hecho esto Pues pensaba que este me iba por qué no me ha hecho o de la menos
1:08:17
un a la un a la un no de la 1 a la men1 pensaba que me iba a hacer a ver si
1:08:23
ponemos aquí uno aquí sí que la pilla Pues pensaba que este me iba a pillar me iba a bajar de todos Pues me ha dejado fatal por qué puede ser que esto no
1:08:31
porque está esta Sabes porque está esta y al final no puede Sabes porque lo empujaría claro Podría tener sentido a
1:08:38
ver no podría tener sentido pensaba que lo iba a pillar con las columnas sí que lo está haciendo ves que va desde la uno
1:08:44
a la menos un que se da el final pero con la Grill r no lo ha hecho pensaba que a lo mejor pillaría todo el espacio
1:08:49
pero entiendo que no podrá a lo mejor por esta del del First Child Pero bueno que que podéis referir de la desde
1:08:55
adelante hacia atrás lo tenéis aquí veis que pone aquí -3 -2 -1 pues ahí lo
1:09:01
tenéis a ver -4 Ah es que es -4 Es que lo he pensado mal claro -1 es en la
1:09:07
abajo a la derecha ha sido error mío eh Porque veis el -1 está aquí claro es el
1:09:12
-4 Debería ser este y así es como ocuparía todo el espacio vale Vale pues ya está ahí es que tendría todas las
1:09:18
filas que serían las cuatro filas disponibles las tendríais aquí tendría una dos tres o sea llegaría hasta el
1:09:23
final vale en este Bueno -4 sí estaría haciendo eso correctamente Vale pues así
1:09:29
es como lo podríais hacer lo podríais hacer también con números negativos pero a ver no es obligatorio solo o sea os lo
1:09:36
explico solo para que sepáis porque claro salen Aquí los números y a lo mejor os volvéis locos Pero lo único que tenéis que entender es que eh la línea
1:09:44
la línea horizontal cuatro se refiere también a la os4 vale o sea que podéis contar al revés que la -3 claro fía
1:09:51
sería como la anterior no pero tened en cuenta lo lo podéis utilizar pero tampoco lo hagáis así de esa forma lo
1:09:56
importante la más importante es cuando queréis ir de punta a punta y no queréis saber cuántos tenéis pues así lo que
1:10:02
podéis hacer es decir del uno al os1 y esto lo que Vais a conseguir es utilizar todo el ancho porque vais del punto uno
1:10:09
vertical no de este punto que tenemos aquí arriba a la izquierda hasta este punto que tenemos arriba a la derecha y
1:10:15
así pues Sería mucho más fácil que lo que lo podáis hacer pero bueno lo las formas abreviadas yo esta forma
1:10:21
abreviada No está mal si la entendéis pero tampoco os diría que os volváis locos un tema importante sobre esto
1:10:28
imaginad vamos a poner que esto vaya del uno a la tres y de la uno a la tres vale aquí ponemos a al primer elemento que
1:10:35
vaya de la de la línea uno a la tres verticalmente y horizontalmente pues
1:10:41
este mismo lo podéis poner en el mismo lugar y veis que se sobreponen esto es una cosa que no se puede lograr en css
1:10:47
De cualquier manera y muchas veces se puede utilizar position absolute para ponerse justo por encima pero Hay pocas
Bloques encima de otros
1:10:54
formas de forma nativa y controlada que lo podáis lograr sin utilizar el left top right eh cambiando márgenes raros y
1:11:02
hacks aquí sí que podéis sobreponer dos elementos de forma totalmente controlada sin tener que mover nada porque le
1:11:09
estáis diciendo que los dos tienen que ponerse en el mismo lugar y lo podéis ver claramente que uno está detrás
1:11:15
debajo del otro veis porque si le pongo opacidad veis que están los dos ahí esto es muy interesante porque a veces en css
1:11:21
la gente se cree que para sobreponer dos elementos hay que hacer cosas más raras y no tiene por qué ser así siempre aquí lo lo estamos haciendo y lo estamos
1:11:28
haciendo totalmente controlado lo interesante además es que dependiendo del Z índex que le pongáis obviamente se
1:11:34
verá uno u otro delante o detrás vale si le ponemos por defecto Debería ser el segundo elemento que es el que tiene más
1:11:41
eh Como más potencia para que se quede encima por eso es este El que se está viendo encima Pero le podríais ciar el Z
1:11:48
índex Y entonces la pregunta del millón Pero por qué querríais hacer esto no Para qué serviría una cosa de esta est
1:11:53
esto sirve para algo La verdad es que sí por ejemplo imaginad que al hacer hover
1:11:58
pues queráis poner que al hacer hover a vuestras columnas pues aparezca algo que se queda ahí detrás por ejemplo en los
1:12:04
ventos lo podéis hacer fácilmente imaginad que estáis aquí y dices Bueno cada vez que haga hover en uno de los
1:12:12
elementos lo que voy a querer es Que aparezca el otro elemento que había detrás y que haga una animación y que no
1:12:18
sé qué Y pues eso lo podríais hacer por ejemplo con esto que estamos viendo así que todo tiene su utilidad cómo se
1:12:24
comporta Ese diseño en responsive perfecto porque al final si es que lo podéis cambiar todo lo que queráis o sea
1:12:29
vosotros podéis poner aquí una media query o sea todos estos diseños no se comportan de forma muy complicada porque
1:12:36
lo bueno que tenéis con esto es decir mira imaginad que es responsive pues lo que podéis hacer es decir Bueno cuando
1:12:42
se haga más pequeño lo que vas a hacer Es que esto se quede arriba esto pasa a estar abajo y esto pasa a estar abajo y
1:12:50
esto lo lo podéis conseguir justamente con los grid template columns o sea cuando justamente podéis ir cambiando
1:12:56
con las medias decís Oye cuando el wid sea mayor a 500 pixels Vale pues vamos a
1:13:03
decirle primero son dos fracciones porque es muy sencillo pero cuando es más grande pues voy a hacer que tenga un
1:13:10
min Max de 200 píxeles una fracción una fracción y una fracción no y así lo que
1:13:16
podéis hacer Ay eh No he hecho bien la la media query porque ay porque he hecho
1:13:23
mal el el css pero fijaos que con esto lo que podéis lograr es básicamente Oh
1:13:29
qué rabia este este B hay un B ahí vale pero veis que podéis cambiar totalmente
1:13:34
la plantilla aquí tendríais imaginad en un Vento Pues algo que sea muy muy muy espectacular pero cuando en móvil hacéis
1:13:41
Solo dos columnas y hacéis que esto se quede arriba y ya está entonces no es excesivamente complicado lograrlo y de
1:13:48
hecho he visto muchos ventos que se ajustan perfectamente y que no hay ningún tipo de problema eh Y que quedan superb eh eres un gran profe Gracias
1:13:55
hombre una calculadora por ejemplo también eh Así sí que es necesario una media query Claro en este caso sí puedes
1:14:01
A ver es que las media query No son no están prohibidas ni mucho menos no el tema es que si las podemos evitar mejor
1:14:07
pero claro si tienes un diseño así tan especial obviamente esto vas a querer controlar Cuándo se ve qué espacio ocupa
1:14:15
cada cosa y es normal que quedas hacer una media query para controlar correctamente Cómo se ve esto automáticamente No te lo va a hacer
1:14:22
sabes No te lo va hacer grid no va a saber cuál es el lo más especial Imagínate es lo que os decía en este
1:14:29
caso lo cuando es muy grande lo especial lo tiene aquí y y esto seguro que con
1:14:35
todo lo que estáis viendo estáis viendo ostras aquí tiene un col span donde este span pues ocupa dos y claro cuando lo
1:14:42
haces media query Pues a lo mejor este elemento
1:14:52
lo esta parte del reloj que justamente esta parte de aquí arriba cuando lo lo
1:14:57
tenemos así más Peque más más grande pues lo podemos poner ahí arriba o lo podemos poner en el centro y cuando
1:15:03
hacemos más pequeño lo movemos arriba o donde queramos o sea que lo importante es que el diseño no se nos rompa
1:15:08
directamente no por qué mejor evitarlas porque añade complejidad las media queries al final no dejan de ser como
1:15:14
condicionales los condicionales en el mundo de la programación en general se tienen que evitar lo al máximo posible
1:15:19
no significa que no utilices condicionales significa que que una bifurcación de tu código al final añade complejidad cuantas más medias queries
1:15:26
tienes más problemas vas a encontrarte entonces son malas las media queries no son malas pero si puedes evitarte una
1:15:34
media query evítate Ela siempre bienvenido evitarte una media query vale o sea que no habría ningún tipo de
1:15:39
problema Bueno os voy a enseñar vamos con otra cosa que está muy muy muy chula que que es increíble y que os va a
Creando un Layout
1:15:46
cambiar la vida para cuando hagamos layouts vale Y es que esto para hacer layouts es la clave y vamos a eliminar
1:15:52
todo esto vamos a poner aquí tres y ponemos esto por aquí vale Mirad vamos a
1:15:58
hacer un un layout que además es un layout muy típico Mirad Este es el html
1:16:04
section Class container tenemos un header el aside el Main y el footer Okay
1:16:09
vamos a estilar primero el container y obviamente con un display grid y vamos a
1:16:15
estilar container el header le voy a poner un colorcito background 09f
1:16:21
básicamente para que veáis los colores vamos a quitarle el margen por defecto que tiene el body para que quede todo
1:16:26
ajustado vamos a poner que el container el aside yo que sé vamos a ponerlo de
1:16:31
color amarillo vale solo para que cada uno tenga un color el Main Vamos a ponerle un
1:16:38
color no sé a ver qué color le podemos poner rojo que es lo más importante y el footer le vamos a poner un color menos
1:16:44
importante light eh c vale que no se vea tanto bueno Vamos a ponerle Grey que así
1:16:51
se verá bien vale o sea tenemos cuatro secciones totalmente diferentes y tal
1:16:56
bueno imaginad que queremos hacer el layout típico típico de toda la vida no
1:17:03
grid template columns voy a hacer esto lo voy a quitar así y así puedo con el
1:17:09
Back este que me está atormentando pero a ver si lo puedo ajustar vale eh grid
1:17:14
template colums vamos a hacer tres columnas tres columnas un FR un FR vale Fíjate que me ha hecho tres columnas y
1:17:20
me está dejando esto mal porque no es exatamente lo que queremos por ahora lo vamos a dejar Más o menos así solo para
1:17:26
que lo tengamos más o menos Claro no vamos a poner eh Rose y template Rose y
1:17:32
vamos a utilizar cosas que hemos ido aprendiendo que se repita esto min Max 50
1:17:38
píxeles una fracción Vale entonces ya va pillando un poco de forma pero qué pasa
1:17:43
que el header yo lo que quiero del header normalmente es que ocupe todo el espacio pues grid column del 1 al men1
1:17:49
esto lo hemos visto no que si queremos que vaya algo en la línea de las columnas De punta a punta le digo me
1:17:56
tienes que desde la fila uno mira lo voy a ver aquí lo vamos a poner aquí para que lo veáis claramente eh en elementos
1:18:02
activamos el grid desde la línea uno hasta la no se ve pero está ahí la menos
1:18:09
un que no Ah ahí vale Hasta la men-1 ves ahí que se ve la -1 pues ahí la tienes
1:18:14
hasta la -1 De punta a punta para que vaya De punta a punta porque si no tendríamos que saber cuántas son las que
1:18:20
queremos que tenga No pues tenemos que poner hasta la línea cuatro si lo queréis hacer así así pero lo mejor que hagáis Así que vaya de punto a punta
1:18:26
porque así no tenéis que saber cuántas columnas son y eso puede cambiar en cualquier momento ahora vamos a hacer el
1:18:31
aside el aside Pues bueno Esto se puede quedar Exactamente igual porque queremos que se quede justo debajo debajo del
1:18:37
heer el footer Mira voy a hacer el footer el footer quiero que le pase un poco lo mismo no que vaya De punta a
1:18:42
punta Y entonces aquí fíjate el footer como tiene que ir de punta a punta pues va a ocupar el 100% y ahora aquí tenemos
1:18:50
el lateral la barra lateral y el contenido solo está ocupando este espacio pero yo quiero que ocupe todo lo
1:18:56
demás Por lo tanto le digo que el grid colum vamos a decirle que span dos para que rellene dos columnas así la site
1:19:04
solo se queda con una y el contenido con otra vamos a hacer que esto tenga más más más espacio así con 100 esto no está
1:19:12
mal o sea quiero decir es algo parecido a lo que normalmente podríamos a hacer obviamente esto soy yo que he puesto
1:19:19
aquí min Max y tal lo ideal es que cada cosa tuviesen Su contenido diferente o sea por ejemplo a lo mejor el header
1:19:25
quieres que sea 50 píxeles o menos eh 35 píxeles la parte del contenido Pues a lo
1:19:31
mejor quieres que sea una fracción Y luego el footer quieres que sean 100 píxeles y ahora el tema es que para que
1:19:36
ocupe todo el espacio obviamente tenemos que asegurarnos que como mínimo esto sea
1:19:42
todo el el tamaño que tenemos aquí disponible No porque si no no
1:19:47
funcionaría Entonces esto sería más o menos un layout que podríamos hacer y que incluso en móvil lo podríamos cambiar ciar Pero esto es un poco rollo
1:19:54
y os voy a explicar Por qué este tipo de de de de templates no se suelen hacer así por qué porque esto es muy típico y
1:20:02
esto al final lo Vais a ver repetido una y otra vez una y otra vez no pero el tema es que va a ser muy complicado que
1:20:09
vayáis al css y entendáis lo que está ocurriendo aquí porque tenéis que ir a cada uno de los elementos para ver cómo
1:20:16
está funcionando esto Qué es lo que está haciendo y todo esto pues vamos a quitar todo esto el grip colum GP colum G vamos
Grid áreas
1:20:23
a quitar todo eso y vamos a hacerlo de otra forma vale lo vamos a hacer de otra forma Vamos a ponerle un nombre a cada
1:20:28
uno de los elementos vamos a decir mira el área de este grid Esto va a ser el header el grid área este Vamos a darle
1:20:36
el nombre que Esto va a ser el cyar vale a este en el área de la cuadrícula le
1:20:42
vamos a decir que es el content y el footer Vamos a ponerle en grid Area y le vamos a decir que es el footer vale ya
1:20:48
hemos nombrado cada uno de los elementos ahora lo que que tendríamos que hacer es
1:20:53
decir Bueno ahora que sabemos cada uno de los elementos A qué se refiere tenemos que Definir la plantilla nuestra
1:21:00
cuadrícula con estos nombres y así en lugar de utilizar el template columns y todo esto que también lo podemos
1:21:06
utilizar lo que le podemos decir es que quiero utilizar template áreas y vamos a definir las áreas y le vamos a decir
1:21:12
mira arriba Quiero el header tres veces vale luego abajo Quiero el cyar el
1:21:19
contenido y el contenido Vale y abajo Quiero el footer el footer y el footer Y
1:21:25
fíjate que hemos logrado lo mismo pero hemos hecho algo visual Imagínate que
1:21:30
por lo que sea dices No no el cyar ya no lo quiero aquí este cyar que lo tengo
1:21:35
aquí ahora quiero que aquí esté el contenido y el cyar lo quiero poner aquí arriba pues ya está el header sigue así
1:21:42
el asai lo tengo ahí y el contenido lo tengo allá ya ya hemos ajustado rápidamente donde tiene que ir cada cosa
1:21:48
Vale vamos a dejar otra vez el s pues no voy a probar a ver qué pasa si el Side Lo pongo aquí derecha pues ya está ya lo
1:21:54
hemos hecho fijaos que de esta forma lo que estamos haciendo es dibujando con css básicamente Cómo es el área y no nos
1:22:02
tenemos que preocupar de si tiene que ir desde una línea desde una columna y no sé qué sino lo que estamos haciendo es
1:22:08
visualmente decir cómo tiene que quedar aquí tenemos tres columnas estamos
1:22:13
definiendo que tiene tres columnas y que en esta posición de la columna va el header aquí va el header aquí va el header aquí va el contenido contenido el
1:22:20
cbar aquí va el footer y estas serían las filas o sea cada línea sera las filas y y si lo miras verticalmente
1:22:27
sería una de las columnas Imagínate que quieres quitar el header pues lo quitas el header ya no aparece Imagínate que
1:22:33
además en la media queries y esto es muy interesante no que puedas tener una media query que digas Vale cuando el wid
1:22:39
eh sea mayor a 400 píxeles vale vamos a hacer una cosa vamos a hacer que tenga
1:22:46
este vamos a hacer esto y esto es una de las cosas que están muy muy muy chulas
1:22:51
porque al final le Puedes cambiar el área dependiendo de cómo quede Entonces vamos a hacer que en el móvil esto el
1:22:58
cyar se vea arriba vale vamos a hacer que en el móvil el cyar se vea arriba
1:23:03
vale vamos a poner el contenido aquí y aquí vamos a poner cyar vale vamos a hacer que en desktop se vea el cyar al
1:23:10
lado pero cuando hagamos pequeño lo que hacemos Es que el cyar vaya arriba a la derecha por ejemplo y así Lo tendríamos
1:23:18
mucho más fácil o sea ahora lo que estamos haciendo es de forma declarativa estamos indicando Qué diseño es el que
1:23:24
tiene que utilizar en cada media query superfácil No aquí decimos Oye Móvil El aside lo tienes que poner arriba a la
1:23:30
derecha y luego si tienes espacio lo pones aquí a la izquierda y ya está O sea fijaos que esto es superpotente
1:23:37
porque no necesitáis ahora ni siquiera pensar en líneas ni nada simplemente le estáis describiendo como dibujando Cómo
1:23:43
queréis que estén las áreas y ahora lo mejor de esto lo que podéis hacer es decir Oye Imagínate que en este sería
1:23:51
este no porque ahora Estamos en modo si no lo hubiera visto no lo hubiera creído totalmente no lo hubieras creído
1:23:57
totalmente eh imaginad que por lo que sea decís mira en desktop no quiero que
1:24:03
aquí aparezca nada no quiero que aquí aparezca nada vale o sea no quiero que en este trozo de la columna haya nada
1:24:09
quiero que haya un hueco pues tenéis que poner un punto y ya está así este header
1:24:14
ocupará dos columnas y en esta tercera columna en esa fila como hemos puesto un
1:24:19
punto habrá un hueco esto lo podéis utilizar Tantas veces como queráis ves ahí ahora Estamos dejando un hueco podemos poner un hueco Aquí también no
1:24:25
habría ningún problema o lo podemos poner aquí podéis poner el hueco donde queráis y esto lo que hace también es
1:24:31
que podáis hacer una composición de una cuadrícula mucho más fácil vale Así que
1:24:36
teníais la posibilidad de decir eh Pues aquí Quiero un hueco y aquí quiero que sí que se vea esto y tal Y así es como
1:24:43
se hacen los layouts cuando muchas veces decís que os cuesta maquetar que no sé qué que no sé cuánto pues lo que tenemos
1:24:50
aquí es una forma muy fácil de hacer la outs es necesario poner el min height de 100 viewport para que ocupe total la
1:24:56
vista sí por qué Porque si yo quito esto cuál es el problema El problema es que el contenido es el que está empujando
1:25:04
normalmente en una página en una página normal esto estaría lleno de contenido tendría texto imágenes y no
1:25:10
necesitaríamos seguramente esto no Pero el tema el tema es que a ver si aquí en
1:25:15
este content empiezas a empujar contenido y tal Claro pues ya a la altura sería Ajustando pero para que lo
1:25:21
veáis lo que he hecho es que el container como mínimo tome la altura del viewport y así es que va a ajustar el
1:25:26
contenido perfectamente vale Si no no lo va no lo va a hacer correctamente porque no va a saber cuál es la altura porque
1:25:32
se basa en el contenido y ya está qué le vamos a hacer Existe algún convenio en las medidas de los media quaris para móvil tabletas no hay convenio y por eso
1:25:39
también es un tema que es normalmente mejor eh evitar siempre que podáis una media query o sea las media query las
1:25:45
necesitáis y hay que utilizarla muchas veces pero el problema es que a día de hoy no hay un convenio de media queries
1:25:51
hay recomendaciones por Internet Pero sabes qué pasa que las recomendaciones cada padre y cada madre dece su
1:25:58
recomendación la media queries la única recomendación son los datos los datos
1:26:03
que tenga tu página web hay págin web que el 60 por de los usuarios son móviles y son móviles muy antiguos si
1:26:09
estás en Japón pues verás que se utiliza una resolución más que otra y a lo mejor no tienes que tener tantas media queries
1:26:16
si estás en Estados Unidos Pues a lo mejor el el dispositivo móvil más usado es el iPhone y es el que tiene tienes
1:26:22
que enfocar depende mucho de tus usuarios y tus datos no tiene sentido ir a internet y buscar una lista
1:26:28
recomendada y más hoy en día que además hay tantos y tantos dispositivos extraños como puede ser los plegables
1:26:34
como pueden ser tablets y tal es Es imposible manejar todos los tamaños que uno pueda pensar y lo mejor es Mirar los
1:26:42
datos de cuáles son tus usuarios qué resoluciones utilizan y basarte en eso basarse en datos eso es lo mejor del
1:26:47
mundo basarse en datos Porque si no al final lo que te estás basando es los datos de otra persona y no tienes en sentido eh Ya habéis visto Así con el
Alineación en línea de los elementos
1:26:53
tema este de de alinear que para hacer laou es brutal otro tema muy importante la alineación en línea de los elementos
1:27:00
vale esto lo hemos visto en Flex que además me dio por culo pero bueno os explico esto a ver ya tenemos Aquí voy a
1:27:07
cambiar un poco cómo está funcionando esto voy a poner que aquí tenga auto Rose vamos a poner Auto Rose y que sea
1:27:15
100 píxeles vale para que todas queden más bueno un poquito menos 50 píxeles para que queden todas igual y vamos a
1:27:20
hacer template Rose tres vamos a hacer tres de un un fragmento vale vamos a quitar aquí
1:27:27
el Ah Mira esto lo vamos a quitar que tampoco lo vamos a utilizar y vamos a quitar todo esto porque ahora lo que os
1:27:33
quiero enseñar es más bien cómo se alinean oye qué he hecho aquí Ah es que he puesto esto y quería poner Esto vale
1:27:39
quería poner columnas grid template columns vale queremos tener tres columnas vale que se repita hemos
1:27:45
utilizado el repeat solo para que lo veáis os quiero Enseñar cómo se alinean los elementos en grid porque también
1:27:52
igual que en Flex se puede hacer También se puede hacer en grid y de hecho vas a ver cómo se puede centrar un dip vas a
1:27:58
ver cómo se puede centrar un dip que es bastante interesante también entonces porque con grid se puede hacer Igual que se puede hacer con Flex igual que se
1:28:04
puede hacer de muchas formas Bueno ya tenemos el contenedor vamos a hacer una cosa Vamos a darle al contenedor un
1:28:09
ancho fijo vale para que lo veamos un poquito diferente vale Y así nos
1:28:15
funcionen vamos a ponerlo así no tenemos un alto de 300 píxeles y aquí tenemos
1:28:20
los elementos vale muy bien lo primero que vamos a querer hacer es alinear en
1:28:25
línea nuestros items los items sería el uno el dos el tres el 4 5 6 7 y tal no O
1:28:31
sea lo que queremos es alinear nuestros elementos en línea por defecto Qué es lo
1:28:37
que está pasando que si miramos el justify items Tenemos aquí diferentes valores el valor que está no es
1:28:44
exactamente así no el valor por defecto sera el normal que funciona de una forma muy parecida al stretch que significa
1:28:51
estirar que por eso estamos viendo que ocupa cada columna dentro el elemento
1:28:56
está ocupando todo el todo el espacio Entonces el justify items lo que vamos a
1:29:01
hacer es alinear en línea vale en línea cómo lo vamos a ver aquí ahora sí que notes la diferencia si hacemos el Center
1:29:08
qué está pasando que está centrando dentro de esa columna en línea está
1:29:13
centrando el elemento Le podremos decir que lo deje al principio no y dentro de esta cuadrícula que sería esta parte de
1:29:20
aquí lo está dejando al al principio no luego si le ponemos el end lo estaría poniendo al final y si no el Center lo
1:29:28
dejaría en el centro y podemos poner el stretch para que se estire ahora bien el justify items lo que hace es cambiar el
1:29:35
valor de cómo se tiene que alinear ese elemento en línea dentro de la
1:29:42
cuadrícula Pero qué pasa que a lo mejor esto lo hacéis para todos los elementos Pero algún elemento en concreto lo
1:29:48
queréis cambiar por ejemplo el First Child que es el verde pues podéis decir vale vale Este quiero que se justifique
1:29:54
a sí mismo al centro y así Vais a ver vale que se ha centrado podéis hacerlo
1:29:59
con los que queráis podéis decirle poner uno por defecto que sea pues al principio al final centrarlo o estirar
1:30:05
para que ocupe todo el espacio y los que queráis podéis justificarlo eh lo podéis alinear en el centro al final Como
1:30:11
queráis y esto muchas veces seguro que cuando veáis ahora lout os daréis cuenta de este tipo de cosas de Ah mira aquí
1:30:17
han hecho esto porque han conseguido que este se alinee así vale pues lo podéis hacer Bueno en este caso para que lo
1:30:22
entendáis ahí tenéis Start end y Center serían los tres más importantes aquí hay
1:30:28
otros como por ejemplo baseline que sería como al principio también que esto también depende de la dirección tenéis
1:30:34
el normal que sea el por defecto que funciona muy parecido a stretch y ya está Vale esto sea justify items
1:30:41
tendríamos también la alineación en bloque no que sería como de arriba a abajo para nosotros que sería align
Alineación en bloque
1:30:47
items y nos pasaría lo mismo si queremos que se alinee arriba para nosotros sea al principio al final o si lo queremos
1:30:54
centrar Vale y se queda centrado centrado no parece o sea no se ve fácilmente pero fíjate la diferencia
1:31:01
vale Y lo mismo esto también podríamos utilizar la Line self para que pase lo mismo que hemos visto para cambiar uno
1:31:07
en concreto un item concreto lo podríamos poner podemos justificar los o sea podemos poner alinear y justificar
1:31:13
Vale entonces ahora lo que vamos a ver es que nos queda podríamos centrarlo de las dos formas podríamos decir que se
1:31:19
Centre Y fíjate que dentro de la cuadrícula que es si lo veis aquí lo Vais a ver más claro vale fíjate la
1:31:24
cuadrícula esta sería la celda de la cuadrícula pero claro si estamos centrando el elemento verticalmente y
1:31:30
horizontalmente no
1:31:39
confundismo Si tú me has dicho que una fracción era tanto espacio no sé qué no
1:31:45
sé cuánto y aquí estás poniendo 50 píxeles y yo te diré es que eso es lo que ocupa la cuadrícula no lo que ocupa
1:31:51
el elemento si tú lo que quieres es que el elemento se estire y ocupe toda la cuadrícula
1:31:57
pues aparte que lo puedes utilizar dejarlo por defecto lo que tienes que utilizar es el stretch vale que es el de
1:32:02
estirar Y entonces lo que hace es estirarse y ocupar todo el espacio pero los tamaños de los que hablamos aquí son
1:32:09
los de la cuadrícula no de los elementos por lo tanto si al final lo que haces es centrar el elemento dentro de la
1:32:15
cuadrícula su tamaño se va a haber reducido porque ya no se está estirando sino que se está centrando y dependerá
1:32:20
del contenido del elemento que será más grande o más pequeño O sea que super importante vale esto sería para los
1:32:27
elementos los items que tenemos pero de la misma forma también podemos centrar
Centrar el contenido
1:32:32
el contenido como centrar alinear el contenido como un todo o sea todo el
1:32:38
bloque todo el contenido de la cuadrícula si miramos aquí y miráis la cuadrícula fijaos que la cuadrícula el
1:32:45
container sería todo esto no Pero la cuadrícula solo ocupa esta parte de aquí
1:32:50
la parte esta que tenemos con la raya amarilla todo lo que tenemos abajo no es parte de la cuadrícula ese espacio que
1:32:56
ha quedado vacío porque no ha necesitado la cuadrícula llegar hasta ahí por qué Porque le hemos añadido aquí una altura
1:33:01
de 300 píxeles si se lo quitamos vamos a ver que la cuadrícula justamente ocupa
1:33:06
lo mismo porque tiene sentido es el único contenido que tiene pero pensad que podríamos tener otros contenidos podríamos tener otras cosas y que al
1:33:13
final quede un espacio vacío que vamos a querer gestionar en este caso lo estoy simulando así pero para que lo tengáis
1:33:18
claro entonces imaginad que la cuadrícula tal y cual como ahora está quedando fijaos que está pegada arriba
1:33:25
pues podéis decir Bueno yo lo que me gustaría es alinear este contenido lo mismo pasaría con la con el ancho
1:33:31
pongamos que tenemos un ancho de 500 píxeles vamos a poner 500 píxeles y las
1:33:36
columnas vamos a poner que sean 50 píxeles Ah Mira vamos a hacer Esto vale y vamos a poner que sea 300 píxeles vale
1:33:44
Claro imaginad que podríamos tener un espacio que dentro tengamos esta cuadrícula que solo ocupa este espacio
1:33:50
Pero tenemos más espacio a su alrededor Entonces qué podríamos hacer podríamos alinear todo el contenido en en línea o
1:33:57
sea horizontalmente con el yify content por ejemplo para centrarlo o por ejemplo
1:34:02
para dejarlo al final o también lo que podríamos decir aquí es decirle que
1:34:08
distribuya el contenido para que tenga espacio alrededor y esto sería horizontalmente vale porque sería en
1:34:15
línea pero lo mismo podríamos decirle con el align content aquí le podemos decir que lo podríamos centrar y lo
1:34:21
haría verticalmente y fijaos que lo que está pasando aquí es que si utilizáis una Line content Center y un justify
1:34:28
content Center estáis centrando los elementos vale que muchas veces pues así
1:34:33
tendréis una explicación de cómo lo haríamos estaríamos centrando el contenido tanto verticalmente como horizontalmente y así lo tendrías de
1:34:40
hecho la forma más corta de conseguir esto es hacer un Place content Center y
1:34:46
esto lo que hace es aplicar tanto el justify como la Line verticalmente y horizontalmente y así tendrías centrado
1:34:53
todos los el todo el contenido vale todo el contenido todo el contenido estaría centrado tanto verticalmente como
1:34:58
horizontalmente que sepáis que hay otros valores que son interesantes yo que sé pues si ponéis el justify content tenéis
1:35:06
el space between también muy parecidos a los que tenéis en Flex vale el Aline lo podríamos poner c Center y ay el content
1:35:13
perdón no el items vale Y ya Lo tendríamos la diferencia el contenido es todo el contenido como la caja la
1:35:20
cuadrícula la grilla vale sería todo el contenido todo el contenido o sea todo esto sería lo que estamos moviendo como
1:35:26
un bloque el items o sea el content es el contenido Como el todo y el item
1:35:32
sería cada uno de los elementos acuérdate porque items es plural y se refiere a más de una cosa y content es
1:35:38
singular y solo se refiere a una vale Así que con eso ya sabrías perfectamente centrar un Deep con grid ese space
1:35:45
between se puede definir espacio de separación no porque el space between lo que hace es separar exactamente los
1:35:50
elementos igual vale Y el ar lo que está haciendo es poner la misma separación al revés si lo que quieres es cambiar la
1:35:55
separación lo que tienes que hacer por ejemplo pones Center Center vale Y en el Gap tú aquí le pones lo que tú quieras
1:36:02
por ejemplo un píxel 10 pixels y ahí tú le puedes indicar cuál es la separación si de fútbol se tratara mid do Def sería
1:36:08
Messi con esta clase Se ganarías un valón de oro bueno Muchas gracias y aquí viendo por milésima vez Cómo se centra un de Bueno pero al final en el curso de
3 formas de centrar un div
1:36:16
css ya hemos visto tres ve Tres formas con position absolute lo hemos visto también con el display Flex y ahora lo
1:36:21
hemos visto también para el display grid