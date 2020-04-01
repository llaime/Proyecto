PRIMER PASO:

Bien una vez nos ha quedado claro los conceptos básicos, vamos a comenzar a realizar una serie de elecciones para poder crear el circuito.

Para empezar debemos escoger que tipo de VGA vamos a utilizar. Para ellos debemos tener claro 3 cosas:

-Velocidad del reloj.

-Resolución de imagen.

-Tiempos de sincronización.

Para ver dichos datos nos metemos en esta web:

http://tinyvga.com/vga-timing

Esta web nos muestra, los diferentes tipos de VGA según la resolución de pantalla. También nos muestra que velocidad de oscilador necesitamos para poder mostrar a una velocidad "x" de hercios dicha resolución.

*insertar explicando-vgatiming.png*

Vamos a usar precisamente la resolución de "800x600" con una velocidad de imagen de 60 hercios y con un oscilador de 40 Mhz.

Voy a explicaros porque uso precisamente esta opción entre todas las que hay. Principalmente me he visto forzado a escoger dicha resolución. Primero porque para poder escoger resoluciones mas grandes, necesitaría un oscilador superior a los 40 Mhz y no es algo barato ni fácil encontrarlo por internet.

Además ahora cuando entremos veremos que cada resolución tiene un timing distinto según la sincronización vertical y horizontal. Ese timing esta en microsegundos y muchas resoluciones tienen timing que no son números enteros, por lo tanto imposibles de recrear de forma analógica. Por lo que descartamos cualquier variante de resolución en el que los timing, no admitan números enteros.

*insertar 800x600-timing.png*



Bien, vamos a reducir la velocidad de la explicación porque quiero que se entienda esto.

En la imagen vemos muchos datos:

SVGA:

El tipo de VGA que admite estas caracteríscas, es el SVGA o el "Súper VGA". La SVGA se creo para resoluciones de 800x600 que creció hasta 1024x768 pixeles además también incluía 4 bits para los colores que se amplió a 8 bits.

General Timing (Tiempo General):

Aquí podemos la tasa de refresco de la pantalla = 60 Hz.

La tasa de refresco de cada línea de pixeles = 37.87 kHz.

La frecuencia de pixeles = 40 MHz.

Bien, que quiere decir esto, principalmente lo que nos interesa, es que necesitamos un oscilador con una velocidad de 40 MHz para poder enviar las señales con los pixeles de la imagen para hacer funcionar esta resolución.

Horizontal Timing (Tiempo de la línea Horizontal):

Aparte de crear la línea la pantalla también necesita tiempo para sincronizarse con la linea vertical y volver al principio. 

Visible Area = Es la imagen, lo que nosotros vemos en la pantalla, tiene unos 800 pixeles, y tiene que recorrerse en un tiempo de 20 microsegundos.

Front Porch = Este intervalo de tiempo y pixeles, es para parar el haz de pixeles, suele ser parte mas corta, necesita 40 pixeles en un periodo de 1 microsegundos.

Sync Pulse (Pulso de sincronización) = Es el pulso para sincronizar la línea horizontal y vertical, la pantalla ya sabe que ha terminado de imprimir pixeles en esta línea horizontal, espera a que se sincronicen. Necesita 128 pixel en un tiempo de 3.2 microsegundos.

Back Porch = En este periodo de tiempo, es cuando el haz de luz vuelve a la posición 0, para volver a empezar a imprimir por pantalla los pixeles.

Bien para entender todo esto, vamos a dividir los datos en dos partes, la parte en donde hay impresión de imagen, y la parte de parpadeo:

Imagen:

En esta parte solo va a estar la Visible Area, es decir la imagen que vemos

Parpadeo:

Se encuentra todo lo demás, el "Front Porch", "Sync Pulse" y el "Black Porch". Durante dicho parpadeo, se ejecutan estas señales de sincroninación y que permiten darle tiempo a la pantalla para seguir mostrando la línea de pixeles.



*insertar Explicacion-VGA.png*

Ahí podemos ver de una forma más clara el funcionamiento de dichas señales.

Para el Vertical Timing la explicación es la misma, pero para la línea vertical.



