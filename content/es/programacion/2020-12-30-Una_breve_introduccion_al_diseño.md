---
title: "Capítulo 2: Una breve introducción al diseño de investigación (1ra parte)"
date: 2020-12-30T18:18:17-08:00
publishdate: 2020-12-30T18:33:17-08:00
description: "En este capítulo, comenzaremos a pensar en las ideas básicas que se necesitan para diseñar un estudio, recopilar datos, verificar si la recopilación de datos funciona, etc."
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
image: images/learning/cap_02.png
---

{{< featuredImage >}}

---

<style>
body {
text-align: justify}
</style>

<a id="id-01"> </a>

En este capítulo, comenzaremos a pensar en las ideas básicas que se necesitan para diseñar un estudio, recopilar datos, verificar si la recopilación de datos funciona, etc. No le dará suficiente información para que pueda diseñar sus propios estudios, pero le dará muchas de las herramientas básicas que necesita para evaluar los estudios realizados por otras personas. Sin embargo, dado que el enfoque de este libro es mucho más el análisis de datos que la recopilación de datos, solo estoy dando una descripción muy breve. Tenga en cuenta que este capítulo es "especial" de dos formas. En primer lugar, es mucho más específico de la psicología que los capítulos posteriores. En segundo lugar, se centra mucho más en el problema científico de la metodología de la investigación y mucho menos en el problema estadístico del análisis de datos. Sin embargo, los dos problemas están relacionados entre sí, por lo que es tradicional que los libros de texto de estadísticas discutan el problema con un pequeño detalle. Este capítulo se basa en gran medida en Campbell y Stanley (1963) para la discusión del diseño del estudio, y Stevens (1946) para la discusión de las escalas de medición. Las versiones posteriores intentarán ser más precisas en las citas.

## Introducción a la medición psicológica {#Cap2.1}
 
Lo primero que hay que entender es que la recopilación de datos se puede considerar como una especie de <span style="color: BlueViolet;">medida</span>. Es decir, lo que estamos tratando de hacer aquí es medir algo sobre el comportamiento humano o la mente humana. ¿Qué quiero decir con "medición"?
 
### Algunas reflexiones sobre la medición psicológica
 
La medición en sí es un concepto sutil, pero básicamente se trata de encontrar alguna forma de asignar números, etiquetas o algún otro tipo de descripciones bien definidas a las "cosas". Por lo tanto, cualquiera de los siguientes contaría como medida psicológica:

{{< boxmd >}} 
- Mi **edad** es *33 años*.
- *No* me **gustan las anchoas*.
- Mi **género cromosómico** es *masculino*.
- Mi **género autoidentificado** es *masculino*. 

{{< /boxmd >}}
 
En la lista corta anterior, la parte en **negrita** es "lo que se va a medir", y la parte en *cursiva* es "la medida en sí". De hecho, podemos ampliar un poco esto, pensando en el conjunto de posibles medidas que podrían haber surgido en cada caso:

{{< boxmd >}}

- Mi **edad** (en años) podría haber sido *0*, *1*, *2*, *3*..., etc. El límite superior de lo que podría ser mi edad es un poco confuso, pero en la práctica estaría seguro al decir que el la edad más grande posible es *150*, ya que ningún ser humano ha vivido tanto tiempo.
- Cuando me preguntaron si me **gustan las anchoas**, podría haber dicho que *sí*, o *no*, o *no tengo opinión*, o *algunas veces sí*.
- Es casi seguro que mi **género cromosómico** sea *masculino* (*XY*) o *femenino* (*XX*), pero hay algunas otras posibilidades. También podría tener el *síndrome de Klinfelter* (*XXY*), que se parece más a los hombres que a las mujeres. E imagino que también hay otras posibilidades.
- Es muy probable que mi **género autoidentificado** sea *masculino* o *femenino*, pero no tiene por qué coincidir con mi género cromosómico. También puedo elegir identificarme con *ninguno* o llamarme explícitamente *transgénero*.

{{< /boxmd >}}

Como puede ver, para algunas cosas (como la edad) parece bastante obvio cuál debería ser el conjunto de medidas posibles, mientras que para otras cosas se vuelve un poco complicado. Pero quiero señalar que incluso en el caso de la edad de alguien, es mucho más sutil que esto. Por ejemplo, en el ejemplo anterior, asumí que estaba bien medir la edad en años. Pero si es un psicólogo del desarrollo, eso es demasiado burdo, por lo que a menudo mide la edad en *años y meses* (si un niño tiene 2 años y 11 meses, esto generalmente se escribe como “2; 11”). Si está interesado en los recién nacidos, es posible que desee medir la edad en *días desde el nacimiento*, tal vez incluso en *horas desde el nacimiento*. En otras palabras, la forma en que especifica los valores de medición permitidos es importante.
 
Mirando esto un poco más de cerca, también puede darse cuenta de que el concepto de "edad" no es tan preciso. En general, cuando decimos "edad", implícitamente queremos decir "el tiempo transcurrido desde el nacimiento". Pero esa no siempre es la forma correcta de hacerlo. Suponga que está interesado en cómo los bebés recién nacidos controlan los movimientos de sus ojos. Si está interesado en niños tan pequeños, también puede comenzar a preocuparse de que el "nacimiento" no sea el único momento significativo en el que preocuparse. Si Baby Alice nace 3 semanas antes de tiempo y Baby Bianca nace 1 semana tarde, ¿realmente tendría sentido decir que tienen la “misma edad” si los encontramos “2 horas después del nacimiento”? En cierto sentido, sí: por convención social, usamos el nacimiento como nuestro punto de referencia para hablar sobre la edad en la vida cotidiana, ya que define la cantidad de tiempo que la persona ha estado operando como una entidad independiente en el mundo, pero desde una perspectiva científica. eso no es lo único que nos importa. Cuando pensamos en la biología de los seres humanos, a menudo es útil pensar en nosotros mismos como organismos que han estado creciendo y madurando desde la concepción, y desde esa perspectiva, Alice y Bianca no tienen la misma edad en absoluto. Por lo tanto, es posible que desee definir el concepto de "edad" de dos formas diferentes: el tiempo transcurrido desde la concepción y el tiempo transcurrido desde el nacimiento. Cuando se trata de adultos, no hay mucha diferencia, pero si se trata de recién nacidos, sí.
 
Más allá de estos temas, está la cuestión de la metodología. ¿Qué "método de medición" específico va a utilizar para averiguar la edad de alguien? Como antes, hay muchas posibilidades diferentes:

{{< boxmd >}}

- Podrías preguntarle a la gente "¿cuántos años tienes?" El método de autoinforme es rápido, económico y fácil, pero solo funciona con personas con la edad suficiente para comprender la pregunta y algunas personas mienten sobre su edad.
- Puede preguntarle a una autoridad (p. Ej., Un padre) "¿Qué edad tiene su hijo?" Este método es rápido, y cuando se trata de niños no es tan difícil ya que los padres casi siempre están cerca. No funciona tan bien si quieres saber la "edad desde la concepción", ya que muchos padres no pueden decir con certeza cuándo tuvo lugar la concepción. Para eso, es posible que necesite una autoridad diferente (por ejemplo, un obstetra).
- Puede buscar registros oficiales, como certificados de nacimiento. Esto lleva mucho tiempo y es molesto, pero tiene sus usos (por ejemplo, si la persona ya está muerta).

{{< /boxmd >}}
 
### Operacionalización: definiendo su medida

Todas las ideas discutidas en la sección anterior se relacionan con el concepto de <span style="color: BlueViolet;">operacionalización</span>. Para ser un poco más precisos sobre la idea, la operacionalización es el proceso mediante el cual tomamos un concepto significativo pero algo vago y lo convertimos en una medida precisa. El proceso de operacionalización puede involucrar varias cosas diferentes:

{{< boxmd >}}

- Ser preciso sobre lo que está tratando de medir. Por ejemplo, ¿"edad" significa "tiempo desde el nacimiento" o "tiempo desde la concepción" en el contexto de su investigación?
- Determinar qué método utilizará para medirlo. ¿Utilizará el autoinforme para medir la edad, preguntarle a un padre o buscar un registro oficial? Si utiliza el autoinforme, ¿cómo formulará la pregunta?
- Definir el conjunto de valores permisibles que puede tomar la medición. Tenga en cuenta que estos valores no siempre tienen que ser numéricos, aunque a menudo lo son. Al medir la edad, los valores son numéricos, pero aún debemos pensar detenidamente qué números están permitidos. ¿Queremos la edad en años, años y meses, días, horas? Etc. Para otros tipos de medidas (por ejemplo, género), los valores no son numéricos. Pero, al igual que antes, debemos pensar en qué valores están permitidos. Si les pedimos a las personas que informen sobre su género, ¿qué opciones les permitimos elegir? ¿Es suficiente permitir solo "hombres" o "mujeres"? ¿Necesita una "otra" opción? ¿O no deberíamos dar a las personas opciones específicas y dejar que respondan con sus propias palabras? Y si abre el conjunto de valores posibles para incluir todas las respuestas verbales, ¿cómo interpretará sus respuestas?

{{< /boxmd >}}

La operacionalización es un negocio complicado y no existe una “única forma verdadera” de hacerlo. La forma en que elija hacer operativo el concepto informal de “edad” o “género” en una medición formal depende de para qué necesite utilizar la medición. A menudo, encontrará que la comunidad de científicos que trabaja en su área tiene algunas ideas bastante bien establecidas sobre cómo hacerlo. En otras palabras, la operacionalización debe analizarse caso por caso. Sin embargo, si bien hay muchos problemas que son específicos de cada proyecto de investigación individual, hay algunos aspectos que son bastante generales.
 
Antes de continuar, quiero tomarme un momento para aclarar nuestra terminología y, en el proceso, introducir un término más. Aquí hay cuatro cosas diferentes que están estrechamente relacionadas entre sí:

{{< boxmd >}}

- <span style="color: BlueViolet;">Una construcción teórica</span>. Esto es lo que está tratando de medir, como "edad", "género" o una "opinión". Una construcción teórica no se puede observar directamente y, a menudo, son un poco vagas.
- <span style="color: BlueViolet;">Una medida</span>. La medida se refiere al método o herramienta que utiliza para realizar sus observaciones. Una pregunta en una encuesta, una observación del comportamiento o un escáner cerebral podrían contar como una medida.
- <span style="color: BlueViolet;">Una operacionalización</span>. El término “operacionalización” se refiere a la conexión lógica entre la medida y el constructo teórico, o al proceso mediante el cual intentamos derivar una medida a partir de un constructo teórico.
- <span style="color: BlueViolet;">Una variable</span>. Finalmente, un nuevo término. Una variable es con lo que terminamos cuando aplicamos nuestra medida a algo en el mundo. Es decir, las variables son los "datos" reales con los que terminamos en nuestros conjuntos de datos.

{{< /boxmd >}}

En la práctica, incluso los científicos tienden a difuminar la distinción entre estas cosas, pero es muy útil tratar de comprender las diferencias.
 



<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Escalas de medida {#Cap2.2}
 
Como indica la sección anterior, el resultado de una medición psicológica se llama variable. Pero no todas las variables son del mismo tipo cualitativo y es muy útil comprender qué tipos existen. Un concepto muy útil para distinguir entre diferentes tipos de variables es lo que se conoce como <span style="color: BlueViolet;">escalas de medida</span>.
 
### Escala nominal
 
Una variable de <span style="color: BlueViolet;">escala nominal</span> (también denominada variable <span style="color: BlueViolet;">categórica</span>) es aquella en la que no existe una relación particular entre las diferentes posibilidades: para este tipo de variables no tiene ningún sentido decir que una de ellas es "mayor" o “Mejor” que cualquier otro, y no tiene ningún sentido promediarlos. El ejemplo clásico de esto es el "color de ojos". Los ojos pueden ser azules, verdes y marrones, entre otras posibilidades, pero ninguno de ellos es “mejor” que otro. Como resultado, sería realmente extraño hablar de un "color de ojos medio". Del mismo modo, el género también es nominal: el hombre no es mejor ni peor que la mujer, ni tiene sentido tratar de hablar de un "género medio". En definitiva, las variables de escala nominal son aquellas de las que lo único que se puede decir de las distintas posibilidades es que son distintas. Eso es.
 
Echemos un vistazo más de cerca a esto. Supongamos que estoy investigando cómo la gente se desplaza hacia y desde el trabajo. Una variable que tendría que medir sería qué tipo de transporte usa la gente para ir al trabajo. Esta variable de "tipo de transporte" podría tener bastantes valores posibles, incluidos: "tren", "autobús", "coche", "bicicleta", etc. Por ahora, supongamos que estas cuatro son las únicas posibilidades, y supongamos que cuando le pregunto a 100 personas cómo llegaron al trabajo hoy, y me sale esto:

| Transporte|Número de personas|
|:---|:----:|
|(1)Tren|12|
|(2)Bus|30|
|(3)Automovil|48|
|(4)Bicicleta|10|

 
Entonces, ¿cuál es el tipo de transporte promedio? Obviamente, la respuesta aquí es que no la hay. Es una pregunta tonta. Se puede decir que viajar en automóvil es el método más popular y viajar en tren es el método menos popular, pero eso es todo. Del mismo modo, observe que el orden en el que enumero las opciones no es muy interesante. Podría haber elegido mostrar los datos de esta manera


| Transporte|Número de personas|
|:---|:----:|
|(1)Automovil|48|
|(2)Tren|12|
|(3)Bicicleta|10|
|(4)Bus|30|
 
y nada cambia realmente.
 
<span style="color: BlueViolet;">Escala ordinal</span> Las variables de escala ordinal tienen un poco más de estructura que las variables de escala nominal, pero no mucho. Una variable de escala ordinal es aquella en la que existe una forma natural y significativa de ordenar las diferentes posibilidades, pero no se puede hacer nada más. El ejemplo habitual de una variable ordinal es "posición final en una carrera". Puede decir que la persona que terminó primero fue más rápida que la persona que terminó segundo, pero *no* sabe cuánto más rápido. Como consecuencia, sabemos que 1ro > 2do, y sabemos que 2do > 3ro, pero la diferencia entre 1ro y 2do puede ser mucho mayor que la diferencia entre 2do y 3ro. 

Aquí hay un ejemplo psicológicamente más interesante. Supongamos que estoy interesado en las actitudes de las personas hacia el cambio climático y les pido que elijan una de estas cuatro afirmaciones que más se acerque a sus creencias: 

{{< boxmd >}}

(1) Las temperaturas están aumentando, debido a la actividad humana 
(2) Las temperaturas están aumentando, pero nosotros no sé por qué 
(3) Las temperaturas están subiendo, pero no debido a los humanos 
(4) Las temperaturas no están subiendo 

{{< /boxmd >}}

Observe que estas cuatro afirmaciones tienen un orden natural, en términos de "la medida en que concuerdan con la ciencia actual". La afirmación 1 es una coincidencia cercana, la afirmación 2 es una coincidencia razonable, la afirmación 3 no es una coincidencia muy buena y la afirmación 4 está en fuerte oposición a la ciencia. Entonces, en términos de lo que me interesa (la medida en que la gente respalda la ciencia), puedo ordenar los elementos como 1 > 2 > 3 > 4. Dado que existe este orden, sería muy extraño enumerar los opciones como esta...

{{< boxmd >}}

(3) Las temperaturas están aumentando, pero no debido a los humanos 
(1) Las temperaturas están aumentando, debido a la actividad humana 
(4) Las temperaturas no están aumentando 
(2) Las temperaturas están aumentando, pero no sabemos por qué... porque parece violar la “estructura” natural de la pregunta.

{{< /boxmd >}}

Entonces, supongamos que le hice estas preguntas a 100 personas y obtuve las siguientes respuestas: Número de respuesta

{{< boxmd >}} 
|Respuesta|Número|
|:----|:---:|
|(1) Las temperaturas están aumentando debido a la actividad humana |51 | 
|(2) Las temperaturas están subiendo, pero no sabemos por qué |20  |
|(3) Las temperaturas están aumentando, pero no debido a los humanos |10 |
|(4) Las temperaturas no suben |19 |

{{< /boxmd >}}

Al analizar estos datos, parece bastante razonable tratar de agrupar (1), (2) y (3) juntos, y decir que 81 de cada 100 personas estaban dispuestas a respaldar *al menos parcialmente* la ciencia. Y *también* es bastante razonable agrupar (2), (3) y (4) juntos y decir que 49 de cada 100 personas registraron *al menos algún desacuerdo* con la visión científica dominante. Sin embargo, sería completamente extraño tratar de agrupar (1), (2) y (4) juntos y decir que 90 de 100 personas dijeron ... ¿qué? No hay nada sensato que le permita agrupar esas respuestas en absoluto.
 
Dicho esto, observe que si bien podemos usar el orden natural de estos elementos para construir agrupaciones sensibles, lo que *no podemos* hacer es promediarlos. Por ejemplo, en mi ejemplo simple aquí, la respuesta "promedio" a la pregunta es 1.97. Si puede decirme qué significa eso, me encantaría saberlo. ¡Porque eso me suena a galimatías!
 
### Escala de intervalo
 
A diferencia de las variables de escala nominal y ordinal, las variables de <span style="color: BlueViolet;">escala de intervalo</span> y de escala de razón son variables para las que el valor numérico es realmente significativo. En el caso de las variables de escala de intervalo, las *diferencias* entre los números son interpretables, pero la variable no tiene un valor cero "natural". Un buen ejemplo de una variable de escala de intervalo es medir la temperatura en grados centígrados. Por ejemplo, si ayer era 15 ° y hoy 18, entonces la diferencia de 3  ° entre los dos es realmente significativa. Además, esa diferencia de 3 ° es *exactamente igual* que la diferencia de 3 ° entre 7 ° y 10 °. En resumen, la suma y la resta son significativas para las variables de escala de intervalo.
 
Sin embargo, tenga en cuenta que 0 no significa "ninguna temperatura en absoluto": en realidad significa "la temperatura a la que el agua se congela", que es bastante arbitrario. Como consecuencia, no tiene sentido intentar multiplicar y dividir temperaturas. Es incorrecto decir que 20° es dos veces más caliente que 10 °, así como es extraño y sin sentido intentar afirmar que 20 ° es negativo dos veces más caliente que -10°.
 
De nuevo, veamos un ejemplo más psicológico. Supongamos que estoy interesado en observar cómo han cambiado las actitudes de los estudiantes universitarios de primer año con el tiempo. Obviamente, voy a querer registrar el año en el que comenzó cada alumno. Esta es una variable de escala de intervalo. Un estudiante que comenzó en 2003 llegó 5 años antes que un estudiante que comenzó en 2008. Sin embargo, sería una locura para mí dividir 2008 por 2003 y decir que el segundo estudiante comenzó “1.0024 veces más tarde” que el primero. Eso no tiene ningún sentido.
 
### Escala de proporción
 
El cuarto y último tipo de variable a considerar es una variable de <span style="color: BlueViolet;">escala de razón</span>, en la que cero realmente significa cero, y está bien multiplicar y dividir. Un buen ejemplo psicológico de una variable de escala de razón es el tiempo de respuesta (RT). En muchas tareas es muy común registrar la cantidad de tiempo que alguien tarda en resolver un problema o responder una pregunta, porque es un indicador de lo difícil que es la tarea. Suponga que Alan tarda 2.3 segundos en responder una pregunta, mientras que Ben tarda 3.1 segundos. Al igual que con una variable de escala de intervalo, la suma y la resta son significativas aquí. Ben realmente tardó 3.1 - 2.3 = 0.8 segundos más que Alan. Sin embargo, observe que la multiplicación y la división también tienen sentido aquí: Ben tardó 3.1 / 2,3 = 1.35 veces más que Alan para responder la pregunta. Y la razón por la que puede hacer esto es que, para una variable de escala de relación como RT, "cero segundos" realmente significa "nada de tiempo".
 
### Variables continuas versus discretas
 
Hay un segundo tipo de distinción que debe tener en cuenta, con respecto a los tipos de variables que puede encontrar. Ésta es la distinción entre variables continuas y variables discretas. La diferencia entre estos es la siguiente:

{{< boxmd >}}

- Una <span style="color: BlueViolet;">variable continua</span> es aquella en la que, para dos valores cualesquiera que pueda imaginar, siempre es lógicamente posible tener otro valor en el medio.
- Una <span style="color: BlueViolet;">variable discreta</span> es, en efecto, una variable que no es continua. Para una variable discreta, a veces sucede que no hay nada en el medio.

{{< /boxmd >}}

Estas definiciones probablemente parezcan un poco abstractas, pero son bastante simples una vez que ve algunos ejemplos. Por ejemplo, el tiempo de respuesta es continuo. Si Alan tarda 3.1 segundos y Ben 2.3 segundos para responder a una pregunta, entonces es posible que el tiempo de respuesta de Cameron se encuentre en el medio, tomando 3.0 segundos. Y, por supuesto, también sería posible que David tardara 3.031 segundos en responder, lo que significa que su RT estaría entre el de Cameron y el de Alan. Y aunque en la práctica podría ser imposible medir la RT con tanta precisión, ciertamente es posible en principio. Como siempre podemos encontrar un nuevo valor para RT entre otros dos, decimos que RT es continuo.
 
Las variables discretas ocurren cuando se viola esta regla. Por ejemplo, las variables de escala nominal son siempre discretas: no hay un tipo de transporte que se encuentre “entre” trenes y bicicletas, no en la forma matemática estricta de que 2.3 se ubica entre 2 y 3. Entonces el tipo de transporte es discreto. De manera similar, las variables de escala ordinal son siempre discretas: aunque el “2do lugar” se ubica entre el “1er lugar” y el “3er lugar”, no hay nada que lógicamente pueda ubicarse entre el “1er lugar” y el “2do lugar”. Las variables de escala de intervalo y escala de razón pueden ir en cualquier dirección. Como vimos anteriormente, el tiempo de respuesta (una variable de escala de proporción) es continuo. La temperatura en grados Celsius (una variable de escala de intervalo) también es continua. Sin embargo, el año en que asistió a la escuela (una variable de escala de intervalo) es discreto. No hay un año entre 2002 y 2003. La cantidad de preguntas que obtiene correctamente en una prueba de verdadero o falso (una variable de escala de razón) también es discreta: dado que una pregunta de verdadero o falso no le permite ser "parcialmente correcto”, no hay nada entre 5/10 y 6/10. La Tabla <a href="#tabla21">2.1</a> resume la relación entre las escalas de medición y la distinción discreta / continuidad. Las celdas con una marca de verificación corresponden a cosas que son posibles. Estoy tratando de recalcar este punto, porque (a) algunos libros de texto lo entienden mal y (b) la gente suele decir cosas como "variable discreta" cuando se refieren a "variable de escala nominal". Es muy lamentable.

<a id="tabla21"> </a>
Tabla 2.1 Relación entre escalas de medida y la distinción discreta/continua. Celdas marcadas corresponden a cosas que son posibles
||Continua|Discreta|
|:---|:---:|:---:|
|Nominal| | X |
|Ordinal||X|
|Intervalo|X|X|
|Ratio|X|X|
 
### Algunas complejidades
 
Bien, sé que te sorprenderá escuchar esto, pero... el mundo real es mucho más complicado de lo que sugiere este pequeño esquema de clasificación. Muy pocas variables en la vida real se incluyen en estas categorías ordenadas y agradables, por lo que debe tener cuidado de no tratar las escalas de medición como si fueran reglas estrictas y rápidas. No funciona así: son pautas, destinadas a ayudarlo a pensar en las situaciones en las que debe tratar diferentes variables de manera diferente. Nada mas.
 
Tomemos un ejemplo clásico, tal vez el ejemplo clásico, de una herramienta de medición psicológica: la <span style="color: BlueViolet;">escala Likert</span>. La humilde escala Likert es la herramienta básica de todo diseño de encuestas. Usted mismo ha completado cientos, tal vez miles de ellos, y es probable que incluso haya usado uno. Supongamos que tenemos una pregunta de la encuesta que se parece a esto:
 
> ¿Cuál de las siguientes opciones describe mejor tu opinión sobre la afirmación de que "todos los piratas son increíblemente increíbles"...
 
y luego las opciones presentadas al participante son estas:

{{< boxmd >}}

(1) Totalmente en desacuerdo  
(2) En desacuerdo  
(3) Ni de acuerdo ni en desacuerdo  
(4) De acuerdo  
(5) Totalmente de acuerdo

{{< /boxmd >}}

Este conjunto de ítems es un ejemplo de una escala Likert de 5 puntos: se pide a las personas que elijan entre varias (en este caso 5) posibilidades claramente ordenadas, generalmente con un descriptor verbal dado en cada caso. Sin embargo, no es necesario que todos los elementos se describan explícitamente. Este también es un ejemplo perfectamente bueno de una escala Likert de 5 puntos:

{{< boxmd >}}

(1) Totalmente en desacuerdo  
(2)  
(3)  
(4)  
(5) Totalmente de acuerdo

{{< /boxmd >}}

Las escalas Likert son herramientas muy útiles, aunque algo limitadas. La pregunta es, ¿qué tipo de variable son? Obviamente, son discretos, ya que no puede dar una respuesta de 2.5. Obviamente, no son de escala nominal, ya que los artículos están ordenados; y tampoco son una escala de razón, ya que no hay un cero natural.
 
Pero, ¿son una escala ordinal o una escala de intervalo? Un argumento dice que realmente no podemos probar que la diferencia entre "totalmente de acuerdo" y "de acuerdo" sea del mismo tamaño que la diferencia entre "de acuerdo" y "ni de acuerdo ni en desacuerdo". De hecho, en la vida cotidiana es bastante obvio que no son iguales en absoluto. Por tanto, esto sugiere que deberíamos tratar las escalas Likert como variables ordinales. Por otro lado, en la práctica, la mayoría de los participantes parecen tomarse la parte completa “en una escala del 1 al 5” con bastante seriedad, y tienden a actuar como si las diferencias entre las cinco opciones de respuesta fueran bastante similares entre sí. Como consecuencia, muchos investigadores tratan los datos de la escala Likert como si fueran una escala de intervalo. No es una escala de intervalo, pero en la práctica es lo suficientemente cercana como para pensar en ella como una <span style="color: BlueViolet;">escala de cuasi intervalo</span>.

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Evaluar la confiabilidad de una medición {#Cap2.3}
 
En este punto hemos pensado un poco sobre cómo operacionalizar un constructo teórico y así crear una medida psicológica; y hemos visto que al aplicar medidas psicológicas terminamos con variables, que pueden ser de muchos tipos diferentes. En este punto, deberíamos comenzar a discutir la pregunta obvia: ¿la medición es buena? Haremos esto en términos de dos ideas relacionadas: *confiabilidad* y *validez*. En pocas palabras, la <span style="color: BlueViolet;">confiabilidad</span> de una medida le dice con qué *precisión* está midiendo algo, mientras que la *validez* de una medida le dice qué tan *precisa* es la medida. En esta sección hablaré sobre confiabilidad; hablaremos de validez en el próximo capítulo.
 
La confiabilidad es en realidad un concepto muy simple: se refiere a la repetibilidad o consistencia de su medición. La medición de mi peso mediante una “báscula de baño” es muy confiable: si subo y me bajo de la báscula una y otra vez, me seguirá dando la misma respuesta. Medir mi inteligencia por medio de “preguntarle a mi mamá” es muy poco confiable: unos días me dice que soy un poco tonta, y otros días me dice que soy un completo idiota. Observe que este concepto de confiabilidad es diferente a la cuestión de si las mediciones son correctas (la exactitud de una medición se relaciona con su validez). Si sostengo un saco de patatas cuando subo y me bajo de la báscula del baño, la medida seguirá siendo fiable: siempre me dará la misma respuesta. Sin embargo, esta respuesta altamente confiable no coincide en absoluto con mi peso real, por lo tanto, es incorrecta. En términos técnicos, esta es una medida *confiable pero no válida*. Del mismo modo, aunque la estimación de mi madre sobre mi inteligencia es un poco poco fiable, podría tener razón. Tal vez no soy demasiado brillante, y si bien su estimación de mi inteligencia fluctúa bastante de un día a otro, básicamente es correcta. Así que esa sería una medida *válida pero poco confiable*. Por supuesto, hasta cierto punto, observe que si las estimaciones de mi madre son demasiado poco confiables, será muy difícil averiguar cuál de sus muchas afirmaciones sobre mi inteligencia es realmente la correcta. Entonces, hasta cierto punto, una medida muy poco confiable tiende a terminar siendo inválida a efectos prácticos; Tanto es así que mucha gente diría que la fiabilidad es necesaria (pero no suficiente) para asegurar la validez.
 
Bien, ahora que tenemos clara la distinción entre confiabilidad y validez, pensemos en las diferentes formas en que podríamos medir la confiabilidad:

{{< boxmd >}}

- <span style="color: BlueViolet;">Fiabilidad test-retest</span>. Esto se relaciona con la coherencia en el tiempo: si repetimos la medición en una fecha posterior, ¿obtenemos la misma respuesta?
- <span style="color: BlueViolet;">Fiabilidad entre</span>. Esto se relaciona con la coherencia entre las personas: si alguien más repite la medición (por ejemplo, alguien más califica mi inteligencia), ¿producirán la misma respuesta?
- <span style="color: BlueViolet;">Fiabilidad de formas paralelas</span>. Esto se relaciona con la coherencia entre medidas teóricamente equivalentes: si utilizo un juego diferente de básculas de baño para medir mi peso, ¿da la misma respuesta?
- <span style="color: BlueViolet;">Fiabilidad de la consistencia interna</span>. Si una medición se construye a partir de muchas partes diferentes que realizan funciones similares (por ejemplo, el resultado de un cuestionario de personalidad se suma a varias preguntas), ¿las partes individuales tienden a dar respuestas similares?

{{< /boxmd >}}

No todas las mediciones necesitan poseer todas las formas de confiabilidad. Por ejemplo, la evaluación educativa se puede considerar como una forma de medición. Una de las asignaturas que enseño, *Ciencias Cognitivas Computacionales*, tiene una estructura de evaluación que tiene un componente de investigación y un componente de examen (más otras cosas). El componente de examen está *destinado* a medir algo diferente del componente de investigación, por lo que la evaluación en su conjunto tiene una consistencia interna baja. Sin embargo, dentro del examen hay varias preguntas que están destinadas a medir (aproximadamente) las mismas cosas y tienden a producir resultados similares; por lo que el examen por sí solo tiene una consistencia interna bastante alta. Lo que es como debería ser. ¡Solo debes exigir confiabilidad en aquellas situaciones en las que quieras que se mida lo mismo!



<p style="text-align:right;font-size:80%;">
<a href="#id-01">Volver</a>
</p>

---

## El "papel" de las variables: predictores y resultados {#Cap2.4}
 
De acuerdo, tengo una última pieza de terminología que necesito explicarte antes de alejarme de las variables. Normalmente, cuando investigamos un poco, terminamos con muchas variables diferentes. Luego, cuando analizamos nuestros datos, generalmente tratamos de explicar algunas de las variables en términos de algunas de las otras variables. Es importante mantener distintos los dos roles "lo que explica" y "lo que se explica". Así que seamos claros sobre esto ahora. En primer lugar, también podríamos acostumbrarnos a la idea de usar símbolos matemáticos para describir variables, ya que va a suceder una y otra vez. Denotemos la variable "por explicar" Y, y denotemos las variables "que hacen la explicación" como *X*<sub>1</sub>, *X*<sub>2</sub>, etc.
 
Ahora, cuando hacemos un análisis, tenemos diferentes nombres para *X* e *Y*, ya que juegan diferentes roles en el análisis. Los nombres clásicos para estos roles son <span style="color: BlueViolet;">variable independiente</span> (VI) y <span style="color: BlueViolet;">variable dependiente</span> (VD). La VI es la variable que se utiliza para explicar (es decir, X) y la VD es la variable que se explica (es decir, Y). La lógica detrás de estos nombres es la siguiente: si realmente existe una relación entre X e Y, entonces podemos decir que Y depende de X, y si hemos diseñado nuestro estudio "correctamente", entonces X no depende de nada más. Sin embargo, personalmente encuentro esos nombres horribles: son difíciles de recordar y son muy engañosos, porque (a) el VI nunca es realmente "independiente de todo lo demás" y (b) si no hay relación, entonces el VD no en realidad no depende de VI. Y de hecho, como no soy la única persona que piensa que VI y VD son nombres horribles, hay una serie de alternativas que encuentro más atractivas. Los términos que usaré en estas notas son <span style="color: BlueViolet;">predictores</span> y <span style="color: BlueViolet;">resultados</span>. La idea aquí es que lo que está tratando de hacer es usar X (los predictores) para hacer conjeturas sobre Y (los resultados). 4 Esto se resume en la Tabla <a href="#tabla22">2.2</a>.

<a id="tabla22"> </a>
Tabla 2. La terminología usada para distinguir entre diferentes roles que una variable puede jugar cuando se analiza un conjunto de datos. Nota que este libro tiene a evadir la terminología clásica en favor de nuevos nombres.

| Rol de la variable | Nombre cásico | Nombre moderno |
| :---- | :---- | :--- |
| "para ser explicada" | variable dependiente (VD) | Respuesta |
| "para hacer la explicación" | variable independiende (VI) | Predictor |

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Investigación experimental y no experimental {#Cap2.5}
 
Una de las grandes distinciones que debe tener en cuenta es la distinción entre "investigación experimental" e "investigación no experimental". Cuando hacemos esta distinción, de lo que realmente estamos hablando es del grado de control que el investigador ejerce sobre las personas y los eventos en el estudio.
 
### Investigación experimental
 
Las características clave de la <span style="color: BlueViolet;">investigación experimental</span> es que el investigador controla todos los aspectos del estudio, especialmente lo que los participantes experimentan durante el estudio. En particular, el investigador manipula o varía las variables predictoras (VI) y luego permite que la variable de resultado (VD) varíe naturalmente. La idea aquí es variar deliberadamente los predictores (VI) para ver si tienen algún efecto causal en los resultados. Además, para garantizar que no exista la posibilidad de que algo más que las variables predictoras esté causando los resultados, todo lo demás se mantiene constante o de alguna otra manera está "equilibrado" para garantizar que no tengan ningún efecto sobre los resultados. En la práctica, es casi imposible *pensar* en todo lo demás que pueda influir en el resultado de un experimento, y mucho menos mantenerlo constante. La solución estándar para esto es la <span style="color: BlueViolet;">aleatorización</span>: es decir, asignamos personas al azar a diferentes grupos y luego le damos a cada grupo un tratamiento diferente (es decir, les asignamos diferentes valores de las variables predictoras). Hablaremos más sobre la aleatorización más adelante en este curso, pero por ahora, es suficiente decir que lo que hace la aleatorización es minimizar (pero no eliminar) las posibilidades de que haya alguna diferencia sistemática entre los grupos.
 
Consideremos un ejemplo muy simple, completamente irreal y extremadamente poco ético. Suponga que quiere saber si fumar causa cáncer de pulmón. Una forma de hacer esto sería encontrar personas que fuman y personas que no fuman, y ver si los fumadores tienen una tasa más alta de cáncer de pulmón. Este *no* es un experimento adecuado, ya que el investigador no tiene mucho control sobre quién fuma y quién no. Y esto realmente importa: por ejemplo, puede ser que las personas que eligen fumar cigarrillos también tiendan a tener una dieta pobre, o tal vez tienden a trabajar en minas de asbesto, o lo que sea. El punto aquí es que los grupos (fumadores y no fumadores) en realidad difieren en muchas cosas, no solo en el tabaquismo. Por tanto, podría ser que la mayor incidencia de cáncer de pulmón entre los fumadores se deba a otra cosa, no al tabaquismo en sí. En términos técnicos, estas otras cosas (por ejemplo, la dieta) se denominan "factores de confusión", y hablaremos de ellos en un momento.
 
Mientras tanto, consideremos ahora cómo se vería un experimento adecuado. Recuerde que nuestra preocupación era que los fumadores y los no fumadores pudieran diferir de muchas maneras. La solución, siempre que no tenga ética, es controlar quién fuma y quién no. Específicamente, si dividimos a los participantes al azar en dos grupos y forzamos a la mitad de ellos a convertirse en fumadores, entonces es muy poco probable que los grupos difieran en cualquier otro aspecto que no sea el hecho de que la mitad de ellos fuma. De esa manera, si nuestro grupo de fumadores contrae cáncer a una tasa más alta que el grupo de no fumadores, entonces podemos estar bastante seguros de que (a) fumar causa cáncer y (b) somos asesinos.
 
### Investigación no experimental
 
La <span style="color: BlueViolet;">investigación no experimental</span> es un término amplio que abarca "cualquier estudio en el que el investigador no tenga tanto control como lo hace en un experimento". Obviamente, el control es algo que a los científicos les gusta tener, pero como ilustra el ejemplo anterior, hay muchas situaciones en las que no se puede o no se debe intentar obtener ese control. Dado que es muy poco ético (y casi con toda seguridad criminal) obligar a las personas a fumar para saber si tienen cáncer, este es un buen ejemplo de una situación en la que no debería intentar obtener un control experimental. Pero también hay otras razones. Incluso dejando de lado las cuestiones éticas, nuestro "experimento de fumar" tiene algunos otros problemas. Por ejemplo, cuando sugerí que "obligáramos" a la mitad de las personas a convertirse en fumadores, debí haber estado hablando de *comenzar* con una muestra de no fumadores y luego obligarlos a convertirse en fumadores. Si bien esto suena como el tipo de diseño experimental sólido y malvado que a un científico loco le encantaría, puede que no sea una forma muy sólida de investigar el efecto en el mundo real. Por ejemplo, suponga que fumar sólo causa cáncer de pulmón cuando las personas tienen una dieta deficiente, y suponga también que las personas que normalmente fuman tienden a tener una dieta deficiente. Sin embargo, dado que los "fumadores" de nuestro experimento no son fumadores "naturales" (es decir, forzamos a los no fumadores a convertirse en fumadores; no adquirieron todas las demás características normales de la vida real que los fumadores tienden a poseer ) probablemente tengan mejores dietas. Como tal, en este ejemplo tonto no tendrían cáncer de pulmón, y nuestro experimento fallará, porque viola la estructura del mundo "natural" (el nombre técnico para esto es un resultado "artefacto"; ver más adelante).
 
Una distinción que vale la pena hacer entre dos tipos de investigación no experimental es la diferencia entre la <span style="color: BlueViolet;">investigación cuasiexperimental</span> y los <span style="color: BlueViolet;">estudios de casos</span>. El ejemplo que mencioné anteriormente, en el que queríamos examinar la incidencia de cáncer de pulmón entre fumadores y no fumadores, sin intentar controlar quién fuma y quién no, es un diseño cuasi-experimental. Es decir, es lo mismo que un experimento, pero no controlamos los predictores (VI). Todavía podemos usar estadísticas para analizar los resultados, es solo que tenemos que ser mucho más cuidadosos.
 
El enfoque alternativo, los estudios de caso, tiene como objetivo proporcionar una descripción muy detallada de uno o unos pocos casos. En general, no se pueden utilizar estadísticas para analizar los resultados de los estudios de casos y, por lo general, es muy difícil sacar conclusiones generales sobre “las personas en general” a partir de unos pocos ejemplos aislados. Sin embargo, los estudios de caso son muy útiles en algunas situaciones. En primer lugar, hay situaciones en las que no tienes alternativa: la neuropsicología tiene mucho este problema. A veces, simplemente no puede encontrar muchas personas con daño cerebral en un área específica, por lo que lo único que puede hacer es describir los casos que tiene con el mayor detalle y el mayor cuidado posible. Sin embargo, también existen algunas ventajas genuinas para los estudios de casos: debido a que no tiene tantas personas para estudiar, tiene la capacidad de invertir mucho tiempo y esfuerzo tratando de comprender los factores específicos en juego en cada caso. Esto es algo muy valioso para hacer. Como consecuencia, los estudios de caso pueden complementar los enfoques más estadísticamente orientados que ve en diseños experimentales y cuasi-experimentales. No hablaremos mucho sobre estudios de caso en estas conferencias, pero son herramientas muy valiosas.


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