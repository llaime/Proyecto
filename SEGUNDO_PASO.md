Segundo Paso.

Ahora tenemos todos los datos de la ecuación para crear la gran parte del circuito.

Para empezar a poder ver algo, vamos a interpretar dichos datos y vamos a transformarlos a un circuito analógico. Lo que vamos a hacer ahora, es preparar los contadores y a entender su utilización en nuestro circuito:

Primero vamos a convertir los datos a contar en binario, ya que nuestros contadores son binarios. Los contadores son binarios para facilitarnos el circuito ahorrandonos la conversion de señal de binario a decimal y viceversa.

Línea Horizontal:

Visible Area : 800          =   11 0010 0000

Front Porch : 40/ 840   =   11 0100 1000

Sync Pulse   : 128/ 968 =   11 1100 1000

Back Porch  : 88/ 1056 =  100 0010 0000

Hemos sumado el valor de cada apartado, porque no vamos a tener un contador para cada elemento de tiempo, si no que vamos a tener un cluster de contadores que van a ir contando. Entonces primero empieza el Visible Area, cuando pasan 800 pulsos va el Front Porch, entonces para cuando haya 840 pulsos empieza el Sync Pulse, y así.

Como podemos ver los números que usamos son de 10 bits y el ultimo de 11. Como mínimo necesitamos contar 11 bits para lo que necesitamos, por lo que necesitaremos 3 contadores para poder contar hasta 11 bits.

El primer contador, contará los 4 últimos bits, el segundo contador los 4 bits del medio, y el tercero contará los 3 últimos.

Cada contador tendrá una salida indicando el estado de cada bit de los 4 que es capaz de contar. Pondremos una puerta NAND recogiendo las 11 salidas conjunto a 11 puertas NOT. Cuando el contador haya contado 800 ticks, la primera puerta, nos dará una salida positiva.

Cuando cuente por 840, la segunda.

Cuando cuente por 968, la tercera.

Cuando cuente por 1056, la cuarta.

Línea Vertical:

Visible Area: 600 	  = 10 0101 1000

Front Porch: 1/ 601   = 10 0101 1001

Sync Pulse: 4/ 604     = 10 0101 1100

Back Porch = 23/ 628= 10 0111 0100

Aquí vamos a usar otros 3 contadores, para poder contar los 10 bits que necesitamos.

Lo mismo que con la linea horizontal, usaremos puertas NAND y NOT para poder obtener una señal positiva cuando los contadores hayan alcanzado dicha suma.