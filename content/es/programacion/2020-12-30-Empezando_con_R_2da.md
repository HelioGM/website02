---
title: "Capítulo 3: Empezando con R (2da parte)"
date: 2020-12-30T18:21:17-08:00
publishdate: 2020-12-31T18:32:17-08:00
description: "(...continuación) En este capítulo discutiré cómo empezar a usar R. Hablaré brevemente sobre cómo descargar e instalar R, pero la mayor parte del capítulo se centrará en que empiece a escribir comandos R."
#output: 
#   html_document:
#    toc: true # table of content true
draft: false
hideToc: false
enableToc: true
enableTocContent: true
author: Helio
authorEmoji: 👽
pinned: false
fig_caption: true
tags:
- R
- Estadística
series:
- RMarkdown
- Aprendiendo estadística con R
categories:
- Programación
libraries:
- katex
- mathjax
image: images/learning/cap_03.png
---

{{< featuredImage >}} 

---

<style>
body {
text-align: justify}
</style>

<a id="id-01"> </a>
...continuación.

## Usar funciones para hacer cálculos 
Los símbolos **+, -, \*** y así sucesivamente son ejemplos de operadores. Como hemos visto, puede hacer muchos cálculos con solo usar estos operadores. Sin embargo, para hacer cálculos más avanzados (y más adelante, para hacer estadísticas reales), necesitará comenzar a usar **funciones**. Hablaré con más detalle sobre las funciones y cómo funcionan en la Sección **8.4**, pero por ahora vamos a sumergirnos y usar algunas. Para empezar, suponga que quisiera sacar la raíz cuadrada de 225. La raíz cuadrada, en caso de que las matemáticas de la escuela secundaria estén un poco oxidadas, es justo lo opuesto a elevar un número al cuadrado. Entonces, por ejemplo, dado que “5 al cuadrado es 25”, puedo decir que “5 es la raíz cuadrada de 25”. La notación habitual para esto es, 

$$ \sqrt[]{25}=5 $$

aunque a veces también lo verá escrito así: $ 25^{0.5} = 5 $ . Esta segunda forma de escribirlo es útil para "recordarle" el hecho matemático de que "raíz cuadrada de x" es en realidad lo mismo que "elevar x a la potencia de 0.5". Personalmente, nunca he encontrado que esto sea terriblemente significativo psicológicamente, aunque debo admitir que es bastante conveniente matemáticamente. De todos modos, no es importante. Lo importante es que recuerde qué es una raíz cuadrada, ya que la necesitaremos más adelante.

Para calcular la raíz cuadrada de 25, puedo hacerlo en mi cabeza con bastante facilidad, ya que memoricé mis tablas de multiplicar cuando era niño. Se vuelve más difícil cuando los números se hacen más grandes y prácticamente imposible si no son números enteros. Aquí es donde algo como R resulta muy útil. Digamos que quería calcular $ \sqrt[]{225} $, la raíz cuadrada de 225. Hay dos formas de hacerlo usando R. En primer lugar, dado que la raíz cuadrada de 255 es lo mismo que elevar 225 a la potencia de 0.5, podría usar la potencia operador ^, como hicimos antes: 

{{< highlight R >}}
> 225 ^ 0.5  
[1] 15

{{< /highlight >}}

Sin embargo, hay una segunda forma de hacerlo, ya que R también proporciona una **función de raíz cuadrada**, **sqrt ( )**. Para calcular la raíz cuadrada de 255 usando esta función, lo que hago es insertar el número 225 entre paréntesis. Es decir, el comando que escribo es este: 

{{< highlight R >}}
> sqrt(225 )  
[1] 15

{{< /highlight >}}

y como es de esperar de nuestra discusión anterior, los espacios entre paréntesis son puramente cosméticos. Podría haber escrito **sqrt( 225)** o **sqrt( 225 )** y obtener el mismo resultado. Cuando usamos una función para hacer algo, generalmente nos referimos a esto como **llamar** a la función, y los valores que escribimos en la función (puede haber más de uno) se conocen como los **argumentos** de esa función. 
Obviamente, la función **sqrt()** realmente no nos brinda ninguna funcionalidad nueva, ya que ya sabíamos cómo hacer cálculos de raíz cuadrada usando el operador de potencia ^, aunque creo que se ve mejor cuando usamos **sqrt()**. Sin embargo, hay muchas otras funciones en R: de hecho, casi todo lo de interés de lo que hablaré en este libro es una función R de algún tipo. Por ejemplo, una función que necesitaremos usar en este libro es la **función de valor absoluto**. Comparada con la función de raíz cuadrada, es extremadamente simple: simplemente convierte números negativos en números positivos y deja los números positivos en paz. Matemáticamente, el valor absoluto de x se escribe | x | o a veces abs(x) . Calcular valores absolutos en R es bastante fácil, ya que R proporciona la función abs ( ) que puede usar para este propósito. Cuando lo alimentas con un número positivo ... 

{{< highlight R >}}
> abs( 21 )  
[1] 21

{{< /highlight >}}

la función de valor absoluto no le afecta en absoluto. Pero cuando lo alimentas con un número negativo, escupe la versión positiva del mismo número, así: 

{{< highlight R >}}
> abs( -13 )  
[1] 13

{{< /highlight >}}

Honestamente, no hay nada que haga la función de valor absoluto que no puedas hacer con solo mirar el número y borrar el signo menos si lo hay. Sin embargo, hay algunos lugares más adelante en el libro donde tenemos que usar valores absolutos, así que pensé que sería una buena idea explicar el significado del término desde el principio.

Antes de continuar, vale la pena señalar que, de la misma manera que R nos permite unir varias operaciones en un comando más largo, como **1 + 2 * 4**, por ejemplo, también nos permite unir funciones e incluso combinar funciones con operadores si lo deseamos. Por ejemplo, el siguiente es un comando perfectamente legítimo: 

{{< highlight R >}}
> sqrt (1 + abs (-8))  
[1] 3

{{< /highlight >}}

Cuando R ejecuta este comando, comienza calculando el valor de **abs( -8)**, lo que produce un valor intermedio de **8**. Una vez hecho esto, el comando se simplifica a **sqrt(1 + 8)**. Para resolver la raíz cuadrada, primero debe sumar **1 + 8** para obtener **9**, momento en el que evalúa **sqrt(9)**, por lo que finalmente genera un valor de **3**. 
 
### Argumentos de función, sus nombres y sus valores predeterminados
Hay dos cosas más bastante importantes que necesita comprender sobre cómo funcionan las funciones en R, y ese es el uso de argumentos "con nombre" y "valores"" predeterminados para los argumentos. No es de sorprender que esto no quiere decir que sea la última vez que escucharemos sobre cómo funcionan las funciones, pero son las últimas cosas que necesitamos discutir desesperadamente para comenzar. Para entender de qué se tratan estos dos conceptos , presentaré otra función. La función **round( )** se puede usar para redondear algún valor al número entero más cercano. Por ejemplo, podría escribir esto: 

{{< highlight R >}}
> round(3.1415 )  
[1] 3

{{< /highlight >}}

Realmente bastante sencillo. Sin embargo, supongamos que solo quisiera redondearlo a dos lugares decimales: es decir, quiero obtener 3,14 como resultado. La función **round()** admite esto, permitiéndole ingresar un segundo argumento a la función que especifica el número de lugares decimales al que desea redondear el número . En otras palabras, podría hacer esto: 

{{< highlight R >}}
> round(3,14165 , 2)  
[1] 3,14

{{< /highlight >}}

Lo que está sucediendo aquí es que he especificado dos argumentos: el primer argumento es el número que debe redondearse (es decir, **3.1415**), el segundo argumento es el número de lugares decimales a los que debe redondearse (es decir, **2**), y los dos argumentos están separados por una coma. En este ejemplo simple, es bastante fácil recordar qué argumento viene primero y cuál viene segundo, pero para funciones más complicadas esto no es fácil. Afortunadamente, la mayoría de las funciones R utilizan **nombres de argumentos**. Para la función **round( )**, por ejemplo, el número que debe redondearse se especifica mediante el argumento **x**, y el número de puntos decimales a los que desea redondear se especifica mediante el argumento **dígitos**. Como tenemos estos nombres disponibles, podemos especificar los argumentos de la función por nombre. Lo hacemos así:

{{< highlight R >}}
> round(x = 3.1415, digits = 2)  
[1] 3,14

{{< /highlight >}}

Note que esto es similar en espíritu a la asignación de variables (Sección **3.4**), excepto que usé **=** aquí, en lugar de **<-**. En ambos casos, estamos especificando valores específicos para asociarlos con una etiqueta. Sin embargo, existen algunas diferencias entre lo que estaba haciendo antes al crear variables y lo que estoy haciendo aquí al especificar argumentos, por lo que, como consecuencia, es importante que use **=** en este contexto.   
Como puede ver, especificar los argumentos por nombre implica escribir mucho más, pero también es mucho más fácil de leer. Debido a esto, los comandos de este libro generalmente especificarán los argumentos por nombre, ya que eso le aclara lo que estoy haciendo. Sin embargo, una cosa importante a tener en cuenta es que al especificar los argumentos usando sus nombres, no importa en qué orden los escriba. Pero si no usa los nombres de los argumentos, entonces debe ingresar los argumentos en la forma correcta. orden. En otras palabras, estos tres comandos producen la misma salida... 

{{< highlight R >}}
> round(3.14165 , 2)  
> round(x = 3.1415, dígitos = 2)  
> round(dígitos = 2, x = 3.1415)

{{< /highlight >}}

pero este no ...

{{< highlight R >}}
> round(2 , 3.14165)

{{< /highlight >}}

¿Cómo averigua cuál es el orden correcto? Hay algunas formas diferentes, pero la más sencilla es consultar la documentación de ayuda de la función (consulte la Sección **4.12**). Sin embargo, si alguna vez no está seguro, probablemente sea mejor escribir el nombre del argumento. 
Bien, eso es lo primero que dije que necesitarías saber: los nombres de los argumentos. La segunda cosa que debe conocer son los valores predeterminados. Observe que la primera vez que llamé a la función **round()** en realidad no especifiqué el argumento **digits** y, sin embargo, R sabía de alguna manera que esto significaba que debería redondearse al número entero más cercano. ¿Cómo pasó eso? La respuesta es que el argumento **digits** tiene un **valor predeterminado** de **0**, lo que significa que si decide no especificar un valor para **digits**, R actuará como si hubiera escrito **digits = 0**. Esto es bastante útil: la gran mayoría de las veces, cuando desea redondear un número, desea redondearlo al número entero más cercano, y sería bastante molesto tener que especificar el argumento **digits** cada vez. Por otro lado, a veces realmente desea redondear a algo que no sea el número entero más cercano, ¡y sería aún más molesto si R no lo permitiera! Por lo tanto, al tener **digits = 0** como valor predeterminado, obtenemos lo mejor de ambos mundos. 

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Dejar que Rstudio te ayude con tus comandos
Es hora de una pequeña digresión. En esta etapa, sabe cómo escribir comandos básicos, incluido cómo usar las funciones R. Y probablemente empiece a darse cuenta de que hay muchas funciones R, todas las cuales tienen sus propios argumentos. Probablemente también esté preocupado de tener que recordarlos todos. Afortunadamente, no es tan malo. De hecho, muy pocos analistas de datos se molestan en intentar recordar todos los comandos. Lo que realmente hacen es utilizar trucos para hacerles la vida más fácil. El primero (y posiblemente el más importante) es utilizar Internet. Si no sabe cómo funciona una función R en particular, busque en Google. En segundo lugar, puede buscar la documentación de ayuda de R. Hablaré más sobre estos dos trucos en la Sección **4.12**. Pero ahora mismo quiero llamar su atención sobre un par de trucos simples que Rstudio pone a su disposición.

### Autocompletar usando "tabulación"
Lo primero que quiero llamar su atención es la capacidad de autocompletar en Rstudio.  
Sigamos nuestro ejemplo anterior y supongamos que lo que quiere hacer es redondear un número. Esta vez, comience a escribir el nombre de la función que desee y luego presione la tecla "tab". Rstudio mostrará una pequeña ventana como la que se muestra en la Figura **3.2**. En esta figura, escribí las letras **ro** en la línea de comando y luego presioné el tabulador. La ventana tiene dos paneles. A la izquierda, hay una lista de variables y funciones que comienzan con las letras que escribí que se muestran en texto negro, y un texto gris que le dice dónde está almacenada esa variable/función. Ignore el texto gris por ahora: no tendrá mucho sentido para usted hasta que hablemos de los paquetes en la Sección **4.2**. En la Figura **3.2** puede ver que hay bastantes cosas que comienzan con las letras **ro:** hay algo llamado **rock**, algo llamado **round**, algo llamado redondo, fecha, etc. El que queremos es redondo, pero si lo escribe usted mismo, notará que cuando presiona la tecla de tabulación, aparece la ventana con la entrada superior (es decir, **rock**) resaltada. Puede utilizar las teclas de flecha hacia arriba y hacia abajo para seleccionar el que desee. O, si ninguna de las opciones le parece correcta , puede presionar la tecla de escape ("esc") o la tecla de flecha izquierda para que la ventana desaparezca.  

En nuestro caso, lo que queremos es la opción redonda, así que la seleccionaremos. Cuando haga esto, verá que el panel de la derecha cambia. Anteriormente, nos había estado diciendo algo sobre el conjunto de datos de rocas (es decir, "Mediciones en 48 muestras de rocas ...") que se distribuye como parte de R. Pero cuando seleccionamos **round**, muestra información sobre la función **round()**, exactamente como se muestra en la Figura **3.2**. Esta pantalla es realmente útil. Lo primero que dice es **round( x, digits = 0)**: lo que esto le dice es que la función **round()** tiene dos argumentos. El primer argumento se llama **x** y no tiene un valor predeterminado. El segundo argumento es **digits** y tiene un valor predeterminado de **0**. En muchas situaciones, esa es toda la información que necesita. Pero Rstudio va un poco más allá y proporciona información adicional sobre la función que se encuentra debajo. A veces, esa información adicional es muy útil, a veces no: Rstudio extrae ese texto de la documentación de ayuda de R, y mi experiencia es que la utilidad de esa documentación varía enormemente. De todos modos, si ha decidido que **round()** es la función que desea usar, puede presionar la flecha derecha o la tecla Intro, y Rstudio terminará de escribir el resto del nombre de la función por usted.  

La herramienta de autocompletar de Rstudio funciona de manera ligeramente diferente si ya ha escrito el nombre de la función y ahora está intentando escribir los argumentos. Por ejemplo, supongamos que escribí **round(** en la consola y luego presioné la tecla tab. Rstudio es lo suficientemente inteligente como para reconocer que ya sé el nombre de la función que quiero, ¡porque ya lo escribí! calcula que lo que me interesa son los argumentos de esa función. Eso es lo que aparece en la ventana pequeña. Puede ver esto en la Figura **3.3**. De nuevo, la ventana tiene dos paneles y puede interactuar con esta ventana exactamente de la misma manera que lo hizo con la ventana que se muestra en la Figura **3.2**. En el panel de la izquierda , puede ver una lista de los nombres de los argumentos.En el lado derecho , muestra información sobre lo que hace el argumento seleccionado.

### Examinando tu historial de comandos
Una cosa que R hace automáticamente es realizar un seguimiento de su "historial de comandos". Es decir, recuerda todos los comandos que ha escrito anteriormente. Puede acceder a este historial de diferentes formas. La forma más sencilla es utilizar las teclas de flecha hacia arriba y hacia abajo. Si presiona la tecla arriba, la consola R le mostrará el comando más reciente que ha escrito. Vuelva a presionarlo y le mostrará el comando anterior. Si desea que desaparezca el texto de la pantalla, presione escape. El uso de las teclas arriba y abajo puede ser muy útil si ha escrito un comando largo que tenía un error tipográfico. En lugar de tener que volver a escribirlo todo desde cero, puede usar la tecla de arriba para abrir el comando y arreglarlo.  

La segunda forma de obtener acceso a su historial de comandos es mirar el panel de historial en Rstudio .  

En la parte superior derecha de la ventana de Rstudio , verá una pestaña denominada "Historial". Haga clic en eso y verá una lista de todos sus comandos recientes que se muestran en ese panel: debería parecerse a la Figura **3.4**. Si hace doble clic en uno de los comandos, se copiará a la consola R. (Puede lograr el mismo resultado seleccionando el comando que desea con el mouse y luego haciendo clic en el botón "A la consola").  

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Almacenando muchos números como un vector
En este punto, hemos cubierto las funciones con suficiente detalle para que podamos pasar con seguridad los siguientes dos capítulos (con una pequeña excepción: consulte la Sección **4.11)**, así que volvamos a nuestra discusión de variables. Cuando presenté las variables en la Sección **3.4**, le mostré cómo podemos usar variables para almacenar un solo número. En esta sección, ampliaremos esta idea y veremos cómo almacenar varios números dentro de una variable. En R, el nombre de una variable que puede almacenar varios valores es un $ \color{DarkMagenta}{vector} $. Así que creemos uno. 
 
### Creando un vector
Sigamos con mi tonto ejemplo de “hacerse rico rápidamente escribiendo un libro de texto”. Supongamos que la compañía de libros de texto (si realmente tuviera una) me envía datos de ventas mensualmente. Dado que mi clase comenzó a fines de febrero, podríamos esperar que la mayoría de las ventas ocurran hacia el comienzo del año. Supongamos que tengo 100 ventas en febrero, 200 ventas en marzo y 50 ventas en abril, y ninguna otra venta durante el resto del año. Lo que me gustaría hacer es tener una variable, llamémosla **ventas.por.mes**, que almacene todos estos datos de ventas. El primer número almacenado debería ser **0** ya que no tuve ventas en enero, el segundo debería ser **100** y así sucesivamente . La forma más sencilla de hacer esto en R es usar la función **combine**, c( ). Para hacerlo, todo lo que tenemos que hacer es escribir todos los números que desea almacenar en una lista separada por comas, como esta: 

{{< highlight R >}}
> ventas.por.mes <- c (0, 100, 200, 50, 0, 0, 0, 0, 0, 0, 0, 0)  
> ventas.por.mes  
[1] 0 100 200 50 0 0 0 0 0 0 0 0

{{< /highlight >}}

Para usar la terminología correcta aquí, tenemos una sola variable llamada **ventas.por.mes**: esta variable es un vector que consta de 12 **elementos**. 
 
### Una útil digresión
Ahora que hemos aprendido a poner información en un vector, lo siguiente que debemos entender es cómo extraer esa información nuevamente. Sin embargo, antes de hacerlo, vale la pena dar un pequeño desvío. Si ha estado siguiendo, escribiendo todos los comandos en R usted mismo, es posible que el resultado que vio cuando imprimimos el vector **ventas.por.mes** fuera ligeramente diferente a lo que mostré anteriormente. Esto habría sucedido si la ventana (o el panel de Rstudio ) que contiene la consola R es muy, muy estrecha. Si ese fuera el caso, es posible que haya visto un resultado parecido a esto: 

{{< highlight R >}}
> ventas.por.mes  
[1] 0 100 200 50 0 0 0 0  
[9] 0 0 0 0

{{< /highlight >}}

Como no había mucho espacio en la pantalla, R imprimió los resultados en dos líneas. Pero eso no es lo importante a notar. El punto importante es que la primera línea tiene un **[1]** delante, mientras que la segunda línea comienza con **[9]**. Está bastante claro lo que está sucediendo aquí. Para la primera fila, R ha impreso desde el primer elemento hasta el octavo elemento, por lo que comienza esa fila con un **[1]**. Para la segunda fila, R imprimió el noveno elemento del vector hasta el duodécimo, por lo que comienza esa fila con un **[9]** para que pueda saber dónde está de un vistazo. Puede parecerle un poco extraño que R haga esto, pero de alguna manera es una bondad, ¡especialmente cuando se trata de conjuntos de datos más grandes! 
 
### Obtener información de los vectores
Para volver a la historia principal, consideremos el problema de cómo obtener información de un vector. En este punto, es posible que tenga la sospecha de que la respuesta tiene algo que ver con las cosas **[1]** y **[9]** que R ha estado imprimiendo. Y por supuesto que tienes razón. Supongamos que solo quiero extraer los datos de ventas de febrero. Febrero es el segundo mes del año, así que intentemos esto: 

{{< highlight R >}}
> ventas.por.mes[2]  
[1] 100

{{< /highlight >}}

Sí, esas son las rebajas de febrero. Pero hay un detalle sutil a tener en cuenta aquí: observe que R produce **[1] 100**, *no* **[2] 100**. Esto se debe a que R está siendo extremadamente literal. Cuando escribimos **ventas.por.mes[2]**, le pedimos a R que encontrara exactamente una cosa, y esa cosa resulta ser el segundo elemento de nuestro vector **ventas.por.mes**. Entonces, cuando genera **[1] 100**, lo que R está diciendo es que *el número que acabamos de pedir* es **100**. Este comportamiento tiene más sentido cuando se da cuenta de que podemos usar este truco para crear nuevas variables. Por ejemplo, podría crear una variable **ventas.de.febrero** como esta: 

{{< highlight R >}}
> ventas.de.febrero <- ventas.por.mes[2]  
> ventas.de.febrero  
[1] 100

{{< /highlight >}}

Obviamente, la nueva variable february.sales solo debe tener un elemento, por lo que cuando imprimo esta nueva variable, la salida R comienza con un [1] porque 100 es el valor del primer (y único) elemento de **ventas.de.febrero**. El hecho de que este también sea el valor del segundo elemento de ventas por mes es irrelevante. Volveremos a retomar este tema en breve (**Sección 3.10**). 
 
### Alterando los elementos de un vector
A veces querrá cambiar los valores almacenados en un vector. Imagínese mi sorpresa cuando el editor me llama para decirme que los datos de ventas de mayo son incorrectos. En realidad, se vendieron 25 libros adicionales en mayo, pero hubo un error o algo así, por lo que no me lo habían dicho. ¿Cómo puedo corregir mi variable **ventas.por.mes**? Una posibilidad sería volver a asignar todo el vector desde el principio, utilizando **c()**. Pero eso es mucho escribir. Además, es un poco derrochador: ¿por qué debería R tener que redefinir las cifras de ventas para los 12 meses, cuando solo el quinto es incorrecto? Afortunadamente, podemos decirle a R que cambie solo el quinto elemento, usando este truco: 

{{< highlight R >}}
> ventas.por.mes[5] <- 25  
> ventas.por.mes  
[1] 0 100 200 50 25 0 0 0 0 0 0 0

{{< /highlight >}}

Otra forma de editar variables es usar las funciones **edit()** o **fix()**. No los discutiré en detalle en este momento, pero puede verlos por su cuenta. 
 
### Cosas útiles que debes saber sobre los vectores
Antes de continuar, quiero mencionar un par de cosas más sobre los vectores. En primer lugar, a menudo se encuentra deseando saber cuántos elementos hay en un vector (generalmente porque lo ha olvidado). Puede usar la función **length()** para hacer esto. Es bastante sencillo: 

{{< highlight R >}}
> length(x = ventas.por.mes)  
[1] 12

{{< /highlight >}}

En segundo lugar, a menudo desea alterar todos los elementos de un vector a la vez. Por ejemplo, supongamos que quisiera calcular cuánto dinero ganaba cada mes. Como estoy ganando $7 por libro (no en serio, eso es bastante parecido a lo que obtienen los autores con los libros de texto muy caros que se espera que compre), lo que quiero hacer es multiplicar cada elemento de **ventas.por.mes** por 7. R hace que esto sea bastante fácil, como muestra el siguiente ejemplo: 

{{< highlight R >}}
> ventas.por.mes * 7  
[1] 0 700 1400 350 0 0 0 0 0 0 0 0

{{< /highlight >}}

En otras palabras, cuando multiplica un vector por un solo número, todos los elementos del vector se multiplican. Lo mismo es cierto para la suma, resta, división y toma de poderes. Entonces eso es genial. Por otro lado, suponga que quisiera saber cuánto dinero estaba ganando por día, en lugar de por mes. Como no todos los meses tienen la misma cantidad de días, necesito hacer algo ligeramente diferente. En primer lugar, crearé dos nuevos vectores: 

{{< highlight R >}}
> dias.por.mes <- c (31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31)  
> beneficio <- ventas.por.mes * 7

{{< /highlight >}}

Obviamente, la variable de **beneficio** es la misma que creamos anteriormente, y la variable **dias.por.mes** es bastante sencilla. Lo que quiero hacer es dividir cada elemento de **beneficio** por el elemento *correspondiente* de **dias.por.mes**. Nuevamente, R hace que esto sea bastante fácil: 

{{< highlight R >}}
> beneficio / dias.por.mes  
[1] 0,00000 25,00000 45,16129 11,66667 0,00000 0,00000 0,00000 0,00000 0,00000  
[10] 0,00000 0,00000 0,00000

{{< /highlight >}}

Todavía no me gustan todos esos ceros, pero eso no es lo que importa aquí. Observe que el segundo elemento de la producción es 25, porque R ha dividido el segundo elemento de **beneficio** (es decir, 700) por el segundo elemento de **dias.por.mes** (es decir, 28). De manera similar, el tercer elemento de la salida es igual a 1400 dividido por 31, y así sucesivamente. Hablaremos más sobre cálculos que involucran vectores más adelante (y en particular una cosa llamada "regla de reciclaje"; Sección **7.12.2**), pero eso es suficiente detalle por ahora. 

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Almacenamiento de datos de texto
La mayoría de las veces, sus datos serán de naturaleza numérica, pero no siempre. A veces, sus datos realmente necesitan describirse usando texto, no usando números. Para abordar esto, debemos considerar la situación en la que nuestras variables almacenan texto. Para crear una variable que almacene la palabra "hola", podemos escribir esto: 

{{< highlight R >}}
> saludo <- "hola"  
> saludo  
[1] "hola"

{{< /highlight >}}

Al interpretar esto, es importante reconocer que las comillas aquí no son parte de la cadena en sí. Son solo algo que usamos para asegurarnos de que R sepa tratar los caracteres que encierran como un fragmento de datos de texto, conocido como una **cadena de caracteres**. En otras palabras, R trata **"hola"** como una cadena que contiene la palabra "hola"; pero si hubiera escrito **hola** en su lugar, ¡R buscaría una variable con ese nombre! También puede usar **'hola'** para especificar una cadena de caracteres. 
Bien, así es como almacenamos el texto. A continuación, es importante reconocer que cuando hacemos esto, R almacena la palabra completa **"hola"** como un solo elemento: nuestra variable de **saludo** ***no*** es un vector de cinco letras diferentes. Más bien, tiene solo un elemento, y ese elemento corresponde a la cadena de caracteres completa **"hola"**. Para ilustrar esto, si realmente le pido a R que encuentre el primer elemento de **saludo**, imprime la cadena completa: 

{{< highlight R >}}
> saludo [ 1]  
[1] "hola"

{{< /highlight >}}

Por supuesto, no hay ninguna razón por la que no pueda crear un vector de cadenas de caracteres. Por ejemplo, si tuviéramos que continuar con el ejemplo de mis intentos de ver los datos de ventas mensuales de mi libro, una variable que podría querer incluiría los nombres de los 12 **meses**. Para hacerlo, podría escribir un comando como este 

{{< highlight R >}}
> meses <- c ( "enero", "febrero", "marzo", "abril", "mayo", "junio",  
+ "Julio", "agosto", "septiembre", "octubre", "noviembre", "diciembre")  
> meses  
[1] "enero" "febrero" "marzo" "abril" "mayo" "junio"  
[7] "julio" "agosto" "septiembre" "octubre" "noviembre" "diciembre"

{{< /highlight >}}

Este es un **vector de caracteres** que contiene 12 elementos, cada uno de los cuales es el nombre de un mes. Entonces, si quisiera que R me dijera el nombre del cuarto mes, todo lo que haría es esto: 

{{< highlight R >}}
> meses[4]  
[1] "abril"

{{< /highlight >}}
 
### Trabajando con texto
Trabajar con datos de texto es algo más complicado que trabajar con datos numéricos, y discutir algunas de las ideas básicas en la Sección **7.8**, pero para los propósitos del capítulo actual sólo necesitamos este bosquejo de croquis. La única otra cosa que quiero hacer antes de continuar es mostrarte un ejemplo de una función que se puede aplicar a datos de texto. Hasta ahora, la mayoría de las funciones que hemos visto (es decir, **sqrt()**, **abs()** y **round()**) solo tienen sentido cuando se aplican a datos numéricos (p. Ej., no se puede calcular la raíz cuadrada de **"hola"**), y hemos visto una función que se puede aplicar a prácticamente cualquier variable o vector (es decir, **length()**). Por lo tanto , sería bueno ver un ejemplo de una función que se puede aplicar al texto. 
La función que les voy a presentar se llama **nchar()**, y lo que hace es contar el número de caracteres individuales que componen una cadena. Recuerde antes que cuando intentamos calcular la **length( )** de nuestra variable de **saludo**, devolvió un valor de **1**: la variable de **saludo** contiene solo una cadena, que resulta ser **"hola"**. Pero, ¿y si quiero saber cuántas letras hay en la palabra? Claro, podría *contarlos*, pero eso es aburrido, y más aún, es una estrategia terrible si lo que quería saber era la cantidad de letras en *Guerra y paz*. Ahí es donde la función **nchar()** es útil: 

{{< highlight R >}}
> nchar(x = saludo)  
[1] 5

{{< /highlight >}}

Eso tiene sentido, ya que de hecho hay 5 letras en la cadena **"hola"**. Mejor aún, puede aplicar **nchar()** a vectores completos. Entonces, por ejemplo, si quiero que R me diga cuántas letras hay en los nombres de cada uno de los 12 meses, puedo hacer esto: 

{{< highlight R >}}
> nchar(x = meses)  
[1] 7 8 5 5 3 4 4 6 9 7 8 8

{{< /highlight >}}

Así que es bueno saberlo. La función **nchar()** puede hacer un poco más que esto, y hay muchas otras funciones que puede hacer para extraer más información del texto o hacer todo tipo de cosas sofisticadas. Sin embargo, ¡ el objetivo aquí no es enseñar nada de eso! El objetivo en este momento es solo ver un ejemplo de una función que realmente funciona cuando se aplica al texto. 

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Almacenamiento de datos "verdaderos o falsos"  
Es hora de pasar a un tercer tipo de datos. Un concepto clave en el que se basa gran parte de R es la idea de **valor lógico**. Un valor lógico es una afirmación sobre si algo es verdadero o falso. Esto se implementa en R de una manera bastante sencilla. Hay dos valores lógicos, a saber, **VERDADERO** y **FALSO**. A pesar de la sencillez, los valores lógicos son cosas muy útiles. Veamos como funcionan. 
 
### Evaluación de verdades matemáticas
En el clásico libro *1984* de George Orwell, una de las consignas utilizadas por el Partido totalitario era “dos más dos es cinco”, con la idea de que el dominio político de la libertad humana se completa cuando es posible subvertir incluso la más básica de las verdades. Es un pensamiento aterrador, especialmente cuando el protagonista Winston Smith finalmente se derrumba bajo tortura y acepta la proposición. “El hombre es infinitamente maleable”, dice el libro. Estoy bastante seguro de que esto no es cierto para los humanos pero definitivamente no es cierto para R. R no es infinitamente maleable. Tiene opiniones bastante firmes sobre el tema de lo que es y no es cierto, al menos en lo que respecta a las matemáticas básicas. Si le pido que calcule **2 + 2**, siempre da la misma respuesta, y no es un maldito 5: 

{{< highlight R >}}
> 2 + 2  
[1] 4

{{< /highlight >}}

Por supuesto, hasta ahora R solo está haciendo los cálculos. No le he pedido que afirme explícitamente que 2 + 2 = 4 es una declaración verdadera. Si quiero que R haga un juicio explícito, puedo usar un comando como este: 

{{< highlight R >}}
> 2 + 2 == 4  
[1] TRUE

{{< /highlight >}}

Lo que he hecho aquí es usar el **operador de igualdad**, **==**, para forzar a R a hacer un juicio de "verdadero o falso". Bien, veamos qué piensa R del eslogan del Partido: 

{{< highlight R >}}
> 2 + 2 == 5  
[1] FALSE

{{< /highlight >}}

¡Booyah! ¡Libertad y ponis para todos! O algo así. De todos modos, vale la pena echar un vistazo a lo que sucede si trato de obligar a R a creer que dos más dos son cinco haciendo una declaración de asignación como **2 + 2 = 5** o **2 + 2 <- 5**. Cuando hago esto, esto es lo que sucede:

{{< highlight R >}}
> 2 + 2 = 5  
Error in 2 + 2 = 5 : target of assignment expands to non-language object

{{< /highlight >}}

A R no le gusta mucho esto. Se reconoce que **2 + 2** *no* es una variable (que es lo que la “parte no lingüística del objeto” está diciendo), y que no va a dejarte intentar “Reasignar” la misma. Si bien R es bastante flexible y, de hecho, le permite hacer cosas bastante notables para redefinir partes de R en sí, hay algunas verdades básicas y primitivas a las que se niega a renunciar. No cambiará las leyes de la suma y no cambiará la definición del número **2**. 
Probablemente sea lo mejor.
 
### Operaciones lógicas
Así que ahora hemos visto operaciones lógicas en funcionamiento, pero hasta ahora solo hemos visto el ejemplo más simple posible. Probablemente no se sorprenda al descubrir que podemos combinar operaciones lógicas con otras operaciones y funciones de una manera más complicada, como esta:

{{< highlight R >}}
> 3 * 3 + 4 * 4 == 5 * 5  
[1] TRUE

{{< /highlight >}}

o esto

{{< highlight R >}}
> sqrt(25 ) == 5  
[1] TRUE

{{< /highlight >}}

<caption>Tabla 3.2: Algunos operadores lógicos. Técnicamente debería llamar a estos “operadores relacionales binarios”, pero francamente no quiero. Es mi libro para que nadie pueda obligarme.</caption>

| operación  | operador | ejemplo de entrada | ejemplo de respuesta  |
| :------------ | :-----------: | -------------------: |-------------------: |
| menor que | <  | 2 < 3  | TRUE |
| menor o igual que | <=  | 2 <= 2 | TRUE |
| mayor que  | > | 2 > 3 | FALSE |
| mayor o igual que | >=  | 2 >= 2 | TRUE |
| igual a  | ==  | 2 == 3   | FALSE |
| no igual a  | !=  | 2 != 3 | TRUE |


No solo eso, sino que, como lo ilustra la Tabla **3.2**, hay varios otros operadores lógicos que puede usar, correspondientes a algunos conceptos matemáticos básicos. Con suerte, todos estos se explican por sí mismos: por ejemplo, el operador **menor que** **<** comprueba si el número de la izquierda es menor que el número de la derecha. Si es menor, entonces R devuelve una respuesta verdadera (**TRUE**): 

{{< highlight R >}}
> 99 <100  
[1] TRUE

{{< /highlight >}}

pero si los dos números son iguales, o si el de la derecha es mayor, entonces R devuelve una respuesta falsa (**FALSE**), como lo ilustran los siguientes dos ejemplos: 

{{< highlight R >}}
> 100 <100  
[1] FALSE  
> 100 <99  
[1] FALSE  

{{< /highlight >}}

Por el contrario, el operador **menor o igual que** **<=** hará exactamente lo que dice. Devuelve un valor de **TRUE** si el número del lado izquierdo es menor o igual que el número del lado derecho. Entonces, si repetimos los dos ejemplos anteriores usando **<=**, esto es lo que obtenemos: 

{{< highlight R >}}
> 100 <= 100  
[1] TRUE  
> 100 <= 99  
[1] FALSE

{{< /highlight >}}

¡Y en este punto espero que sea bastante obvio qué hacen el operador **mayor que** **>** y el operador **mayor o igual que** **>=**! ¡El siguiente en la lista de operadores lógicos es el operador **no igual a** **!=** que , como todos los demás, hace lo que dice que hace. Devuelve un valor de TRUE cuando las cosas de ambos lados no son idénticas entre sí. Por lo tanto, dado que 2 + 2 no es igual a 5, obtenemos: 

{{< highlight R >}}
> 2 + 2!= 5  
[1] TRUE

{{< /highlight >}}

Aún no hemos terminado. Hay tres operaciones lógicas más que vale la pena conocer, enumeradas en la Tabla **3.3**. Estos son los  operadores **no** **!**, el operador **and** **&**, y el operador **or** **|** . Al igual que los otros operadores lógicos, su comportamiento es más o menos exactamente lo que cabría esperar dados sus nombres. Por ejemplo, si le pido que evalúe la afirmación de que “2 + 2 = 4 o 2 + 2 = 5”, diría que es verdad. Dado que es una declaración de "una o la otra", todo lo que necesitamos es que una de las dos partes sea verdadera. Eso es lo que | el operador hace: 

<caption>Tabla 3.3: Algunos operadores más lógicos.</caption>

| operación  | operador | ejemplo de entrada | ejemplo de respuesta  |
| :------------ | :-----------: | -------------------: |-------------------: |
| not | \! | \!(1==1)  | FALSE |
| or | \|  | (1==1) \| (2==3) | TRUE |
| and  | \&  | (1==1) \& (2==3) | FALSE |

 
{{< highlight R >}}
> (2 + 2 == 4) | (2 + 2 == 5)  
[1] VERDADERO

{{< /highlight >}}

Por otro lado, si le pido que evalúe la afirmación de que "2 + 2 = 4 y 2 + 2 = 5", diría que es falsa. Dado que esta es una declaración y , necesitamos que ambas partes sean verdaderas. Y eso es lo que hace el operador & : 

{{< highlight R >}}
> (2 + 2 == 4) y (2 + 2 == 5)  
[1] FALSO

{{< /highlight >}}

Finalmente, está el operador not, que es simple pero molesto de describir en inglés. Si le pido que evalúe mi afirmación de que “no es cierto que 2 + 2 = 5”, entonces diría que mi afirmación es verdadera; porque mi afirmación es que "2 + 2 = 5 es falso". Y tengo razón. Si escribimos esto como un comando R , obtenemos esto: 

{{< highlight R >}}
>! (2 + 2 == 5)  
[1] VERDADERO

{{< /highlight >}}

En otras palabras, dado que 2 + 2 == 5 es una declaración FALSA, ¡debe ser el caso que! (2 + 2 == 5) es VERDADERO. Esencialmente, lo que realmente hemos hecho es afirmar que "no falso" es lo mismo que "verdadero". Obviamente, esto no es del todo correcto en la vida real. Pero R vive en un mundo mucho más blanco o negro: para R todo es verdadero o falso. No se permiten tonos de gris. De hecho, podemos ver esto mucho más explícitamente, así: 

{{< highlight R >}}
>! FALSO  
[1] VERDADERO

{{< /highlight >}}

Por supuesto, en nuestro ejemplo 2 + 2 = 5, ¡realmente no necesitábamos usar "no "! y "igual a" == como dos operadores separados. ¡Podríamos haber usado el operador "no es igual a" ! = así: 

{{< highlight R >}}
> 2+ 2! = 5  
[1] VERDADERO

{{< /highlight >}}

¡Pero hay muchas situaciones en las que realmente necesitas usar ! operador. Veremos algunos más adelante.
 
### Almacenamiento y uso de datos lógicos
Hasta este punto, he introducido datos numéricos (en las Secciones 3.4 y 3.7) y datos de caracteres (en
Sección 3.8). Por lo tanto, es posible que no se sorprenda al descubrir que estos valores VERDADERO y FALSO que ha estado produciendo R son en realidad un tercer tipo de datos, llamados datos lógicos. Es decir, cuando le pregunté a R si 2 + 2 == 5 y dijo [1] FALSO en respuesta, en realidad estaba produciendo información que podemos almacenar en variables. Por ejemplo, podría crear una variable llamada is.the.Party.correct , que almacenaría la opinión de R: 

{{< highlight R >}}
> es.la.parte.correcta <- 2 + 2 == 5  
> es.la.parte.correcta
[1] FALSO

{{< /highlight >}}

Alternativamente, puede asignar el valor directamente, escribiendo VERDADERO o FALSO en su comando. Me gusta esto:

{{< highlight R >}}
> es.la.parte.correcta <- FALSO  
> es.la.parte.correcta  
[1] FALSO

{{< /highlight >}}

Mejor aún, debido a que es un poco tedioso escribir VERDADERO o FALSO una y otra vez, R le proporciona un atajo: puede usar T y F en su lugar (pero distingue entre mayúsculas y minúsculas: t y f no funcionarán). 27 Entonces esto funciona: 

{{< highlight R >}}
> es.la.parte.correcta <- F  
> es.la.parte.correcta  
[1] FALSO

{{< /highlight >}}

pero esto no:

{{< highlight R >}}
> es.la.parte.correcta <- f  
Error: objeto 'f' no encontrado
 
{{< /highlight >}}

### Vectores de lógicas
Lo siguiente que se debe mencionar es que puede almacenar vectores de valores lógicos exactamente de la misma manera que puede almacenar vectores de números (Sección 3.7) y vectores de datos de texto (Sección 3.8). Nuevamente, podemos definirlos directamente a través de la función c ( ), así: 

{{< highlight R >}}
> x <- c ( VERDADERO, VERDADERO, FALSO)  
> x  
[1] VERDADERO VERDADERO FALSO

{{< /highlight >}}

o puede producir un vector de lógicas aplicando un operador lógico a un vector. Es posible que esto no tenga mucho sentido para ti, así que vamos a descomprimirlo lentamente. Primero, supongamos que tenemos un vector de números (es decir, un "vector no lógico"). Por ejemplo, podríamos usar el vector ventas por mes que usamos en la sección 3.7. Suponga que quisiera que R me dijera, para cada mes del año, si realmente vendí un libro en ese mes. Puedo hacerlo escribiendo esto: 

{{< highlight R >}}
> ventas por mes > 0  
[1] FALSO TRUE TRUE TRUE TRUE FALSO FALSO FALSO FALSO FALSO FALSO FALSO  

{{< /highlight >}}

y nuevamente, puedo almacenar esto en un vector si quiero, como ilustra el siguiente ejemplo:  

{{< highlight R >}}
> cualquier.ventas .este.meso <- ventas.por.meses > 0  
> cualquier.ventas .este . mes  
[1] FALSO TRUE TRUE TRUE TRUE FALSO FALSO FALSO FALSO FALSO FALSO FALSO   

{{< /highlight >}}

En otras palabras, any.sales .this.month es un vector lógico cuyos elementos son VERDADEROS solo si el elemento correspondiente de sales.by.month es mayor que cero. Por ejemplo, dado que no vendí libros en enero, el primer elemento es FALSO. 
 
### Aplicar una operación lógica al texto
En un momento (Sección 3.10) le mostraré por qué estas operaciones lógicas y vectores lógicos son tan útiles, pero antes de hacerlo, quiero señalar brevemente que puede aplicarlos tanto al texto como a los datos lógicos . Es solo que debemos ser un poco más cuidadosos al comprender cómo R interpreta las diferentes operaciones. En esta sección hablaré sobre cómo se aplica el operador igual a == al texto, ya que este es el más importante. Obviamente, el operador no es igual a ! = da las respuestas exactamente opuestas a ==, así que implícitamente también estoy hablando de ese, pero no daré comandos específicos que muestren el uso de! =. En cuanto a los otros operadores, aplazaré una discusión más detallada de este tema hasta la Sección 7.8.5. 
Bien, veamos cómo funciona. En cierto sentido, es muy simple. Por ejemplo, puedo preguntarle a R si la palabra "gato" es lo mismo que la palabra "perro ", así: 

{{< highlight R >}}
> "gato" == "perro"  
[1] FALSO

{{< /highlight >}}

Eso es bastante obvio, y es bueno saber que incluso R puede darse cuenta de eso. De manera similar, R reconoce que un "gato" es un "gato ":

{{< highlight R >}}
> "gato" == "gato"  
[1] VERDADERO

{{< /highlight >}}

Una vez más, eso es exactamente lo que esperaríamos. Sin embargo, lo que debe tener en cuenta es que R no es para nada tolerante cuando se trata de gramática y espaciado. Si dos cadenas difieren de alguna manera, R dirá que no son iguales entre sí, como indican los siguientes ejemplos: 

{{< highlight R >}}
> "gato" == "gato"  
[1] FALSO  
> "gato" == "GATO"  
[1] FALSO  
> "gato" == "ca t"  
[1] FALSO

{{< /highlight >}}

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Vectores de indexación
Una última cosa que agregar antes de terminar este capítulo. Hasta ahora, siempre que he tenido que obtener información de un vector, todo lo que he hecho es escribir algo como meses [ 4]; y cuando hago esto, R imprime el cuarto elemento del vector de meses. En esta sección, le mostraré dos trucos adicionales para obtener información del vector. 

### Extrayendo varios elementos
Una cosa muy útil que podemos hacer es extraer más de un elemento a la vez. En el ejemplo anterior, solo usamos un solo número (es decir, 2) para indicar qué elemento queríamos. Alternativamente, podemos usar un vector. Entonces, supongamos que quisiera los datos de febrero, marzo y abril. Lo que podría hacer es usar el vector c ( 2,3,4) para indicar qué elementos quiero que R extraiga. Es decir, escribiría esto: 

{{< highlight R >}}
> ventas.por.mes [c (2,3,4)]  
[1] 100 200 50

{{< /highlight >}}

Tenga en cuenta que el orden importa aquí. Si solicité los datos en el orden inverso (es decir, primero de abril, luego de marzo, luego de febrero) usando el vector c ( 4,3,2), entonces R genera los datos en el orden inverso: 

{{< highlight R >}}
> ventas.por.mes [c (4,3,2)]  
[1] 50 200 100

{{< /highlight >}}

Una segunda cosa a tener en cuenta es que R le proporciona atajos útiles para situaciones muy comunes.
Por ejemplo, supongamos que quisiera extraer todo desde el segundo mes hasta el octavo mes.
Una forma de hacer esto es hacer lo mismo que hice anteriormente y usar el vector c ( 2,3,4,5,6,7,8) para indicar los elementos que quiero. Eso funciona bien 

{{< highlight R >}}
> ventas.por.mes [c (2,3,4,5,6,7,8)]  
[1] 100 200 50 0 0 0 0

{{< /highlight >}}

pero es como escribir mucho. Para ayudar a que esto sea más fácil, R le permite usar 2: 8 como abreviatura de c ( 2,3,4,5,6,7,8), lo que simplifica mucho las cosas. Primero, verifiquemos que esto sea cierto: 

{{< highlight R >}}
> 2: 8  
[1] 2 3 4 5 6 7 8

{{< /highlight >}}

A continuación, verifiquemos que podemos usar la abreviatura 2: 8 como una forma de extraer los elementos del segundo al octavo de sales.by.months: 

{{< highlight R >}}
> ventas por mes [2: 8]  
[1] 100 200 50 0 0 0 0

{{< /highlight >}}

Así que eso es genial.
 
### Indexación lógica
En este punto, puedo presentar una herramienta extremadamente útil llamada indexación lógica. En la última sección, creé un vector lógico any.sales .this.month , cuyos elementos son VERDADEROS para cualquier mes en el que vendí al menos un libro, y FALSO para todos los demás. Sin embargo, esa gran lista de VERDADEROS y FALSOS es un poco difícil de leer, así que lo que me gustaría hacer es que R seleccione los nombres de los meses por los que vendí libros. Anteriormente, creé un vector de meses que contiene los nombres de cada uno de los meses. Aquí es donde la indexación lógica es útil. Lo que necesito hacer es esto: 

{{< highlight R >}}
> meses [ ventas.por.mes > 0]  
[1] "febrero" "marzo" "abril" "mayo"

{{< /highlight >}}

Para comprender lo que está sucediendo aquí, es útil notar que sales.by.month > 0 es la misma expresión lógica que usamos para crear el vector any.sales.this.month en la última sección. De hecho, podría haber hecho esto: 

{{< highlight R >}}
> meses [ cualquier.ventas.este . mes ]  
[1] "febrero" "marzo" "abril" "mayo"

{{< /highlight >}}

y obtuve exactamente el mismo resultado. Para averiguar qué elementos de meses incluir en la salida, lo que hace R es ver si el elemento correspondiente en any.sales .this.month es VERDADERO. Por lo tanto, dado que el elemento 1 de cualquier.ventas .este . mes es FALSO, R no incluye "enero" como parte de la salida; pero como el elemento 2 de any.sales.this.month es TRUE, R incluye "febrero" en la salida. Tenga en cuenta que no hay ninguna razón por la que no pueda utilizar el mismo truco para encontrar las cifras de ventas reales de esos meses. El comando para hacer eso sería simplemente este: 

{{< highlight R >}}
> ventas por mes [ ventas por mes > 0]  
[1] 100 200 50 25

{{< /highlight >}}

De hecho, podemos hacer lo mismo con el texto. He aquí un ejemplo. Supongamos que, para continuar con la saga de las ventas de libros de texto, luego descubro que la librería solo tenía existencias suficientes para algunos meses del año. Me dicen que a principios del año que tenían las poblaciones de "alto", que luego se redujo a niveles "bajos", y de hecho durante un mes que estaban "fuera" de copias del libro durante un tiempo antes de que fueran capaces de reponer ellas . Por lo tanto, podría tener una variable llamada stock.levels que se ve así: 

{{< highlight R >}}
> niveles de existencias  
[1] "alto" "alto" "bajo" "fuera" "fuera" "alto" "alto" "alto" "alto" "alto" "alto"  
[12] "alto"

{{< /highlight >}}

Por lo tanto, si quiero saber los meses en los que la librería estuvo fuera de mi libro, podría aplicar el truco de indexación lógica , pero con el vector de caracteres stock.levels , así: 

{{< highlight R >}}
> meses [ stock.levels == "out"]  
[1] "abril" "mayo"

{{< /highlight >}}

Alternativamente, si quiero saber cuándo la librería tenía pocas copias o no tenía copias, podría hacer esto: 

{{< highlight R >}}
> meses [ stock.levels == "out" | stock.levels == "bajo"]  
[1] "marzo" "abril" "mayo"

{{< /highlight >}}

o esto

{{< highlight R >}}
> meses [ stock.levels ! = "high"]  
[1] "marzo" "abril" "mayo"

{{< /highlight >}}

De cualquier manera, obtengo la respuesta que quiero.
En este punto, espero que pueda ver por qué la indexación lógica es tan útil. Es una forma muy básica pero muy poderosa de manipular datos. Hablaremos mucho más sobre cómo manipular los datos en el Capítulo 7, ya que es una habilidad crítica para la investigación del mundo real que a menudo se pasa por alto en las clases de introducción a los métodos de investigación (o al menos, esa ha sido mi experiencia). Se necesita un poco de práctica para sentirse completamente cómodo usando la indexación lógica, por lo que es una buena idea jugar con este tipo de comandos. Intente crear algunas variables diferentes por su cuenta, y luego hágase preguntas como "¿cómo hago para que R escupe todos los elementos que son [bla]]". La práctica hace la perfección, y solo practicando la indexación lógica perfeccionará el arte de gritar insultos frustrados en su computadora. 

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Salir de R
Hay una última cosa que debería cubrir en este capítulo: cómo dejar de fumar R. Cuando digo esto, no estoy tratando de dar a entender que R es algún tipo de adición patológica y que necesita llamar a R QuitLine o usar parches para controlar los antojos (aunque ciertamente podría argumentar que hay algo seriamente patológico en ser adicto a R). Solo me refiero a cómo salir del programa. Suponiendo que está ejecutando R de la manera habitual (es decir, a través de Rstudio o la GUI predeterminada en una computadora con Windows o Mac), entonces puede cerrar la aplicación de la manera normal. Sin embargo, R también tiene una función, llamada q ( ) que puede usar para salir, que es bastante útil si está ejecutando R en una ventana de terminal.  
Independientemente del método que utilice para salir de R, cuando lo haga por primera vez, probablemente R le preguntará si desea guardar la “imagen del espacio de trabajo”. Hablaremos mucho más sobre cargar y guardar datos en la Sección 4.5, pero pensé que sería mejor que cubrimos esto rápidamente, de lo contrario, se molestará cuando cierre R al final del capítulo. Si está utilizando Rstudio , verá un cuadro de diálogo que se parece al que se muestra en la Figura 3.5. Si está utilizando una interfaz basada en texto , verá esto: 

{{< highlight R >}}
> q ( )

{{< /highlight >}}

¿Guardar imagen del espacio de trabajo? [s / n / c]:  
La parte y / n / c aquí es la abreviatura de "sí / no / cancelar". Escriba y si desea guardar, n si no lo hace y c si ha cambiado de opinión y no quiere salir después de todo. 

¿Qué significa esto realmente? Lo que sucede es que R quiere saber si desea guardar todas esas variables que ha estado creando, para poder usarlas más tarde. Parece una gran idea, por lo que es muy tentador escribir y o hacer clic en el botón "Guardar". Para ser honesto, aunque, muy rara vez hago esto, y que tipo de me molesta un poco ... lo que realmente está pidiendo R es si lo desea almacenar estas variables en un archivo de datos “por defecto”, que automáticamente se recarga para usted la próxima vez que abra R. Y, francamente, si quisiera guardar las variables, ya las habría guardado antes de intentar salir. No solo eso, los habría guardado en una ubicación de mi elección, para poder encontrarlos nuevamente más tarde. Así que personalmente nunca me preocupo por esto.

De hecho, cada vez que instalo R en una máquina nueva, una de las primeras cosas que hago es cambiar la configuración para que nunca vuelva a preguntarme. Puede hacer esto en Rstudio muy fácilmente: use el sistema de menús para encontrar la opción Rstudio ; el cuadro de diálogo que aparece le dará una opción para decirle a R que nunca más se queje de esto (vea la Figura 3.6). En una Mac, puede abrir esta ventana yendo al menú " Rstudio " y seleccionando "Preferencias". En una máquina con Windows, vaya al menú "Herramientas" y seleccione "Opciones globales". En la pestaña "General", verá una opción que dice "Guardar espacio de trabajo en. Rdata a la salida ”. De forma predeterminada, se establece en "preguntar". Si desea que R deje de preguntar, cámbielo a "nunca". 

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Resumen
Cada libro que trata de presentar ideas básicas de programación a los principiantes tiene que cubrir aproximadamente los mismos temas y aproximadamente en el mismo orden. El mío no es una excepción, por lo que en la gran tradición de hacerlo de la misma manera que todos los demás lo hicieron, este capítulo cubrió los siguientes temas:   

- Empezando. Descargamos e instalamos R y Rstudio (Sección 3.1).

- Comandos básicos. Hablamos un poco sobre la lógica de cómo funciona R y, en particular, sobre cómo escribir comandos en la consola R (Sección 3.2), y al hacerlo aprendimos cómo realizar cálculos básicos usando los operadores aritméticos +, -, *, / y ^ . (Sección 3.3) 

- Introducción a las funciones. Vimos varias funciones diferentes, tres que se utilizan para realizar cálculos numéricos (sqrt (), abs (), round (); Sección 3.5), una que se aplica al texto ( nchar (); Sección 3.8.1) y una que funciona con cualquier variable (length (); Sección 3.7.5). Al hacerlo, hablamos un poco sobre cómo funcionan los nombres de los argumentos y aprendimos sobre los valores predeterminados para los argumentos. (Sección 3.5.1)

- Introducción a las variables. Aprendimos la idea básica detrás de las variables y cómo asignar valores a las variables usando el operador de asignación <- (Sección 3.4). También aprendimos cómo crear vectores usando la función de combinación c ( ). (Sección 3.7)

- Tipos de datos. Aprendió la distinción entre datos numéricos, de caracteres y lógicos; incluyendo los conceptos básicos de cómo ingresar y usar cada uno de ellos. (Secciones 3.4 a 3.9) 

- Operaciones lógicas. Aprendí a usar los operadores lógicos = = ,! =, <,>, <=, =>,! , & y | . (Sección 3.9). Y aprendí a usar la indexación lógica. (Sección 3.10) 

Todavía no hemos llegado a nada que se parezca a un "conjunto de datos", por supuesto. Quizás el próximo Capítulo nos acerque un poco más...


---
<p style="text-align:right;font-size:80%;">
Escrito por Navarro, Danielle; traducido por García-Mendívil, Helio A.
</p>