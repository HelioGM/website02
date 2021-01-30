---
title: "Capítulo 1: ¿Por qué aprendemos estadística?"
date: 2020-12-30T18:17:17-08:00
publishdate: 2020-12-30T18:27:17-08:00
description: "No es sorprendente que haya una proporción bastante grande de la base de estudiantes que no está contenta con el hecho de que su carrera tenga tantas estadísticas. En vista de esto, pensé que el lugar correcto para comenzar podría ser responder algunas de las preguntas más comunes que la gente tiene sobre las estadísticas... "
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
image: images/learning/cap_01.png
---

{{< featuredImage >}} 

---

<style>
body {
text-align: justify}
</style>

<a id="id-01"> </a>

## Sobre la psicología de la estadística 

Para sorpresa de muchos estudiantes, la estadística es una parte bastante importante de la educación psicológica. Para sorpresa de nadie, la estadística rara vez es la parte favorita de la educación psicológica. Después de todo, si realmente te encantó la idea de hacer estadística, probablemente estarías inscrito en una clase de estadística ahora mismo, no en una clase de psicología. Entonces, no es sorprendente que haya una proporción bastante grande de la base de estudiantes que no está contenta con el hecho de que la psicología tenga tantas estadísticas. En vista de esto, pensé que el lugar correcto para comenzar podría ser responder algunas de las preguntas más comunes que la gente tiene sobre las estadísticas...
 
Gran parte de este tema se relaciona con la idea misma de estadística. ¿Qué es? ¿Para qué está ahí? ¿Y por qué los científicos están tan obsesionados con él? Todas estas son buenas preguntas, cuando lo piensas. Así que comencemos con el último. Como grupo, los científicos parecen estar extrañamente obsesionados con realizar pruebas estadísticas en todo. De hecho, usamos estadísticas con tanta frecuencia que a veces nos olvidamos de explicarle a la gente por qué lo hacemos. Es una especie de artículo de fe entre los científicos, y especialmente los científicos sociales, que no se puede confiar en sus hallazgos hasta que haya hecho algunas estadísticas. A los estudiantes de pregrado se les puede perdonar que piensen que todos estamos completamente locos, porque nadie se toma el tiempo para responder una pregunta muy simple:
 
> ***"¿Por qué haces estadísticas? ¿Por qué los científicos no usan el <u>sentido común</u>?"***

Es una pregunta ingenua de alguna manera, pero la mayoría de las buenas preguntas lo son. Hay muchas buenas respuestas, 2 pero por mi dinero, la mejor respuesta es una muy simple: no confiamos lo suficiente en nosotros mismos. Nos preocupa que seamos humanos y susceptibles a todos los prejuicios, tentaciones y debilidades que sufren los humanos. Gran parte de las estadísticas es básicamente una salvaguardia. Usar el “sentido común” para evaluar la evidencia significa confiar en el instinto, confiar en argumentos verbales y usar el poder puro de la razón humana para encontrar la respuesta correcta. La mayoría de los científicos no cree que este enfoque funcione. 
 
De hecho, ahora que lo pienso, esto me suena mucho a una pregunta psicológica, y dado que trabajo en un departamento de psicología, parece una buena idea profundizar un poco más aquí. ¿Es realmente plausible pensar que este enfoque de “sentido común” es muy confiable? Los argumentos verbales deben construirse en el lenguaje, y todos los lenguajes tienen sesgos: algunas cosas son más difíciles de decir que otras, y no necesariamente porque sean falsas (por ejemplo, la electrodinámica cuántica es una buena teoría, pero difícil de explicar con palabras). Los instintos de nuestro "intestino" no están diseñados para resolver problemas científicos, están diseñados para manejar inferencias del día a día, y dado que la evolución biológica es más lenta que el cambio cultural, deberíamos decir que están diseñados para resolver los problemas cotidianos de un mundo diferente al que vivimos. Fundamentalmente, razonar con sensatez requiere que las personas se involucren en la “inducción”, haciendo conjeturas acertadas y yendo más allá de la evidencia inmediata de los sentidos para hacer generalizaciones sobre el mundo. Si crees que puedes hacer eso sin ser influenciado por varios distractores, bueno, tengo un puente en Brooklyn que me gustaría venderte. Demonios, como muestra la siguiente sección, ni siquiera podemos resolver problemas “deductivos” (aquellos en los que no se requiere adivinar) sin ser influenciados por nuestros prejuicios preexistentes.

### La maldición del sesgo de creencias 

La mayoría de las personas son bastante inteligentes. Ciertamente somos más inteligentes que las otras especies con las que compartimos el planeta (aunque muchas personas pueden estar en desacuerdo). Nuestras mentes son cosas bastante asombrosas y parece que somos capaces de las hazañas más increíbles del pensamiento y la razón. Sin embargo, eso no nos hace perfectos. Y entre las muchas cosas que los psicólogos han demostrado a lo largo de los años es que realmente nos resulta difícil ser neutrales, evaluar la evidencia de manera imparcial y sin dejarnos influir por prejuicios preexistentes. Un buen ejemplo de esto es el <span style="color: BlueViolet;">efecto de sesgo de creencias</span> en el razonamiento lógico: si le pide a la gente que decida si un argumento en particular es lógicamente válido (es decir, la conclusión sería verdadera si las premisas fueran verdaderas), tendemos a estar influenciados por la credibilidad de la conclusión, incluso cuando no deberíamos. Por ejemplo, aquí hay un argumento válido donde la conclusión es creíble:

{{< boxmd >}}
 
- Ningún cigarrillo es barato (Premisa 1)  
- Algunas cosas adictivas son económicas (premisa 2)  
- Por tanto, algunas cosas adictivas no son los cigarrillos (Conclusión) 

{{< /boxmd >}}

Y aquí hay un argumento válido donde la conclusión no es creíble:

{{< boxmd >}}

- Ninguna cosa adictiva es barata (Premisa 1)  
- Algunos cigarrillos son económicos (premisa 2)  
- Por tanto, algunos cigarrillos no son adictivos (Conclusión)

{{< /boxmd >}}

La estructura lógica del argumento n.°2 es idéntica a la estructura del argumento n.°1 y ambos son válidos. Sin embargo, en el segundo argumento, hay buenas razones para pensar que la premisa 1 es incorrecta y, como resultado, es probable que la conclusión también sea incorrecta. Pero eso es completamente irrelevante para el tema en cuestión: un argumento es deductivamente válido si la conclusión es una consecuencia lógica de las premisas. Es decir, un argumento válido no tiene por qué involucrar declaraciones verdaderas.
 
Por otro lado, aquí hay un argumento inválido que tiene una conclusión creíble: 

{{< boxmd >}}
 
- Ninguna cosa adictiva es barata (Premisa 1)  
- Algunos cigarrillos son económicos (premisa 2)  
- Por tanto, algunas cosas adictivas no son los cigarrillos (Conclusión)

{{< /boxmd >}}

Y finalmente, un argumento inválido con una conclusión increíble:

{{< boxmd >}}

- Ningún cigarrillo es barato (Premisa 1)  
- Algunas cosas adictivas son económicas (premisa 2)  
- Por tanto, algunos cigarrillos no son adictivos (Conclusión)

{{< /boxmd >}}

Ahora, suponga que las personas realmente son perfectamente capaces de dejar de lado sus prejuicios preexistentes sobre lo que es verdad y lo que no, y evaluar puramente un argumento por sus méritos lógicos. Esperaríamos que el 100% de la gente diga que los argumentos válidos son válidos y el 0% de la gente diga que los argumentos inválidos son válidos. Entonces, si realizara un experimento con esto, esperaría ver datos como este:

|       | la conclusión se siente verdadera | la conclusión se siente falsa     |
| :---        |    :----:   |          :----: |
| El argumento es valido  | 100% dijo "valido" | 100% dijo "valido" |
| El argumento es invalido | 0% dijo "valido" | 0% dijo "valido" |
 
Si los datos psicológicos se viesen así (o incluso una buena aproximación a esto), podríamos sentirnos seguros simplemente confiando en nuestros instintos. Es decir, estaría perfectamente bien dejar que los científicos evalúen los datos en función de su sentido común, y no molestarse con todas estas turbias estadísticas. Sin embargo, ustedes han tomado clases de psicología, y a estas alturas probablemente ya sepan a dónde va esto ...
 
En un estudio clásico, <span style="color: red;">JSBT Evans, Barston y Pollard (1983)</span> realizaron un experimento que analiza exactamente esto. Lo que encontraron es que cuando los prejuicios preexistentes (es decir, las creencias) estaban de acuerdo con la estructura de los datos, todo salió de la manera esperada:

|       | la conclusión se siente verdadera | la conclusión se siente falsa     |
| :---        |    :----:   |          :----: |
| El argumento es valido  | 92% dijo "valido" |  |
| El argumento es invalido |  | 8% dijo "valido" |

No es perfecto, pero está bastante bien. Pero mire lo que sucede cuando nuestros sentimientos intuitivos sobre la verdad de la conclusión van en contra de la estructura lógica del argumento:

|       | conclusion se siente verdadera | conclusion se siente falsa     |
| :---        |    :----:   |          :----: |
| El argumento es valido  | 92% dijo "valido" | **46% dijo "valido"** |
| El argumento es invalido | **92% dijo "valido"** | 8% dijo "valido" |
 
Dios mío, eso no es tan bueno. Aparentemente, cuando a las personas se les presenta un argumento fuerte que contradice nuestras creencias preexistentes, nos resulta bastante difícil incluso percibirlo como un argumento sólido (las personas solo lo hicieron el 46% de las veces). Peor aún, cuando a las personas se les presenta un argumento débil que está de acuerdo con nuestros prejuicios preexistentes, casi nadie puede ver que el argumento es débil (¡la gente se equivocó el 92% de las veces!) 
 
Si lo piensa, no es que estos datos sean terriblemente condenatorios. En general, a las personas les fue mejor que al azar a la hora de compensar sus prejuicios anteriores, ya que alrededor del 60% de los juicios de las personas fueron correctos (esperaría que el 50% por casualidad). Aun así, si fueras un "evaluador de pruebas" profesional y alguien se acercara y te ofreciera una herramienta mágica que mejora tus posibilidades de tomar la decisión correcta del 60% al (digamos) 95%, probablemente te lanzarías, ¿cierto? Por supuesto que sí. Afortunadamente, tenemos una herramienta que puede hacer esto. Pero no es magia, son estadísticas. Así que esa es la razón número uno por la que los científicos aman las estadísticas. Es demasiado fácil para nosotros "creer lo que queremos creer"; así que si queremos "creer en los datos" en cambio, vamos a necesitar un poco de ayuda para mantener nuestros prejuicios personales bajo control. Eso es lo que hacen las estadísticas: nos ayuda a mantenernos honestos.


<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## El cuento con moraleja de la paradoja de Simpson
 
La siguiente es una historia real (creo que...). En 1973, la Universidad de California, Berkeley tenía algunas preocupaciones sobre la admisión de estudiantes en sus cursos de posgrado. Específicamente, lo que causó el problema fue que el desglose por género de sus admisiones, que se veía así ...
 
 |       | Número de aplicantes | Porcentaje de admisiones   |
| :---        |    :----:   |          :----: |
| Hombres  | 8442 | 44% |
| Mujeres | 4321 | 35% |
 
... y la estaban preocupados por ser demandado. Dado que había casi 13.000 solicitantes, una diferencia del 9% en las tasas de admisión entre hombres y mujeres es demasiado grande para ser una coincidencia. Datos bastante convincentes, ¿verdad? Y si te dijera que estos datos en realidad reflejan un sesgo débil a favor de las mujeres (¡más o menos!), Probablemente pensarías que estoy loca o sexista.
 
Curiosamente, en realidad es una especie de verdad... cuando la gente comenzó a buscar con más cuidado los datos de admisión (Bickel, Hammel, y O'Connell, 1975), estos contaron una historia bastante diferente. Específicamente, cuando lo analizaron departamento por departamento, resultó que la mayoría de los departamentos en realidad tenían una tasa de éxito ligeramente mayor para las solicitantes mujeres que para los hombres. La siguiente tabla muestra las cifras de admisión para los seis departamentos más grandes (con los nombres de los departamentos eliminados por razones de privacidad):
 
 |  Departamento | Hombres (aplicantes) | Hombres (admitidos, %) | Mujeres (aplicantes) | Mujeres (admitidos, %) |
| :---        |    :----:   |          :----: |    :----:   |          :----: |
| A | 825 | 62% | 108 | 82% |
| B | 560 | 63% | 25 | 68% |
| C | 325 | 37% | 593 | 34% |
| D | 417 | 33% | 375 | 35% |
| E | 191 | 28% | 393 | 34% |
| F | 272 | 6% |  341 | 7% |


¡Sorprendentemente, la mayoría de los departamentos tenían una tasa más alta de admisiones de mujeres que de hombres! Sin embargo, la tasa general de admisión en la universidad para las mujeres fue más baja que para los hombres. ¿Cómo puede ser esto? ¿Cómo pueden ser ciertas estas dos declaraciones al mismo tiempo?
 
Esto es lo que está pasando. En primer lugar, observe que los departamentos no son iguales entre sí en términos de sus porcentajes de admisión: algunos departamentos (por ejemplo, ingeniería, química) tienden a admitir un alto porcentaje de los solicitantes calificados, mientras que otros (por ejemplo, inglés) tienden a rechazar a la mayoría de los candidatos, aunque fueran de alta calidad. Entonces, entre los seis departamentos que se muestran arriba, observe que el departamento A es el más generoso, seguido de B, C, D, E y F en ese orden. A continuación, observe que los hombres y las mujeres tienden a postularse para diferentes departamentos. Si clasificamos los departamentos en términos del número total de solicitantes masculinos, obtenemos **A**>**B**>D>C>F>E (los departamentos “fáciles” están en negrita). En general, los hombres tendían a postularse en los departamentos que tenían altas tasas de admisión. Ahora compare esto con cómo se distribuyeron las mujeres solicitantes. Clasificación de los departamentos en términos del número total de mujeres aplicantes produce un orden muy diferente C>E>D>F>A>B . En otras palabras, lo que estos datos parecen sugerir es que las mujeres solicitantes tienden a postularse en departamentos "más difíciles". Y de hecho, si miramos todo el Gráfico <a href="#graph01">1.1</a>, vemos que esta tendencia es sistemática y bastante sorprendente. Este efecto se conoce como <span style="color: BlueViolet;">paradoja de Simpson</span>. No es común, pero sucede en la vida real, y la mayoría de las personas se sorprenden cuando lo encuentran por primera vez, y muchas personas se niegan incluso a creer que es real. Es muy real. Y aunque hay muchas lecciones estadísticas muy sutiles enterradas allí, quiero usarlas para hacer un punto mucho más importante... investigar es difícil, y hay muchas trampas sutiles y contradictorias al acecho de los incautos. Esa es la razón número 2 por la que a los científicos les encantan las estadísticas y por qué enseñamos métodos de investigación. Porque la ciencia es difícil y la verdad a veces se esconde astutamente en los rincones y recovecos de datos complicados.
<a id="graph01"> </a>
{{< img src="/images/learning/graph01.png" title="Figura 1.1" caption="Datos de admisiones universitarias de Berkeley 1973. Esta cifra traza la tasa de admisión de los 85 departamentos que tenían al menos una solicitante mujer, en función del porcentaje de solicitantes que eran mujeres. El gráfico es un nuevo dibujo de la Figura 1 de Bickel et al. (1975). Los círculos trazan departamentos con más de 40 solicitantes; el área del círculo es proporcional al número total de solicitantes. El departamento de parcelas cruza con menos de 40 solicitantes." alt="image alt" width="720px" position="justify" >}} 

Antes de dejar este tema por completo, quiero señalar algo más realmente crítico que a menudo se pasa por alto en una clase de métodos de investigación. Las estadísticas solo resuelven *parte* del problema. Recuerde que comenzamos todo esto con la preocupación de que los procesos de admisión de Berkeley pudieran estar injustamente sesgados en contra de las postulantes. Cuando nos fijamos en los datos “agregados”, que parecía como la universidad se discrimina a las mujeres, pero cuando nos “desagregado” y mirado en el individuo el comportamiento de todos los departamentos, resultó que los departamentos eran reales, si cualquier cosa, ligeramente sesgada a favor de las mujeres. El sesgo de género en las admisiones totales se debió al hecho de que las mujeres tendían a auto-seleccionarse para los departamentos más difíciles. Desde una perspectiva legal, eso probablemente dejaría a la universidad en claro. Las admisiones de posgrado se determinan a nivel de departamento individual (y hay buenas razones para hacerlo), y a nivel de departamentos individuales, las decisiones son más o menos imparciales (el sesgo débil a favor de las mujeres en ese nivel es pequeño y no es coherente en todos los departamentos). Dado que la universidad no puede dictar a qué departamentos la gente elige postularse, y la toma de decisiones se lleva a cabo a nivel de departamento, difícilmente se puede responsabilizar por los sesgos que esas elecciones produzcan.
 
Esa fue la base de mis comentarios un tanto simplistas anteriores, pero esa no es exactamente toda la historia, ¿verdad? Después de todo, si estamos interesados en esto desde una perspectiva más sociológica y psicológica, podríamos querer preguntarnos *por qué* hay diferencias de género tan fuertes en las aplicaciones. ¿Por qué los hombres tienden a postularse a la ingeniería con más frecuencia que las mujeres, y por qué esto se invierte en el departamento de inglés? Y por qué es que el caso de que los departamentos que tienden a tener un sesgo de aplicación femenina tienden a tener tasas de ingreso, en general, inferiores a los departamentos que tienen un sesgo de aplicación masculina? ¿No podría esto reflejar un sesgo de género, a pesar de que cada departamento es en sí mismo imparcial? Que podría. Supongamos, hipotéticamente, que los hombres prefieren postularse a las "ciencias duras" y las mujeres prefieren las "humanidades". Y suponga además que la razón por la cual los departamentos de humanidades tienen bajas tasas de admisión es porque el gobierno no quiere financiar las humanidades (los lugares de doctorado, por ejemplo, a menudo están vinculados a proyectos de investigación financiados por el gobierno). ¿Eso constituye un sesgo de género? ¿O simplemente una visión poco inteligente del valor de las humanidades? ¿Qué pasa si alguien de alto nivel en el gobierno recorta los fondos de humanidades porque siente que las humanidades son “cosas inútiles para chicas”? Eso parece bastante *descaradamente* sesgado por el género. Nada de esto cae dentro del ámbito de las estadísticas, pero es importante para el proyecto de investigación. Si está interesado en los efectos estructurales generales de los sutiles sesgos de género, probablemente desee examinar los datos agregados y desagregados. Si está interesado en el proceso de toma de decisiones en Berkeley, probablemente solo le interesen los datos desagregados.
 
En resumen, hay muchas preguntas críticas que no puede responder con estadísticas, pero las respuestas a esas preguntas tendrán un gran impacto en la forma en que analiza e interpreta los datos. Y esta es la razón por la que siempre debes pensar en las estadísticas como una herramienta que te ayude a conocer tus datos, ni más ni menos. Es una herramienta poderosa para ese fin, pero nada sustituye a un pensamiento cuidadoso.

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Estadística en psicología
 
Espero que la discusión anterior haya ayudado a explicar por qué la ciencia en general se centra tanto en las estadísticas. Pero supongo que tienes muchas más preguntas sobre qué papel juega la estadística en psicología, y específicamente por qué las clases de psicología siempre dedican tantas conferencias a las estadísticas. Así que aquí está mi intento de responder a algunos de ellos ...
 
> ***"¿Por qué la psicología tiene tantas estadísticas?"***
 
Para ser completamente honesto, hay algunas razones diferentes, algunas de las cuales son mejores que otras. La razón más importante es que la psicología es una ciencia estadística. Lo que quiero decir con eso es que las "cosas" que estudiamos son personas. Gente real, complicada, gloriosamente desordenada, exasperantemente perversa. Las "cosas" de la física incluyen objetos como los electrones, y aunque hay todo tipo de complejidades que surgen en la física, los electrones no tienen mente propia. No tienen opiniones, no difieren entre sí de formas extrañas y arbitrarias, no se aburren en medio de un experimento, no se enojan con el experimentador y luego deliberadamente intentan sabotear el conjunto de datos (no es que haya hecho eso ...). En un nivel fundamental, la psicología es más difícil que la física.
 
Básicamente, les enseñamos estadísticas como psicólogos porque necesitan ser mejores en estadísticas que los físicos. De hecho, hay un dicho que se usa a veces en física, en el sentido de que "si su experimento necesita estadísticas, debería haber hecho un experimento mejor". Tienen el lujo de poder decir eso porque sus objetos de estudio son patéticamente simples en comparación con el vasto lío al que se enfrentan los científicos sociales. No es solo psicología, en realidad: la mayoría de las ciencias sociales dependen desesperadamente de las estadísticas. No porque seamos malos experimentadores, sino porque hemos elegido un problema más difícil de resolver. Te enseñamos estadísticas porque realmente las necesitas.
 
> ***"¿No puede alguien más hacer las estadísticas?"***
 
Hasta cierto punto, pero no del todo. Es cierto que no necesitas convertirte en un estadístico completamente capacitado solo para estudiar psicología, pero debes alcanzar un cierto nivel de competencia estadística. En mi opinión, hay tres razones por las que todo investigador psicológico debería poder hacer estadísticas básicas:

1. En primer lugar, está la razón fundamental: la estadística está profundamente entrelazada con el diseño de la investigación. Si quiere ser bueno diseñando estudios psicológicos, necesita al menos comprender los conceptos básicos de las estadísticas.
 
2. En segundo lugar, si quieres ser bueno en el lado psicológico de la investigación, entonces necesitas ser capaz de comprender la literatura psicológica, ¿verdad? Pero casi todos los artículos de la literatura psicológica informan los resultados de análisis estadísticos. Entonces, si realmente desea comprender la psicología, debe poder comprender lo que otras personas hicieron con sus datos. Y eso significa comprender una cierta cantidad de estadísticas.
 
3. En tercer lugar, existe un gran problema práctico al depender de otras personas para realizar todas sus estadísticas: el análisis estadístico es caro. Si alguna vez se aburre y desea ver cuánto cobra el gobierno australiano por las tasas universitarias, notará algo interesante: las estadísticas están designadas como una categoría de "prioridad nacional", por lo que las tasas son mucho, mucho más bajas que las de cualquier otra área de estudio. Esto se debe a que existe una enorme escasez de estadísticos. Entonces, desde su perspectiva como investigador psicológico, ¡las leyes de la oferta y la demanda no están exactamente de su lado aquí! Como resultado, en casi cualquier situación de la vida real en la que desee realizar una investigación psicológica, el hecho cruel será que no tiene suficiente dinero para pagar un estadístico. Entonces, la economía de la situación significa que tienes que ser bastante autosuficiente.

Tenga en cuenta que muchas de estas razones se generalizan más allá de los investigadores. Si desea ser un psicólogo en ejercicio y mantenerse en la cima del campo, es útil poder leer la literatura científica, que se basa en gran medida en las estadísticas.
 
> ***"No me preocupan los trabajos, la investigación o el trabajo clínico. ¿Necesito estadísticas?"***
 
Bien, ahora solo estás jugando conmigo. Aún así, creo que también debería importarte. Las estadísticas deben importarle de la misma manera que las estadísticas deben importarle a todos: vivimos en el siglo XXI y los datos están en todas partes. Francamente, dado el mundo en el que vivimos estos días, ¡un conocimiento básico de las estadísticas está muy cerca de una herramienta de supervivencia! Cuál es el tema de la siguiente sección...

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Estadísticas en la vida cotidiana
 
Cuando comencé a escribir mis notas de clase, tomé los 20 artículos de noticias más recientes publicados en el sitio web de noticias ABC. De esos 20 artículos, resultó que 8 de ellos involucraban una discusión de algo que yo llamaría un tema estadístico; 6 de ellos cometieron un error. El error más común, si tiene curiosidad, fue no informar los datos de referencia (por ejemplo, el artículo menciona que el 5% de las personas en la situación X tienen alguna característica Y, ¡pero no dice qué tan común es la característica para todos los demás! ) El punto que estoy tratando de hacer aquí no es que los periodistas sean malos en estadísticas (aunque casi siempre lo son), es que un conocimiento básico de estadísticas es muy útil para tratar de averiguar cuándo alguien más está cometiendo un error o, incluso, mintiendote. De hecho, una de las cosas más importantes que le produce el conocimiento de las estadísticas es que se enoje con el periódico o con Internet con mucha más frecuencia.

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---
 
## Los métodos de investigación son más que estadísticas
 
Hasta ahora, la mayor parte de lo que he hablado son estadísticas, por lo que se le perdonará por pensar que la estadística es lo único que me importa en la vida. Para ser justos, no estaría muy equivocado, pero la metodología de investigación es un concepto más amplio que la estadística. Por lo tanto, la mayoría de los cursos de métodos de investigación cubrirán una gran cantidad de temas que se relacionan mucho más con la pragmática del diseño de la investigación y, en particular, los problemas con los que se encuentra al intentar investigar con humanos. Sin embargo, alrededor del 99% de los temores de los estudiantes se relacionan con la parte de estadísticas del curso, por lo que me he centrado en las estadísticas en esta discusión y espero haberlos convencido de que las estadísticas son importantes y, lo que es más importante, que no se deben temer. Dicho esto, es bastante típico que las clases de métodos de investigación introductorios tengan muchas estadísticas. Esto no se debe (generalmente) a que los conferenciantes sean personas malvadas. De hecho, todo lo contrario. Las clases introductorias se enfocan mucho en las estadísticas porque casi siempre se encuentra necesitando estadísticas antes de necesitar la capacitación en otros métodos de investigación. ¿Por qué? Porque casi todas sus asignaciones en otras clases dependerán de la capacitación estadística, en mucha mayor medida de lo que dependen de otras herramientas metodológicas. No es común que las asignaciones de pregrado requieran que diseñe su propio estudio desde cero (en cuyo caso necesitaría saber mucho sobre el diseño de investigación), pero es común que las asignaciones le pidan que analice e interprete datos que fueron recopilados en un estudio diseñado por otra persona (en cuyo caso se necesitan estadísticas). En ese sentido, desde la perspectiva de permitirle hacerlo bien en todas sus otras clases, las estadísticas son más urgentes.
 
Pero tenga en cuenta que "urgente" es diferente de "importante": ambos importan. Realmente quiero enfatizar que el diseño de la investigación es tan importante como el análisis de datos, y este libro dedica bastante tiempo a ello. Sin embargo, aunque las estadísticas tienen una especie de universalidad y proporcionan un conjunto de herramientas básicas que son útiles para la mayoría de los tipos de investigación psicológica, el lado de los métodos de investigación no es tan universal. Hay algunos principios generales en los que todo el mundo debería pensar, pero gran parte del diseño de investigación es muy idiosincrásico y específico del área de investigación en la que desea participar. En la medida en que lo que importa son los detalles, esos detalles no Suele aparecer en una clase de introducción a las estadísticas y los métodos de investigación.

<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

<p style="text-align:right;font-size:80%;">
Escrito por Navarro, Danielle; traducido y editado por García-Mendívil, Helio A.
</p>