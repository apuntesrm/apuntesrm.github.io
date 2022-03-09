---
layout: page
title: Tarjetas de Sonido
permalink: /04_TarjetasDeSonido/
---

<link rel="stylesheet" type="text/css" href="css/estilos.css"/>

# Tarjeta de sonido

Dispositivo que permite la **reproducción**, **grabación** y **digitalización del sonido**, normalmente a través de software específico. Las placas base actuales normalmente disponen del sistema de sonido integrado y suelen ser de calidad, así que es poco usual ampliar con tarjetas de expansión de sonido.

![Tarjetas de Sonido](imgs/TarjetasSonido.png#Width70){width=60%}

Normalmente la encontramos ncorporada e la placa base. Se añade una tarjeta de sonido si se necesita un uso profesional (músicos, compositores ...)  

- Combinado con un software específico, permite la reproducción, grabación y digitalización del sonido
- Actualmente encontramos conexiones PCI-e 1x, PCI y USB

## Canales y polifonia

### Multicanal  

Se denomina **audio multicana**l o **sonido multicanal** al uso de **múltiples pistas de audio** para reconstruir el sonido en un sistema de múltiples altavoces o de sonido envolvente. No debe confundirse el sonido multicanal con altavoces de 2 vías o 3 vías (altavoces), puestos que estos últimos utilizan un solo canal de audio por altavoz aunque utilicen varios altavoces para reproducirlo según la frecuencia.  
  
Para definir las distintas configuraciones de altavoces utilizadas, se usan dos dígitos separados por un punto decimal (2.1, 3.0, 5.1, 6.1, 7.1, etc.), dependiendo de la cantidad de pistas de audio que se utilicen.  

- El **primer dígito** muestra el número de canales primarios o completos, cada uno de ellos reproducido en un altavoz individual
- El **segundo dígito** se refiere a la presencia de un canal para efectos de baja frecuencia (abreviado, LFE, por sus siglas en inglés) que se reproduce en un altavoz de subgraves. 

Así:  

- **1.0** corresponde al sonido mono (que significa un solo canal).
- **2.0** corresponde al sonido estéreo
- **2.1** corresponde al sonido estéreo con un canal adicional para efectos de baja frecuencia.  

Normalmente se denomina audio o sonido multicanal a partir de una configuración de 3 canales (2.1 o 3.0).

Las configuraciones multicanal habituales son:  

[![Tabla Canales para audio multicanal](imgs/TablaCanalesSonido.png#Width70){width=60%}](https://es.wikipedia.org/wiki/Audio_multicanal)

En cuanto a la **distribución sonora**, los sonidos que se emiten por los distintos canales suelen ser de diferente rango para crear una sensación de sonido envolvente. Los rangos utilizados por cada canal suelen ser los siguientes:  

- Los canales frontales izquierdo y derecho utilizan rango completo, emitiendo sonidos de todo tipo, a excepción de los bajos.
- El canal frontal central suele ser para rangos medios, emitiendo sonidos medios o de voz.
- Los canales laterales y traseros se utilizan para sonidos de ambientación.
- El canal de subgraves se utiliza para los sonidos graves con frecuencias de hasta 100 Hz aproximadamente.

![Distintas configuraciones de sonido multicanal](imgs/SonidosDistribucion.png#Width70){width=60%}

En la actualidad se utilizan las tarjetas de sonido envolvente (surround), principalmente Dolby Digital 8.1 o superior.

## Operaciones básicas

- **Grabación**: el sonido se recoge normalmente a través de un micrófono y llega a la tarjeta a través de los conectores. Esta señal se recoge, se procesa y se almacena en el formato seleccionado.  
  
- **Reproducción**: la señal digitalizada de un sonido se envía a la tarjeta que la procesa y la manda a través de los conectores de salida hacia los altavoces, auriculares, etc.  
  
- **Síntesis**: procedimiento mediante el que las tarjetas reproducen sonidos a partir de datos o representaciones simbólicas, como pueden ser los códigos MIDI.

  - **Síntesis FM**: imita el sonido de un instrumento musical manipulando la onda, su amplitud y frecuencia
  - S**íntesis por Tabla de Onda (WaveTable)**: la tarjeta de sonido alberga en la memoria una colección completa de notas de instrumentos en forma de secuencias sonoras reales muy cortas previamente digitalizadas. Cuando el archivo sonoro se va reproduciendo, la tarjeta busca en la tabla y escoge el sonido que corresponde a cada caso.
  - **Síntesis de Modelado Físico**: se simula el sonido de un instrumento musical mediante el cálculo numérico de las ondas de sonido (se tienen en cuenta parámetros como la vibración del sonido en un tubo, una cuerda, una membrana en percusión, etc).  

## MIDI (Music Instrument Digital Interface)

Estándar industrial adoptado por la industria musical y el mundo informático que regula la forma en que se conectan instrumentos y ordenadores, a través de qué cables y el formato de los mensajes que se intercambian.  
  
MIDI permite a los instrumentos electrónicos musicales comunicarse bidireccionalmente con el ordenador.  
  
Los códigos MIDI no transmiten música, sino órdenes musicales. Un mensaje MIDI consta de un byte de estado seguido de un cero o más bytes de datos; cada mensaje corresponde a un evento musical del tipo de la pulsación de una tecla o un pedal, el giro o desplazamiento de un control, etc. A cada instrumento musical se le asigna un código MIDI de un total de 128 disponibles.

![Cabla MIDI](imgs/CableMIDI.png#Width70){width=60%}

## Componentes

Los elementos que componen una tarjeta de sonido son los siguientes:  

![Componentes de una tarjeta de sonido](imgs/TarjetaSonidoElementos.png#Width80){width=75%}

### Mezclador

Se encarga de mezclar los distintos tipos de sonido que le llegan o que envía al exterior. Puede emitir sonido sintetizado y reproducido a la vez. Normalmente se controla por software. 

### ADC (Analog to Digital Converter)

Se encarga del proceso de convertir una señal de ondas analógica en su equivalente digital (denominado modulación digital). Para ello se captura el sonido almacenando en los valores de amplitud de una onda a intervalos regulares de tiempo. La amplitud de la onda de sonido determina su volumen, la frecuencia determina su escala (en el rango más grave o más aguda).  

### DAC (Digital to Analog Converter)

Realiza la de modulación digital, permitiendo reproducir el sonido tras convertir las señales digitales en analógicas.  

### DSP (Digital Signal Processor)

Pequeño microprocesador que efectúa los cálculos necesarios para gestionar el sonido, con tareas como la compresión y la descompresión de su señal. También realiza otras tareas como producir efectos de sonido, ecos, reverberaciones, coros, etc, empleando para ellos varios tipos de algoritmos.  

### Búffer

Pequeña memoria que almacena temporalmente los datos que se envían entre ordenador y tarjeta. Permite una gestión de ajustes de tiempo.  

Además de los _**sintetizadores FM**_ y por _**tablas de ondas**_ que permiten la genearción de sonidos a partir de frecuencias y ondas.  

### Interfaz con la placa madre

Permite transmitir información entre tarjeta y ordenador. En la actualidad es a través del PCI express.

## Salidas

### Salidas analógicas tipo "jack"

Las salidas de una tarjeta de sonido son las siguientes:

![Salidas de una tarjeta de sonido](imgs/TarjetaSonidoSalidas.png#Width70){width=60%}

**Código de colores**: hay que consultar el manual pero generalmente son:  

- **Rosa**: Entrada analógica micrófono
- **Azul**: Entrada analógica de línea
- **Verde**: Salida analógica altavoces frontales
- **Negro**: Salida analógica altavoces traseros
- **Plateado**: Salida analógica altavoces laterales
- **Naranja**: Salida subwoofer o S / PDIF

![Salida tarjeta de sonido analógica](imgs/TarjetaSonidoSalidas2.png#Width50){width=50%}

### S/PIDF

Formato de Interfaz digital y Analógica Sony/Phillips

![Salidas de audio S/PIDF](imgs/SPIDF.png#Width50){width=50%}

Dos posibilidades:  

- Analógica. Cable Coaxial. Conectores RCA

- Digital: Fibra óptica. Conector Toslink:

![Conectores S/PDIF](imgs/SPIDF_CableAnalogico.png#Width50){width=40%} 

![Conectores S/PDIF](imgs/SPIDF_CableAnalogico2.png#Width50){width=40%}