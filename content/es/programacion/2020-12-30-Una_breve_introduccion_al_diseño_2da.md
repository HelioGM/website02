---
title: "Capítulo 2: Una breve introducción al diseño de investigación (2da parte)"
date: 2020-12-30T18:19:17-08:00
publishdate: 2020-12-31T18:26:17-08:00
description: "(...continuación) En este capítulo, comenzaremos a pensar en las ideas básicas que se necesitan para diseñar un estudio, recopilar datos, verificar si la recopilación de datos funciona, etc."
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

## Evaluar la validez de un estudio
 
Más que cualquier otra cosa, un científico quiere que su investigación sea "válida". La idea conceptual detrás de la validez es muy simple: ¿puedes confiar en los resultados de tu estudio? De lo contrario, el estudio no es válido. Sin embargo, si bien es fácil de establecer, en la práctica es mucho más difícil verificar la validez que verificar la confiabilidad. Y con toda honestidad, no hay una noción precisa y claramente acordada de lo que realmente es la validez. De hecho, hay muchos tipos diferentes de validez, cada uno de los cuales plantea sus propios problemas, y no todas las formas de validez son relevantes para todos los estudios. Voy a hablar de cinco tipos diferentes:

{{< boxmd >}}

- Validez interna
- Validez externa
- Construir validez
- Validez aparente
- Validez ecológica

{{< /boxmd >}}

Para darle una guía rápida sobre lo que importa aquí ... (1) La validez interna y externa son las más importantes, ya que se relacionan directamente con la pregunta fundamental de si su estudio realmente funciona. (2) La validez de constructo pregunta si estás midiendo lo que crees que eres. (3) La validez aparente no es muy importante excepto en la medida en que te preocupas por las "apariencias". (4) La validez ecológica es un caso especial de validez aparente que corresponde a un tipo de apariencia que puede interesarle mucho.
 
### Validez interna
 
La validez interna se refiere a la medida en que puede sacar las conclusiones correctas sobre las relaciones causales entre las variables. Se llama "interno" porque se refiere a las relaciones entre las cosas "dentro" del estudio. Ilustremos el concepto con un ejemplo sencillo. Suponga que está interesado en saber si una educación universitaria le ayuda a escribir mejor. Para hacerlo, reúne a un grupo de estudiantes de primer año, pídales que escriban un ensayo de 1000 palabras y cuente el número de errores ortográficos y gramaticales que cometen. Luego encuentras algunos estudiantes de tercer año, que obviamente han tenido más educación universitaria que los de primer año, y repites el ejercicio. Y supongamos que resulta que los alumnos de tercer año producen menos errores. Y entonces concluye que una educación universitaria mejora las habilidades de escritura. ¿Correcto? Excepto ... el gran problema que tienes con este experimento es que los estudiantes de tercer año son mayores y han tenido más experiencia escribiendo cosas. Así que es difícil saber con certeza cuál es la relación causal: ¿Las personas mayores escriben mejor? ¿O personas que han tenido más experiencia en la escritura? ¿O personas que han tenido más educación? ¿Cuál de las anteriores es la verdadera causa del desempeño superior de los de tercer año? ¿Años? ¿Experiencia? ¿Educación? No se puede decir. Este es un ejemplo de una falla en la validez interna, porque su estudio no separa adecuadamente las relaciones causales entre las diferentes variables.
 
### Validez externa
 
La validez externa se relaciona con la posibilidad de generalizar sus hallazgos. Es decir, en qué medida espera ver el mismo patrón de resultados en la "vida real" que vio en su estudio. Para decirlo con un poco más de precisión, cualquier estudio que hagas en psicología involucrará un conjunto bastante específico de preguntas o tareas, ocurrirá en un entorno específico e involucrará a participantes que provienen de un subgrupo particular. Entonces, si resulta que los resultados en realidad no se generalizan a personas y situaciones más allá de las que estudió, entonces lo que tiene es una falta de validez externa.
 
El ejemplo clásico de este problema es el hecho de que una gran proporción de los estudios de psicología utilizarán estudiantes de licenciatura en psicología como participantes. Sin embargo, es obvio que a los investigadores no solo les preocupan los estudiantes de psicología; se preocupan por la gente en general. Dado eso, un estudio que utiliza solo estudiantes de psiquiatría como participantes siempre conlleva el riesgo de carecer de validez externa. Es decir, si hay algo “especial” en los estudiantes de psicología que los hace diferentes de la población en general en algún aspecto relevante, entonces podemos empezar a preocuparnos por la falta de validez externa.
 
Dicho esto, es absolutamente fundamental darse cuenta de que un estudio que utiliza solo a estudiantes de psicología no necesariamente tiene un problema de validez externa. Hablaré de esto nuevamente más tarde, pero es un error tan común que lo mencionaré aquí. La validez externa se ve amenazada por la elección de la población si (a) la población de la que muestreó a sus participantes es muy limitada (por ejemplo, estudiantes de psicología) y (b) la población restringida de la que tomó la muestra es sistemáticamente diferente de la población general , en algún aspecto que sea relevante para el fenómeno psicológico que pretende estudiar. La parte en cursiva es la parte que mucha gente olvida: es cierto que los estudiantes de psicología se diferencian de la población en general en muchos aspectos, por lo que un estudio que solo utilice estudiantes de psicología puede tener problemas con la validez externa. Sin embargo, si esas diferencias no son muy relevantes para el fenómeno que está estudiando, entonces no hay nada de qué preocuparse. Para hacer esto un poco más concreto, aquí hay dos ejemplos extremos:

{{< boxmd >}}

- Quiere medir las “actitudes del público en general hacia la psicoterapia”, pero todos sus participantes son estudiantes de psicología. Es casi seguro que este estudio tenga un problema de validez externa.
- Quiere medir la efectividad de una ilusión visual y sus participantes son todos estudiantes de psicología. Es muy poco probable que este estudio tenga un problema de validez externa.

{{< /boxmd >}}

Habiendo dedicado los últimos dos párrafos a centrarse en la elección de los participantes (ya que ese es el gran problema del que todos tienden a preocuparse más), vale la pena recordar que la validez externa es un concepto más amplio. Los siguientes también son ejemplos de cosas que podrían representar una amenaza para la validez externa, según el tipo de estudio que esté realizando:
 
Las personas pueden responder un "cuestionario de psicología" de una manera que no refleja lo que harían en la vida real.
{{< boxmd >}} 
- Su experimento de laboratorio sobre (digamos) “aprendizaje humano” tiene una estructura diferente a los problemas de aprendizaje que enfrentan las personas en la vida real.
{{< /boxmd >}}

### Construir validez
 
La validez de constructo es básicamente una cuestión de si estás midiendo lo que quieres medir. Una medición tiene una buena validez de constructo si en realidad mide el constructo teórico correcto y una mala validez de constructo si no lo hace. Para dar un ejemplo muy simple (aunque ridículo), suponga que estoy tratando de investigar las tasas con las que los estudiantes universitarios hacen trampa en sus exámenes. Y la forma en que intento medirlo es pidiendo a los estudiantes que hacen trampa que se pongan de pie en la sala de conferencias para poder contarlos. Cuando hago esto con una clase de 300 estudiantes, 0 personas dicen ser tramposos. Por tanto, llego a la conclusión de que la proporción de tramposos en mi clase es del 0%. Claramente esto es un poco ridículo. Pero el punto aquí no es que este sea un ejemplo metodológico muy profundo, sino más bien para explicar qué es la validez de constructo. El problema con mi medida es que mientras intento medir "la proporción de personas que engañan", lo que en realidad estoy midiendo es "la proporción de personas lo suficientemente estúpidas como para admitir haber hecho trampas, o lo suficientemente sangrientas hacer". ¡Obviamente, estos no son lo mismo! Así que mi estudio salió mal, porque mi medición tiene una validez de constructo muy pobre.
 
### Validez aparente
 
La validez aparente simplemente se refiere a si una medida "parece" que está haciendo lo que se supone que debe hacer, nada más. Si diseño una prueba de inteligencia, y la gente la mira y dice “no, esa prueba no mide la inteligencia”, entonces la medida carece de validez aparente. Es tan simple como eso. Obviamente, la validez aparente no es muy importante desde una perspectiva científica pura. Después de todo, lo que nos importa es si la medida realmente hace lo que se supone que debe hacer, no si parece que hace lo que se supone que debe hacer. Como consecuencia, generalmente no nos importa mucho la validez aparente. Dicho esto, el concepto de validez aparente tiene tres útiles propósitos pragmáticos:
 
- A veces, un científico experimentado tendrá el "presentimiento" de que una medida en particular no funcionará. Si bien este tipo de corazonadas no tienen un valor probatorio estricto, a menudo vale la pena prestarles atención. Porque muchas veces las personas tienen un conocimiento que no pueden verbalizar del todo, por lo que puede haber algo de qué preocuparse incluso si no puede decir por qué. En otras palabras, cuando alguien en quien confía critica la validez aparente de su estudio, vale la pena tomarse el tiempo para pensar más detenidamente sobre su diseño para ver si puede pensar en las razones por las que podría salir mal. Eso sí, si no encuentra ningún motivo de preocupación, probablemente no debería preocuparse: después de todo, la validez aparente realmente no importa mucho.
 
- A menudo (muy a menudo), las personas completamente desinformadas también tendrán la "corazonada" de que su investigación es una mierda. Y lo criticarán en Internet o algo así. En una inspección más cercana, a menudo notará que estas críticas en realidad se centran por completo en cómo "se ve" el estudio, pero no en nada más profundo. El concepto de validez aparente es útil para explicar suavemente a las personas que necesitan fundamentar más sus argumentos.
 
- Ampliando el último punto, si las creencias de personas no capacitadas son críticas (por ejemplo, este suele ser el caso de la investigación aplicada en la que realmente desea convencer a los responsables de la formulación de políticas de algo u otro), debe preocuparse por la validez aparente. Simplemente porque, te guste o no, mucha gente usará la validez aparente como un sustituto de la validez real. Si quiere que el gobierno cambie una ley sobre bases científicas y psicológicas, entonces no importará cuán buenos sean sus estudios "realmente". Si carecen de validez aparente, descubrirás que los políticos te ignoran. Por supuesto, es algo injusto que la política a menudo dependa más de la apariencia que de los hechos, pero así es como van las cosas.
 
### Validez ecológica
 
La validez ecológica es una noción diferente de validez, que es similar a la validez externa, pero menos importante. La idea es que, para que sea ecológicamente válido, toda la estructura del estudio debe aproximarse mucho al escenario del mundo real que se está investigando. En cierto sentido, la validez ecológica es una especie de validez aparente: se relaciona principalmente con si el estudio "parece" correcto, pero con un poco más de rigor. Para ser ecológicamente válido, el estudio debe verse bien de una manera bastante específica. La idea detrás de esto es la intuición de que un estudio que es ecológicamente válido tiene más probabilidades de ser válido externamente. No es garantía, por supuesto. Pero lo bueno de la validez ecológica es que es mucho más fácil comprobar si un estudio es ecológicamente válido que comprobar si un estudio es válido externamente. Un ejemplo simple serían los estudios de identificación de testigos presenciales. La mayoría de estos estudios tienden a realizarse en un entorno universitario, a menudo con una variedad bastante simple de rostros para mirar en lugar de una fila. El período de tiempo entre ver al "criminal" y que se le pide que identifique al sospechoso en la "fila" suele ser más corto. El "crimen" no es real, por lo que no hay posibilidad de que el testigo esté asustado y no haya agentes de policía presentes, por lo que no hay tantas posibilidades de sentirse presionado. Todas estas cosas significan que el estudio definitivamente carece de validez ecológica. Pueden significar (pero no) que también carece de validez externa.


<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Confusiones, artefactos y otras amenazas a la validez
 
Si miramos el tema de la validez de la manera más general, las dos mayores preocupaciones que tenemos son las confusiones y los artefactos. Estos dos términos se definen de la siguiente manera:
 
- Confusión: Una confusión es una variable 5 adicional, a menudo no medida, que resulta estar relacionada tanto con los predictores como con los resultados. La existencia de factores de confusión amenaza la validez interna del estudio porque no se puede decir si el predictor causa el resultado o si la variable de confusión lo causa, etc.
 
- Artefacto: se dice que un resultado es “artefacto” si solo se cumple en la situación especial que usted probó en su estudio. La posibilidad de que su resultado sea un artefacto describe una amenaza a su validez externa, porque plantea la posibilidad de que no pueda generalizar sus resultados a la población real que le interesa.
 
Como regla general, las confusiones son una preocupación mayor para los estudios no experimentales, precisamente porque no son experimentos adecuados: por definición, estás dejando muchas cosas sin controlar, por lo que hay mucho margen para que las confusiones se abran paso en tu estudio. . La investigación experimental tiende a ser mucho menos vulnerable a las confusiones: cuanto más control tenga sobre lo que sucede durante el estudio, más podrá evitar que aparezcan confusiones.
 
Sin embargo, siempre hay columpios y rotondas, y cuando empezamos a pensar en artefactos en lugar de confusiones, el zapato está muy firmemente en el otro pie. En su mayor parte, los resultados de artefactos tienden a ser una preocupación para los estudios experimentales que para los estudios no experimentales. Para ver esto, es útil darse cuenta de que la razón por la que muchos estudios no son experimentales es precisamente porque lo que el investigador está tratando de hacer es examinar el comportamiento humano en un contexto más naturalista. Al trabajar en un contexto más del mundo real, pierde el control experimental (haciéndose vulnerable a las confusiones), pero debido a que tiende a estudiar psicología humana "en la naturaleza", reduce las posibilidades de obtener un resultado artificial. O, para decirlo de otra manera, cuando sacas la psicología de la naturaleza y la llevas al laboratorio (lo que generalmente tenemos que hacer para ganar nuestro control experimental), siempre corres el riesgo de estudiar accidentalmente algo diferente de lo que querías. estudio: que es más o menos la definición de un artefacto. Sin embargo, tenga cuidado: lo anterior es solo una guía aproximada. Es absolutamente posible tener confusiones en un experimento y obtener resultados artificiales con estudios no experimentales. Esto puede suceder por todo tipo de razones, entre las que se encuentra el error del investigador. En la práctica, es muy difícil pensar en todo con anticipación, e incluso los investigadores muy buenos cometen errores. Pero otras veces es inevitable, simplemente porque el investigador tiene ética (por ejemplo, ver "desgaste diferencial").
 
Bueno. Hay un sentido en el que casi cualquier amenaza a la validez puede caracterizarse como una confusión o un artefacto: son conceptos bastante vagos. Así que echemos un vistazo a algunos de los ejemplos más comunes ...
 
### Efectos de la historia
 
Los efectos del historial se refieren a la posibilidad de que ocurran eventos específicos durante el estudio mismo que podrían influir en los resultados. Por ejemplo, podría suceder algo entre una prueba previa y una prueba posterior. O, entre probar al participante 23 y al participante 24. Alternativamente, podría ser que esté viendo un estudio más antiguo, que era perfectamente válido para su época, pero el mundo ha cambiado lo suficiente desde entonces que las conclusiones ya no son confiables. Ejemplos de cosas que contarían como efectos históricos:
 
- Le interesa cómo piensa la gente sobre el riesgo y la incertidumbre. Comenzó su recopilación de datos en diciembre de 2010. Pero encontrar participantes y recopilar datos lleva tiempo, por lo que todavía está encontrando gente nueva en febrero de 2011. Desafortunadamente para usted (y más desafortunadamente para otros), las inundaciones de Queensland ocurrieron en enero de 2011, causando miles de millones de dólares en daños y matando a muchas personas. No es sorprendente que las personas evaluadas en febrero de 2011 expresen creencias bastante diferentes sobre el manejo del riesgo que las personas evaluadas en diciembre de 2010. ¿Cuál (si alguna) de éstas refleja las creencias “verdaderas” de los participantes? Creo que la respuesta es probablemente ambas: las inundaciones de Queensland cambiaron genuinamente las creencias del público australiano, aunque posiblemente solo temporalmente. La clave aquí es que la “historia” de las personas probadas en febrero es bastante diferente a la de las personas probadas en diciembre.
 
- Está probando los efectos psicológicos de un nuevo medicamento contra la ansiedad. Entonces, lo que se hace es medir la ansiedad antes de administrar el fármaco (por ejemplo, mediante un autoinforme y tomando medidas fisiológicas, digamos), luego se administra el fármaco y luego se toman las mismas medidas. En el medio, sin embargo, debido a que sus laboratorios están en Los Ángeles, hay un terremoto que aumenta la ansiedad de los participantes.
 
### Efectos de maduración
 
Como ocurre con los efectos de la historia, los efectos de maduración tienen que ver fundamentalmente con el cambio en el tiempo. Sin embargo, los efectos de la maduración no responden a eventos específicos. Más bien, se relacionan con cómo las personas cambian por sí mismas con el tiempo: envejecemos, nos cansamos, nos aburrimos, etc. Algunos ejemplos de efectos de maduración:
 
- Al realizar una investigación en psicología del desarrollo, debe tener en cuenta que los niños crecen con bastante rapidez. Entonces, suponga que desea averiguar si algún truco educativo ayuda con el tamaño del vocabulario entre los niños de 3 años. Una cosa que debe tener en cuenta es que el tamaño del vocabulario de los niños de esa edad está creciendo a un ritmo increíble (varias palabras por día), por sí solo. Si diseña su estudio sin tener en cuenta este efecto de maduración, no podrá saber si su truco educativo funciona.
 
- Cuando se realiza un experimento muy largo en el laboratorio (digamos, algo que dura 3 horas), es muy probable que las personas comiencen a aburrirse y a cansarse, y que este efecto de maduración haga que el rendimiento disminuya, independientemente de lo que suceda. en el experimento
 
### Efectos de prueba repetidos
 
Un tipo importante de efecto histórico es el efecto de las pruebas repetidas. Supongamos que quiero tomar dos medidas de algún constructo psicológico (por ejemplo, ansiedad). Una cosa que podría preocuparme es si la primera medición tiene un efecto sobre la segunda medición. En otras palabras, se trata de un efecto histórico en el que el "evento" que influye en la segunda medición es la primera medición en sí. Esto no es nada raro. Ejemplos de esto incluyen:
 
- Aprendizaje y práctica: por ejemplo, la “inteligencia” en el tiempo 2 puede parecer que aumenta en relación con el tiempo 1 porque los participantes aprendieron las reglas generales de cómo resolver preguntas de “estilo de prueba de inteligencia” durante la primera sesión de prueba.
 
- Familiaridad con la situación de la prueba: por ejemplo, si las personas están nerviosas en el momento 1, esto podría hacer que el rendimiento disminuya; Después de pasar por la primera situación de prueba, es posible que se calmen mucho precisamente porque han visto cómo se ve la prueba.
 
- Cambios auxiliares causados por las pruebas: por ejemplo, si un cuestionario que evalúa el estado de ánimo es aburrido, entonces es más probable que el estado de ánimo en la medición en el momento 2 se "aburra", precisamente debido a la medición aburrida realizada en el momento 1.
 
### Sesgo de selección
 
El sesgo de selección es un término bastante amplio. Suponga que está ejecutando un experimento con dos grupos de participantes, donde cada grupo recibe un "tratamiento" diferente, y desea ver si los diferentes tratamientos conducen a diferentes resultados. Sin embargo, suponga que, a pesar de sus mejores esfuerzos, ha terminado con un desequilibrio de género entre los grupos (digamos, el grupo A tiene un 80% de mujeres y el grupo B un 50% de mujeres). Puede parecer que esto nunca podría suceder, pero créame, puede. Este es un ejemplo de un sesgo de selección, en el que las personas "seleccionadas" en los dos grupos tienen características diferentes. Si alguna de esas características resulta ser relevante (digamos, su tratamiento funciona mejor en mujeres que en hombres), entonces está en un gran problema.
 
### Desgaste diferencial
 
Un peligro bastante sutil a tener en cuenta se llama desgaste diferencial, que es una especie de sesgo de selección causado por el estudio en sí. Supongamos que, por primera vez en la historia de la psicología, logro encontrar la muestra de personas perfectamente equilibrada y representativa. Empiezo a ejecutar el “experimento increíblemente largo y tedioso de Dan” en mi muestra perfecta, pero luego, debido a que mi estudio es increíblemente largo y tedioso, mucha gente comienza a abandonar. No puedo detener esto: como discutiremos más adelante en el capítulo sobre ética de la investigación, los participantes tienen absolutamente el derecho de dejar de hacer cualquier experimento, en cualquier momento, por la razón que quieran, y como investigadores somos moral (y profesionalmente) ) obligada a recordar a las personas que tienen este derecho. Por lo tanto, suponga que "el experimento increíblemente largo y tedioso de Dan" tiene una tasa de abandono muy alta. ¿Cuáles cree que son las probabilidades de que esta deserción sea aleatoria? Respuesta: cero. Es casi seguro que las personas que se quedan son más conscientes, más tolerantes con el aburrimiento, etc. que las que se van. En la medida en que (digamos) la conciencia es relevante para el fenómeno psicológico que me importa, este desgaste puede disminuir la validez de mis resultados.
 
Al pensar en los efectos de la deserción diferencial, a veces es útil distinguir entre dos tipos diferentes. El primero es el desgaste homogéneo, en el que el efecto de desgaste es el mismo para todos los grupos, tratamientos o condiciones. En el ejemplo que di anteriormente, la deserción diferencial sería homogénea si (y solo si) los participantes que se aburren fácilmente abandonan todas las condiciones de mi experimento aproximadamente al mismo ritmo. En general, es probable que el efecto principal de la deserción homogénea sea que haga que su muestra no sea representativa. Como tal, la mayor preocupación que tendrá es que la generalizabilidad de los resultados disminuya: en otras palabras, pierde validez externa.
 
El segundo tipo de deserción diferencial es la deserción heterogénea, en la que el efecto de deserción es diferente para diferentes grupos. Este es un problema mucho mayor: no solo tienes que preocuparte por tu validez externa, también tienes que preocuparte por tu validez interna. Para ver por qué este es el caso, consideremos un estudio muy tonto en el que quiero ver si insultar a las personas las hace actuar de una manera más obediente. No sé por qué alguien querría estudiar en realidad, pero supongamos que esto realmente me importaba profundamente. Entonces, diseño mi experimento con dos condiciones. En la condición de "tratamiento", el experimentador insulta al participante y luego le da un cuestionario diseñado para medir la obediencia. En la condición de "control", el experimentador se involucra en una pequeña charla inútil y luego les da el cuestionario. Dejando de lado los méritos científicos cuestionables y la ética dudosa de tal estudio, pensemos en lo que podría salir mal aquí. Como regla general, cuando alguien me insulta en la cara, tiendo a ser mucho menos cooperativo. Por lo tanto, es muy probable que muchas más personas abandonen la condición de tratamiento que la condición de control. Y esta deserción no será aleatoria. Las personas más propensas a abandonar probablemente serían las personas a las que no les importa demasiado la importancia de sentarse obedientemente durante el experimento. Dado que las personas más sangrientas y desobedientes abandonaron el grupo de tratamiento, pero no el grupo de control, hemos introducido una confusión: las personas que realmente respondieron el cuestionario en el grupo de tratamiento ya tenían más probabilidades de ser obedientes y obedientes que las personas en el grupo de control. En resumen, en este estudio, insultar a las personas no las hace más obedientes: ¡hace que las personas más desobedientes abandonen el experimento! La validez interna de este experimento está completamente disparada.
 
### Sesgo de no respuesta
 
El sesgo de no respuesta está estrechamente relacionado con el sesgo de selección y con el desgaste diferencial. La versión más simple del problema es la siguiente. Envía una encuesta a 1000 personas y solo 300 de ellas responden. Es casi seguro que las 300 personas que respondieron no son una submuestra aleatoria. Las personas que responden a las encuestas son sistemáticamente diferentes a las que no lo hacen. Esto introduce un problema al intentar generalizar desde esas 300 personas que respondieron, a la población en general; ya que ahora tiene una muestra muy no aleatoria. Sin embargo, la cuestión del sesgo de no respuesta es más general que esto. Entre las (digamos) 300 personas que respondieron la encuesta, es posible que no todos respondan todas las preguntas. Si (digamos) 80 personas optaron por no responder una de sus preguntas, ¿esto presenta problemas? Como siempre, la respuesta es quizás. Si la pregunta que no fue respondida estaba en la última página del cuestionario, y esas 80 encuestas fueron devueltas sin la última página, es muy probable que los datos faltantes no sean un gran problema: probablemente las páginas simplemente se cayeron . Sin embargo, si la pregunta que no respondieron 80 personas fue la pregunta personal más agresiva o agresiva del cuestionario, es casi seguro que tienes un problema. En esencia, lo que está tratando aquí es lo que se llama el problema de los datos faltantes. Si los datos que faltan se “perdieron” al azar, entonces no es un gran problema. Si falta sistemáticamente, puede ser un gran problema.
 
### Regresión a la media
 
La regresión a la media es una variación curiosa del sesgo de selección. Se refiere a cualquier situación en la que seleccione datos en función de un valor extremo en alguna medida. Debido a que la medida tiene una variación natural, es casi seguro que significa que cuando tome una medición posterior, esa medición posterior será menos extrema que la primera, por pura casualidad.
 
He aquí un ejemplo. Supongamos que estoy interesado en saber si una educación en psicología tiene un efecto adverso en los niños muy inteligentes. Para hacer esto, busco a los 20 estudiantes de Psicología I con las mejores calificaciones de la escuela secundaria y observo qué tan bien les está yendo en la universidad. Resulta que lo están haciendo mucho mejor que el promedio, pero no están encabezando la clase en la universidad, a pesar de que obtuvieron los mejores resultados en la escuela secundaria. ¿Que esta pasando? El primer pensamiento natural es que esto debe significar que las clases de psicología deben tener un efecto adverso en esos estudiantes. Sin embargo, aunque esa podría ser la explicación, es más probable que lo que está viendo sea un ejemplo de "regresión a la media". Para ver cómo funciona, tomemos un momento para pensar en lo que se requiere para obtener la mejor nota en una clase, sin importar si esa clase es en la escuela secundaria o en la universidad. Cuando tengas una clase grande, habrá mucha gente muy inteligente inscrita. Para obtener la mejor nota hay que ser muy inteligente, trabajar muy duro y tener un poco de suerte. El examen tiene que formular las preguntas adecuadas para sus habilidades idiosincrásicas, y no debe cometer ningún error tonto (todos lo hacemos a veces) al responderlas. Y esa es la cuestión: la inteligencia y el trabajo duro se pueden transferir de una clase a otra. La suerte no lo es. Las personas que tuvieron suerte en la escuela secundaria no serán las mismas que las que tuvieron suerte en la universidad. Esa es la definición misma de "suerte". La consecuencia de esto es que, cuando selecciona personas en los valores muy extremos de una medición (los 20 mejores estudiantes), está seleccionando por trabajo duro, habilidad y suerte. Pero debido a que la suerte no se transfiere a la segunda medición (solo la habilidad y el trabajo), se espera que todas estas personas bajen un poco cuando las mida por segunda vez (en la universidad). Entonces sus puntajes retroceden un poco, hacia todos los demás. Esta es una regresión a la media.
 
La regresión a la media es sorprendentemente común. Por ejemplo, si dos personas muy altas tienen hijos, estos tenderán a ser más altos que el promedio, pero no tan altos como los padres. Lo contrario sucede con los padres muy bajos: dos padres muy bajos tenderán a tener hijos bajos, pero sin embargo, esos niños tenderán a ser más altos que los padres. También puede ser extremadamente sutil. Por ejemplo, se han realizado estudios que sugirieron que las personas aprenden mejor de los comentarios negativos que de los positivos. Sin embargo, la forma en que la gente trataba de demostrar esto era darles un refuerzo positivo cuando lo hacían bien y un refuerzo negativo cuando lo hacían mal. Y lo que ves es que después del refuerzo positivo, la gente tendía a hacerlo peor; pero después del refuerzo negativo tendieron a hacerlo mejor. ¡Pero! Observe que hay un sesgo de selección aquí: cuando a las personas les va muy bien, está seleccionando valores "altos", por lo que debe esperar (debido a la regresión a la media) que el rendimiento en la siguiente prueba sea peor, independientemente de si se da refuerzo. Del mismo modo, después de una mala prueba, las personas tenderán a mejorar por sí mismas. La aparente superioridad de la retroalimentación negativa es un artefacto causado por la regresión a la media (ver Kahneman & Tversky, 1973, para discusión).
 
### Sesgo del experimentador
 
El sesgo del experimentador puede presentarse de múltiples formas. La idea básica es que el experimentador, a pesar de las mejores intenciones, puede terminar influyendo accidentalmente en los resultados del experimento al comunicar sutilmente la “respuesta correcta” o el “comportamiento deseado” a los participantes. Por lo general, esto ocurre porque el experimentador tiene un conocimiento especial que el participante no tiene, ya sea la respuesta correcta a las preguntas que se formulan o el conocimiento del patrón de desempeño esperado para la condición en la que se encuentra el participante, etc. El ejemplo clásico de esto es el caso de estudio de “Clever Hans”, que se remonta a 1907 (Pfungst, 1911; Hothersall, 2004). Clever Hans era un caballo que aparentemente podía leer y contar, y realizar otras hazañas de inteligencia humanas. Después de que Clever Hans se hizo famoso, los psicólogos comenzaron a examinar su comportamiento más de cerca. Resultó que, como era de esperar, Hans no sabía cómo hacer matemáticas. Más bien, Hans estaba respondiendo a los observadores humanos que lo rodeaban. Porque sabían contar y el caballo había aprendido a cambiar su comportamiento cuando la gente cambiaba el suyo.
 
La solución general al problema del sesgo del experimentador es participar en estudios doble ciego, donde ni el experimentador ni el participante saben en qué condición se encuentra el participante, o saben cuál es el comportamiento deseado. Esto proporciona una muy buena solución al problema, pero es importante reconocer que no es del todo ideal y es difícil de lograr a la perfección. Por ejemplo, la forma obvia en que podría intentar construir un estudio doble ciego es tener uno de mis doctores. los estudiantes (uno que no sabe nada sobre el experimento) realizan el estudio. Eso parece que debería ser suficiente. La única persona (yo) que conoce todos los detalles (por ejemplo, respuestas correctas a las preguntas, asignaciones de los participantes a las condiciones) no tiene interacción con los participantes, y la persona que habla con la gente (el estudiante de doctorado) ) no sabe nada. Excepto que es muy poco probable que esa última parte sea cierta. Para que el Ph.D. estudiante para ejecutar el estudio de manera eficaz, deben haber sido informados por mí, el investigador. Y resulta que el Ph.D. El estudiante también me conoce, y sabe un poco sobre mis creencias generales sobre las personas y la psicología (por ejemplo, tiendo a pensar que los humanos son mucho más inteligentes de lo que los psicólogos creen). Como resultado de todo esto, es casi imposible que el experimentador evite conocer un poco las expectativas que tengo. E incluso un poco de conocimiento puede tener un efecto: supongamos que el experimentador transmite accidentalmente el hecho de que se espera que los participantes lo hagan bien en esta tarea. Bueno, hay algo llamado “efecto Pigmalión”: si esperas grandes cosas de las personas, estarán a la altura de las circunstancias; pero si espera que fallen, también lo harán. En otras palabras, las expectativas se convierten en una profecía autocumplida.
 
### Efectos de demanda y reactividad
 
Cuando se habla de sesgo del experimentador, la preocupación es que el conocimiento o los deseos del experimentador para el experimento se comuniquen a los participantes y que estos afecten el comportamiento de las personas (Rosenthal, 1966). Sin embargo, incluso si logra evitar que esto suceda, es casi imposible evitar que las personas sepan que son parte de un estudio psicológico. Y el mero hecho de saber que alguien te está mirando / estudiando puede tener un efecto bastante grande en el comportamiento. Esto se conoce generalmente como efectos de reactividad o demanda. La idea básica es captada por el efecto Hawthorne: las personas alteran su desempeño debido a la atención que el estudio les presta. El efecto toma su nombre de la fábrica "Hawthorne Works" en las afueras de Chicago (ver Adair, 1984). Un estudio realizado en la década de 1920 que analizó los efectos de la iluminación en la productividad de los trabajadores en la fábrica resultó ser un efecto del hecho de que los trabajadores sabían que estaban siendo estudiados, en lugar de la iluminación.
 
Para ser un poco más específico sobre algunas de las formas en que el mero hecho de participar en un estudio puede cambiar la forma en que se comportan las personas, es útil pensar como un psicólogo social y observar algunos de los roles que las personas podrían adoptar durante un experimento. pero podría no adoptar si los eventos correspondientes estuvieran ocurriendo en el mundo real:
 
El buen participante intenta ser demasiado útil para el investigador: busca descubrir las hipótesis del experimentador y confirmarlas.
 
- El participante negativo hace exactamente lo contrario del participante bueno: busca romper o destruir el estudio o la hipótesis de alguna manera.
 
- El participante fiel es anormalmente obediente: busca seguir las instrucciones a la perfección, independientemente de lo que pueda haber sucedido en un entorno más realista.
 
- El participante aprensivo se pone nervioso por ser examinado o estudiado, tanto que su comportamiento se vuelve altamente antinatural o demasiado deseable socialmente
 
### Efectos placebo
 
El efecto placebo es un tipo específico de efecto de demanda que nos preocupa mucho. Se refiere a la situación en la que el mero hecho de ser tratado provoca una mejora en los resultados. El ejemplo clásico proviene de los ensayos clínicos: si le das a las personas un fármaco químicamente inerte y les dices que es una cura para una enfermedad, tenderán a mejorar más rápido que las personas que no reciben ningún tratamiento. En otras palabras, es la creencia de las personas de que están siendo tratadas lo que mejora los resultados, no el medicamento.
 
### Efectos de situación, medición y subpoblación
 
En algunos aspectos, estos términos son un término general para "todas las demás amenazas a la validez externa". Se refieren al hecho de que la elección de la subpoblación de la que extrae a sus participantes, la ubicación, el momento y la forma en que realiza su estudio (incluido quién recopila los datos) y las herramientas que utiliza para realizar sus mediciones pueden estar influyendo Los resultados. Específicamente, la preocupación es que estas cosas podrían estar influyendo en los resultados de tal manera que los resultados no se generalizarán a una gama más amplia de personas, lugares y medidas.
 
### Fraude, engaño y autoengaño
 
Una última cosa que siento que debería mencionar. Mientras leía lo que los libros de texto a menudo dicen sobre la evaluación de la validez del estudio, no pude evitar notar que parecen suponer que el investigador es honesto. Encuentro esto divertido. Si bien la gran mayoría de los científicos son honestos, al menos en mi experiencia, algunos no lo son. 6 No solo eso, como mencioné anteriormente, los científicos no son inmunes al sesgo de creencias; es fácil que un investigador termine engañándose a sí mismo haciéndose creer lo incorrecto, y esto puede llevarlo a realizar una investigación sutilmente defectuosa y luego ocultar esas fallas. cuando lo escriban. Por lo tanto, debe considerar no solo la posibilidad (probablemente improbable) de un fraude total, sino también la posibilidad (probablemente bastante común) de que la investigación sea "sesgada" involuntariamente. Abrí algunos libros de texto estándar y no encontré mucha discusión sobre este problema, así que aquí está mi propio intento de enumerar algunas formas en las que pueden surgir estos problemas:
 
- Fabricación de datos. A veces, las personas simplemente inventan los datos. Esto se hace ocasionalmente con "buenas" intenciones. Por ejemplo, el investigador cree que los datos fabricados reflejan la verdad y, de hecho, pueden reflejar versiones "ligeramente depuradas" de los datos reales. En otras ocasiones, el fraude es deliberado y malicioso. Algunos ejemplos de alto perfil en los que se ha alegado o mostrado la fabricación de datos incluyen a Cyril Burt (un psicólogo que se cree que ha fabricado algunos de sus datos), Andrew Wakefield (que ha sido acusado de fabricar sus datos que conectan la vacuna MMR con el autismo) y Hwang Woo-suk (quien falsificó muchos de sus datos sobre la investigación con células madre).
 
- Bromas. Los engaños comparten muchas similitudes con la fabricación de datos, pero difieren en el propósito previsto. Un engaño es a menudo una broma, y muchos de ellos están destinados a ser (eventualmente) descubiertos. A menudo, el objetivo de un engaño es desacreditar a alguien o algún campo. Hay bastantes engaños científicos bien conocidos que se han producido a lo largo de los años (por ejemplo, el hombre de Piltdown), algunos de los cuales fueron intentos deliberados de desacreditar campos particulares de investigación (por ejemplo, el caso Sokal).
 
- Tergiversación de datos. Si bien el fraude ocupa la mayoría de los titulares, en mi experiencia es mucho más común ver que los datos se tergiversan. Cuando digo esto, no me refiero a que los periódicos se equivoquen (lo que hacen, casi siempre). Me refiero al hecho de que, a menudo, los datos en realidad no dicen lo que los investigadores creen que dicen. Mi suposición es que, casi siempre, esto no es el resultado de una deshonestidad deliberada, se debe a una falta de sofisticación en los análisis de datos. Por ejemplo, piense en el ejemplo de la paradoja de Simpson que comenté al principio de estas notas. Es muy común ver a personas presentar datos "agregados" de algún tipo; y, a veces, cuando profundiza y encuentra los datos sin procesar, descubre que los datos agregados cuentan una historia diferente a los datos desagregados. Alternativamente, puede encontrar que algún aspecto de los datos se está ocultando, porque cuenta una historia inconveniente (por ejemplo, el investigador podría optar por no referirse a una variable en particular). Hay muchas variantes en esto; muchos de los cuales son muy difíciles de detectar.
 
- Estudie "diseño incorrecto". De acuerdo, este es sutil. Básicamente, el problema aquí es que un investigador diseña un estudio que tiene fallas incorporadas, y esas fallas nunca se informan en el documento. Los datos que se reportan son completamente reales y están correctamente analizados, pero son producidos por un estudio que en realidad está muy mal elaborado. El investigador realmente quiere encontrar un efecto en particular, por lo que el estudio está configurado de tal manera que sea "fácil" observar (de forma artificial) ese efecto. Una forma engañosa de hacer esto, en caso de que tenga ganas de incursionar en un poco de fraude, es diseñar un experimento en el que sea obvio para los participantes lo que "se supone" que deben hacer, y luego dejar que la reactividad funcione. es magia para ti. Si lo desea, puede agregar todos los adornos de la experimentación a doble ciego, etc. No hará ninguna diferencia, ya que los materiales de estudio en sí le dicen sutilmente a la gente lo que usted quiere que hagan. Cuando escribe los resultados, el fraude no será obvio para el lector: lo que es obvio para el participante cuando está en el contexto experimental no siempre es obvio para la persona que lee el artículo. Por supuesto, la forma en que he descrito esto hace que parezca que siempre es un fraude: probablemente hay casos en los que esto se hace deliberadamente, pero en mi experiencia, la mayor preocupación ha sido el diseño incorrecto no intencional. El investigador cree ... y entonces el estudio acaba con un defecto incorporado, y ese defecto se borra mágicamente cuando el estudio se redacta para su publicación.
 
- Minería de datos e hipótesis post hoc. Otra forma en que los autores de un estudio pueden mentir más o menos sobre lo que encontraron es participando en lo que se conoce como “minería de datos”. Como discutiremos más adelante en la clase, si sigues intentando analizar tus datos de muchas formas diferentes, eventualmente encontrarás algo que “parece” un efecto real pero no lo es. Esto se conoce como "minería de datos". Solía ser bastante raro porque el análisis de datos solía llevar semanas, pero ahora que todos tienen un software estadístico muy poderoso en sus computadoras, se está volviendo muy común. La minería de datos en sí no es "incorrecta", pero cuanto más lo hace, mayor es el riesgo que corre. Lo que está mal, y sospecho que es muy común, es la minería de datos no reconocida. Es decir, el investigador realiza todos los análisis posibles conocidos por la humanidad, encuentra el que funciona y luego finge que este fue el único análisis que realizó. Peor aún, a menudo "inventan" una hipótesis después de mirar los datos, para encubrir la minería de datos. Para ser claros: no está mal cambiar sus creencias después de mirar los datos y volver a analizar sus datos utilizando sus nuevas hipótesis "post hoc". Lo que está mal (y sospecho que es común) es no reconocer que lo ha hecho. Si reconoce que lo hizo, otros investigadores pueden tener en cuenta su comportamiento. Si no lo hace, no pueden. Y eso hace que su comportamiento sea engañoso. ¡Malo!
 
- Sesgo de publicación y autocensura. Por último, un sesgo generalizado es "no informar" de los resultados negativos. Esto es casi imposible de prevenir. Las revistas no publican todos los artículos que se les envían: prefieren publicar artículos que encuentran “algo”. Entonces, si 20 personas realizan un experimento para ver si leer Finnegans Wake causa locura en los humanos, y 19 de ellos descubren que no es así, ¿cuál crees que se publicará? Obviamente, es el único estudio que encontró que Finnegans Wake causa locura 7. Este es un ejemplo de sesgo de publicación: dado que nadie publicó los 19 estudios que no encontraron un efecto, un lector ingenuo nunca sabría que existieron. Peor aún, la mayoría de los investigadores "internalizan" este sesgo y terminan autocensurando su investigación. Sabiendo que los resultados negativos no serán aceptados para su publicación, ni siquiera intentan informarlos. Como dice un amigo mío, “por cada experimento que publicas, también tienes 10 fracasos”. Y ella tiene razón. El problema es que, si bien algunos (tal vez la mayoría) de esos estudios fracasan por razones aburridas (por ejemplo, usted se emborrachó), otros podrían ser resultados genuinos "nulos" que debe reconocer cuando escribe el experimento "bueno". Y decir cuál es cuál es a menudo difícil de hacer. Un buen lugar para comenzar es un artículo de Ioannidis (2005) con el deprimente título “Por qué la mayoría de los hallazgos de investigación publicados son falsos”. También sugiero echar un vistazo al trabajo de Kühberger, Fritz y Scherndl (2014) que presenta evidencia estadística de que esto realmente sucede en psicología.
 
Probablemente haya muchos más temas como este en los que pensar, pero eso servirá para empezar. Lo que realmente quiero señalar es la verdad deslumbrantemente obvia de que la ciencia del mundo real está dirigida por humanos reales, y solo las personas más crédulos asumen automáticamente que todos los demás son honestos e imparciales. Los científicos de verdad no suelen ser tan ingenuos, pero por alguna razón al mundo le gusta fingir que lo somos, y los libros de texto que solemos escribir parecen reforzar ese estereotipo.


<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>

---

## Resumen
 
En realidad, este capítulo no está destinado a proporcionar una discusión exhaustiva de los métodos de investigación psicológica: requeriría otro volumen tan largo como este para hacer justicia al tema. Sin embargo, en la vida real, las estadísticas y el diseño de estudios están estrechamente entrelazados, por lo que es muy útil discutir algunos de los temas clave. En este capítulo, he analizado brevemente los siguientes temas:
 
- Introducción a la medición psicológica (Sección 2.1). ¿Qué significa operacionalizar un constructo teórico? ¿Qué significa tener variables y tomar medidas?
 
- Escalas de medida y tipos de variables (Sección 2.2). Recuerde que aquí hay dos distinciones diferentes: existe la diferencia entre datos discretos y continuos, y existe la diferencia entre los cuatro tipos de escala diferentes (nominal, ordinal, intervalo y relación).
 
- Fiabilidad de una medición (Sección 2.3). Si mido lo "mismo" dos veces, ¿debería esperar ver el mismo resultado? Solo si mi medida es confiable. Pero, ¿qué significa hablar de hacer “lo mismo”? Bueno, por eso tenemos diferentes tipos de confiabilidad. Asegúrese de recordar cuáles son.
 
- Terminología: predictores y resultados (Sección 2.4). ¿Qué papel juegan las variables en un análisis? ¿Puede recordar la diferencia entre predictores y resultados? ¿Variables dependientes e independientes? Etc.
 
- Diseños de investigación experimentales y no experimentales (Sección 2.5). ¿Qué hace que un experimento sea un experimento? ¿Es una bonita bata blanca de laboratorio o tiene algo que ver con el control del investigador sobre las variables?
 
Validez y sus amenazas (Sección 2.6). ¿Tu estudio mide lo que quieres que mida? ¿Cómo pueden salir mal las cosas? ¿Y es mi imaginación, o es una lista muy larga de posibles formas en las que las cosas pueden salir mal?
 
Todo esto debería aclararle que el diseño del estudio es una parte fundamental de la metodología de investigación. Construí este capítulo a partir del pequeño libro clásico de Campbell y Stanley (1963), pero, por supuesto, hay una gran cantidad de libros de texto sobre diseño de investigación. Dedique unos minutos a su motor de búsqueda favorito y encontrará decenas.



<p style="text-align:right;">
<a href="#id-01">Volver</a>
</p>


---

<p style="text-align:right;font-size:80%;">
Escrito por Navarro, Danielle; traducido por García-Mendívil, Helio A.
</p>