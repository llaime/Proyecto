# Ante Proyecto

## Alumno : *Jaime Corrales Pecino*

## Tutor: *Paquito Ávila*

## Nombre Proyecto: *Circuito Tarjeta Grafica VGA*

 

# Introducción.

 

## Descripción del proyecto.

Crear un circuito que muestre una imagen en una pantalla a través de un adaptador VGA.

## Finalidad.

Mostrar una imagen preparada por pantalla sin necesidad de tener una tarjeta gráfica. Además poder enseñar y aprender el funcionamiento a nivel muy bajo y básico de cualquier tarjeta gráfica y monitores y de aprender el funcionamiento de VGA.

## Objetivos.

 

A través de un circuito electrónico que contiene puertas lógicas, contadores, un reloj y una memoria EEPROM o en su caso, una Raspberry o una tarjeta Arduino,  emular el funcionamiento de una tarjeta gráfica, transformando una imagen en pulsos, siendo capaz de mostrarla en pantalla a través de un adaptador VGA.

Siendo especifico, el circuito lo que hará es recorrer la horizontal y la vertical de una resolución de pantalla en un tiempo adecuado(ya que VGA, necesita que para 800x600, la línea de 800 pixeles se recorra entera en 300ms, y la vertical de 600 pixeles en otros 300ms). Además, el circuito procesará una imagen que se transformará en señales eléctricas entendibles para VGA, ya que VGA solo tiene 3 entradas de color (rojo, verde y azul). Esa imagen se transformará en dichas salidas y se transmitirá en el tiempo adecuado para poder mostrar una imagen solida por la pantalla sin necesidad de una tarjeta gráfica.

Las imágenes de una forma sencilla, se transformaran en pulsos con un script y se flasheará en una EEPROM, se procesaran en una tarjeta Raspberry o Arduino según el caso.

El objetivo es poder mostrar al menos una solución adecuada. Se mostrará una imagen estática con una resolución inicial de 800x600.

 

## Medios necesarios.

 

1 – Oscilador de cuarzo de una velocidad de 40Mhz

8 a 32 Puertas lógicas NAND de 8 pines o en su defecto un valor mayor.

8 a 32 Contadores de pulsos electrónicos

1 - Cable VGA

1 – Pantalla con entrada VGA

Varias Protoboards.

1 - Arduino o Raspberry, o en su defecto 1 memoria EEPROM de entre 64K a 1Mb con 8 pines de entrada.

Es Posible que necesite alguna puerta lógica más, o una entrada de energía, pero hasta que no genere las dos primeras partes de la planificación no podré determinar de forma correcta que necesito exactamente.

## Planificación.

·     *Estudio del adaptador VGA, tipos de VGA, entradas y salidas, velocidades de entrada y salida, resoluciones: 20 horas.*

·     *Planificación de circuito y calculo digital de las entradas y salidas y puertas lógicas y contadores necesarios para crear el circuito. 20 horas.*

·     *Generar un circuito en un simulador digital, crear distintos proyectos para comprobar distintas estructuras de montajes y funcionamiento correcto de forma digital. 20 horas.*

·     *Elección de puertas lógicas, contadores, y relojes. 2 horas.*

·     *Montaje del circuito. 16 horas.*

·     *Montaje de Arduino/Raspberry o en su defecto EEPROM. 1 hora.*

·     *Planificación de programa transformador de imágenes: 4 horas.*

·     *Realización del programa transformador de imágenes: 10 horas.*

·     *Preparar imágenes de forma que puedan ser transformadas a pulsos. 4 horas.*

·     *Prueba de todo el proyecto en condiciones reales: 20 horas.*

·     *Preparación de la documentación del proyecto: 12h horas.*



*Horas totales que se planifican para el proyecto: 129 horas.*      
