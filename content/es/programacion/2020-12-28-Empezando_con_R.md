---
title: "Capítulo 1: Empezando con R"
date: 2020-12-28T16:46:00+09:00
description: "En este capítulo discutiré cómo empezar a usar R. Hablaré brevemente sobre cómo descargar e instalar R, pero la mayor parte del capítulo se centrará en que empiece a escribir comandos R."
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
categories:
- Programación
image: images/learning/cap_01.png
---

<style>
body {
text-align: justify}
</style>


En este capítulo discutiré cómo empezar a usar R. Hablaré brevemente sobre cómo descargar e instalar R, pero la mayor parte del capítulo se centrará en que empiece a escribir comandos R. Nuestro objetivo en este capítulo no es aprender ningún concepto estadístico: solo estamos tratando de aprender los conceptos básicos de cómo funciona R y sentirnos cómodos interactuando con el sistema. Para hacer esto, pasaremos un poco de tiempo usando R como una simple calculadora, ya que eso es lo más fácil de hacer con R. Al hacerlo, obtendrá una idea de cómo es trabajar en R. A partir de ahí, presentaré algunas ideas de programación muy básicas: en particular, hablaré sobre la idea de definir variables para almacenar información y algunas cosas que puede hacer con estas variables.

Sin embargo, antes de entrar en detalles, vale la pena hablar un poco sobre por qué es posible que desee usar R. Dado que estás leyendo esto, probablemente tengas tus propias razones. Sin embargo, si esas razones son "porque eso es lo que usa mi clase de estadísticas", podría valer la pena explicar un poco por qué su profesor ha elegido usar R para la clase. Por supuesto, realmente no sé por qué otras personas eligen R, así que realmente estoy hablando de por qué lo uso.

- Es algo obvio, pero vale la pena decirlo de todos modos: hacer sus estadísticas en una computadora es más rápido, más fácil y más poderoso que hacer estadísticas a mano. Las computadoras sobresalen en tareas repetitivas sin sentido, y muchos cálculos estadísticos son tanto inconscientes como repetitivos. Para la mayoría de las personas, la única razón para hacer cálculos estadísticos con lápiz y papel es con fines de aprendizaje. En mi clase, de vez en cuando sugiero hacer algunos cálculos de esa manera, pero el único valor real es pedagógico. Le ayuda a tener una "idea" de las estadísticas para hacer algunos cálculos usted mismo, por lo que vale la pena hacerlo una vez. ¡Pero solo una vez!  

- Hacer estadísticas en una hoja de cálculo (por ejemplo, Microsoft Excel) es generalmente una mala idea a largo plazo. Aunque es probable que muchas personas se sientan más familiarizadas con ellos, las hojas de cálculo son muy limitadas en términos de los análisis que le permiten hacer. Si adquiere el hábito de intentar realizar su análisis de datos de la vida real utilizando hojas de cálculo, entonces se ha metido en un agujero muy profundo.  

- Evitar el software propietario es una muy buena idea. Hay muchos paquetes comerciales que puedes comprar, algunos de los cuales me gustan y otros no. Suelen tener un aspecto muy brillante y, en general, muy potentes (mucho más potentes que las hojas de cálculo). Sin embargo, también son muy caros: por lo general, la empresa vende "versiones para estudiantes" (versiones paralizadas de lo real) a muy bajo precio; venden “versiones educativas” con toda la potencia a un precio que me hace estremecer; y venden licencias comerciales a un precio asombrosamente alto. El modelo de negocio aquí es absorberlo durante sus días de estudiante y luego dejarlo dependiente de sus herramientas cuando salga al mundo real. Es difícil culparlos por intentarlo, pero personalmente no estoy a favor de desembolsar miles de dólares si puedo evitarlo. Y puede evitarlo: si utiliza paquetes como R que son de código abierto y gratuitos, nunca se verá atrapado en el pago de tarifas de licencia exorbitantes.  

- Algo que quizás no aprecie ahora, pero que le encantará más adelante si hace algo que implique el análisis de datos, es el hecho de que R es altamente extensible. Cuando descarga e instala R, obtiene todos los "paquetes" básicos, y estos son muy poderosos por sí mismos. Sin embargo, debido a que R es tan abierto y tan ampliamente utilizado, se ha convertido en una especie de herramienta estándar en estadística, por lo que mucha gente escribe sus propios paquetes que amplían el sistema. Y estos también están disponibles gratuitamente. Una de las consecuencias de esto, me he dado cuenta, es que si abres un libro de texto avanzado (es decir, uno reciente) en lugar de libros de texto introductorios, es que muchos de ellos usan R. En otras palabras, si aprendes cómo hacer sus estadísticas básicas en R, entonces está mucho más cerca de poder utilizar los métodos más avanzados de lo que estaría si hubiera comenzado con un sistema "más simple": así que si quiere convertirse en Un verdadero experto en análisis de datos psicológicos, aprender R es un muy buen uso de su tiempo. 

- Relacionado con el punto anterior: R es un lenguaje de programación real. A medida que mejora en el uso de R para el análisis de datos, también está aprendiendo a programar. Para algunas personas, esto puede parecer algo malo, pero en realidad, la programación es una habilidad de investigación central en muchas de las ciencias sociales y del comportamiento . Piense en cuántas encuestas y experimentos se realizan en línea o se presentan en computadoras. Piense en todos esos entornos sociales en línea que podría interesarle estudiar; y tal vez recopilar datos de forma automatizada. Piense en sistemas de inteligencia artificial, visión por computadora y reconocimiento de voz. Si alguna de estas son cosas en las que cree que le gustaría participar, es decir, como alguien que "investiga en psicología", necesitará saber un poco de programación. Y si aún no sabe cómo programar, entonces aprender a hacer estadísticas usando R es una buena manera de comenzar.

Esas son las principales razones por las que uso R. No está exento de defectos: no es fácil de aprender y tiene algunas peculiaridades muy molestas con las que todos estamos bastante atrapados, pero en general creo que las fortalezas superan la debilidad; más que cualquier otra opción que haya encontrado hasta ahora.

## Instalación de R
De acuerdo, basta con el argumento de venta. Empecemos. Al igual que con cualquier software, R debe instalarse en una "computadora", que es una caja mágica que hace cosas interesantes y entrega ponis gratis. O algo por el estilo: puedo estar confundiendo las computadoras con las campañas de marketing del iPad. De todos modos, R se distribuye gratuitamente en línea y puede descargarlo desde la página de inicio de R, que es:

http://cran.r-project.org/

En la parte superior de la página, bajo el título "Descargar e instalar R", verá enlaces separados para usuarios de Windows, usuarios de Mac y usuarios de Linux. Si sigue el enlace correspondiente, verá que las instrucciones en línea se explican por sí mismas, pero lo guiaré a través de la instalación de todos modos. En el momento de escribir este artículo, la versión actual de R es 3.0.2 ("Frisbee Sailing"), pero normalmente publican actualizaciones cada seis meses, por lo que probablemente tendrá una versión más nueva.

### Instalación de R en una computadora con Windows
La página de inicio de CRAN cambia de vez en cuando y, francamente, no es particularmente bonita ni está tan bien diseñada. Pero no es difícil encontrar lo que busca. En general , encontrará un enlace en la parte superior de la página con el texto "Descargar R para Windows". Si hace clic en eso, lo llevará a una página que le ofrece algunas opciones. Nuevamente, en la parte superior de la página se le indicará que haga clic en un enlace que dice que haga clic aquí si está instalando R por primera vez. Probablemente eso es lo que quieres. Esto lo llevará a una página que tiene un vínculo destacado en la parte superior llamado "Descargar R 3.0.2 para Windows". Ese es el que quieres. Haga clic en eso y su navegador debería comenzar a descargar un archivo llamado R-3.0.2-win.exe, o cualquier número de versión equivalente para cuando lea esto. El archivo de la versión 3.0.2 tiene un tamaño aproximado de 54 MB, por lo que puede llevar algún tiempo dependiendo de la velocidad de su conexión a Internet. Una vez que haya descargado el archivo, haga doble clic para instalarlo. Al igual que con cualquier software que descargue en línea, Windows le hará algunas preguntas sobre si confía en el archivo, etc. Después de hacer clic en ellos, le preguntará dónde desea instalarlo y qué componentes desea instalar. Los valores predeterminados deberían estar bien para la mayoría de las personas, así que nuevamente, simplemente haga clic. Una vez hecho todo esto, debería tener R instalado en su sistema. Puede acceder a él desde el menú Inicio o desde el escritorio si le pidió que agregue un acceso directo allí. Ahora puede abrir R de la forma habitual si lo desea, pero lo que voy a sugerir es que, en lugar de hacerlo, ahora debería instalar Rstudio.

### Instalación de R en una Mac
Al hacer clic en el enlace de Mac OS X, debería encontrarse en una página con el título "R para Mac OS X". La gran mayoría de los usuarios de Mac tendrán una versión bastante reciente del sistema operativo: siempre que esté ejecutando Mac OS X 10.6 (Snow Leopard) o superior, estará bien. Hay un enlace bastante destacado en la página llamado "R-3.0.2.pkg", que es el que desea. Haga clic en ese enlace y comenzará a descargar el archivo de instalación, que (como era de esperar) se llama R-3.0.2.pkg. Tiene un tamaño aproximado de 61 MB, por lo que la descarga puede tardar un poco en conexiones a Internet más lentas.
Una vez que haya descargado R-3.0.2.pkg, todo lo que necesita hacer es abrirlo haciendo doble clic en el archivo del paquete. La instalación debería realizarse sin problemas a partir de ahí: simplemente siga todas las instrucciones tal como lo hace normalmente cuando instala algo. Una vez que haya terminado, encontrará un archivo llamado R.app en la carpeta Aplicaciones. Ahora puede abrir R de la forma habitual 4 si lo desea, pero lo que voy a sugerir es que en lugar de hacer eso, ahora debería instalar Rstudio.

### Instalación de R en una computadora Linux
Si está logrando ejecutar con éxito una caja de Linux, independientemente de la distribución, entonces debería encontrar las instrucciones en el sitio web lo suficientemente fáciles. Puede compilar R desde la fuente usted mismo si lo desea, o instalarlo a través de su sistema de administración de paquetes, que probablemente tendrá R en él. Alternativamente, el sitio CRAN tiene binarios precompilados para Debian, Red Hat, Suse y Ubuntu y tiene instrucciones separadas para cada uno. Una vez que tenga R instalado, puede ejecutarlo desde la línea de comando simplemente escribiendo R. Sin embargo, si siente envidia de los usuarios de Windows y Mac por sus elegantes GUI, también puede descargar Rstudio.

### Descarga e instalación de Rstudio
Bien, independientemente del sistema operativo que estés usando, lo último que te dije que hicieras es descargar Rstudio . Para comprender por qué he sugerido esto, debe comprender un poco más sobre R en sí. El término R realmente no se refiere a una aplicación específica en su computadora. Más bien, se refiere al lenguaje estadístico subyacente. Puede utilizar este idioma a través de muchas aplicaciones diferentes. Cuando instala R inicialmente, viene con una aplicación que le permite hacer esto: es la aplicación R.exe en una máquina con Windows y la aplicación R.app en una Mac. Pero esa no es la única forma de hacerlo. Hay muchas aplicaciones diferentes que puedes usar que te permitirán interactuar con R. Una de ellas se llama Rstudio, y es la que te voy a sugerir que uses. Rstudio proporciona una interfaz limpia y profesional para R con la que me resulta mucho más agradable trabajar que los valores predeterminados de Windows o Mac. Al igual que R, Rstudio es un software gratuito: puedes encontrar todos los detalles en su página web. Mientras tanto, puedes descargarlo aquí:

http://www.rstudio.org/ 

Cuando visite el sitio web de Rstudio , probablemente se sorprenderá de lo más limpio y simple que es el sitio web de CRAN, 5 y lo obvio que es lo que debe hacer: haga clic en el gran botón verde que dice "Descargar".
Cuando haga clic en el botón de descarga en la página de inicio, le pedirá que elija si desea la versión de escritorio o la versión del servidor. Quieres la versión de escritorio. Después de elegir la versión de escritorio, lo llevará a una página (http://www.rstudio.org/download/desktop) que muestra varias descargas posibles: hay una diferente para cada sistema operativo. Sin embargo, la amable gente de Rstudio ha diseñado la página web para que recomiende automáticamente la descarga más apropiada para su computadora. Haga clic en el enlace correspondiente y el archivo de instalación de Rstudio comenzará a descargarse.
Una vez que haya terminado de descargar, abra el archivo de instalación de la forma habitual para instalar Rstudio. Una vez finalizada la instalación, puede iniciar R abriendo Rstudio. No necesita abrir R.app o R.exe para acceder a R. Rstudio se encargará de eso por usted. Para ilustrar cómo se ve Rstudio , la Figura 3.1 muestra una captura de pantalla de una sesión de R en progreso. En esta captura de pantalla, puede ver que se está ejecutando en una Mac, pero se ve casi idéntica sin importar el sistema operativo que tenga. La versión de Windows se parece más a una aplicación de Windows (por ejemplo, los menús están adjuntos a la ventana de la aplicación y la combinación de colores es ligeramente diferente), pero es más o menos idéntica. Hay algunas diferencias menores en la ubicación de las cosas en los menús (las señalaré a medida que avanzamos) y en las teclas de acceso directo, porque Rstudio está tratando de "sentirse" como una aplicación Mac adecuada o una aplicación Windows adecuada, y esto significa que tiene que cambiar un poco su comportamiento dependiendo de la computadora en la que se esté ejecutando. Aun así, estas diferencias son muy pequeñas: comencé usando la versión para Mac de Rstudio y luego comencé a usar la versión de Windows también para escribir estas notas.
El único "defecto" que he encontrado con Rstudio es que, al momento de escribir este artículo, todavía es un trabajo en progreso. La versión actual que escribo es 0.98.501, lo que significa que está en prueba beta (la versión oficial es la 1.0). Aun así, creo que la versión beta de Rstudio ofrece una mejor experiencia de usuario que cualquier otra cosa que haya probado: realmente es la mejor opción disponible en mi opinión. El "problema" es que siguen mejorando. Las nuevas funciones siguen apareciendo en los lanzamientos más recientes, por lo que es muy probable que para cuando lea este libro haya una versión que tenga algunas cosas realmente interesantes que no estaban en la versión que estoy usando ahora.

### Arrancando R
De una forma u otra, independientemente del sistema operativo que esté usando e independientemente de si está usando Rstudio , o la GUI predeterminada, o incluso la línea de comandos, es hora de abrir R y comenzar. Cuando hagas eso, lo primero que verás (suponiendo que estés mirando la consola R) es una gran cantidad de texto que no tiene mucho sentido. Debería verse algo como esto:
La mayor parte de este texto carece de interés y, al hacer análisis de datos reales , nunca le prestará mucha atención. La parte importante es esta ...

> \>

... que tiene un cursor intermitente al lado. Ese es el símbolo del sistema. Cuando vea esto, significa que R está esperando pacientemente a que haga algo.

## Escribir comandos en la consola R
Una de las cosas más fáciles que puede hacer con R es usarlo como una calculadora simple, por lo que es un buen lugar para comenzar. Por ejemplo, intente escribir 10 + 20 y presione enter. 6 Cuando hace esto, ha ingresado un comando y R "ejecutará" ese comando. Lo que ve en la pantalla ahora será esto:


> \>10 + 20  
[1] 30

No hay muchas sorpresas en este extracto. Pero hay algunas cosas de las que vale la pena hablar, incluso con un ejemplo tan simple. En primer lugar, es importante que comprenda cómo leer el extracto. En este ejemplo, lo que escribí fue la parte 10 + 20. No escribí el símbolo >: es solo el símbolo del sistema R y no es parte del comando real. Y tampoco escribí la parte [1] 30. Eso es lo que imprimió R en respuesta a mi comando. En segundo lugar, es importante comprender cómo se formatea la salida. Obviamente, la respuesta correcta a la suma 10 + 20 es 30, y no es sorprendente que R lo haya impreso como parte de su respuesta. Pero también está impresa esta parte [1], que probablemente no tenga mucho sentido para ti en este momento. Vas a ver eso mucho. Hablaré sobre lo que esto significa con un poco más de detalle más adelante, pero por ahora puedes pensar en [1] 30 como si R estuviera diciendo “la respuesta a la primera pregunta que hiciste es 30”. Eso no es del todo cierto, pero está lo suficientemente cerca por ahora. Y en cualquier caso, no es muy interesante en este momento: solo le pedimos a R que calcule una cosa, por lo que obviamente solo hay una respuesta impresa en la pantalla. Más adelante esto cambiará y la parte [1] comenzará a tener un poco más de sentido. Por ahora, simplemente no quiero que se confunda o se preocupe.
 
### Tenga mucho cuidado de evitar errores tipográficos
Antes de pasar a hablar sobre otros tipos de cálculos que podemos hacer con R, hay algunas otras cosas que quiero señalar. Lo primero es que, aunque R es un buen software, sigue siendo software. Es bastante estúpido y, como es estúpido, no puede manejar errores tipográficos. Se da por sentado que tu intención era escribir exactamente lo que escribiste. Por ejemplo, suponga que olvidó presionar la tecla Mayús al intentar escribir + y , como resultado, su comando terminó siendo 10 = 20 en lugar de 10 + 20. Esto es lo que sucede:


> \> 10 = 20  
 Error en 10 = 20: no válido ( do_set ) del lado izquierdo de la asignación

Lo que sucedió aquí es que R ha intentado interpretar 10 = 20 como un comando y escupe un mensaje de error porque el comando no tiene ningún sentido. Cuando un humano mira esto, y luego mira su teclado y ve que + y = están en la misma tecla, es bastante obvio que el comando fue un error tipográfico. Pero R no sabe esto, así que se enoja. Y, si lo miras desde su perspectiva, esto tiene sentido. Todo lo que R "sabe" es que 10 es un número legítimo, 20 es un número legítimo y = también es una parte legítima del lenguaje. En otras palabras, desde su perspectiva, esto realmente parece que el usuario quería escribir 10 = 20, ya que todas las partes individuales de esa declaración son legítimas y es demasiado estúpido para darse cuenta de que probablemente sea un error tipográfico. Por lo tanto, R confía en que esto es exactamente lo que quisiste decir ... solo “descubre” que el comando es una tontería cuando intenta seguir tus instrucciones, con errores tipográficos y todo. Y luego lloriquea y escupe un error.
Aún más sutil es el hecho de que algunos errores tipográficos no producirán ningún error, porque resulta que corresponden a comandos R "bien formados". Por ejemplo, suponga que no solo me olvidé de presionar la tecla de mayúsculas al intentar escribir 10 + 20, sino que también logré presionar la tecla junto a la que quería decir. El error tipográfico resultante produciría el comando 10 - 20. Claramente, R no tiene forma de saber que pretendías sumar 20 a 10, no restar 20 de 10, así que lo que sucede esta vez es esto:

> \>10 - 20  
[1] -10


En este caso, R produce la respuesta correcta, pero a la pregunta equivocada.
Hasta cierto punto, estoy diciendo lo obvio aquí, pero es importante. Las personas que escribieron R son inteligentes. Tú, el usuario, eres inteligente. Pero R en sí es tonto. Y debido a que es tonto, tiene que ser obediente sin pensar. Hace exactamente lo que le pide que haga. No hay equivalente a "autocorrección" en R, y por una buena razón. Cuando se hacen cosas avanzadas, e incluso las estadísticas más simples son bastante avanzadas en muchos sentidos, es peligroso permitir que un autómata sin sentido como R intente anular al usuario humano. Pero debido a esto, es su responsabilidad tener cuidado. Asegúrese siempre de escribir exactamente lo que quiere decir. Cuando se trata de computadoras, no es suficiente escribir “aproximadamente” lo correcto. En general, debes ser absolutamente preciso en lo que le dices a R ... como todas las máquinas, es demasiado estúpido para ser algo más que absurdamente literal en su interpretación.
 
### R es (un poco) flexible con espaciado
Por supuesto, ahora que he sido tan tenso acerca de la importancia de ser siempre preciso, debo señalar que hay algunas excepciones. O, más exactamente, hay algunas situaciones en las que R muestra un poco más de flexibilidad de lo que sugiere mi descripción anterior. Lo primero que R es lo suficientemente inteligente como para hacer es ignorar el espaciado redundante. Lo que quiero decir con esto es que, cuando escribí 10 + 20 antes, igualmente podría haber hecho esto

> \> 10 +    20  
[1] 30

o esto

> \> 10 + 20  
[1] 30

y obtendría exactamente la misma respuesta. Sin embargo, eso no significa que pueda insertar espacios en cualquier lugar antiguo. Cuando miramos la documentación de inicio en la Sección 3.1.5, sugirió que podría escribir citation ( ) para obtener información sobre cómo citar R. Si lo hago ...

> \> citation ( )  
To cite R in publications use:  
  R Core Team (2013). R: A language and environment  
  for statistical computing. R Foundation for  
  Statistical Computing, Vienna, Austria. URL  
  http://www.R-project.org/.  
  BLAH BLAH BLAH  
We have invested a lot of time and effort in creating  
R, please cite it when using it for data analysis. See  
also ?citation("pkgname")? for citing R packages
 
... me dice que cite el manual de R (R Core Team, 2013). Obviamente, la parte BLAH BLAH BLAH no es en realidad parte de lo que imprime R: cuando ves eso significa que he eliminado algunas partes de la salida que no creo que sean muy interesantes o relevantes. Haré mucho eso. De todos modos, volviendo a mi punto original, veamos qué sucede cuando intento cambiar el espaciado. Si inserto espacios entre la palabra y el paréntesis, o dentro de los paréntesis, entonces todo está bien. Es decir, cualquiera de estos dos comandos

> \> citation ()  
\> citation (  )

producirá exactamente la misma respuesta. Sin embargo, lo que no puedo hacer es insertar espacios en el medio de la palabra. Si trato de hacer esto, R se enoja:

> \> citat ion()   
Error: símbolo inesperado en " citat ion"

A lo largo de este libro, variaré un poco la forma en que utilizo el espaciado, solo para darle una idea de las diferentes formas en que se puede usar el espaciado. Sin embargo, intentaré no hacerlo demasiado, ya que generalmente se considera una buena práctica ser consistente en la forma en que formatea los comandos.
 
### R a veces puede decir que aún no has terminado (pero no a menudo)
Una cosa más que debo señalar. Si presiona enter en una situación en la que es "obvio" para R que no ha terminado de escribir el comando, R es lo suficientemente inteligente como para seguir esperando. Por ejemplo, si escribe 10 + y luego presiona Intro, incluso R es lo suficientemente inteligente como para darse cuenta de que probablemente quería ingresar otro número. Así que esto es lo que sucede:

> \> 10+  
+

y hay un cursor parpadeante junto al signo más. Lo que esto significa es que R todavía está esperando que termines. “Piensa” que todavía estás escribiendo tu comando, por lo que aún no ha intentado ejecutarlo. En otras palabras, este signo más es en realidad otro símbolo del sistema. Es diferente del habitual (es decir, el símbolo >) para recordarle que R va a "agregar" lo que escriba ahora a lo que escribió la última vez. Por ejemplo, si sigo escribiendo 3 y presiono enter, lo que obtengo es esto: 

> \> 10+  
+ 20  
[1] 30

Y en lo que respecta a R, esto es exactamente lo mismo que si hubiera escrito 10 + 20. De manera similar, considere el comando citation ( ) del que hablamos en la sección anterior. Suponga que presiona enter después de escribir la cita (. Una vez más, R es lo suficientemente inteligente como para darse cuenta de que debe haber más por venir, ya que debe agregar el carácter ), por lo que espera. Incluso puedo presionar enter varias veces y seguirá esperando:

> \> cita (  
+  
+  
+)

Haré mucho uso de esto en este libro. Muchos de los comandos que tendremos que escribir son bastante largos y visualmente son un poco más fáciles de leer si los divido en varias líneas. Si comienza a hacer esto usted mismo, eventualmente se meterá en problemas (nos pasa a todos). Tal vez empiece a escribir un comando y luego se dé cuenta de que ha cometido un error. Por ejemplo,

> \> citblation (  
+  
+

Probablemente prefieras que R no intente ejecutar este comando, ¿verdad? Si desea salir de esta situación, simplemente presione la tecla 'Esc'. R lo regresará al símbolo del sistema normal (es decir, >) sin intentar ejecutar el comando fallido.  
Dicho esto, no es frecuente que R sea lo suficientemente inteligente como para decir que vendrán más. Por ejemplo, de la misma manera que no puedo agregar un espacio en el medio de una palabra, tampoco puedo presionar Enter en el medio de una palabra. Si presiono enter después de escribir citat , aparece un error, porque R cree que estoy interesado en un "objeto" llamado citat y no puedo encontrarlo:

> \> citat  
Error: no se encontró el objeto ' citat '

¿Qué pasa si escribí una cita y presiono enter? En este caso obtenemos algo muy extraño, algo que definitivamente no queremos, al menos en esta etapa. Esto es lo que sucede:

> \> cita  
función (paquete = "base", lib.loc = NULL, auto = NULL)  
{  
dir <- system.file (paquete = paquete, lib.loc = lib.loc )  
si ( dir == "")  
stop ( gettextf ("paquete '% s' no encontrado", paquete), dominio = NA)  
BLA, BLA, BLA

donde el BLAH BLAH BLAH continúa durante bastante tiempo, y aún no sabes lo suficiente R para entender lo que realmente significa todo este galimatías. Esta salida incomprensible puede resultar bastante intimidante para los usuarios novatos y, lamentablemente , es muy fácil olvidarse de escribir los paréntesis; por lo que es casi seguro que lo hará por accidente. No entre en pánico cuando esto suceda. Simplemente ignore el galimatías. A medida que adquiera más experiencia, este galimatías comenzará a tener sentido y le resultará muy útil imprimirlo. Pero por ahora, intente recordar agregar los paréntesis al escribir sus comandos.

Tabla 3.1: Operaciones aritméticas básicas en R. Estos cinco operadores se usan con mucha frecuencia a lo largo del texto, por lo que es importante familiarizarse con ellos desde el principio. También hay otros, de los que hablaré en el capítulo 7.
 
## Hacer cálculos simples con R
Bien, ahora que hemos discutido algunos de los tediosos detalles asociados con la escritura de comandos R, volvamos a aprender cómo usar el software estadístico más poderoso del mundo como una calculadora de $2. Hasta ahora, todo lo que sabemos hacer es sumar. Claramente, una calculadora que solo hiciera sumas sería un poco estúpida, así que debería decirte cómo realizar otros cálculos simples usando R. Pero primero, algo más de terminología. La suma es un ejemplo de una "operación" que puede realizar (específicamente, una operación aritmética), y el operador que la realiza es +. Para las personas con experiencia en programación o matemáticas, esta terminología probablemente se sienta bastante natural, pero para otras personas puede parecer que estoy tratando de hacer que algo muy simple (suma) suene más complicado de lo que es (llamándolo una operación aritmética). Hasta cierto punto, eso es cierto: si la suma fuera la única operación que nos interesa, sería un poco tonto introducir toda esta terminología adicional. Sin embargo, a medida que avancemos, comenzaremos a usar más y más tipos diferentes de operaciones, por lo que probablemente sea una buena idea aclarar el lenguaje ahora, ¡mientras seguimos hablando de conceptos muy familiares como la suma!
 
### Sumar, restar, multiplicar y dividir
Entonces, ahora que tenemos la terminología, aprendamos a realizar algunas operaciones aritméticas en R. Para ello, la Tabla 3.1 enumera los operadores que corresponden a la aritmética básica que aprendimos en la escuela primaria: suma, resta, multiplicación y división. Como puede ver, R usa símbolos bastante estándar para denotar cada una de las diferentes operaciones que podría querer realizar: la suma se realiza usando el operador +, la resta se realiza mediante el operador -, y así sucesivamente. Entonces, si quisiera averiguar qué es 57 por 61 (¿y quién no?), Puedo usar R en lugar de una calculadora, así:

> \> 57 * 61  
[1] 3477

Eso es útil.

### Tomando poderes
Las primeras cuatro operaciones enumeradas en la tabla 3.1 son cosas que todos aprendimos en la escuela primaria, pero no son las únicas operaciones aritméticas integradas en R. Hay otras tres operaciones aritméticas que probablemente debería mencionar: tomar poderes, hacer división de enteros y calcular un módulo. De los tres, el único que tiene una importancia real para los propósitos de este libro es tomar poderes, así que discutiré ese uno aquí: los otros dos se analizan en el Capítulo 7.
Para aquellos de ustedes que todavía pueden recordar sus matemáticas de la escuela secundaria , esto debería resultarles familiar. Pero para algunas personas las matemáticas de la escuela secundaria fueron hace mucho tiempo, y otros de nosotros no escuchamos con atención en la escuela secundaria. No es complicado. Como estoy seguro de que todos probablemente recordarán el momento en que lean esto, el acto de multiplicar un número x por sí mismo n veces se llama “elevar x a la enésima potencia”. Matemáticamente, esto se escribe como x n. Algunos valores de n tienen nombres especiales: en particular, x 2 se llama x al cuadrado, y x 3 se llama x al cubo. Entonces, la cuarta potencia de 5 se calcula así:
Una forma en la que podríamos calcular 5 ^ 4 en R sería escribir la multiplicación completa como se muestra en la ecuación anterior. Es decir, podríamos hacer esto

> \> 5 * 5 * 5 * 5  
[1] 625

pero parece un poco tedioso. De hecho, sería muy molesto si quisiera calcular 5 15, ya que el comando terminaría siendo bastante largo. Por lo tanto, para hacernos la vida más fácil, utilizamos el operador de energía en su lugar. Cuando hacemos eso, nuestro comando para calcular 5 4 es así:

> \> 5 ^ 4  
[1] 625

Más fácil.
 
### Realización de cálculos en el orden correcto
Bueno. En este punto, ya sabe cómo tomar una de las piezas de software estadístico más poderosas del mundo y usarla como una calculadora de 2. Y como beneficio adicional, ha aprendido algunos conceptos de programación muy básicos. Eso no es nada (podría argumentar que se acaba de ahorrar 2) pero, por otro lado, tampoco es mucho. Para usar R de manera más efectiva, necesitamos introducir más conceptos de programación.
En la mayoría de las situaciones en las que desee utilizar una calculadora, es posible que desee realizar varios cálculos. R le permite hacer esto, simplemente escribiendo comandos más largos. De hecho, ya hemos visto un ejemplo de esto antes, cuando escribí 5 * 5 * 5 * 5. Sin embargo, probemos un ejemplo ligeramente diferente:

> \> 1 + 2 * 4  
[1] 9

Claramente, esto tampoco es un problema para R. Sin embargo, vale la pena detenerse un segundo y pensar en lo que acaba de hacer R. Claramente, dado que nos dio una respuesta de 9, debe haber multiplicado 2 * 4 (para obtener una respuesta intermedia de 8) y luego sumar 1 a eso. Pero, supongamos que hubiera decidido ir de izquierda a derecha: si R hubiera decidido sumar 1 + 2 (para obtener una respuesta intermedia de 3) y luego multiplicado por 4, habría obtenido una respuesta de 12.
Para responder a esto, necesita conocer el orden de operaciones que usa R. Si recuerdas las clases de matemáticas de la secundaria , en realidad es el mismo orden que te enseñaron cuando estabas en la escuela: el orden " bedmas ". 9 Es decir, primero calcule las cosas dentro de corchetes (), luego calcule los exponentes ^, luego la división / y la multiplicación *, luego la suma + y la resta -. Entonces, para continuar con el ejemplo anterior, si queremos forzar a R a calcular la parte 1 + 2 antes de la multiplicación, todo lo que tendríamos que hacer es encerrarlo entre corchetes:

> \> (1 + 2) * 4  
[1] 12

Esto es algo bastante útil de poder hacer. La única otra cosa que debo señalar sobre el orden de las operaciones es qué esperar cuando tienes dos operaciones que tienen la misma prioridad: es decir, ¿cómo resuelve R los lazos? Por ejemplo, la multiplicación y la división son en realidad la misma prioridad, pero ¿qué debemos esperar cuando le damos a R un problema como 4/2 * 3 para resolver? Si evalúa primero la multiplicación y luego la división, calcularía un valor de dos tercios. Pero si evalúa primero la división calcula un valor de 6. La respuesta, en este caso, es que R va de izquierda a derecha, por lo que en este caso el paso de división vendría primero:

> \> 4/2 * 3  
[dieciséis

Dicho todo lo anterior, es útil recordar que los corchetes siempre son lo primero. Por lo tanto, si alguna vez no está seguro sobre el orden en el que R hará las cosas, una solución fácil es incluir primero entre paréntesis lo que desea que haga. No hay nada que le impida escribir (4/2) * 3. Al encerrar la división entre corchetes , aclaramos qué se supone que debe suceder primero. En este caso, no lo habría necesitado, ya que R habría hecho la división primero de todos modos, pero cuando recién comienza, ¡es mejor asegurarse de que R haga lo que quiere!
 
## Almacenando un número como variable
Una de las cosas más importantes que se pueden hacer en R (o cualquier lenguaje de programación, para el caso) es almacenar información en variables. Las variables en R no son exactamente lo mismo que las variables de las que hablamos en el último capítulo sobre métodos de investigación, pero son similares. A un nivel conceptual, puede pensar en una variable como una etiqueta para una determinada información, o incluso varias piezas diferentes de información. Al hacer un análisis estadístico en R, todos sus datos (las variables que midió en su estudio) se almacenarán como variables en R, pero como verá más adelante en el libro, encontrará que también termina creando variables para otras cosas. Sin embargo, antes de profundizar en todos los detalles confusos de los conjuntos de datos y el análisis estadístico, veamos los conceptos básicos de cómo creamos variables y trabajamos con ellas.
 
### Asignación de variables usando <- y ->
Como hemos estado trabajando con números hasta ahora, comencemos por crear variables para almacenar nuestros números. Y como a la mayoría de la gente le gustan los ejemplos concretos, inventemos uno. Suponga que estoy tratando de calcular cuánto dinero voy a ganar con este libro. Es posible que desee almacenar varios números diferentes. En primer lugar, necesito averiguar cuántas copias venderé. Esto no es exactamente Harry Potter, así que supongamos que solo venderé una copia por alumno de mi clase. Eso es 350 ventas, así que creemos una variable llamada ventas. Lo que quiero hacer es asignar un valor a mis ventas variables, y ese valor debería ser 350. Hacemos esto usando el operador de asignación, que es < -. Así es como lo hacemos:

> \> ventas <- 350

Cuando presiona enter, R no imprime ninguna salida. 10 Simplemente le brinda otro símbolo del sistema. Sin embargo, detrás de escena, R ha creado una variable llamada ventas y le ha dado un valor de 350. Puede comprobar que esto ha sucedido pidiendo a R que imprima la variable en la pantalla. Y la forma más sencilla de hacerlo es escribir el nombre de la variable y presionar enter 11

> \> ventas  
[1] 350

Así que es bueno saberlo. Siempre que no recuerde lo que R tiene almacenado en una variable en particular, puede simplemente escribir el nombre de la variable y presionar enter.
Bien, ahora sabemos cómo asignar variables. De hecho, hay algo más que debería saber. En primer lugar, una de las características curiosas de R es que hay varias formas diferentes de realizar asignaciones. Además del operador <-, también podemos usar -> y =, y es muy importante comprender las diferencias entre ellos. 12 Comencemos considerando - >, ya que es el más fácil (discutiremos el uso de = en la Sección 3.5.1). Como es de esperar con solo mirar el símbolo, es casi idéntico a < -. Es solo que la flecha (es decir, la asignación) va de izquierda a derecha. Entonces, si quisiera definir mi variable de ventas usando - >, lo escribiría así:

> \> 350 -> ventas

Esto tiene el mismo efecto: y todavía significa que solo voy a vender 350 copias. Suspiro. Aparte de esta diferencia superficial, <- y -> son idénticos. De hecho, en lo que respecta a R, en realidad son el mismo operador, solo en una “forma izquierda” y una “forma derecha”. 13
 
### Hacer cálculos usando variables
Bien, volvamos a mi historia original. En mi búsqueda por hacerme rico, he escrito este libro de texto. Para averiguar qué tan buena es una estrategia, comencé a crear algunas variables en R. Además de definir una variable de ventas que cuente la cantidad de copias que voy a vender, también puedo crear una variable llamada regalías, que indica cómo Cuánto dinero obtengo por copia. Digamos que mis regalías son alrededor de $ 7 por libro:

> \> ventas <- 350  
> realeza <- 7
 
Lo bueno de las variables (de hecho, el objetivo de tener variables) es que podemos hacer cualquier cosa con una variable que deberíamos poder hacer con la información que almacena. Es decir, como R me permite multiplicar 350 por 7

> \> 350 * 7
[1] 2450

también me permite multiplicar las ventas por regalías

> \> ventas * regalías  
[1] 2450

En lo que respecta a R, el comando sales * royalty es el mismo que el comando 350 * 7. No es sorprendente que pueda asignar el resultado de este cálculo a una nueva variable, a la que llamaré ingresos. Y cuando hacemos esto, el nuevo ingreso variable obtiene el valor 2450. Así que hagamos eso, y luego hagamos que R imprima el valor de los ingresos para que podamos verificar que se hizo lo que pedimos:

> \> ingresos <- ventas * regalías  
\> ingresos  
[1] 2450

Eso es bastante sencillo. Una cosa un poco más sutil que podemos hacer es reasignar el valor de mi variable, en función de su valor actual. Por ejemplo, supongamos que uno de mis estudiantes (sin duda bajo la influencia de psicofármacos) ama tanto el libro que me dona 550 dólares extra. La forma más sencilla de capturar esto es mediante un comando como este:

> \> ingresos <- ingresos + 550  
\> ingresos  
[1] 3000  

En este cálculo, R ha tomado el valor anterior de ingresos (es decir, 2450) y agregó 550 a ese valor, produciendo un valor de 3000. Este nuevo valor se asigna a la variable de ingresos, sobrescribiendo su valor anterior. En cualquier caso, ahora sabemos que espero ganar $ 3000 con esto. Muy dulce, que piensa que a mí mismo. O al menos, eso es lo que pienso hasta que hago algunos cálculos más y averiguo cuál es el salario por hora implícito que estoy ganando.
 
### Reglas y convenciones para nombrar variables
En los ejemplos que hemos visto hasta ahora, mis nombres de variables (ventas e ingresos) solo han sido palabras en inglés escritas con letras minúsculas. Sin embargo, R permite mucha más flexibilidad cuando se trata de nombrar sus variables, como lo ilustra la siguiente lista de reglas 14:

- Los nombres de las variables solo pueden utilizar los caracteres alfabéticos en mayúsculas de la A a la Z, así como los caracteres en minúsculas de la A a la z. También puede incluir caracteres numéricos del 0 al 9 en el nombre de la variable, así como el punto. o carácter de subrayado _. En otras palabras, puede usar SaL.e_s como nombre de variable (aunque no puedo pensar por qué querría hacerlo), pero no puede usar Sales.          
- Los nombres de las variables no pueden incluir espacios: por lo tanto, my sales no es un nombre válido, pero my.sales sí lo es.          
- Los nombres de las variables distinguen entre mayúsculas y minúsculas: es decir, Ventas y Ventas son nombres de variable diferentes.
- Los nombres de las variables deben comenzar con una letra o un punto. No puede usar algo como _sales o 1sales como nombre de variable. Puede utilizar .sales como nombre de variable si lo desea, pero no suele ser una buena idea. Por convención, las variables que comienzan con a. se utilizan para fines especiales, por lo que debe evitar hacerlo.          
- Los nombres de las variables no pueden ser una de las palabras clave reservadas. Estos son nombres especiales que R necesita para mantenernos “a salvo” de nosotros, los meros usuarios, por lo que no puede usarlos como nombres de variables. Las palabras clave son: if, else, repeat, while, function, for, in, next, break, TRUE, FALSE, NULL, Inf, NaN , NA, NA_integer _, NA_real _, NA_complex _, y finalmente, NA_character _. No se sienta especialmente obligado a memorizarlos : si comete un error y trata de utilizar una de las palabras clave como nombre de variable, R se quejará como el pequeño autómata quejumbroso que es. 

Además de las reglas que R aplica, existen algunas convenciones informales que las personas tienden a seguir al nombrar variables. Uno de ellos ya ha visto: es decir, no use variables que comiencen con un punto. Pero hay varios más. No está obligado a seguir estas convenciones y hay muchas situaciones en las que es aconsejable ignorarlas, pero en general es una buena idea seguirlas cuando pueda:

- Utilice nombres de variables informativos. Como regla general, se prefiere el uso de nombres significativos como ventas e ingresos a los arbitrarios como variable1 y variable 2. De lo contrario , es muy difícil recordar cuál es el contenido de las diferentes variables y se vuelve difícil entender qué hacen realmente sus comandos.          
- Utilice nombres cortos de variables. Escribir es una molestia y a nadie le gusta hacerlo. Por eso, preferimos usar un nombre como ventas sobre un nombre como ventas para este libro que está leyendo . Obviamente, existe un poco de tensión entre el uso de nombres informativos (que tienden a ser largos) y el uso de nombres cortos (que tienden a no tener sentido), así que use un poco de sentido común al intercambiar estas dos convenciones.          
- Utilice uno de los estilos de nomenclatura convencionales para nombres de variables de varias palabras. Supongamos que quiero nombrar una variable que almacena "mi nuevo salario". Obviamente, no puedo incluir espacios en el nombre de la variable, entonces, ¿cómo debo hacer esto? Hay tres convenciones diferentes que a veces ve que emplean los usuarios de R. En primer lugar, puede separar las palabras usando puntos, lo que le daría my.new.salary como nombre de variable. Alternativamente, puede separar palabras usando guiones bajos, como en my_new_salary . Finalmente, puede usar letras mayúsculas al principio de cada palabra (excepto la primera), lo que le da myNewSalary como nombre de variable. No creo que haya ninguna razón sólida para preferir uno sobre el otro, 15 pero es importante ser coherente.          
 
## Usar funciones para hacer cálculos
Los símbolos +, -, * y así sucesivamente son ejemplos de operadores. Como hemos visto, puede hacer muchas
cálculos simplemente utilizando estos operadores. Sin embargo, para hacer cálculos más avanzados (y luego
encendido, para hacer estadísticas reales), necesitará comenzar a usar funciones. 16 Hablaré con más detalle sobre
funciones y cómo funcionan en la Sección 8.4, pero por ahora vamos a sumergirnos y usar algunas. Para empezar,
supongamos que quisiera sacar la raíz cuadrada de 225. La raíz cuadrada, en caso de que tus matemáticas de secundaria sean un poco
oxidado, es justo lo opuesto a elevar un número al cuadrado. Entonces, por ejemplo, dado que "5 al cuadrado es 25", puedo decir que
“5 es la raíz cuadrada de 25”. La notación habitual para esto es
 
aunque a veces también lo verá escrito así 25 0.5 “5 . Esta segunda forma de escribirla es útil para "recordarle" el hecho matemático de que "raíz cuadrada de x" es en realidad lo mismo que "elevar x a la potencia de 0,5". Personalmente, nunca he encontrado que esto sea terriblemente significativo psicológicamente, aunque debo admitir que es bastante conveniente matemáticamente. De todos modos, no es importante. Lo importante es que recuerdes qué es una raíz cuadrada, ya que la necesitaremos más adelante.  

Para calcular la raíz cuadrada de 25, puedo hacerlo en mi cabeza con bastante facilidad, ya que memoricé mis tablas de multiplicar cuando era niño. Se vuelve más difícil cuando los números crecen, y casi imposible si no son números enteros. Aquí es donde algo como R resulta muy útil. Digamos que quería calcular 225 , la raíz cuadrada de 225. Hay dos formas de hacerlo usando R. En primer lugar, dado que la raíz cuadrada de 255 es lo mismo que elevar 225 a la potencia de 0,5, podría usar la potencia operador ^, como hicimos antes: 

> \> 225 ^ 0.5  
[1] 15

Sin embargo, hay una segunda forma de hacerlo, ya que R también proporciona una función de raíz cuadrada, sqrt ( ). Para calcular la raíz cuadrada de 255 usando esta función, lo que hago es insertar el número 225 entre paréntesis. Es decir, el comando que escribo es este: 

> \> raíz cuadrada (225 )  
[1] 15

y como es de esperar de nuestra discusión anterior, los espacios entre paréntesis son puramente cosméticos. Podría haber escrito sqrt ( 225) o sqrt (225) y obtener el mismo resultado. Cuando usamos una función para hacer algo, generalmente nos referimos a esto como llamar a la función, y los valores que escribimos en la función (puede haber más de uno) se conocen como los argumentos de esa función. 
Obviamente, la función sqrt ( ) realmente no nos brinda ninguna funcionalidad nueva, ya que ya sabíamos cómo hacer cálculos de raíz cuadrada usando el operador de potencia ^, aunque creo que se ve mejor cuando usamos sqrt (). Sin embargo, hay muchas otras funciones en R: de hecho, casi todo lo de interés de lo que hablaré en este libro es una función R de algún tipo. Por ejemplo, una función que necesitaremos usar en este libro es la función de valor absoluto. Comparada con la función de raíz cuadrada, es extremadamente simple: simplemente convierte números negativos en números positivos y deja los números positivos en paz. Matemáticamente, el valor absoluto de x se escribe | x | oa veces abspxq . Calcular valores absolutos en R es bastante fácil, ya que R proporciona la función abs ( ) que puede usar para este propósito. Cuando lo alimentas con un número positivo ... 

> \> abdominales (21 )  
[1] 21

la función de valor absoluto no le afecta en absoluto. Pero cuando lo alimentas con un número negativo, escupe la versión positiva del mismo número, así: 

> \> abs ( -13)  
[1] 13

Honestamente, no hay nada que haga la función de valor absoluto que no puedas hacer con solo mirar el número y borrar el signo menos si lo hay. Sin embargo, hay algunos lugares más adelante en el libro donde tenemos que usar valores absolutos, así que pensé que sería una buena idea explicar el significado del término desde el principio.

Antes de continuar, vale la pena señalar que, de la misma manera que R nos permite unir varias operaciones en un comando más largo, como 1 + 2 * 4, por ejemplo, también nos permite unir funciones e incluso combinar funciones con operadores si lo deseamos. Por ejemplo, el siguiente es un comando perfectamente legítimo: 

> \> sqrt (1 + abs (-8))  
[1] 3

Cuando R ejecuta este comando, comienza calculando el valor de abs ( -8), lo que produce un valor intermedio de 8. Una vez hecho esto, el comando se simplifica a sqrt (1 + 8). Para resolver la raíz cuadrada 17, primero debe sumar 1 + 8 para obtener 9, momento en el que evalúa sqrt ( 9), por lo que finalmente genera un valor de 3. 
 
### Argumentos de función, sus nombres y sus valores predeterminados
Hay dos cosas más bastante importantes que necesita comprender sobre cómo funcionan las funciones en R, y ese es el uso de argumentos "con nombre" y "valores"" predeterminados para los argumentos. No es de sorprender que esto no quiere decir que sea la última vez que escucharemos sobre cómo funcionan las funciones, pero son las últimas cosas que necesitamos discutir desesperadamente para comenzar. Para entender de qué se tratan estos dos conceptos , presentaré otra función. La función round ( ) se puede usar para redondear algún valor al número entero más cercano. Por ejemplo, podría escribir esto: 

> \> redondo (3.1415 )  
[1] 3

Realmente bastante sencillo. Sin embargo, supongamos que solo quisiera redondearlo a dos lugares decimales: es decir, quiero obtener 3,14 como resultado. La función round ( ) admite esto, permitiéndole ingresar un segundo argumento a la función que especifica el número de lugares decimales al que desea redondear el número . En otras palabras, podría hacer esto: 

> \> redondo (3,14165 , 2)  
[1] 3,14

Lo que está sucediendo aquí es que he especificado dos argumentos: el primer argumento es el número que debe redondearse (es decir, 3,1415) , el segundo argumento es el número de lugares decimales a los que debe redondearse (es decir, 2), y los dos argumentos están separados por una coma. En este ejemplo simple, es bastante fácil recordar qué argumento viene primero y cuál viene segundo, pero para funciones más complicadas esto no es fácil. Afortunadamente, la mayoría de las funciones R utilizan nombres de argumentos. Para la función round ( ), por ejemplo, el número que debe redondearse se especifica mediante el argumento x, y el número de puntos decimales a los que desea redondear se especifica mediante el argumento dígitos. Como tenemos estos nombres disponibles, podemos especificar los argumentos de la función por nombre. Lo hacemos así:

> \> redondo (x = 3,1415, dígitos = 2)  
[1] 3,14

Note que esto es similar en espíritu a la asignación de variables (Sección 3.4), excepto que usé = aquí, en lugar de < -. En ambos casos, estamos especificando valores específicos para asociarlos con una etiqueta. Sin embargo, existen algunas diferencias entre lo que estaba haciendo antes al crear variables y lo que estoy haciendo aquí al especificar argumentos, por lo que, como consecuencia, es importante que use = en este contexto.   
Como puede ver, especificar los argumentos por nombre implica escribir mucho más, pero también es mucho más fácil de leer. Debido a esto, los comandos de este libro generalmente especificarán los argumentos por nombre, 18 ya que eso le aclara lo que estoy haciendo. Sin embargo, una cosa importante a tener en cuenta es que al especificar los argumentos usando sus nombres, no importa en qué orden los escriba. Pero si no usa los nombres de los argumentos, entonces debe ingresar los argumentos en la forma correcta. orden. En otras palabras, estos tres comandos producen la misma salida... 

> \> redondo (3,14165 , 2)  
\> redondo (x = 3,1415, dígitos = 2)  
\> redondear (dígitos = 2, x = 3,1415)

pero este no ...

> \> redondo (2 , 3,14165)

¿Cómo averigua cuál es el orden correcto? Hay algunas formas diferentes, pero la más sencilla es consultar la documentación de ayuda de la función (consulte la Sección 4.12). Sin embargo, si alguna vez no está seguro, probablemente sea mejor escribir el nombre del argumento. 
Bien, eso es lo primero que dije que necesitarías saber: los nombres de los argumentos. La segunda cosa que debe conocer son los valores predeterminados. Observe que la primera vez que llamé a la función round ( ) en realidad no especifiqué el argumento de los dígitos y, sin embargo, R sabía de alguna manera que esto significaba que debería redondearse al número entero más cercano. ¿Cómo pasó eso? La respuesta es que el argumento de dígitos tiene un valor predeterminado de 0, lo que significa que si decide no especificar un valor para los dígitos, R actuará como si hubiera escrito dígitos = 0. Esto es bastante útil: la gran mayoría de las veces, cuando desea redondear un número, desea redondearlo al número entero más cercano, y sería bastante molesto tener que especificar el argumento de los dígitos cada vez. Por otro lado, a veces realmente desea redondear a algo que no sea el número entero más cercano, ¡y sería aún más molesto si R no lo permitiera ! Por lo tanto, al tener dígitos = 0 como valor predeterminado, obtenemos lo mejor de ambos mundos. 
 
## Dejar que Rstudio te ayude con tus comandos
Es hora de una pequeña digresión. En esta etapa, sabe cómo escribir comandos básicos, incluido cómo usar las funciones R. Y probablemente empiece a darse cuenta de que hay muchas funciones R, todas las cuales tienen sus propios argumentos. Probablemente también esté preocupado de tener que recordarlos todos. Afortunadamente, no es tan malo. De hecho, muy pocos analistas de datos se molestan en intentar recordar todos los comandos. Lo que realmente hacen es utilizar trucos para hacerles la vida más fácil. El primero (y posiblemente el más importante) es utilizar Internet. Si no sabe cómo funciona una función R en particular, busque en Google. En segundo lugar, puede buscar la documentación de ayuda de R. Hablaré más sobre estos dos trucos en la Sección 4.12. Pero ahora mismo quiero llamar su atención sobre un par de trucos simples que Rstudio pone a su disposición.

### Autocompletar usando "tabulación"
Lo primero que quiero llamar su atención es la capacidad de autocompletar en Rstudio.  
Sigamos nuestro ejemplo anterior y supongamos que lo que quiere hacer es redondear un número. Esta vez, comience a escribir el nombre de la función que desee y luego presione la tecla "tabulación". Rstudio mostrará una pequeña ventana como la que se muestra en la Figura 3.2. En esta figura, escribí las letras ro en la línea de comando y luego presioné el tabulador. La ventana tiene dos paneles. A la izquierda, hay una lista de variables y funciones que comienzan con las letras que escribí que se muestran en texto negro, y un texto gris que le dice dónde está almacenada esa variable / función. Ignore el texto gris por ahora: no tendrá mucho sentido para usted hasta que hablemos de los paquetes en la Sección 4.2. En la Figura 3.2 puede ver que hay bastantes cosas que comienzan con las letras ro : hay algo llamado roca, algo llamado redondo, algo llamado redondo, fecha, etc. El que queremos es redondo, pero si lo escribe usted mismo, notará que cuando presiona la tecla de tabulación, aparece la ventana con la entrada superior (es decir, la roca) resaltada. Puede utilizar las teclas de flecha hacia arriba y hacia abajo para seleccionar el que desee. O, si ninguna de las opciones le parece correcta , puede presionar la tecla de escape ("esc") o la tecla de flecha izquierda para que la ventana desaparezca.  

En nuestro caso, lo que queremos es la opción redonda, así que la seleccionaremos. Cuando haga esto, verá que el panel de la derecha cambia. Anteriormente, nos había estado diciendo algo sobre el conjunto de datos de rocas (es decir, "Mediciones en 48 muestras de rocas ...") que se distribuye como parte de R. Pero cuando seleccionamos round, muestra información sobre la función round ( ) , exactamente como se muestra en la Figura 3.2. Esta pantalla es realmente útil. Lo primero que dice es round ( x, digits = 0): lo que esto le dice es que la función round () tiene dos argumentos. El primer argumento se llama x y no tiene un valor predeterminado . El segundo argumento son dígitos y tiene un valor predeterminado de 0. En muchas situaciones, esa es toda la información que necesita. Pero Rstudio va un poco más allá y proporciona información adicional sobre la función que se encuentra debajo. A veces, esa información adicional es muy útil, a veces no: Rstudio extrae ese texto de la documentación de ayuda de R, y mi experiencia es que la utilidad de esa documentación varía enormemente. De todos modos, si ha decidido que round ( ) es la función que desea usar, puede presionar la flecha derecha o la tecla Intro, y Rstudio terminará de escribir el resto del nombre de la función por usted.  

La herramienta de autocompletar de Rstudio funciona de manera ligeramente diferente si ya ha escrito el nombre de la función y ahora está intentando escribir los argumentos. Por ejemplo, supongamos que escribí round (en la consola y luego presioné la tecla tab. Rstudio es lo suficientemente inteligente como para reconocer que ya sé el nombre de la función que quiero, ¡porque ya lo escribí! calcula que lo que me interesa son los argumentos de esa función. Eso es lo que aparece en la ventana pequeña. Puede ver esto en la Figura 3.3. De nuevo, la ventana tiene dos paneles y puede interactuar con esta ventana exactamente de la misma manera que lo hizo con la ventana que se muestra en la Figura 3.2.En el panel de la izquierda , puede ver una lista de los nombres de los argumentos.En el lado derecho , muestra información sobre lo que hace el argumento seleccionado.

### Examinando tu historial de comandos
Una cosa que R hace automáticamente es realizar un seguimiento de su "historial de comandos". Es decir, recuerda todos los comandos que ha escrito anteriormente. Puede acceder a este historial de diferentes formas. La forma más sencilla es utilizar las teclas de flecha hacia arriba y hacia abajo. Si presiona la tecla arriba, la consola R le mostrará el comando más reciente que ha escrito. Vuelva a presionarlo y le mostrará el comando anterior. Si desea que desaparezca el texto de la pantalla, presione escape. 20 El uso de las teclas arriba y abajo puede ser muy útil si ha escrito un comando largo que tenía un error tipográfico. En lugar de tener que volver a escribirlo todo desde cero, puede usar la tecla de arriba para abrir el comando y arreglarlo.  

La segunda forma de obtener acceso a su historial de comandos es mirar el panel de historial en Rstudio .  

En la parte superior derecha de la ventana de Rstudio , verá una pestaña denominada "Historial". Haga clic en eso y verá una lista de todos sus comandos recientes que se muestran en ese panel: debería parecerse a la Figura 3.4. Si hace doble clic en uno de los comandos, se copiará a la consola R. (Puede lograr el mismo resultado seleccionando el comando que desea con el mouse y luego haciendo clic en el botón "A la consola"). 
 
## Almacenando muchos números como un vector
En este punto, hemos cubierto las funciones con suficiente detalle para que podamos pasar con seguridad los siguientes dos capítulos (con una pequeña excepción: consulte la Sección 4.11), así que volvamos a nuestra discusión de variables. Cuando presenté las variables en la Sección 3.4, le mostré cómo podemos usar variables para almacenar un solo número. En esta sección, ampliaremos esta idea y veremos cómo almacenar varios números dentro de una variable. En R, el nombre de una variable que puede almacenar varios valores es un vector. Así que creemos uno. 
 
### Creando un vector
Sigamos con mi tonto ejemplo de “hacerse rico rápidamente escribiendo un libro de texto”. Supongamos que la compañía de libros de texto (si realmente tuviera una) me envía datos de ventas mensualmente. Dado que mi clase comenzó a fines de febrero, podríamos esperar que la mayoría de las ventas ocurran hacia el comienzo del año. Supongamos que tengo 100 ventas en febrero, 200 ventas en marzo y 50 ventas en abril, y ninguna otra venta durante el resto del año. Lo que me gustaría hacer es tener una variable, llamémosla ventas por mes , que almacene todos estos datos de ventas. El primer número almacenado debería ser 0 ya que no tuve ventas en enero, el segundo debería ser 100 y así sucesivamente . La forma más sencilla de hacer esto en R es usar la función de combinación, c ( ). Para hacerlo, todo lo que tenemos que hacer es escribir todos los números que desea almacenar en una lista separada por comas, como esta: 

> \> ventas por mes <- c (0, 100, 200, 50, 0, 0, 0, 0, 0, 0, 0, 0)  
\> ventas por mes  
[1] 0100200 50 0 0 0 0 0 0 0 0

Para usar la terminología correcta aquí, tenemos una sola variable llamada ventas.por.mes : esta variable es un vector que consta de 12 elementos. 
 
### Una útil digresión
Ahora que hemos aprendido a poner información en un vector, lo siguiente que debemos entender es cómo extraer esa información nuevamente. Sin embargo, antes de hacerlo, vale la pena dar un pequeño desvío. Si ha estado siguiendo, escribiendo todos los comandos en R usted mismo, es posible que el resultado que vio cuando imprimimos el vector sales.by.month fuera ligeramente diferente a lo que mostré anteriormente. Esto habría sucedido si la ventana (o el panel de Rstudio ) que contiene la consola R es muy, muy estrecha. Si ese fuera el caso, es posible que haya visto un resultado parecido a esto: 

> \> ventas por mes  
[1] 0100200 50 0 0 0 0  
[9] 0 0 0 0

Como no había mucho espacio en la pantalla, R imprimió los resultados en dos líneas. Pero eso no es lo importante a notar. El punto importante es que la primera línea tiene un [1] delante, mientras que la segunda línea comienza con [9 ]. Está bastante claro lo que está sucediendo aquí. Para la primera fila, R ha impreso desde el primer elemento hasta el octavo elemento, por lo que comienza esa fila con un [1 ]. Para la segunda fila, R imprimió el noveno elemento del vector hasta el duodécimo, por lo que comienza esa fila con un [9] para que pueda saber dónde está de un vistazo. Puede parecerle un poco extraño que R haga esto, pero de alguna manera es una bondad, ¡especialmente cuando se trata de conjuntos de datos más grandes! 
 
### Obtener información de los vectores
Para volver a la historia principal, consideremos el problema de cómo obtener información de un vector. En este punto, es posible que tenga la sospecha de que la respuesta tiene algo que ver con las cosas [1] y [9] que R ha estado imprimiendo. Y por supuesto que tienes razón. Supongamos que solo quiero extraer los datos de ventas de febrero. Febrero es el segundo mes del año, así que intentemos esto: 

> \> ventas.por.mes [2]  
[1] 100

Sí, esas son las rebajas de febrero. Pero hay un detalle sutil a tener en cuenta aquí: observe que R produce [1] 100, no [2] 100. Esto se debe a que R está siendo extremadamente literal. Cuando escribimos sales.by.month [2], le pedimos a R que encontrara exactamente una cosa, y esa cosa resulta ser el segundo elemento de nuestro vector sales.by.month . Entonces, cuando genera [1] 100, lo que R está diciendo es que el primer número que acabamos de pedir es 100. Este comportamiento tiene más sentido cuando se da cuenta de que podemos usar este truco para crear nuevas variables. Por ejemplo, podría crear una variable february.sales como esta: 

> \> February.sales <- sales.by.month [2]  
\> ventas de febrero  
[1] 100

Obviamente, la nueva variable february.sales solo debe tener un elemento, por lo que cuando imprimo esta nueva variable, la salida R comienza con un [1] porque 100 es el valor del primer (y único) elemento de february.sales . El hecho de que este también sea el valor del segundo elemento de ventas por mes es irrelevante. Volveremos a retomar este tema en breve (Sección 3.10). 
 
### Alterando los elementos de un vector
A veces querrá cambiar los valores almacenados en un vector. Imagínese mi sorpresa cuando el editor me llama para decirme que los datos de ventas de mayo son incorrectos. En realidad, se vendieron 25 libros adicionales en mayo, pero hubo un error o algo así, por lo que no me lo habían dicho. ¿Cómo puedo corregir mi variable sales.by.month ? Una posibilidad sería volver a asignar todo el vector desde el principio, utilizando c ( ). Pero eso es mucho escribir. Además, es un poco derrochador: ¿por qué debería R tener que redefinir las cifras de ventas para los 12 meses, cuando solo el quinto es incorrecto? Afortunadamente, podemos decirle a R que cambie solo el quinto elemento, usando este truco: 

> \> ventas.por.mes [5] <- 25  
\> ventas por mes  
[1] 0100200 50 25 0 0 0 0 0 0 0

Otra forma de editar variables es usar las funciones edit ( ) o fix (). No los discutiré en detalle en este momento, pero puede verlos por su cuenta. 
 
### Cosas útiles que debes saber sobre los vectores
Antes de continuar, quiero mencionar un par de cosas más sobre los vectores. En primer lugar, a menudo se encuentra deseando saber cuántos elementos hay en un vector (generalmente porque lo ha olvidado). Puede usar la función length ( ) para hacer esto. Es bastante sencillo: 

> \> longitud (x = ventas por mes )  
[1] 12

En segundo lugar, a menudo desea alterar todos los elementos de un vector a la vez. Por ejemplo, supongamos que quisiera calcular cuánto dinero ganaba cada mes. Como estoy ganando $ 7 por libro (no en serio, eso es bastante parecido a lo que obtienen los autores con los libros de texto muy caros que se espera que compre), lo que quiero hacer es multiplicar cada elemento de las ventas. .month vector por 7. R hace que esto sea bastante fácil, como muestra el siguiente ejemplo: 

> \> ventas por mes * 7  
[1] 0700 1400 350 0 0 0 0 0 0 0 0

En otras palabras, cuando multiplica un vector por un solo número, todos los elementos del vector se multiplican. Lo mismo es cierto para la suma, resta, división y toma de poderes. Entonces eso es genial. Por otro lado, suponga que quisiera saber cuánto dinero estaba ganando por día, en lugar de por mes. Como no todos los meses tienen la misma cantidad de días, necesito hacer algo ligeramente diferente. En primer lugar, crearé dos nuevos vectores: 

> \> días.por.mes <- c (31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31)  
\> beneficio <- ventas por mes * 7

Obviamente, la variable de ganancias es la misma que creamos anteriormente, y la variable days.per.month es bastante sencilla. Lo que quiero hacer es dividir cada elemento de beneficio por el elemento correspondiente de días por mes . Nuevamente, R hace que esto sea bastante fácil: 

> \> beneficio / días por mes  
[1] 0,00000 25,00000 45,16129 11,66667 0,00000 0,00000 0,00000 0,00000 0,00000  
[10] 0,00000 0,00000 0,00000

Todavía no me gustan todos esos ceros, pero eso no es lo que importa aquí. Observe que el segundo elemento de la producción es 25, porque R ha dividido el segundo elemento de la ganancia (es decir, 700) por el segundo elemento de días por mes (es decir, 28). De manera similar, el tercer elemento de la salida es igual a 1400 dividido por 31, y así sucesivamente. Hablaremos más sobre cálculos que involucran vectores más adelante (y en particular una cosa llamada "regla de reciclaje"; Sección 7.12.2), pero eso es suficiente detalle por ahora. 
 
## Almacenamiento de datos de texto
La mayoría de las veces, sus datos serán de naturaleza numérica, pero no siempre. A veces, sus datos realmente necesitan describirse usando texto, no usando números. Para abordar esto, debemos considerar la situación en la que nuestras variables almacenan texto. Para crear una variable que almacene la palabra "hola", podemos escribir esto: 

> \> saludo <- "hola"  
\> saludo  
[1] "hola"

Al interpretar esto, es importante reconocer que las comillas aquí no son parte de la cadena en sí. Son solo algo que usamos para asegurarnos de que R sepa tratar los caracteres que encierran como un fragmento de datos de texto, conocido como una cadena de caracteres. En otras palabras, R trata "hola" como una cadena que contiene la palabra "hola"; pero si hubiera escrito hola en su lugar, ¡R buscaría una variable con ese nombre! También puede usar 'hola' para especificar una cadena de caracteres. 
Bien, así es como almacenamos el texto. A continuación, es importante reconocer que cuando hacemos esto, R almacena la palabra completa "hola" como un solo elemento: nuestra variable de saludo no es un vector de cinco letras diferentes. Más bien, tiene solo un elemento, y ese elemento corresponde a la cadena de caracteres completa "hola". Para ilustrar esto, si realmente le pido a R que encuentre el primer elemento de saludo, imprime la cadena completa: 

> \> saludo [ 1]  
[1] "hola"

Por supuesto, no hay ninguna razón por la que no pueda crear un vector de cadenas de caracteres. Por ejemplo, si tuviéramos que continuar con el ejemplo de mis intentos de ver los datos de ventas mensuales de mi libro, una variable que podría querer incluiría los nombres de los 12 meses. 23 Para hacerlo, podría escribir un comando como este 

> \> meses <- c ( "enero", "febrero", "marzo", "abril", "mayo", "junio",  
+ "Julio", "agosto", "septiembre", "octubre", "noviembre", "diciembre")  
\> meses  
[1] "enero" "febrero" "marzo" "abril" "mayo" "junio"  
[7] "julio" "agosto" "septiembre" "octubre" "noviembre" "diciembre"

Este es un vector de caracteres que contiene 12 elementos, cada uno de los cuales es el nombre de un mes. Entonces, si quisiera que R me dijera el nombre del cuarto mes, todo lo que haría es esto: 

> \> meses [ 4]  
[1 de abril"
 
### Trabajando con texto
Trabajar con datos de texto es algo más complicado que trabajar con datos numéricos, y discutir algunas de las ideas básicas en la Sección 7.8, pero para los propósitos del capítulo actual sólo necesitamos este desnudos huesos de croquis. La única otra cosa que quiero hacer antes de continuar es mostrarte un ejemplo de una función que se puede aplicar a datos de texto. Hasta ahora, la mayoría de las funciones que hemos visto (es decir, sqrt ( ), abs () y round ()) solo tienen sentido cuando se aplican a datos numéricos (p. Ej., No se puede calcular la raíz cuadrada de "hola") , y hemos visto una función que se puede aplicar a prácticamente cualquier variable o vector (es decir, length ()). Por lo tanto , sería bueno ver un ejemplo de una función que se puede aplicar al texto. 
La función que les voy a presentar se llama nchar ( ), y lo que hace es contar el número de caracteres individuales que componen una cadena. Recuerde antes que cuando intentamos calcular la longitud ( ) de nuestra variable de saludo, devolvió un valor de 1: la variable de saludo contiene solo una cadena, que resulta ser "hola". Pero, ¿y si quiero saber cuántas letras hay en la palabra? Claro, podría contarlos, pero eso es aburrido, y más aún, es una estrategia terrible si lo que quería saber era la cantidad de letras en Guerra y paz. Ahí es donde la función nchar ( ) es útil: 

> \> nchar (x = saludo)  
[15

Eso tiene sentido, ya que de hecho hay 5 letras en la cadena "hola ". Mejor aún, puede aplicar nchar ( ) a vectores completos. Entonces, por ejemplo, si quiero que R me diga cuántas letras hay en los nombres de cada uno de los 12 meses, puedo hacer esto: 

> \> nchar (x = meses)  
[1] 7 8 5 5 3 4 4 6 9 7 8 8

Así que es bueno saberlo. La función nchar ( ) puede hacer un poco más que esto, y hay muchas otras funciones que puede hacer para extraer más información del texto o hacer todo tipo de cosas sofisticadas. Sin embargo, ¡ el objetivo aquí no es enseñar nada de eso! El objetivo en este momento es solo ver un ejemplo de una función que realmente funciona cuando se aplica al texto. 
 
## Almacenamiento de datos "verdaderos o falsos"  
Es hora de pasar a un tercer tipo de datos. Un concepto clave en el que se basa gran parte de R es la idea de valor lógico . Un valor lógico es una afirmación sobre si algo es verdadero o falso. Esto se implementa en R de una manera bastante sencilla. Hay dos valores lógicos, a saber, VERDADERO y FALSO. A pesar de la sencillez, los valores lógicos son cosas muy útiles. Veamos como funcionan. 
 
### Evaluación de verdades matemáticas
En el clásico libro 1984 de George Orwell, una de las consignas utilizadas por el Partido totalitario era “dos más dos es cinco”, con la idea de que el dominio político de la libertad humana se completa cuando es posible subvertir incluso la más básica de las verdades. Es un pensamiento aterrador, especialmente cuando el protagonista Winston Smith finalmente se derrumba bajo tortura y acepta la proposición. “El hombre es infinitamente maleable”, dice el libro. Estoy bastante seguro de que esto no es cierto para los humanos 24 pero definitivamente no es cierto para R. R no es infinitamente maleable. Tiene opiniones bastante firmes sobre el tema de lo que es y no es 
cierto, al menos en lo que respecta a las matemáticas básicas. Si le pido que calcule 2 + 2, siempre da la misma respuesta, y no es un maldito 5: 

> \> 2 + 2  
[1] 4

Por supuesto, hasta ahora R solo está haciendo los cálculos. No le he pedido que afirme explícitamente que 2 + 2 = 4 es una declaración verdadera. Si quiero que R haga un juicio explícito, puedo usar un comando como este: 

> \> 2 + 2 == 4  
[1] VERDADERO

Lo que he hecho aquí es usar el operador de igualdad, ==, para forzar a R a hacer un juicio de "verdadero o falso". 25 Bien, veamos qué piensa R del eslogan del Partido: 

> \> 2 + 2 == 5  
[1] FALSO

¡Booyah! ¡Libertad y ponis para todos! O algo así. De todos modos, vale la pena echar un vistazo a lo que sucede si trato de obligar a R a creer que dos más dos son cinco haciendo una declaración de asignación como 2 
+ 2 = 5 o 2 + 2 <- 5. Cuando hago esto, esto es lo que sucede:

> \> 2 + 2 = 5  
Error en 2 + 2 = 5: el destino de la asignación se expande a un objeto que no es del idioma

A R no le gusta mucho esto. Se reconoce que 2 + 2 no es una variable (que es lo que el “no lingüística parte objeto” está diciendo), y que no va a dejar de intentar “Reasignar” la misma. Si bien R es bastante flexible y, de hecho , le permite hacer cosas bastante notables para redefinir partes de R en sí, hay algunas verdades básicas y primitivas a las que se niega a renunciar. No cambiará las leyes de la suma y no cambiará la definición del número 2. 
Probablemente sea lo mejor.
 
### Operaciones lógicas
Así que ahora hemos visto operaciones lógicas en funcionamiento, pero hasta ahora solo hemos visto el ejemplo más simple posible. Probablemente no se sorprenda al descubrir que podemos combinar operaciones lógicas con otras operaciones y funciones de una manera más complicada, como esta:

> \> 3 * 3 + 4 * 4 == 5 * 5  
[1] VERDADERO

o esto

> \> raíz cuadrada (25 ) == 5  
[1] VERDADERO

Tabla 3.2: Algunos operadores lógicos. Técnicamente debería llamar a estos “operadores relacionales binarios”, pero francamente no quiero. Es mi libro para que nadie pueda obligarme . 
No solo eso, sino que, como lo ilustra la Tabla 3.2, hay varios otros operadores lógicos que puede usar,
correspondiente a algunos conceptos matemáticos básicos. Con suerte, todos estos se explican por sí mismos: por ejemplo, el operador menor que <comprueba si el número de la izquierda es menor que el número de la derecha. Si es menor, entonces R devuelve una respuesta VERDADERA: 
> \> 99 <100  
[1] VERDADERO

pero si los dos números son iguales, o si el de la derecha es mayor, entonces R devuelve una respuesta FALSO, como lo ilustran los siguientes dos ejemplos: 

> \> 100 <100  
[1] FALSO  
\> 100 <99  
[1] FALSO  

Por el contrario, el operador menor o igual que <= hará exactamente lo que dice. Devuelve un valor de VERDADERO si el número del lado izquierdo es menor o igual que el número del lado derecho. Entonces, si repetimos los dos ejemplos anteriores usando < =, esto es lo que obtenemos: 

> \> 100 <= 100  
[1] VERDADERO  
\> 100 <= 99  
[1] FALSO

¡Y en este punto espero que sea bastante obvio qué hacen el operador mayor que> y el operador mayor o igual que> =! ¡El siguiente en la lista de operadores lógicos es el operador no igual a ! = que , como todos los demás, hace lo que dice que hace. Devuelve un valor de VERDADERO cuando las cosas de ambos lados no son idénticas entre sí. Por lo tanto, dado que 2 `2 no es igual a 5, obtenemos: 

> \> 2 + 2! = 5  
[1] VERDADERO

Aún no hemos terminado. Hay tres operaciones lógicas más que vale la pena conocer, enumeradas en la Tabla 3.3. ¡Estos son los no operadores! , el operador and &, y el operador or | . Al igual que los otros operadores lógicos, su comportamiento es más o menos exactamente lo que cabría esperar dados sus nombres. Por ejemplo, si le pido que evalúe la afirmación de que “2 + 2 = 4 o 2 + 2 = 5”, diría que es verdad. Dado que es una declaración de "una o la otra", todo lo que necesitamos es que una de las dos partes sea verdadera. Eso es lo que | el operador hace: 

Tabla 3.3: Algunos operadores más lógicos.
 
> \> (2 + 2 == 4) | (2 + 2 == 5)  
[1] VERDADERO

Por otro lado, si le pido que evalúe la afirmación de que "2 + 2 = 4 y 2 + 2 = 5", diría que es falsa. Dado que esta es una declaración y , necesitamos que ambas partes sean verdaderas. Y eso es lo que hace el operador & : 

> \> (2 + 2 == 4) y (2 + 2 == 5)  
[1] FALSO

Finalmente, está el operador not, que es simple pero molesto de describir en inglés. Si le pido que evalúe mi afirmación de que “no es cierto que 2 + 2 = 5”, entonces diría que mi afirmación es verdadera; porque mi afirmación es que "2 + 2 = 5 es falso". Y tengo razón. Si escribimos esto como un comando R , obtenemos esto: 

> \>! (2 + 2 == 5)  
[1] VERDADERO

En otras palabras, dado que 2 + 2 == 5 es una declaración FALSA, ¡debe ser el caso que! (2 + 2 == 5) es VERDADERO. Esencialmente, lo que realmente hemos hecho es afirmar que "no falso" es lo mismo que "verdadero". Obviamente, esto no es del todo correcto en la vida real. Pero R vive en un mundo mucho más blanco o negro: para R todo es verdadero o falso. No se permiten tonos de gris. De hecho, podemos ver esto mucho más explícitamente, así: 

> \>! FALSO  
[1] VERDADERO

Por supuesto, en nuestro ejemplo 2 + 2 = 5, ¡realmente no necesitábamos usar "no "! y "igual a" == como dos operadores separados. ¡Podríamos haber usado el operador "no es igual a" ! = así: 

> \> 2+ 2! = 5  
[1] VERDADERO

¡Pero hay muchas situaciones en las que realmente necesitas usar ! operador. Veremos algunos más adelante.
 
### Almacenamiento y uso de datos lógicos
Hasta este punto, he introducido datos numéricos (en las Secciones 3.4 y 3.7) y datos de caracteres (en
Sección 3.8). Por lo tanto, es posible que no se sorprenda al descubrir que estos valores VERDADERO y FALSO que ha estado produciendo R son en realidad un tercer tipo de datos, llamados datos lógicos. Es decir, cuando le pregunté a R si 2 + 2 == 5 y dijo [1] FALSO en respuesta, en realidad estaba produciendo información que podemos almacenar en variables. Por ejemplo, podría crear una variable llamada is.the.Party.correct , que almacenaría la opinión de R: 

> \> es.la.parte.correcta <- 2 + 2 == 5  
\> es.la.parte.correcta
[1] FALSO

Alternativamente, puede asignar el valor directamente, escribiendo VERDADERO o FALSO en su comando. Me gusta esto:

> \> es.la.parte.correcta <- FALSO  
\> es.la.parte.correcta  
[1] FALSO

Mejor aún, debido a que es un poco tedioso escribir VERDADERO o FALSO una y otra vez, R le proporciona un atajo: puede usar T y F en su lugar (pero distingue entre mayúsculas y minúsculas: t y f no funcionarán). 27 Entonces esto funciona: 

> \> es.la.parte.correcta <- F  
\> es.la.parte.correcta  
[1] FALSO

pero esto no:

> \> es.la.parte.correcta <- f  
Error: objeto 'f' no encontrado
 
### Vectores de lógicas
Lo siguiente que se debe mencionar es que puede almacenar vectores de valores lógicos exactamente de la misma manera que puede almacenar vectores de números (Sección 3.7) y vectores de datos de texto (Sección 3.8). Nuevamente, podemos definirlos directamente a través de la función c ( ), así: 

> \> x <- c ( VERDADERO, VERDADERO, FALSO)  
\> x  
[1] VERDADERO VERDADERO FALSO

o puede producir un vector de lógicas aplicando un operador lógico a un vector. Es posible que esto no tenga mucho sentido para ti, así que vamos a descomprimirlo lentamente. Primero, supongamos que tenemos un vector de números (es decir, un "vector no lógico"). Por ejemplo, podríamos usar el vector ventas por mes que usamos en la sección 3.7. Suponga que quisiera que R me dijera, para cada mes del año, si realmente vendí un libro en ese mes. Puedo hacerlo escribiendo esto: 

> \> ventas por mes > 0  
[1] FALSO TRUE TRUE TRUE TRUE FALSO FALSO FALSO FALSO FALSO FALSO FALSO  

y nuevamente, puedo almacenar esto en un vector si quiero, como ilustra el siguiente ejemplo:  

> \> cualquier.ventas .este.meso <- ventas.por.meses > 0  
\> cualquier.ventas .este . mes  
[1] FALSO TRUE TRUE TRUE TRUE FALSO FALSO FALSO FALSO FALSO FALSO FALSO   

En otras palabras, any.sales .this.month es un vector lógico cuyos elementos son VERDADEROS solo si el elemento correspondiente de sales.by.month es mayor que cero. Por ejemplo, dado que no vendí libros en enero, el primer elemento es FALSO. 
 
### Aplicar una operación lógica al texto
En un momento (Sección 3.10) le mostraré por qué estas operaciones lógicas y vectores lógicos son tan útiles, pero antes de hacerlo, quiero señalar brevemente que puede aplicarlos tanto al texto como a los datos lógicos . Es solo que debemos ser un poco más cuidadosos al comprender cómo R interpreta las diferentes operaciones. En esta sección hablaré sobre cómo se aplica el operador igual a == al texto, ya que este es el más importante. Obviamente, el operador no es igual a ! = da las respuestas exactamente opuestas a ==, así que implícitamente también estoy hablando de ese, pero no daré comandos específicos que muestren el uso de! =. En cuanto a los otros operadores, aplazaré una discusión más detallada de este tema hasta la Sección 7.8.5. 
Bien, veamos cómo funciona. En cierto sentido, es muy simple. Por ejemplo, puedo preguntarle a R si la palabra "gato" es lo mismo que la palabra "perro ", así: 

> \> "gato" == "perro"  
[1] FALSO

Eso es bastante obvio, y es bueno saber que incluso R puede darse cuenta de eso. De manera similar, R reconoce que un "gato" es un "gato ":

> \> "gato" == "gato"  
[1] VERDADERO

Una vez más, eso es exactamente lo que esperaríamos. Sin embargo, lo que debe tener en cuenta es que R no es para nada tolerante cuando se trata de gramática y espaciado. Si dos cadenas difieren de alguna manera, R dirá que no son iguales entre sí, como indican los siguientes ejemplos: 

> \> "gato" == "gato"  
[1] FALSO  
\> "gato" == "GATO"  
[1] FALSO  
\> "gato" == "ca t"  
[1] FALSO

## Vectores de indexación
Una última cosa que agregar antes de terminar este capítulo. Hasta ahora, siempre que he tenido que obtener información de un vector, todo lo que he hecho es escribir algo como meses [ 4]; y cuando hago esto, R imprime el cuarto elemento del vector de meses. En esta sección, le mostraré dos trucos adicionales para obtener información del vector. 

### Extrayendo varios elementos
Una cosa muy útil que podemos hacer es extraer más de un elemento a la vez. En el ejemplo anterior, solo usamos un solo número (es decir, 2) para indicar qué elemento queríamos. Alternativamente, podemos usar un vector. Entonces, supongamos que quisiera los datos de febrero, marzo y abril. Lo que podría hacer es usar el vector c ( 2,3,4) para indicar qué elementos quiero que R extraiga. Es decir, escribiría esto: 

> \> ventas.por.mes [c (2,3,4)]  
[1] 100 200 50

Tenga en cuenta que el orden importa aquí. Si solicité los datos en el orden inverso (es decir, primero de abril, luego de marzo, luego de febrero) usando el vector c ( 4,3,2), entonces R genera los datos en el orden inverso: 

> \> ventas.por.mes [c (4,3,2)]  
[1] 50 200 100

Una segunda cosa a tener en cuenta es que R le proporciona atajos útiles para situaciones muy comunes.
Por ejemplo, supongamos que quisiera extraer todo desde el segundo mes hasta el octavo mes.
Una forma de hacer esto es hacer lo mismo que hice anteriormente y usar el vector c ( 2,3,4,5,6,7,8) para indicar los elementos que quiero. Eso funciona bien 

> \> ventas.por.mes [c (2,3,4,5,6,7,8)]  
[1] 100 200 50 0 0 0 0

pero es como escribir mucho. Para ayudar a que esto sea más fácil, R le permite usar 2: 8 como abreviatura de c ( 2,3,4,5,6,7,8), lo que simplifica mucho las cosas. Primero, verifiquemos que esto sea cierto: 

> \> 2: 8  
[1] 2 3 4 5 6 7 8

A continuación, verifiquemos que podemos usar la abreviatura 2: 8 como una forma de extraer los elementos del segundo al octavo de sales.by.months: 

> \> ventas por mes [2: 8]  
[1] 100 200 50 0 0 0 0

Así que eso es genial.
 
### Indexación lógica
En este punto, puedo presentar una herramienta extremadamente útil llamada indexación lógica. En la última sección, creé un vector lógico any.sales .this.month , cuyos elementos son VERDADEROS para cualquier mes en el que vendí al menos un libro, y FALSO para todos los demás. Sin embargo, esa gran lista de VERDADEROS y FALSOS es un poco difícil de leer, así que lo que me gustaría hacer es que R seleccione los nombres de los meses por los que vendí libros. Anteriormente, creé un vector de meses que contiene los nombres de cada uno de los meses. Aquí es donde la indexación lógica es útil. Lo que necesito hacer es esto: 

> \> meses [ ventas.por.mes > 0]  
[1] "febrero" "marzo" "abril" "mayo"

Para comprender lo que está sucediendo aquí, es útil notar que sales.by.month > 0 es la misma expresión lógica que usamos para crear el vector any.sales.this.month en la última sección. De hecho, podría haber hecho esto: 

> \> meses [ cualquier.ventas.este . mes ]  
[1] "febrero" "marzo" "abril" "mayo"

y obtuve exactamente el mismo resultado. Para averiguar qué elementos de meses incluir en la salida, lo que hace R es ver si el elemento correspondiente en any.sales .this.month es VERDADERO. Por lo tanto, dado que el elemento 1 de cualquier.ventas .este . mes es FALSO, R no incluye "enero" como parte de la salida; pero como el elemento 2 de any.sales.this.month es TRUE, R incluye "febrero" en la salida. Tenga en cuenta que no hay ninguna razón por la que no pueda utilizar el mismo truco para encontrar las cifras de ventas reales de esos meses. El comando para hacer eso sería simplemente este: 

> \> ventas por mes [ ventas por mes > 0]  
[1] 100 200 50 25

De hecho, podemos hacer lo mismo con el texto. He aquí un ejemplo. Supongamos que, para continuar con la saga de las ventas de libros de texto, luego descubro que la librería solo tenía existencias suficientes para algunos meses del año. Me dicen que a principios del año que tenían las poblaciones de "alto", que luego se redujo a niveles "bajos", y de hecho durante un mes que estaban "fuera" de copias del libro durante un tiempo antes de que fueran capaces de reponer ellas . Por lo tanto, podría tener una variable llamada stock.levels que se ve así: 

> \> niveles de existencias  
[1] "alto" "alto" "bajo" "fuera" "fuera" "alto" "alto" "alto" "alto" "alto" "alto"  
[12] "alto"

Por lo tanto, si quiero saber los meses en los que la librería estuvo fuera de mi libro, podría aplicar el truco de indexación lógica , pero con el vector de caracteres stock.levels , así: 

> \> meses [ stock.levels == "out"]  
[1] "abril" "mayo"

Alternativamente, si quiero saber cuándo la librería tenía pocas copias o no tenía copias, podría hacer esto: 

> \> meses [ stock.levels == "out" | stock.levels == "bajo"]  
[1] "marzo" "abril" "mayo"

o esto

> \> meses [ stock.levels ! = "high"]  
[1] "marzo" "abril" "mayo"

De cualquier manera, obtengo la respuesta que quiero.
En este punto, espero que pueda ver por qué la indexación lógica es tan útil. Es una forma muy básica pero muy poderosa de manipular datos. Hablaremos mucho más sobre cómo manipular los datos en el Capítulo 7, ya que es una habilidad crítica para la investigación del mundo real que a menudo se pasa por alto en las clases de introducción a los métodos de investigación (o al menos, esa ha sido mi experiencia). Se necesita un poco de práctica para sentirse completamente cómodo usando la indexación lógica, por lo que es una buena idea jugar con este tipo de comandos. Intente crear algunas variables diferentes por su cuenta, y luego hágase preguntas como "¿cómo hago para que R escupe todos los elementos que son [bla]]". La práctica hace la perfección, y solo practicando la indexación lógica perfeccionará el arte de gritar insultos frustrados en su computadora. 

## Salir de R
Hay una última cosa que debería cubrir en este capítulo: cómo dejar de fumar R. Cuando digo esto, no estoy tratando de dar a entender que R es algún tipo de adición patológica y que necesita llamar a R QuitLine o usar parches para controlar los antojos (aunque ciertamente podría argumentar que hay algo seriamente patológico en ser adicto a R). Solo me refiero a cómo salir del programa. Suponiendo que está ejecutando R de la manera habitual (es decir, a través de Rstudio o la GUI predeterminada en una computadora con Windows o Mac), entonces puede cerrar la aplicación de la manera normal. Sin embargo, R también tiene una función, llamada q ( ) que puede usar para salir, que es bastante útil si está ejecutando R en una ventana de terminal.  
Independientemente del método que utilice para salir de R, cuando lo haga por primera vez, probablemente R le preguntará si desea guardar la “imagen del espacio de trabajo”. Hablaremos mucho más sobre cargar y guardar datos en la Sección 4.5, pero pensé que sería mejor que cubrimos esto rápidamente, de lo contrario, se molestará cuando cierre R al final del capítulo. Si está utilizando Rstudio , verá un cuadro de diálogo que se parece al que se muestra en la Figura 3.5. Si está utilizando una interfaz basada en texto , verá esto: 

> \> q ( )

¿Guardar imagen del espacio de trabajo? [s / n / c]:  
La parte y / n / c aquí es la abreviatura de "sí / no / cancelar". Escriba y si desea guardar, n si no lo hace y c si ha cambiado de opinión y no quiere salir después de todo. 

¿Qué significa esto realmente? Lo que sucede es que R quiere saber si desea guardar todas esas variables que ha estado creando, para poder usarlas más tarde. Parece una gran idea, por lo que es muy tentador escribir y o hacer clic en el botón "Guardar". Para ser honesto, aunque, muy rara vez hago esto, y que tipo de me molesta un poco ... lo que realmente está pidiendo R es si lo desea almacenar estas variables en un archivo de datos “por defecto”, que automáticamente se recarga para usted la próxima vez que abra R. Y, francamente, si quisiera guardar las variables, ya las habría guardado antes de intentar salir. No solo eso, los habría guardado en una ubicación de mi elección, para poder encontrarlos nuevamente más tarde. Así que personalmente nunca me preocupo por esto.

De hecho, cada vez que instalo R en una máquina nueva, una de las primeras cosas que hago es cambiar la configuración para que nunca vuelva a preguntarme. Puede hacer esto en Rstudio muy fácilmente: use el sistema de menús para encontrar la opción Rstudio ; el cuadro de diálogo que aparece le dará una opción para decirle a R que nunca más se queje de esto (vea la Figura 3.6). En una Mac, puede abrir esta ventana yendo al menú " Rstudio " y seleccionando "Preferencias". En una máquina con Windows, vaya al menú "Herramientas" y seleccione "Opciones globales". En la pestaña "General", verá una opción que dice "Guardar espacio de trabajo en. Rdata a la salida ”. De forma predeterminada, se establece en "preguntar". Si desea que R deje de preguntar, cámbielo a "nunca". 

## Resumen
Cada libro que trata de presentar ideas básicas de programación a los principiantes tiene que cubrir aproximadamente los mismos temas y aproximadamente en el mismo orden. El mío no es una excepción, por lo que en la gran tradición de hacerlo de la misma manera que todos los demás lo hicieron, este capítulo cubrió los siguientes temas:   

- Empezando. Descargamos e instalamos R y Rstudio (Sección 3.1).

- Comandos básicos. Hablamos un poco sobre la lógica de cómo funciona R y, en particular, sobre cómo escribir comandos en la consola R (Sección 3.2), y al hacerlo aprendimos cómo realizar cálculos básicos usando los operadores aritméticos +, -, *, / y ^ . (Sección 3.3) 

- Introducción a las funciones. Vimos varias funciones diferentes, tres que se utilizan para realizar cálculos numéricos (sqrt (), abs (), round (); Sección 3.5), una que se aplica al texto ( nchar (); Sección 3.8.1) y una que funciona con cualquier variable (length (); Sección 3.7.5). Al hacerlo, hablamos un poco sobre cómo funcionan los nombres de los argumentos y aprendimos sobre los valores predeterminados para los argumentos. (Sección 3.5.1)

- Introducción a las variables. Aprendimos la idea básica detrás de las variables y cómo asignar valores a las variables usando el operador de asignación <- (Sección 3.4). También aprendimos cómo crear vectores usando la función de combinación c ( ). (Sección 3.7)

- Tipos de datos. Aprendió la distinción entre datos numéricos, de caracteres y lógicos; incluyendo los conceptos básicos de cómo ingresar y usar cada uno de ellos. (Secciones 3.4 a 3.9) 

- Operaciones lógicas. Aprendí a usar los operadores lógicos = = ,! =, <,>, <=, =>,! , & y | . (Sección 3.9). Y aprendí a usar la indexación lógica. (Sección 3.10) 

Todavía no hemos llegado a nada que se parezca a un "conjunto de datos", por supuesto. Quizás el próximo Capítulo nos acerque un poco más...


