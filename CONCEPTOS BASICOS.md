CONCEPTOS BASICOS.

Bien antes de nada voy a explicar una serie de conceptos básicos para entender como funciona todo el proyecto y así poder avanzar sin tener que pararme a explicar nada. Vamos a ir poco a poco.

El proyecto se basa mediante VGA y un circuito de contadores junto con una EEPROM mostrar una imagen por pantalla.

VGA.

VGA ("Video Graphics Array") es un conector de tres hileras de 5 pines por el cual se transmiten datos para poder mostrar una imagen por pantalla. La forma para poder hacerlo, se le transmite una serie de datos en un tiempo correcto y VGA va cuadrando la información en pantalla, es decir que si en un periodo de tiempo le damos unos colores, VGA plasmara dicho color en un pixel de la pantalla. En el siguiente tic de tiempo, plasmara el siguiente, y el siguiente... así hasta que una línea horizontal esté llena. Una vez que la línea horizontal este llena de pixeles, salta hacia la línea de arriba y vuelta a empezar. Por lo que poco a poco va rellenando la pantalla según los datos que le vamos dando en esos tics de tiempo.

Datos como: 

Color Rojo.

Color Verde.

Color Azul.

Sincronización Vertical y Horizontal.

Velocidad del reloj.

*Incluir Patillaje VGA.png*

*insertar VGA-real.png*

Si conseguimos manejar esos 5 tipos de datos, podremos mostrar una imagen por pantalla. Lo que voy a realizar es un circuito que de forma analógica sea capaz de transmitir esos datos de forma correcta.

Los colores esta claro que dependiendo de la señal que entre en dichos pines saldrá un color u otro.

La sincronización y Horizontal:

Son dos pines, una para la vertical y otro para la horizontal, estos pines solo entienden de cuando la pantalla para de rellenar pixeles y empieza una nueva línea. Esto es muy importante, porque dependiendo de las entradas que les demos pues estaremos estructurando la resolución de una pantalla.

La velocidad del reloj.

Sirve para poder cuadrarlo todo. Por esta entrada le decimos a VGA los tics de tiempo que queremos que coja dicha información.

Resumen:

Necesitamos para que VGA pueda mostrar una imagen por pantalla necesitamos poder darle en los pin seis datos que controlaremos con nuestro circuito.

Electrónica:

Señal:

Es simplemente la información que viaja a través del circuito, puede ser positiva o nula es decir ó 1 ó 0.

Puerta Lógica:

Una puerta lógica es un chip que se encarga según la entrada de una/as señal/les, modificarlas, gestionarlas o valorarlas, dando un resultado en una señal de salida.

Una puerta logia

De electrónica solo voy a explicar las cosas que voy a usar que van a ser las siguientes:

-Un oscilador de cristal de X hercios.

-Contadores binarios de 4 bits

-Puertas NOT

-Puertas NAND

Vamos por partes:

Un oscilador de cristal:

Es un chip que se encarga de enviar una señal (una señal que sea 0 ó 1) a una velocidad predeterminada que siempre esta medido en hercios. Esos hercios nos van a indicar la frecuencia por la que el oscilador va girando y nos va a dar la señal negativa o positiva.

Es el núcleo del circuito, lo que le da potencia. Dependiendo de la velocidad del oscilador que vayamos a usar, tendremos que usar un circuito u otro.

*insertar oscilador-real.png*

*insertar oscilador-digital.png*

Contadores binarios de 4 bits:

Vamos a usar varios contadores binarios. Estos chips lo único que hacen es contar hasta 4 bits en binario según una entrada. Vamos a conectar el oscilador que le va a ir dando la señal a una velocidad y el contador va contando cuantas veces le entra dicha señal y va devolviendo el numero de veces que ha entrado dicha señal en 4 entradas, cada una con un bit.

Entonces si hay un tic el contador nos devolverá 0001, al siguiente tic, 0010, al siguiente 0011, y así. El numero entero decimal que el contador puede llegar a contar como máximo es el 1111 = 15, en el tic 16, el contador se volverá a 0000, y volverá otra vez a contar.

*insertar contador-digital.png*

*insertar contador-real.png*

Puertas NOT:

Estas puertas simplemente se encargan de invertir la señal de entrada. Si la señal de entrada es un 1, la puerta NOT la convertirá en un 0, y si la señal es un 0, la convertirá en un 1.

*insertar not-digital.png*

*insertar not-real.png*

Puertas NAND:

Una puerta NAND hace lo contrario de una puerta AND, su nombre correcto es "Not AND", invierte la puerta AND. 

El funcionamiento de la puerta AND, es valorar con un AND lógico, las señales de entrada, dando como resultado una señal de salida con la respuesta. 

El AND lógico es un punto básico de la lógica. Se encarga de valorar si dos o mas "cosas" son verdaderas o no. Lo usamos comúnmente en la lógica de nuestro lenguaje:

"Mañana es lunes y hoy es jueves"-> Si valoramos los bloques mañana es lunes y hoy es jueves, podemos decir que la sentencia es falsa.

Una puerta AND hace lo mismo pero con señales, si le entra un 0 y un 1, la valoración es falsa.

*insertar tabla-and.png*

Bien pues a ese resultado que da la puerta AND, le metemos al final una puerta lógica NOT y tendremos el resultado que queremos. Para no tener que estar jugando con dos puertas lógicas y dos chips distintos, se creó un chip que lo engloba todo, la puerta lógica NAND.

*insertar NAND-digital.png*

insertar NAND-real.png*

Ya que estoy explicando todas las piezas que vamos a usar en nuestro circuito eléctrico, voy a añadir también:

Protoboard:

Simplemente es una placa de pruebas para poder diseñar cualquier circuito sin la necesidad de soldaduras, permitiendo la módificacion de una forma muy simple.

*insertar protoboard.png*



Y aquá terminan los conceptos básicos.



