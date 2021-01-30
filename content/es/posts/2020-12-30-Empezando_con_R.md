---
title: "Capítulo 3: Empezando con R (1ra parte)"
date: 2020-12-30T18:20:17-08:00
publishdate: 2020-12-31T18:29:17-08:00
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
- Aprendiendo estadística con R
categories:
- Programación
image: images/learning/cap_03.png
---

{{< featuredImage >}} 

---

<style>
body {
text-align: justify}
</style>

<a id="id-01"> </a>

En este capítulo discutiré cómo empezar a usar R. Hablaré brevemente sobre cómo descargar e instalar R, pero la mayor parte del capítulo se centrará en que empiece a escribir comandos R. Nuestro objetivo en este capítulo no es aprender ningún concepto estadístico: solo estamos tratando de aprender los conceptos básicos de cómo funciona R y sentirnos cómodos interactuando con el sistema. Para hacer esto, pasaremos un poco de tiempo usando R como una simple calculadora, ya que eso es lo más fácil de hacer con R. Al hacerlo, obtendrá una idea de cómo es trabajar en R. A partir de ahí, presentaré algunas ideas de programación muy básicas: en particular, hablaré sobre la idea de definir variables para almacenar información y algunas cosas que puede hacer con estas variables. 

Sin embargo, antes de entrar en detalles, vale la pena hablar un poco sobre por qué es posible que desee usar R. Dado que estás leyendo esto, probablemente tengas tus propias razones. Sin embargo, si esas razones son "porque eso es lo que usa mi clase de estadísticas", podría valer la pena explicar un poco por qué su profesor ha elegido usar R para la clase. Por supuesto, realmente no sé por qué otras personas eligen R, así que realmente estoy hablando de por qué lo uso.

- Es algo obvio, pero vale la pena decirlo de todos modos: hacer sus estadísticas en una computadora es más rápido, más fácil y más poderoso que hacer estadísticas a mano. Las computadoras sobresalen en tareas repetitivas sin sentido, y muchos cálculos estadísticos son tanto inconscientes como repetitivos. Para la mayoría de las personas, la única razón para hacer cálculos estadísticos con lápiz y papel es con fines de aprendizaje. En mi clase, de vez en cuando sugiero hacer algunos cálculos de esa manera, pero el único valor real es pedagógico. Le ayuda a tener una "idea" de las estadísticas para hacer algunos cálculos usted mismo, por lo que vale la pena hacerlo una vez. ¡Pero solo una vez!  

- Hacer estadísticas en una hoja de cálculo (por ejemplo, Microsoft Excel) es generalmente una mala idea a largo plazo. Aunque es probable que muchas personas se sientan más familiarizadas con ellos, las hojas de cálculo son muy limitadas en términos de los análisis que le permiten hacer. Si adquiere el hábito de intentar realizar su análisis de datos de la vida real utilizando hojas de cálculo, entonces se ha metido en un agujero muy profundo.  

- Evitar el software propietario es una muy buena idea. Hay muchos paquetes comerciales que puedes comprar, algunos de los cuales me gustan y otros no. Suelen tener un aspecto muy brillante y, en general, muy potentes (mucho más potentes que las hojas de cálculo). Sin embargo, también son muy caros: por lo general, la empresa vende "versiones para estudiantes" (versiones paralizadas de lo real) a muy bajo precio; venden “versiones educativas” con toda la potencia a un precio que me hace estremecer; y venden licencias comerciales a un precio asombrosamente alto. El modelo de negocio aquí es absorberlo durante sus días de estudiante y luego dejarlo dependiente de sus herramientas cuando salga al mundo real. Es difícil culparlos por intentarlo, pero personalmente no estoy a favor de desembolsar miles de dólares si puedo evitarlo. Y puede evitarlo: si utiliza paquetes como R que son de código abierto y gratuitos, nunca se verá atrapado en el pago de tarifas de licencia exorbitantes.  

- Algo que quizás no aprecie ahora, pero que le encantará más adelante si hace algo que implique el análisis de datos, es el hecho de que R es altamente extensible. Cuando descarga e instala R, obtiene todos los "paquetes" básicos, y estos son muy poderosos por sí mismos. Sin embargo, debido a que R es tan abierto y tan ampliamente utilizado, se ha convertido en una especie de herramienta estándar en estadística, por lo que mucha gente escribe sus propios paquetes que amplían el sistema. Y estos también están disponibles gratuitamente. Una de las consecuencias de esto, me he dado cuenta, es que si abres un libro de texto avanzado (es decir, uno reciente) en lugar de libros de texto introductorios, es que muchos de ellos usan R. En otras palabras, si aprendes cómo hacer sus estadísticas básicas en R, entonces está mucho más cerca de poder utilizar los métodos más avanzados de lo que estaría si hubiera comenzado con un sistema "más simple": así que si quiere convertirse en Un verdadero experto en análisis de datos psicológicos, aprender R es un muy buen uso de su tiempo. 

- Relacionado con el punto anterior: R es un lenguaje de programación real. A medida que mejora en el uso de R para el análisis de datos, también está aprendiendo a programar. Para algunas personas, esto puede parecer algo malo, pero en realidad, la programación es una habilidad de investigación central en muchas de las ciencias sociales y del comportamiento . Piense en cuántas encuestas y experimentos se realizan en línea o se presentan en computadoras. Piense en todos esos entornos sociales en línea que podría interesarle estudiar; y tal vez recopilar datos de forma automatizada. Piense en sistemas de inteligencia artificial, visión por computadora y reconocimiento de voz. Si alguna de estas son cosas en las que cree que le gustaría participar, es decir, como alguien que "investiga en psicología", necesitará saber un poco de programación. Y si aún no sabe cómo programar, entonces aprender a hacer estadísticas usando R es una buena manera de comenzar.

Esas son las principales razones por las que uso R. No está exento de defectos: no es fácil de aprender y tiene algunas peculiaridades muy molestas con las que todos estamos bastante atrapados, pero en general creo que las fortalezas superan la debilidad; más que cualquier otra opción que haya encontrado hasta ahora.



---

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

{{< highlight R >}}

R version 3.0.2 (2013-09-25) -- "Frisbee Sailing"  
Copyright (C) 2013 The R Foundation for Statistical Computing  
Platform: x86_64-apple-darwin10.8.0 (64-bit)  
R is free software and comes with ABSOLUTELY NO WARRANTY.  
You are welcome to redistribute it under certain conditions.  
Type ’license()’ or ’licence()’ for distribution details.  
Natural language support but running in an English locale  
R is a collaborative project with many contributors.  
Type ’contributors()’ for more information and  
’citation()’ on how to cite R or R packages in publications.  
Type ’demo()’ for some demos, ’help()’ for on-line help, or  
’help.start()’ for an HTML browser interface to help.  
Type ’q()’ to quit R.

{{< /highlight >}}


La mayor parte de este texto carece de interés y, al hacer análisis de datos reales , nunca le prestará mucha atención. La parte importante es esta ...

{{< highlight R >}}
>

{{< /highlight >}}

... que tiene un cursor intermitente al lado. Ese es el símbolo del sistema. Cuando vea esto, significa que R está esperando pacientemente a que haga algo.

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Escribir comandos en la consola R
Una de las cosas más fáciles que puede hacer con R es usarlo como una calculadora simple, por lo que es un buen lugar para comenzar. Por ejemplo, intente escribir 10 + 20 y presione enter. 6 Cuando hace esto, ha ingresado un comando y R "ejecutará" ese comando. Lo que ve en la pantalla ahora será esto:


{{< highlight R >}}
>10 + 20  
[1] 30

{{< /highlight >}}

No hay muchas sorpresas en este extracto. Pero hay algunas cosas de las que vale la pena hablar, incluso con un ejemplo tan simple. En primer lugar, es importante que comprenda cómo leer el extracto. En este ejemplo, lo que escribí fue la parte 10 + 20. No escribí el símbolo >: es solo el símbolo del sistema R y no es parte del comando real. Y tampoco escribí la parte [1] 30. Eso es lo que imprimió R en respuesta a mi comando. En segundo lugar, es importante comprender cómo se formatea la salida. Obviamente, la respuesta correcta a la suma 10 + 20 es 30, y no es sorprendente que R lo haya impreso como parte de su respuesta. Pero también está impresa esta parte [1], que probablemente no tenga mucho sentido para ti en este momento. Vas a ver eso mucho. Hablaré sobre lo que esto significa con un poco más de detalle más adelante, pero por ahora puedes pensar en [1] 30 como si R estuviera diciendo “la respuesta a la primera pregunta que hiciste es 30”. Eso no es del todo cierto, pero está lo suficientemente cerca por ahora. Y en cualquier caso, no es muy interesante en este momento: solo le pedimos a R que calcule una cosa, por lo que obviamente solo hay una respuesta impresa en la pantalla. Más adelante esto cambiará y la parte [1] comenzará a tener un poco más de sentido. Por ahora, simplemente no quiero que se confunda o se preocupe.
 
### Tenga mucho cuidado de evitar errores tipográficos
Antes de pasar a hablar sobre otros tipos de cálculos que podemos hacer con R, hay algunas otras cosas que quiero señalar. Lo primero es que, aunque R es un buen software, sigue siendo software. Es bastante estúpido y, como es estúpido, no puede manejar errores tipográficos. Se da por sentado que tu intención era escribir exactamente lo que escribiste. Por ejemplo, suponga que olvidó presionar la tecla Mayús al intentar escribir + y, como resultado, su comando terminó siendo 10 = 20 en lugar de 10 + 20. Esto es lo que sucede:


{{< highlight R >}}
> 10 = 20  
Error in 10 = 20 : invalid (do_set) left-hand side to assignment

{{< /highlight >}}

Lo que sucedió aquí es que R ha intentado interpretar 10 = 20 como un comando y escupe un mensaje de error porque el comando no tiene ningún sentido. Cuando un humano mira esto, y luego mira su teclado y ve que + y = están en la misma tecla, es bastante obvio que el comando fue un error tipográfico. Pero R no sabe esto, así que se enoja. Y, si lo miras desde su perspectiva, esto tiene sentido. Todo lo que R "sabe" es que 10 es un número legítimo, 20 es un número legítimo y = también es una parte legítima del lenguaje. En otras palabras, desde su perspectiva, esto realmente parece que el usuario quería escribir 10 = 20, ya que todas las partes individuales de esa declaración son legítimas y es demasiado estúpido para darse cuenta de que probablemente sea un error tipográfico. Por lo tanto, R confía en que esto es exactamente lo que quisiste decir... solo “descubre” que el comando es una tontería cuando intenta seguir tus instrucciones, con errores tipográficos y todo. Y luego lloriquea y escupe un error.  
Aún más sutil es el hecho de que algunos errores tipográficos no producirán ningún error, porque resulta que corresponden a comandos R "bien formados". Por ejemplo, suponga que no solo me olvidé de presionar la tecla de mayúsculas al intentar escribir 10 + 20, sino que también logré presionar la tecla junto a la que quería. El error tipográfico resultante produciría el comando 10 - 20. Claramente, R no tiene forma de saber que pretendías **sumar** 20 a 10, no **restar** 20 de 10, así que lo que sucede esta vez es esto:

{{< highlight R >}}
>10 - 20  
[1] -10

{{< /highlight >}}


En este caso, R produce la respuesta correcta, pero a la pregunta equivocada.  
Hasta cierto punto, estoy diciendo lo obvio aquí, pero es importante. Las personas que escribieron R son inteligentes. Tú, el usuario, eres inteligente. Pero R en sí es tonto. Y debido a que es tonto, tiene que ser obediente sin pensar. Hace exactamente lo que le pide que haga. No hay equivalente a "autocorrección" en R, y por una buena razón. Cuando se hacen cosas avanzadas, e incluso las estadísticas más simples son bastante avanzadas en muchos sentidos, es peligroso permitir que un autómata sin sentido como R intente anular al usuario humano. Pero debido a esto, es su responsabilidad tener cuidado. Asegúrese siempre de escribir exactamente lo que quiere decir. Cuando se trata de computadoras, no es suficiente escribir “aproximadamente” lo correcto. En general, debes ser absolutamente preciso en lo que le dices a R ... como todas las máquinas, es demasiado estúpido para ser algo más que absurdamente literal en su interpretación.
 
### R es (un poco) flexible con espaciado
Por supuesto, ahora que he sido tan tenso acerca de la importancia de ser siempre preciso, debo señalar que hay algunas excepciones. O, más exactamente, hay algunas situaciones en las que R muestra un poco más de flexibilidad de lo que sugiere mi descripción anterior. Lo primero que R es lo suficientemente inteligente como para hacer es ignorar el espaciado redundante. Lo que quiero decir con esto es que, cuando escribí 10 + 20 antes, igualmente podría haber hecho esto

{{< highlight R >}}
> 10 +    20  
[1] 30

{{< /highlight >}}

o esto

{{< highlight R >}}
> 10 + 20  
[1] 30

{{< /highlight >}}

y obtendría exactamente la misma respuesta. Sin embargo, eso no significa que pueda insertar espacios en cualquier lugar antiguo. Cuando miramos la documentación de inicio en la Sección 3.1.5, sugirió que podría escribir citation ( ) para obtener información sobre cómo citar R. Si lo hago ...

{{< highlight R >}}
> citation ( )  
To cite R in publications use:  
  R Core Team (2013). R: A language and environment  
  for statistical computing. R Foundation for  
  Statistical Computing, Vienna, Austria. URL  
  http://www.R-project.org/.  
  BLAH BLAH BLAH  
We have invested a lot of time and effort in creating  
R, please cite it when using it for data analysis. See  
also ?citation("pkgname")? for citing R packages

{{< /highlight >}}

... me dice que cite el manual de R (R Core Team, 2013). Obviamente, la parte BLAH BLAH BLAH no es en realidad parte de lo que imprime R: cuando ves eso significa que he eliminado algunas partes de la salida que no creo que sean muy interesantes o relevantes. Haré mucho eso. De todos modos, volviendo a mi punto original, veamos qué sucede cuando intento cambiar el espaciado. Si inserto espacios entre la palabra y el paréntesis, o dentro de los paréntesis, entonces todo está bien. Es decir, cualquiera de estos dos comandos

{{< highlight R >}}
> citation ()  
> citation (  )

{{< /highlight >}}

producirá exactamente la misma respuesta. Sin embargo, lo que no puedo hacer es insertar espacios en el medio de la palabra. Si trato de hacer esto, R se enoja:

{{< highlight R >}}
> citat ion()   
Error: unexpected symbol in "citat ion"

{{< /highlight >}}

A lo largo de este libro, variaré un poco la forma en que utilizo el espaciado, solo para darle una idea de las diferentes formas en que se puede usar el espaciado. Sin embargo, intentaré no hacerlo demasiado, ya que generalmente se considera una buena práctica ser consistente en la forma en que formatea los comandos.
 
### R a veces puede decir que aún no has terminado (pero no a menudo)
Una cosa más que debo señalar. Si presiona enter en una situación en la que es "obvio" para R que no ha terminado de escribir el comando, R es lo suficientemente inteligente como para seguir esperando. Por ejemplo, si escribe 10 + y luego presiona Intro, incluso R es lo suficientemente inteligente como para darse cuenta de que probablemente quería ingresar otro número. Así que esto es lo que sucede:

{{< highlight R >}}
> 10+  
+

{{< /highlight >}}

y hay un cursor parpadeante junto al signo más. Lo que esto significa es que R todavía está esperando que termines. “Piensa” que todavía estás escribiendo tu comando, por lo que aún no ha intentado ejecutarlo. En otras palabras, este signo más es en realidad otro símbolo del sistema. Es diferente del habitual (es decir, el símbolo >) para recordarle que R va a "agregar" lo que escriba ahora a lo que escribió la última vez. Por ejemplo, si sigo escribiendo 3 y presiono enter, lo que obtengo es esto: 

{{< highlight R >}}
> 10+  
+ 20  
[1] 30

{{< /highlight >}}

Y en lo que respecta a R, esto es exactamente lo mismo que si hubiera escrito 10 + 20. De manera similar, considere el comando citation ( ) del que hablamos en la sección anterior. Suponga que presiona enter después de escribir la cita (. Una vez más, R es lo suficientemente inteligente como para darse cuenta de que debe haber más por venir, ya que debe agregar el carácter ), por lo que espera. Incluso puedo presionar enter varias veces y seguirá esperando:

{{< highlight R >}}
> cita (  
+  
+  
+)

{{< /highlight >}}

Haré mucho uso de esto en este libro. Muchos de los comandos que tendremos que escribir son bastante largos y visualmente son un poco más fáciles de leer si los divido en varias líneas. Si comienza a hacer esto usted mismo, eventualmente se meterá en problemas (nos pasa a todos). Tal vez empiece a escribir un comando y luego se dé cuenta de que ha cometido un error. Por ejemplo,

{{< highlight R >}}
> citblation (  
+  
+

{{< /highlight >}}

Probablemente prefieras que R no intente ejecutar este comando, ¿verdad? Si desea salir de esta situación, simplemente presione la tecla 'Esc'. R lo regresará al símbolo del sistema normal (es decir, >) sin intentar ejecutar el comando fallido.  
Dicho esto, no es frecuente que R sea lo suficientemente inteligente como para decir que vendrán más. Por ejemplo, de la misma manera que no puedo agregar un espacio en el medio de una palabra, tampoco puedo presionar Enter en el medio de una palabra. Si presiono enter después de escribir citat , aparece un error, porque R cree que estoy interesado en un "objeto" llamado citat y no puedo encontrarlo:

{{< highlight R >}}
> citat  
Error: object ’citat’ not found

{{< /highlight >}}

¿Qué pasa si escribí una cita y presiono enter? En este caso obtenemos algo muy extraño, algo que definitivamente no queremos, al menos en esta etapa. Esto es lo que sucede:

{{< highlight R >}}
> citation  
function (package = "base", lib.loc = NULL, auto = NULL)
{
dir <- system.file(package = package, lib.loc = lib.loc)
if (dir == "")
stop(gettextf("package ’%s’ not found", package), domain = NA)
BLAH BLAH BLAH

{{< /highlight >}}

donde el BLAH BLAH BLAH continúa durante bastante tiempo, y aún no sabes lo suficiente R para entender lo que realmente significa todo este galimatías. Esta salida incomprensible puede resultar bastante intimidante para los usuarios novatos y, lamentablemente , es muy fácil olvidarse de escribir los paréntesis; por lo que es casi seguro que lo hará por accidente. No entre en pánico cuando esto suceda. Simplemente ignore el galimatías. A medida que adquiera más experiencia, este galimatías comenzará a tener sentido y le resultará muy útil imprimirlo. Pero por ahora, intente recordar agregar los paréntesis al escribir sus comandos.

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---
 
## Hacer cálculos simples con R
Bien, ahora que hemos discutido algunos de los tediosos detalles asociados con la escritura de comandos R, volvamos a aprender cómo usar el software estadístico más poderoso del mundo como una calculadora de $2. Hasta ahora, todo lo que sabemos hacer es sumar. Claramente, una calculadora que solo hiciera sumas sería un poco estúpida, así que debería decirte cómo realizar otros cálculos simples usando R. Pero primero, algo más de terminología. La suma es un ejemplo de una "operación" que puede realizar (específicamente, una operación aritmética), y el operador que la realiza es +. Para las personas con experiencia en programación o matemáticas, esta terminología probablemente se sienta bastante natural, pero para otras personas puede parecer que estoy tratando de hacer que algo muy simple (suma) suene más complicado de lo que es (llamándolo una operación aritmética). Hasta cierto punto, eso es cierto: si la suma fuera la única operación que nos interesa, sería un poco tonto introducir toda esta terminología adicional. Sin embargo, a medida que avancemos, comenzaremos a usar más y más tipos diferentes de operaciones, por lo que probablemente sea una buena idea aclarar el lenguaje ahora, ¡mientras seguimos hablando de conceptos muy familiares como la suma!

<caption>Tabla 3.1: Operaciones aritméticas básicas en R. Estos cinco operadores se usan con mucha frecuencia a lo largo del texto, por lo que es importante familiarizarse con ellos desde el principio. También hay otros, de los que hablaré en el capítulo 7.</caption>

| operación  | operador | ejemplo de entrada | ejemplo de respuesta  |
| :------------ | :-----------: | -------------------: |-------------------: |
| suma     | +          |10 + 2 | 12 |
| resta    | -      | 9 - 3 | 6    |
| multiplicación  | * | 5 * 5 | 25 |
| división     | /  | 10 / 3 | 3 |
| potencia     | ^  | 5 ^ 2  | 25 |
 
### Sumar, restar, multiplicar y dividir
Entonces, ahora que tenemos la terminología, aprendamos a realizar algunas operaciones aritméticas en R. Para ello, la Tabla 3.1 enumera los operadores que corresponden a la aritmética básica que aprendimos en la escuela primaria: suma, resta, multiplicación y división. Como puede ver, R usa símbolos bastante estándar para denotar cada una de las diferentes operaciones que podría querer realizar: la suma se realiza usando el **operador** +, la resta se realiza mediante el operador -, y así sucesivamente. Entonces, si quisiera averiguar qué es 57 por 61 (¿y quién no?), puedo usar R en lugar de una calculadora, así:

{{< highlight R >}}
> 57 * 61  
[1] 3477

{{< /highlight >}}

Eso es útil.

### Tomando poderes
Las primeras cuatro operaciones enumeradas en la tabla 3.1 son cosas que todos aprendimos en la escuela primaria, pero no son las únicas operaciones aritméticas integradas en R. Hay otras tres operaciones aritméticas que probablemente debería mencionar: tomar poderes, hacer división de enteros y calcular un módulo. De los tres, el único que tiene una importancia real para los propósitos de este libro es tomar poderes, así que discutiré ese uno aquí: los otros dos se analizan en el Capítulo 7.  
Para aquellos de ustedes que todavía pueden recordar sus matemáticas de la escuela secundaria , esto debería resultarles familiar. Pero para algunas personas las matemáticas de la escuela secundaria fueron hace mucho tiempo, y otros de nosotros no escuchamos con atención en la escuela secundaria. No es complicado. Como estoy seguro de que todos probablemente recordarán el momento en que lean esto, el acto de multiplicar un número x por sí mismo n veces se llama “elevar x a la enésima potencia”. Matemáticamente, esto se escribe como x n. Algunos valores de n tienen nombres especiales: en particular, x 2 se llama x al cuadrado, y x 3 se llama x al cubo. Entonces, la cuarta potencia de 5 se calcula así:  



> 5<sup>4</sup> = 5 x 5 x 5 x 5 



Una forma en la que podríamos calcular 5<sup>4</sup> en R sería escribir la multiplicación completa como se muestra en la ecuación anterior. Es decir, podríamos hacer esto

{{< highlight R >}}
> 5 * 5 * 5 * 5  
[1] 625

{{< /highlight >}}

pero parece un poco tedioso. De hecho, sería muy molesto si quisiera calcular 5<sup>15</sup>, ya que el comando terminaría siendo bastante largo. Por lo tanto, para hacernos la vida más fácil, utilizamos el operador de energía en su lugar. Cuando hacemos eso, nuestro comando para calcular 5<sup>4</sup> es así:

{{< highlight R >}}
> 5 ^ 4  
[1] 625

{{< /highlight >}}

Más fácil.
 
### Realización de cálculos en el orden correcto
Bueno. En este punto, ya sabe cómo tomar una de las piezas de software estadístico más poderosas del mundo y usarla como una calculadora de 2. Y como beneficio adicional, ha aprendido algunos conceptos de programación muy básicos. Eso no es nada (podría argumentar que se acaba de ahorrar 2) pero, por otro lado, tampoco es mucho. Para usar R de manera más efectiva, necesitamos introducir más conceptos de programación.  
En la mayoría de las situaciones en las que desee utilizar una calculadora, es posible que desee realizar varios cálculos. R le permite hacer esto, simplemente escribiendo comandos más largos. De hecho, ya hemos visto un ejemplo de esto antes, cuando escribí 5 * 5 * 5 * 5. Sin embargo, probemos un ejemplo ligeramente diferente:

{{< highlight R >}}
> 1 + 2 * 4  
[1] 9

{{< /highlight >}}

Claramente, esto tampoco es un problema para R. Sin embargo, vale la pena detenerse un segundo y pensar en lo que acaba de hacer R. Claramente, dado que nos dio una respuesta de 9, debe haber multiplicado 2 * 4 (para obtener una respuesta intermedia de 8) y luego sumar 1 a eso. Pero, supongamos que hubiera decidido ir de izquierda a derecha: si R hubiera decidido sumar 1 + 2 (para obtener una respuesta intermedia de 3) y luego multiplicado por 4, habría obtenido una respuesta de 12.  
Para responder a esto, necesita conocer el orden de operaciones que usa R. Si recuerdas las clases de matemáticas de la secundaria , en realidad es el mismo orden que te enseñaron cuando estabas en la escuela: el orden "BEDMAS". 9 Es decir, primero calcule las cosas dentro de corchetes () (Brackets), luego calcule los exponentes ^, luego la división / y la multiplicación *, luego la adición + y la sustracción -. Entonces, para continuar con el ejemplo anterior, si queremos forzar a R a calcular la parte 1 + 2 antes de la multiplicación, todo lo que tendríamos que hacer es encerrarlo entre corchetes:

{{< highlight R >}}
> (1 + 2) * 4  
[1] 12

{{< /highlight >}}

Esto es algo bastante útil de poder hacer. La única otra cosa que debo señalar sobre el orden de las operaciones es qué esperar cuando tienes dos operaciones que tienen la misma prioridad: es decir, ¿cómo resuelve R los lazos? Por ejemplo, la multiplicación y la división son en realidad la misma prioridad, pero ¿qué debemos esperar cuando le damos a R un problema como 4/2 * 3 para resolver? Si evalúa primero la multiplicación y luego la división, calcularía un valor de dos tercios. Pero si evalúa primero la división calcula un valor de 6. La respuesta, en este caso, es que R va de izquierda a derecha, por lo que en este caso el paso de división vendría primero:

{{< highlight R >}}
> 4/2 * 3  
[1] 6

{{< /highlight >}}

Dicho todo lo anterior, es útil recordar que los corchetes siempre son lo primero. Por lo tanto, si alguna vez no está seguro sobre el orden en el que R hará las cosas, una solución fácil es incluir primero entre paréntesis lo que desea que haga. No hay nada que le impida escribir (4/2) * 3. Al encerrar la división entre corchetes , aclaramos qué se supone que debe suceder primero. En este caso, no lo habría necesitado, ya que R habría hecho la división primero de todos modos, pero cuando recién comienza, ¡es mejor asegurarse de que R haga lo que quiere!

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---
 
## Almacenando un número como variable
Una de las cosas más importantes que se pueden hacer en R (o cualquier lenguaje de programación, para el caso) es almacenar información en variables. Las variables en R no son exactamente lo mismo que las variables de las que hablamos en el último capítulo sobre métodos de investigación, pero son similares. A un nivel conceptual, puede pensar en una variable como una *etiqueta* para una determinada información, o incluso varias piezas diferentes de información. Al hacer un análisis estadístico en R, todos sus datos (las variables que midió en su estudio) se almacenarán como variables en R, pero como verá más adelante en el libro, encontrará que también termina creando variables para otras cosas. Sin embargo, antes de profundizar en todos los detalles confusos de los conjuntos de datos y el análisis estadístico, veamos los conceptos básicos de cómo creamos variables y trabajamos con ellas.
 
### Asignación de variables usando <- y ->
Como hemos estado trabajando con números hasta ahora, comencemos por crear variables para almacenar nuestros números. Y como a la mayoría de la gente le gustan los ejemplos concretos, inventemos uno. Suponga que estoy tratando de calcular cuánto dinero voy a ganar con este libro. Es posible que desee almacenar varios números diferentes. En primer lugar, necesito averiguar cuántas copias venderé. Esto no es exactamente Harry Potter, así que supongamos que solo venderé una copia por alumno de mi clase. Eso son 350 ventas, así que creemos una variable llamada **ventas**. Lo que quiero hacer es asignar un **valor** a mi variable **ventas**, y ese valor debería ser 350. Hacemos esto usando el operador de asignación, que es < -. Así es como lo hacemos:

{{< highlight R >}}
> ventas <- 350

{{< /highlight >}}

Cuando presiona enter, R no imprime ninguna salida. Simplemente le brinda otro símbolo del sistema. Sin embargo, detrás de escena, R ha creado una variable llamada **ventas** y le ha dado un valor de **350**. Puede comprobar que esto ha sucedido pidiendo a R que imprima la variable en la pantalla. Y la forma más sencilla de hacerlo es escribir el nombre de la variable y presionar enter

{{< highlight R >}}
> ventas  
[1] 350

{{< /highlight >}}

Así que es bueno saberlo. Siempre que no recuerde lo que R tiene almacenado en una variable en particular, puede simplemente escribir el nombre de la variable y presionar enter.  
Bien, ahora sabemos cómo asignar variables. De hecho, hay algo más que debería saber. En primer lugar, una de las características curiosas de R es que hay varias formas diferentes de realizar asignaciones. Además del operador **<-**, también podemos usar **->** y **=**, y es muy importante comprender las diferencias entre ellos. Comencemos considerando **->**, ya que es el más fácil (discutiremos el uso de **=** en la Sección 3.5.1). Como es de esperar con solo mirar el símbolo, es casi idéntico a **<-**. Es solo que la flecha (es decir, la asignación) va de izquierda a derecha. Entonces, si quisiera definir mi variable de **ventas** usando **->**, lo escribiría así:

{{< highlight R >}}
> 350 -> ventas

{{< /highlight >}}

Esto tiene el mismo efecto: y **todavía** significa que solo voy a vender *350* copias. Aparte de esta diferencia superficial, **<-** y **->** son idénticos. De hecho, en lo que respecta a R, en realidad son el mismo operador, solo en una “forma izquierda” y una “forma derecha”.
 
### Hacer cálculos usando variables
Bien, volvamos a mi historia original. En mi búsqueda por hacerme rico, he escrito este libro de texto. Para averiguar qué tan buena es una estrategia, comencé a crear algunas variables en R. Además de definir una variable de ventas que cuente la cantidad de copias que voy a vender, también puedo crear una variable llamada **regalias**, que indica cómo Cuánto dinero obtengo por copia. Digamos que mis regalías son alrededor de $7 por libro:

{{< highlight R >}}
> ventas <- 350  
> regalias <- 7

{{< /highlight >}}
 
Lo bueno de las variables (de hecho, el objetivo de tener variables) es que podemos hacer cualquier cosa con una variable que deberíamos poder hacer con la información que almacena. Es decir, como R me permite multiplicar **350** por **7**

{{< highlight R >}}
> 350 * 7
[1] 2450

{{< /highlight >}}

también me permite multiplicar las **ventas** por **regalias**

{{< highlight R >}}
> ventas * regalias  
[1] 2450

{{< /highlight >}}

En lo que respecta a R, el comando **ventas \* regalias** es el mismo que el comando **350 \* 7**. No es sorprendente que pueda asignar el resultado de este cálculo a una nueva variable, a la que llamaré **ingresos**. Y cuando hacemos esto, el nuevo ingreso variable obtiene el valor **2450**. Así que hagamos eso, y luego hagamos que R imprima el valor de **ingresos** para que podamos verificar que se hizo lo que pedimos:

{{< highlight R >}}
> ingresos <- ventas * regalias  
> ingresos  
[1] 2450

{{< /highlight >}}

Eso es bastante sencillo. Una cosa un poco más sutil que podemos hacer es reasignar el valor de mi variable, en función de su valor actual. Por ejemplo, supongamos que uno de mis estudiantes (sin duda bajo la influencia de psicofármacos) ama tanto el libro que me dona 550 dólares extra. La forma más sencilla de capturar esto es mediante un comando como este:

{{< highlight R >}}
> ingresos <- ingresos + 550  
> ingresos  
[1] 3000  

{{< /highlight >}}

En este cálculo, R ha tomado el valor anterior de **ingresos** (es decir, 2450) y agregó 550 a ese valor, produciendo un valor de 3000. Este nuevo valor se asigna a la variable de **ingresos**, sobrescribiendo su valor anterior. En cualquier caso, ahora sabemos que espero ganar $3000 con esto. Muy dulce, podría pensar. O al menos, hasta que hago algunos cálculos más y averiguo cuál es el salario por hora implícito que estoy ganando.
 
### Reglas y convenciones para nombrar variables
En los ejemplos que hemos visto hasta ahora, mis nombres de variables (**ventas** e **ingresos**) solo han sido palabras en inglés escritas con letras minúsculas. Sin embargo, R permite mucha más flexibilidad cuando se trata de nombrar sus variables, como lo ilustra la siguiente lista de reglas 14:

- Los nombres de las variables solo pueden utilizar los caracteres alfabéticos en mayúsculas de la **A-Z**, así como los caracteres en minúsculas de la A a la z. También puede incluir caracteres numéricos del **0-9** en el nombre de la variable, así como el punto. o carácter de subrayado _. En otras palabras, puede usar **SaL.e_s** como nombre de variable (aunque no puedo pensar por qué querría hacerlo), pero no puede usar **Sales?**.          
- Los nombres de las variables no pueden incluir espacios: por lo tanto, **my sales** no es un nombre válido, pero **my.sales** sí lo es.      
- Los nombres de las variables distinguen entre mayúsculas y minúsculas: es decir, **Sales** y **sales** son nombres de variable diferentes.
- Los nombres de las variables deben comenzar con una letra o un punto. No puede usar algo como **_sales** o **1sales** como nombre de variable. Puede utilizar **.sales** como nombre de variable si lo desea, pero no suele ser una buena idea. Por convención, las variables que comienzan con un **.** se utilizan para fines especiales, por lo que debe evitar hacerlo.          
- Los nombres de las variables no pueden ser una de las palabras clave reservadas. Estos son nombres especiales que R necesita para mantenernos “a salvo” de nosotros, los meros usuarios, por lo que no puede usarlos como nombres de variables. Las palabras clave son: **if**, **else**, **repeat**, **while**, **function**, **for**, **in**, **next**, **break**, **TRUE**, **FALSE**, **NULL**, **Inf**, **NaN**, **NA**, NA_integer_, NA_real_, NA_complex_, y finalmente, NA_character_. No se sienta especialmente obligado a memorizarlos: si comete un error y trata de utilizar una de las palabras clave como nombre de variable, R se quejará como el pequeño autómata quejumbroso que es. 

Además de las reglas que R aplica, existen algunas convenciones informales que las personas tienden a seguir al nombrar variables. Uno de ellos ya ha visto: es decir, no use variables que comiencen con un punto. Pero hay varios más. No está obligado a seguir estas convenciones y hay muchas situaciones en las que es aconsejable ignorarlas, pero en general es una buena idea seguirlas cuando pueda:

- Utilice nombres de variables informativos. Como regla general, se prefiere el uso de nombres significativos como **ventas** e **ingresos** a los arbitrarios como **variable1** y **variable2**. De lo contrario, es muy difícil recordar cuál es el contenido de las diferentes variables y se vuelve difícil entender qué hacen realmente sus comandos.          
- Utilice nombres cortos de variables. Escribir es una molestia y a nadie le gusta hacerlo. Por eso, preferimos usar un nombre como **ventas** sobre un nombre como **ventas.para.este.libro.que.esta.leyendo**. Obviamente, existe un poco de tensión entre el uso de nombres informativos (que tienden a ser largos) y el uso de nombres cortos (que tienden a no tener sentido), así que use un poco de sentido común al intercambiar estas dos convenciones.          
- Utilice uno de los estilos de nomenclatura convencionales para nombres de variables de varias palabras. Supongamos que quiero nombrar una variable que almacena "mi nuevo salario". Obviamente, no puedo incluir espacios en el nombre de la variable, entonces, ¿cómo debo hacer esto? Hay tres convenciones diferentes que a veces ve que emplean los usuarios de R. En primer lugar, puede separar las palabras usando puntos, lo que le daría **my.new.salary** como nombre de variable. Alternativamente, puede separar palabras usando guiones bajos, como en **my_new_salary**. Finalmente, puede usar letras mayúsculas al principio de cada palabra (excepto la primera), lo que le da **myNewSalary** como nombre de variable. No creo que haya ninguna razón sólida para preferir uno sobre el otro, pero es importante ser coherente.          

<p style="text-align:right;">
Continúa en la siguiente entrada...
</p>

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

<p style="text-align:right;font-size:80%;">
Escrito por Navarro, Danielle; traducido por García-Mendívil, Helio A.
</p>
