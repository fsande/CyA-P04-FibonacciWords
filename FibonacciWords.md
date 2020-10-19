# Práctica 04. Palabras de Fibonacci

### Objetivos
Los objetivos de esta práctica son: 

* Que el alumnado conozca la herramienta Doxygen y utilice ese formato para la documentación de sus programas
* Poner en práctica los conocimientos de programación estructurada
* Poer en práctica conocimientos de programación Orientada a Objetos en C++
* Practicar operaciones de entrada/salida (E/S) en ficheros de texto

### Rúbrica de evaluacion de esta práctica
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva)
que se tendrán en cuenta a la hora de evaluar esta práctica:

* El alumnado ha de acreditar conocimientos para trabajar con la shell de GNU/Linux en su VM
* El código ha de estar escrito de acuerdo al estándar de la [Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html).
* El alumnado ha de acreditar que es capaz de formatear su código usando VSC de acuerdo al estándar anterior
* El alumnado ha de acreditar capacidad para editar ficheros remotos en la VM de la asignautra usando VSC
* El programa desarrollado deberá compilarse utilizando la herramienta `make` y un fichero `Makefile`
* El comportamiento del programa debe ajustarse a lo solicitado en este documento.
* Ha de acreditarse capacidad para introducir cambios en el programa desarrollado.
* Los comentarios del programa han de escribirse en formato Doxygen.
* Modularidad: el programa ha de escribirse de modo que las diferentes funcionalidades que se precisen sean encapsuladas en funciones y/o métodos cuya extensión textual se mantenga acotada.
* El programa ha de ser fiel al paradigma de programación orientada a objetos (OOP).

Si el alumnado tiene dudas respecto a cualquiera de estos aspectos, debiera acudir al
foro de discusiones de la asignatura para plantearlas allı́. 
Se espera que, a través de ese foro, el alumnado intercambie experiencias y conocimientos, ayudándose mutuamente
a resolver dichas dudas. 
También el profesorado de la asignatura intervendrá en las discusiones que pudieran suscitarse, si fuera necesario.
    
### Introducción
Las palabras de Fibonacci, F<sub>1</sub>, F<sub>2</sub>, F<sub>3</sub>, ... se definen como:
* F<sub>1</sub> = "a"
* F<sub>2</sub> = "b"
* Para cualquier n ≥ 3, F<sub>n</sub> es el resultado de concatenar F<sub>n-2</sub> con F<sub>n-1</sub>.

Las primeras siete palabras de la secuencia de Fibonacci son:
F<sub>1</sub> = "a",
F<sub>2</sub> = "b",
F<sub>3</sub> = "ab",
F<sub>4</sub> = "bab",
F<sub>5</sub> = "abbab",
F<sub>6</sub> = "bababbab",
F<sub>7</sub> = "abbabbababbab".

### Ejercicio práctico
Diseñar e implementar en C++ un programa `fibonacci_words.cc` que dada una secuencia de palabras indique 
si son palabras de Fibonacci o no.
Para aquellas que lo sean, el programa ha de indicar su posición en la secuencia.

Realice un enfoque orientado a objetos para el desarrollo de su programa: identifique objetos en el problema
que se propone resolver y modele esos objetos mediante las clases y métodos que considere más adecuados.

El programa tomará su entrada de un fichero de texto, y su salida la escribirá igualmente en otro.
Si el fichero de entrada contiene las siguientes palabras:

```
a
b
ba
aaa
bb
bababbab
```

y el fichero se llama `input.txt`, cuando el programa se invoque como

`$> ./fibonacci_words input.txt output.txt`

el contenido del fichero `output.txt` debiera ser el que se muestra a continuación:

```
a is the word number 1
b is the word number 2
ba is not a Fibonacci word
aaa is not a Fibonacci word
bb is not a Fibonacci word
bababbab is the word number 6
```

Cuando el programa se invoque sin pasarle parámetros en la línea de comandos, deberá finalizar su ejecución,
imprimiendo en pantalla un mensaje de una única línea que indique la forma correcta de ejecución.
Si el programa se invoca pasándole por línea de comandos el parámetro `--help`:

`$> ./fibonacci_words --help`

El programa deberá igualmente finalizar su ejecución pero indicando en este caso el modo correcto de invocarlo
así como una breve explicación de la finalidad del programa.

### Doxygen
[Doxygen](https://www.doxygen.nl/index.html) es un generador de documentación para código fuente que permite
generar la documentación completa de un proyecto software.
La documentación está escrita en en el código, y por lo tanto es relativamente fácil de mantener actualizada. 
Doxygen puede hacer referencias cruzadas entre la documentación y el código, de modo que posibilita que
el lector de un documento pueda referirse fácilmente al código fuente de la aplicación.
Doxygen es un software libre y al igual que Javadoc extrae la documentación de los comentarios de los ficheros fuente. 
La herramienta puede generar documentación en HTML así como en otros formatos.

A partir de esta práctica, todos los programas que se desarrollen deberán contener su documentación escrita en
formato Doxygen.
Se propone que no se ocupen tanto del uso de la herramienta en sí, sino de que la documentación de su código
se escriba de aucuerdo al estándar de esa herramienta.
Para iniciarse en el uso de Doxygen se propone que estudie las siguientes referencias:

### Referencias
* [Doxygen](https://www.doxygen.nl/index.html) 
* [Documenting the code](https://www.doxygen.nl/manual/docblocks.html#specialblock) 
* [How to document your code for doxygen](https://www-numi.fnal.gov/offline_software/srt_public_context/WebDocs/doxygen-howto.html)
* [Doxygen comments in VSC](https://devblogs.microsoft.com/cppblog/visual-studio-code-c-extension-july-2020-update-doxygen-comments-and-logpoints/)
