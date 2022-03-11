---
layout: default
title: Tarjetas gráficas
permalink: /03_TarjetasGraficas/
---

<!-- <link rel="stylesheet" type="text/css" href="/css/estilos.css"/> -->

# Tarjetas gráficas

La **tarjeta gráfica**, también conocida como _**tarjeta de vídeo**_, _**tarjeta aceleradora de gráficos**_ o _**adaptador de pantalla**_, es una de las más importantes del equipo, al ser la responsable de mostrar texto, imágenes y gráficos en el monitor.

Muchas placas base actuales integran esta función; sin embargo, la mayoría de los ordenadores utilizan tarjetas gráficas para potenciar y mejorar la salida de datos hacia el monitor.

Controla la apariencia, el movimiento, el color, el brillo y la claridad de las imágenes mostradas en el monitor o la televisión, procesando cada bit de datos enviado.

::: important
La mayoría de las tarjetas gráficas actuales están diseñadas para la ranura **PCI Express x16**; las tarjetas **PCI** y **AGP** están prácticamente extintas.
:::

![Esquema tarjeta gráfica](imgs/EsquemaTarjetaGrafica.png#Width90)

## Componentes

###  GPU (Graphics Processing Unit)

**Procesador** dedicado **específicamente al procesamiento de gráficos** para disminuir la carga de la CPU. Está **optimizado para el cálculo en coma flotante**, predominante en las funciones 3D. Busca mayor realismo en los efectos.

Implementa determinadas **operaciones** gráficas llamadas **primitivas** que están optimizadas para el procesamiento gráfico como la primitiva **antialiasing** (suaviza los bordes de las figuras).

**Frecuencia de reloj del núcleo** o núcleo gráfico (core) actualmente lo normal es entre 400 MHz y 900 MHz.

Dos grandes fabricantes: **nVIDIA** y **ATI** (comprada por **AMD**), pero las empresas que fabrican tarjetas gráficas como ***ASUS***, ***MSI*** o ***GIGABYTE*** optan por utilizar estos componentes y ya tienen en el mercado tarjetas gráficas que van equipadas con dos GPU, como puede ser la ***ATI ASUS 3870 X2***.  

### Memoria de vídeo

En el caso de que la tarjeta gráfica esté integrada en la placa base, se utilizará la memoria RAM propia del ordenador, y si se instala **como tarjeta de expansión**, la tarjeta gráfica dispondrá de una **memoria propia**. Dicha memoria es la memoria de vídeo o **VRAM**.

Así, pues existen memorias gráficas de dos tipos:  

- **Dedicada**: cuando la tarjeta gráfica o la **GPU dispone** exclusivamente para sí esas memorias, esta manera es la más eficiente y la que mejores resultados da.
- **Compartida**: cuando se utiliza memoria en detrimento de la memoria de acceso aleatorio (RAM).

![UEFI de tarjeta con gráfica integrada](imgs/UEFIMISIIntegrada.png#Width80)

Su tamaño oscila entre los 128 MB y 1 TB.  

La memoria actual está **basada en tecnología DDR**, destacando *GDDR2*, *GDDR3*, *GDDR4*, *GDDR5* y *GDDR6*, y en la nueva tecnología de AMD *HBM* (High Bandwidth Memory) y *HBM2*.

La **frecuencia de reloj** de la memoria se encuentra en la mayoría de las tarjetas actuales entre 400 MHz y 14 GHz. Frecuencias de reloj de memoria por tecnología:

| Tecnología | Frecuencia efectiva (MHz) | Ancho de banda GB/s) \
| --- | :---: | :---: |
| GDDR | 166 - 950 | 1.2 - 30.4 |
| GDDR2 | 533 - 1000 | 8.2 - 16 |
| GDDR3 | 700 - 1700 | 5.6 - 54.4 |
| GDDR4 | 1600 - 1800 | 64 - 86.4 |
| GDDR5 | 3200 - 7000 | 24 - 448 |
| GDDR6 | 12000 - 14000 | 48 - 846 |
| HBM | 500 | 512 |
| HBM2 | 500 - 1700 | 1.2 TB/s |

Fuente: [Wikipedia: Tarjetas Gráficas](https://es.wikipedia.org/wiki/Tarjeta_gr%C3%A1fica#GRAM)

La memoria de vídeo tiene los siguientes **parámetros**:  

- **Altura** : número de píxeles desde la parte inferior a la parte superior de la pantalla.
- **Anchura** : número de píxeles desde la parte izquierda a la parte derecha de la pantalla.
- **Profundidad del color** : número de bits usados para cada píxel o cantidad de colores que puede mostrar una imagen. Cuantos más colores mejor calidad y por tanto, mayor fidelidad con el original.
- **Resolución** : número de puntos (píxeles) que es capaz de presentar una tarjeta de vídeo en la pantalla, tanto en horizontal como en vertical. Por ejemplo, 800 x 600 significa que la imagen está formada en total por 600 líneas horizontales de 800 puntos cada una.

- **Píxel** : punto de color de la pantalla.
- **Número de píxeles** : ancho x alto

La resolución se expresa como ancho x alto.  

- **Cantidad de memoria de una tarjeta gráfica** (en bytes) : ancho x alto x profundidad de color / 8.

**A mayor cantidad de memoria de vídeo**, mayor será la cantidad de texturas que la tarjeta gráfica podrá controlar cuando muestre gráficos 3D. Las tarjetas gráficas deben tener memoria suficiente para almacenar la información de los datos de una pantalla.  
La capacidad de la memoria también es importante porque afecta el número y la resolución de imágenes que puede almacenarse.  

![Profundida del color o número de bits](imgs/ProfundidadColor.png#Width90)

![Ejemplo de profundidad de color](imgs/ProfundidadesColor.png#Width70)


- ¿Cómo calcular la memoria necesaria que se necesita para cierta configuración de pantalla?

  - 1280 x 1024 con 32 bits por pixel
  - 1280 x 1024 = 1.310.720 pixels:  
      
  - Cada uno de esos pixels necesita 32 bits para almacenar su color.: 1.310.720 x 32 = 41.943.040 bits
  - Transformando a Bytes: 41.943.040 bits / 8 = 5.242.880 Bytes
  - 5.242.880 / 1024 = 5.120 KBytes / 1024 = 5 MB

- ¿Cómo calcular la memoria necesaria que se necesita para cierta configuración de pantalla?

  - 1920 x 1200 con 32 bits por pixel
  - 1920 x 1200 = 2.304.000 píxels
  - Cada uno de esos píxeles necesita 32 bits para almacenar su color: 2.304.000 x 32 = 73.728.000 bits
  - Transformando a Bytes: 73.728.000 bits / 8 = 9.216.000 Bytes
  - 9.216.000 / 1024 = 9.000 KBytes / 1024 = 8.79 MB = ~ 9MB  

...
> Recuerda las resoluciones de pantalla estañar:

| Siglas | Denominación | Resolución (Pixels) |
| --- | ---| ---: |
| **SD** | Standard Definition | 640 x 480 |
| **qHD** | Quartes of High Definition | 960 x 540 |
| **HD** | High Definition | 1.280 x 720 |
| **FHD** | Full HD o Full High Definition | 1.920 x 1.080 |
| **QHD** | Quad High Definition | 2.560 x 1.440 |
| **UHD** | Ultra High Definition | 3.840 x 2.160 |
| **UHD** | Ultra High Definition 8K | 7.680 x 4.320 |

...
### RAMDAC

El **convertidor digital-analógico de memoria de acceso aleatorio** (RAMDAC) es un conversor de señal digital a señal analógica de memoria RAM. Se usa en la **transformación de señales digitales** (con las que trabaja la tarjeta gráfica) **a señales analógicas** (para poder ser interpretadas por algunos monitores).  
  
El **RAMDAC** es capaz de dar soporte a diferentes velocidades de refresco del monitor (se recomienda trabajar a partir de 75 Hz, nunca con menos de 60).  
  
Debido a la popularidad de los monitores digitales y a que parte de su funcionalidad se ha trasladado a la placa base, _**el RAMDAC está quedando obsoleto.**_  
  
La frecuencia de actualización (o velocidad de refresco) es el número de veces que se dibuja la imagen en la pantalla por segundo y se mide en herzios. Por ejemplo, 72 Hz significa que la pantalla se dibuja 72 veces por segundo.  

## GPU y Arquitectura

Los procesadores gráficos tienen una infinidad de parámetros de rendimiento y además están construidos bajo distintas arquitecturas y fabricantes. En esta lista solamente podremos las últimas tecnologías de cada fabricante, así como las características que debes ser tenidas en cuenta para cada uno de ellos.  

### Arquitectura Turing (Nvidia)

Toda tarjeta gráfica que lleve en su nombre RTX, será de tecnología Turing, y es la tecnología más novedosa de la marca y que nos ofrece las tarjetas gráficas de mayor rendimiento en la actualidad.  

La arquitectura Turing fabrica procesadores con transistores de 12 nm y optimizados para el *Ray Tracing* , o trazado de rayos en tiempo real, Realidad Virtual (VR) e Inteligencia Artificial.  

En las características de los procesadores de las Nvidia RTX podremos identificar los núcleos CUDA, núcleos Tensor y núcleos RT (procesador de Rayos dedicados) dedicados), y la frecuencia de reloj del procesador.  

Mientras mayores sean las cifras de estos núcleos y frecuencia, mayor rendimiento ofrecerá la tarjeta gráfica.  

Los núcleos **CUDA** (*Compute Unified Device Architecture*), también llamado ***CUDA Core*** o ***CUDA Cores***, es como un **mini procesador** que se encarga de cierto tipo de instrucciones, que suelen poder ejecutarse de manera paralela con kits de desarrollo de software de *NVIDIA CUDA 10*, *FleX* y *PhysX* para crear simulaciones complejas, como dinámicas de partículas o fluidos para visualizaciones científicas, entornos virtuales y efectos especiales.

### Diferencias entre CPU y GPU

La **GPU** está especializada en cómputo intensivo, **computación** altamente **paralela** y sus transistores se dedican al procesamiento de datos en lugar de almacenamiento en caché de datos y control de flujo  
  
La **CPU** **pocos** **núcleos** pero **complejos**.  
  
La **GPU** tiene **miles** de **núcleos** **sencillos**, orientados al cálculo (unidades de cálculo FPU independientes).  
  
La GPU no sigue la arquitectura Von Neuman, sino el Modelo Circulante basado en la Segmentación y el Procesamiento Paralelo.  
  
La CPU sigue la arquitectura Von Neuman.

![Diferencias Arquitecturas CPU y GPU](imgs/GPUArquitectura.png#Width80)

## Interfaces con la Placa Base

Existen varios tipos de interfaces que se utilizan para conectar las tarjetas gráficas, aunque en la actualidad prácticamente han desaparecido los formatos PCI y AGP y solo se usa el PCI Express x16.

![Interfaces de conexión AGP](imgs/AGPInterface.png#Width70)

Actualmente se están vendiendo tarjetas gráficas que además de los 16 lanes (x16) soportan el estándar 2.1, lo que supone una tasa de transmisión de 1 GB/s por lan, llegando a los 16 GB/s de ancho de banda (1 GB/s x 16).

![Interfaces de conexión PCI express](imgs/PCIeInterface.png#Width70)

Diferencias entre diferentes ranuras PCIe

![Diferencias entre diferentes ranuras PCIe](imgs/PCIeInterface_2.png#Width70)

Ejemplo tarjetas gráficas con PCIe x16

![Ejemplos de tarjetas gráficas con PCIe x16](imgs/nVIDIAGTX1080.png#Width70)

## Salidas/conectores de la tarjeta gráfica

### SVGA (Super Video Graphic Array - Super VGA)

Conjunto de estándares gráficos diseñados en la década de 1990 para dispositivos CRT; monitor analógico de rayos catódicos.

![Monitor CTR](imgs/MonitorCTR.png#Width50)

Sufre de ruido eléctrico y distorsión por la conversión de digital a analógico. El conector utilizado es el D-sub de 15 pines (DB-15).

![Conector VGA](imgs/ConectorVGA.png#Width40)
  
### DVI  

Sustituto del anterior, fue diseñado para obtener la máxima calidad de visualización en las pantallas digitales.  
  
El DVI también tiene implementado un sistema de mayor envergadura denominado DVI Dual-Link, que permite resoluciones de 2048 × 1536 píxeles.

Hace corresponder directamente un píxel a representar con uno del monitor en su resolución nativa.  
  
Interfaz de video diseñada para obtener la máxima calidad de visualización en pantallas digitales (TFT, LCD, Plasma).  
  
La ventaja frente a VGA está en que el monitor (que es digital) ya recibe la información en formato digital y no se deben hacer conversiones.

![Conector DVI](imgs/ConectorDVI.png#Width30)

Los conectores DVI se clasifican en tres tipos en función de qué señales admiten:  

- DVI-D (solamente digital)
- DVI-A (solamente analógica)
- DVI-I (digital y analógica)
  
A veces se denomina DVI-DL a los conectores que admiten dos enlaces.  

[![Tipos de conectores DVI](imgs/DVI_Connector_Types.jpg#Width70)](https://www.mundovideo.com.co/como-reparar-tragamonedas-manuales-tragamonedas/tipos-de-conectores-dvi-y-diferencias)

### HDMI (High-Definition Multimedia Interface)

Se trata de una interfaz capaz de transmitir señal de vídeo estándar, mejorado o de alta definición, así como audio de alta definición (de hasta ocho canales). Actualmente se está utilizando la versión 2.1.  
Las especificaciones de este tipo de conector permiten un ancho de banda de 48GB/s para dar soporte de 64Hz para monitores 8K y 120Hz para 4K. Compatible con HD-DVD y Blu-Ray.   

| Revisión HDMI | 1.0 | 1.1 | 1.2/1.2a | 1.3/1.3a | 1.4/1.4a/1.4b | 2.0/2.0a/2.0b |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| Máximo ancho de banda de señal (MHz) | 165 | 165 | 165 | 340 | 340 | N/A |  
| Máximo ancho de banda | 4.95 | 4.95 | 4.95 | 10.2 | 10.2 | 18 |  
| Máximo ancho de banda de video (Gbit/s) | 3.96 | 3.96 | 3.96 | 8.16 | 8.16 | N/A |  
| Máximo ancho de banda de audio (MBits/s) | 36.86 | 36.86 | 36.83 | 36.86 | 36.86 | N/A |  
| Resoluciones posibles sobre una señal simple HDMI a 24 bits por pixel | 1920x1080p @60Hz | 1920x1080p @60Hz | 1920x1080p @60Hz | 2560x1440p @60Hz | 4096x2160p @60Hz | 4096x2160p @60Hz |  
| Máxima profundidad de color (bits por pixel) | 24 | 24 | 24 | 48 | 48 | N/A |

Fuente: [Wikipedia](https://es.wikipedia.org/wiki/High-Definition_Multimedia_Interface) 

El conector estándar de HDMI tipo A (que es el que se utiliza actualmente) tiene 19 pines.  
![Conector HDMI. Pinout](imgs/ConectorHDMI.png#Width40)

Se ha definido también una versión de 29 pines (tipo B), que permite llevar un canal de vídeo expandido para pantallas de alta resolución, superiores a las del formato 1080p.

![Conector HDMI](imgs/ConectorHDMI_2.png#Width40)

El HDMI tipo A es compatible con un conector tipo DVI; es decir, que una tarjeta gráfica DVI puede conectarse a un monitor HDMI, y viceversa, mediante un adaptador.

![Conversor DVI a HDMI](imgs/ConversorDVI-HDMI.png#Width50)

### DisplayPort

Puerto para tarjetas gráficas creado por VESA y rival del HDMI, transfiere vídeo a alta resolución y audio.  
  
Sus ventajas son que está libre de patentes, y por ende de regalías para incorporarlo a los aparatos, también dispone de unas pestañas para anclar el conector impidiendo que se desconecte el cable accidentalmente.  

![Conector DisplayPort](imgs/ConectorDP.png#Width50)

Cada vez más tarjetas gráficas van adoptando este sistema, aunque sigue siendo su uso minoritario, existe una versión reducida de dicho conector llamada Mini DisplayPort, muy usada para tarjetas gráficas con multitud de salidas simultáneas, como pueden ser 5.  

![Conector Mini DisplayPort](imgs/ConectorMiniDP.png#Width50)

Al igual que ocurre con HDMI, DisplayPort también es capaz de enviar audio, donde cada versión de dicha interfaz agrega mejoras en este apartado por norma general. Así, es capaz de transmitir audio Dolby, MAT, DRA o DTS HD con un máximo de 8 canales sin compresión a 192 kHz, 24 bits y 6,144 Mb/s.

Lo que más define a DisplayPort es la velocidad y los tipos de conectores que ha ido adquiriendo a modo de compatibilidad con el paso de las versiones.

[![HDMI o DisplayPort ¿Cuál es más adecuado según el tipo de uso? - MuyComputer](imgs/ConectorDP.jpg#Width40)](https://www.muycomputer.com/2019/04/01/hdmi-o-displayport/)

![HDMI o DisplayPort ¿Cuál es más adecuado según el tipo de uso? - MuyComputer](imgs/ConectorDP_2.png#Width30)

Actualmente, VESA ha presentado la versión 2.0, la cual es la más avanzada hasta la fecha y trae grandes mejoras. DisplayPort comenzó con una velocidad máxima de 8,64 Gb/s en mayor de 2006, apoyándose en un cableado de cobre y fibra, con soporte para HDCP y DPCP y sonido 7.1 digital.  
  
Con el paso de las versiones se han añadido soporte para MST, mejoras de la sincronización de audio y vídeo, adaptadores pasivos, soporte para 4K, 8K y 16K (15360 x 8460 @ 60 Hz), soporte para HDMI 2.0, DockPort, un aumento de velocidad de hasta 77,4 Gb/s, mapeo del flujo de datos, soporte para Thunderbolt y USB-C y un menor consumo.  
  
Actualmente, más de 280 fabricantes apoyan directamente esta interfaz, en especial Intel, AMD y NVIDIA, los cuales están apostando muy fuerte por ella debido a sus mayores posibilidades y velocidades frente a HDMI.

### Thunderbolt

La interfaz **Thunderbolt** es un estándar para la **transmisión de datos y energía** en diferentes tipos de dispositivo. Originalmente conocido como Light Peak, fue desarrollado por Intel en colaboración con Apple, que fue la única que dio respaldo comercial realmente sólido a esta interfaz, a la que dio ese nombre por el que fue conocida a posteriori. Su tercera versión fue presentada en 2015, y es la que nos ocupa hoy.  
  
Existe un poco de confusión a la hora de hablar de esta tecnología, sobre todo a la hora de diferenciarla del USB de tipo C. Esto es así porque el **Thunderbolt 3 utiliza un puerto USB-C**, o sea que su aspecto es el mismo exteriormente, pero **no todos los USB de tipo C son Thunderbolt** debido a diferencias en su interior.

![Conector Thunderbolt](imgs/ConectorThunderbolt.png#Width30)

La **velocidad de transmisión** del Thunderbolt 3 es de hasta **40 Gbps (5 GB/s)**, cuatro veces más que el USB 3.1 y el Thunderbolt original. Que ofrecían 10 Gbps. (los discos duros SSD andan entre 200 y 550 MB/s). Además, también soporta conexiones DisplayPort 1.2, HDMI 2.0, y Ethernet 10 Gigabit.  
  
Gracias a la velocidad, el Thunderbolt 3 puede utilizarse para conectar monitores de alta resolución al mismo tiempo. Por ejemplo, uno 5K, dos 4K, o tres FullHD. También permite enchufar las siempre exigentes tarjetas gráficas externas, todo con un mismo conector que también servirá para estar cargando tu equipo.

### Tarjetas gráficas mediante USB

Aunque existen en el mercado desde hace tiempo, no han tenido mucha aceptación entre el público debido  
a su poca potencia.  
  
Son relativamente baratas y normalmente se van a utilizar para dotar a un equipo de más monitores o proyectores en paralelo.  
  
La mayoría dispone de los tipos de salida VGA y DVI, aunque aprovechando la tecnología USB 3.0 se están fabricando tarjetas gráficas USB con salida HDMI.  

![Conversor USB to VGA](imgs/ConversorUSB-VGA.png#Width50)

![Conversor USB Multiple](imgs/ConversolUSB-Multiple.png#Width50)

### Diferencias VGA, DVI, HDMI, DisplayPort y ThunderBolt:

![Todos los conectores](imgs/TodosConectores.png#Width70)
- Video Youtube: Diferencia entre VGA, DVI, HDMI, DisplayPort y ThunderBolt  
  [![Diferencia entre VGA, DVI, HDMI, DisplayPort y ThunderBolt](imgs/YoutubeConectores.png#Width50)](https://youtu.be/ZIE--T0N934)

## Adaptadores 

Dada la diversidad de conectores que hemos visto, existen una serie de apartados entre uno y otros:

### Desde DVI a VGA  

![Conversor DVI to VGA](imgs/ConversorDVI-VGA.png#Width50)

###De HDMI a VGA

![Conversor HDMI to VGA](imgs/ConversorHDMI-VGA.png#Width50)

### De DisplayPort a DVI  

![Conversor DisplayPort to DVI](imgs/ConversorDP-DVI.png#Width50)


### De DisplayPort a HDMI

![Conversor DisplayPort to HDMI](imgs/ConversorDP-HDMI.png#Width50)

## Tarjetas Gráficas Integradas

Las unidades de procesamiento gráfico se clasifican normalmente en dos tipos: GPU integradas y GPU dedicadas.  
  
Las **tarjetas gráficas integradas** tienen la ventaja de ser **más baratas**, lo que a su vez conduce a un ordenador menos costoso. También **disipan mucho menos calor** que las GPU dedicadas y, por lo tanto, permiten máquinas compactas con sistemas de refrigeración relativamente pequeños.  
  
Además, un portátil que se basa únicamente en gráficas integradas será más eficiente en el consumo de energía para una mayor duración de la batería.  
  
La compensación es, por supuesto, el rendimiento que obtienes. Las GPU integradas son perfectas para tareas casuales como ver vídeos y procesar documentos gráficos.  
  
Las **unidades dedicadas o discretas**, por otra parte, vienen con su **propia memoria de vídeo**, que es usada de manera exclusiva para el procesamiento gráfico. Además cuestan más y requieren fuentes de alimentación y sistemas de refrigeración elaborados. Para juegos intensos, son la mejor opción.

La recomendación de uso sería:  

- **Procesador con tarjeta gráfica integrada**: Usuarios que son jugadores ocasionales que no le importa bajar la resolución (720p) y sus filtros (calidad baja o media), tareas básicas: ofimática, navegación web, ver vídeos o retocar a nivel amateur retoque fotográfico.
- **Tarjeta gráfica dedicada**: Usuarios que quieren jugar fluidamente, con buena resolución y gráficamente al máximo en su ordenador. También da un empujón en el renderizado de vídeos o en aplicaciones que sacan el máximo provecho a su tarjeta gráfica. Sin olvidarnos, de aquellos usuarios que quieren estar siempre a la última.  

Diferentes tipos de tarjetas integradas:

### iGPU

Algunas CPU pueden incorporar un procesador gráfico llamado **iGPU**, que no es sino una GPU integrada pero que funciona de manera independiente. De esta manera, se consigue que sin necesidad de una tarjeta gráfica dedicada podamos visualizar el contenido en un monitor, aunque en estos casos el rendimiento es bastante bajo debido a las limitaciones físicas que tienen.

![iGPU dentro de un procesador](imgs/iGPU.png#Width60)

Como características principales tenemos:

- Comparte encapsulado normalmente con la CPU pero también podemos encontrar versiones soldadas a la placa.
- Una iGPU consume RAM del equipo.
- Las iGPU integradas tienen una pequeña cantidad de memoria que puede ser de diferentes tipos pero a la hora de cargar juegos o aplicaciones gráficas intensivas recurren a la RAM principal y la utilizan como memoria de vídeo.
- La RAM del PC se verá reducida en relación al consumo de la iGPU. Si nuestro equipo tiene 4 GB y la iGPU consume 2 GB sólo tendremos otros 2 GB para el sistema.
- Al recurrir a la RAM principal en el ancho de banda de la iGPU influye la velocidad de trabajo de la memoria (Hay que apostar por configuraciones en doble canal o superiores para mejorar el rendimiento).

### APU

Como una variante de las CPU con iGPU, en 2011 AMD lanzó el concepto de **APU**, que se diferencia de éstas en que el hardware para gráficos que integra no solo es bastante más potente (de hecho, AMD las vende como dispositivos para jugar), sino que tienen una diferencia fundamental, la arquitectura HSA (heterogénea).

![AMD APU](imgs/APU.png#Width60)

La arquitectura **HSA** permite el **procesamiento paralelo** y permite que la _**GPU**_ trabaje junto con la _**CPU**_, lo que da un rendimiento general superior.

De este modo, la APU elimina el bus entre la CPU y la GPU para integrar ambas unidades en el mismo chip. Por tanto, una APU es más rápida en tareas gráficas pequeñas, que una CPU y GPU por separado.

Obviamente, tiene sus limitaciones: no podemos pretender que los gráficos integrados de la APU den el mismo rendimiento que una GPU dedicada en, por ejemplo, videojuegos. Sin embargo, en tareas pequeñas, tener una GPU puede ser un malgasto, siendo mejor opción una APU.

### Versiones **AMD APU** y **IntelHD**

**[AMD: APU:](https://es.wikipedia.org/wiki/AMD_Accelerated_Processing_Unit)**  

- Excavator architecture (2016): Bristol Ridge and Stoney Ridge
- Zen architecture (2017): Raven Ridge INTEL HD and Iris Graphics

[![AMD APU](imgs/AMD_APU.png#Width30)](https://www.guiahardware.es/procesadores-amd-apu/) 

**[IntelHD and Iris Graphics](https://en.wikipedia.org/wiki/Intel_Graphics_Technology)**  

- Iris Pro Graphics 6200 (128MB memoria dedicada de vídeo).
- Intel HD Graphics 6000 (64MB de memoria dedicada de vídeo).

[![IntelHD](imgs/IntelHD.png#Width50)](https://www.muycomputer.com/2016/05/25/todo-sobre-gpus-integradas-de-intel/)


## SLI/Crossfire

El **procesamiento en paralelo** es un método para conectar dos o más tarjetas de video PCI Express para producir una sola señal de salida que incremente la capacidad de procesamiento disponible para gráficos En un principio las dos tarjetas deberían ser idénticas mismo fabricante y modelo, sin embargo, hoy no es necesario siempre que se empleen las últimas versiones de los controladores suministrados por el fabricante  
  
El **excedente de memoria no se utilizaría en el funcionamiento conjunto** y además las **GPU** de las tarjetas deben de ser **idénticas**.  
  
**Según** sea el **fabricante** de GPU se la denomina  

- **SLI** (Scalable Link Interface), de la empresa **nVidia**
- **Crossfire** de la empresa **ATI/AMD**

![GeForce GTX 980 TI SLI](imgs/SLI_nVIDIA.png#Width60)

![AMD Crossfire](imgs/AMD_Crossfire.png#Width60) 

**Para unir dos o más tarjetas gráficas** se emplea un **conector** que hace de puente entre ellas, normalmente en la parte superior, y **solamente una de las tarjetas se conectara con el monitor.**

En todo caso, es una tecnología que **no esta prestando los servicios que se esperaban**. El muti-GPU parece que solo aprovecha juegos 4K y ofrecen **problemas** para comportase como se espera, por lo que la evución de estas tecnologías dejo de promoverse en 2018

## Refrigeración

Las tarjetas gráficas alcanzan temperaturas muy altas debido a carga trabajo si no se soluciona puede fallar o averiarse.  
  
Solución dispositivos refrigerantes tipos:  
  
### Disipador dispositivo pasivo

- Sin partes móviles y por tanto silencioso.
- Hecho de material conductor del calor que lo extrae de la tarjeta.
- Suelen ser bastante voluminosos.

![Refrigeración mediante disipador](imgs/Refrigeracion_Disipador.png#Width70)

### Ventilador dispositivo activo

- Con partes móviles y produce ruido.
- Aleja el calor emanado de la tarjeta al mover el aire cercano.
- Es más eficiente que un disipador

![Refregeración mediante ventilador](imgs/Refrigeracion_Ventilador.png#Width70)

Ambos tipos de dispositivos refrigerantes son compatibles entre sí y suelen montarse juntos en las tarjetas gráficas: un disipador sobre la GPU (componente que más calor genera) extrae el calor y un ventilador sobre él aleja el aire caliente del conjunto.  
  
Además de los dispositivos refrigerantes propios de la tarjeta, se pueden instalar en el ordenador otros ventiladores externos.

## Alimentacion

Actualmente casi todas las tarjeta gráficas dedicadas requieren **alimentación auxiliar**, dado que estas tarjetas de expansión, cada vez consumen más y **el puerto PCIe de nuestra placa base no es capaz de suministrar más de 75 W** de potencia, es habitual que incluso modelos de gama baja necesiten este tipo de alimentación.

En un principio esta alimentación adicional no era necesaria, pero poco a poco la potencia de las tarjetas ha demandado más energía y ha propiciado la necesidad de suministro externo.

A continuación tenemos los diferentes conectores usados a lo largo de los años para alimentar las tarjetas gráficas:

![Evolucion de los conectores de tarjetas gráficas](imgs/EvolucionConectoresGraficas.png#Width70)
  
Inicialmente se utilizaban conectores Molex, pero en la actualidad es más habitual encontrar conectores PCI-E de 6 u 8 pines.  

![Alimetación de tarjetas gráficas PCIe](imgs/AlimGraficaPCIeAux.png#Width70)

Es necesario **comprobar que la potencia de la fuente de alimentación** del equipo sea suficiente. Las nuevas tarjetas gráficas de gran potencia necesitan una alimentación específica que dependerá del modelo y sus prestaciones.  

![Alimentación gráfica ATX 12v](imgs/AlimGraficaATX_12.png#Width30)

El cable de alimentación auxiliar para tarjetas gráficas se caracteriza por tomar toda su potencia desde el raíl **+12 V** de la fuente de alimentación. Ello es así porque las gráficas solo usan ese tipo de alimentación para funcionar. Los colores de los cables individuales suelen ser amarillo (para la tensión) y negro para el neutro.  
  
También hay cables adaptadores que permiten usar conectores de alimentación molex o SATA para suplir la ausencia de estos en nuestra fuente de alimentación.

![Adaptador alimantecion SATA](imgs/AlimAdaptSATA.png#Width50)
 
Este tipo de cable es más moderno. Inicialmente se usaban adaptadores que se conectaban a dos conectores molex de la fuente de alimentación. De hecho, hoy en día, este tipo de adaptador de alimentación sigue siendo el más extendido. Y el que más suelen distribuir los fabricantes de tarjetas gráficas con sus modelos.

![Adaptador alimentación tipo Molex](imgs/AlimAdaptMolex.png#Width50)

Como ya se ha comentado, el conector de alimentación es del tipo 6+2. Esto significa que su cuerpo principal es un conector de 6 pines. Al que se le pueden añadir dos pines extra, si la gráfica lo necesitara.

![Adaptador gráfica PCIe](imgs/AlimGraficaPCIe.png#Width50)

Esto da mucha flexibilidad a los fabricantes de gráficas y fuentes. Así como beneficia a los usuarios, en el caso de tener alguna de las primeras gráficas que usaban solo el conector inicial de 6 pines.

![Adaptador gráfica PCIe](imgs/AlimGraficaPCIe_2.png#Width50)

El motivo de la existencia de los dos tipos de conectores, es que uno de ellos es capaz de proporcionar 75 W extra (el de 6 pines), mientras que el otro conector proporciona hasta 150 W de potencia extra (el de 8 pines). A esto hay que sumarle los 75 W que proporciona la ranura PCIe de la placa base a la tarjeta gráfica.

Fuente: [Tipos de alimentación para tarjetas gráficas](https://hardzone.es/tutoriales/componentes/tipos-cables-alimentacion-grafica/)

## Multimonitor

Con la bajada de precios de los monitores actuales y el aumento de la potencia de las tarjetas gráficas, cada vez se está extendiendo más la utilización de varios monitores en paralelo, tanto para juegos como para trabajo (diseño gráfico, hojas de cálculo muy grandes, etc.). 

![Sistema informáticon con dos monitores](imgs/DosMonitores.png#Width60)
Para ello y dependiendo del hardware del que dispongamos, se puede llegar a utilizar más de seis pantallas simultáneamente con un único ordenador. Dispondremos de varios formatos de trabajo, entre ellos:  

*   **En espejo**: Se replica la imagen en todos los monitores. En todos se ve lo mismo.
*   **Escritorio extendido**: Se detectan y enumeran los monitores, y en cada uno de ellos se muestra parte de nuestro escritorio. Puede orientarse en vertical u horizontal.

![Configuración dos pantallas en sistema Windows 10](imgs/ConfigPantallaWindows.png#Width70)

![Configuración dos pantallas en sistema Windows 10](imgs/ConfigPantallaWindows_2.png#Width70)

Para realizar estas tareas de configuración utilizaremos normalmente el sistema operativo o el software propietario de la marca de nuestra tarjeta gráfica:

![Configuración de doble monitor con software de tarjeta](imgs/ConfigPantallaWindows_3.png#Width70)