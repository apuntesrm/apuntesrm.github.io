---
layout: page
title: Tarjetas de Red
permalink: /04_TarjetasDeRed/
---

<link rel="stylesheet" type="text/css" href="css/estilos.css"/>

# Tarjetas de Red

También conocidas como adaptador de red o **NIC** (**_Network Interface Card_**) y se usan para conectar ordenadores entre sí para compartir recursos y poder formar una red.  
  
Hay distintos tipos de tarjetas de red, en función del tipo de cable o arquitectura que se utilice en la red (coaxial fino, coaxial grueso, fibra de vidrio, etc.) pero el más utilizado es del tipo Ethernet con un conector **RJ-45** (la mayoría de placas base la tienen integrada). 

![Tarjeta de red Ethernet](imgs/TarjetaRed_1.png#Width60){width=50%}

Por otra parte, cada vez está más extendido el uso de redes **Wi-Fi**.

![Tarjeta red WiFi](imgs/TarjetaRedWifi.png#Width60){width=50%}

## Tarjetas de Red Cableadas
Las redes pequeñas se denominan redes de área local o LAN (Local Area Network). En este caso, la red se establece con un cable y componentes hardware que comunican todos los ordenadores.
La tarjeta de red comunica al ordenador con una red local, y suele instalarse en una ranura PCIe de la placa, aunque también tenemos otras alternativas tal y como veremos a continuación.  

Comencemos viendo un ejemplo de tarjeta de red con interfaz **PCIe 1x**, que viene acompañada de sus dos brackets para ajustar a cajas con perfil alto o bajo.

![Tarjeta red se adapta al perfil de chasis](imgs/TarjetaRedPCIe.png#Width60){width=50%}

### Conectores

La salida de conexión de la tarjeta de red debe ser del mismo tipo que el cableado a usar conector más utilizado RJ-45 para el cable de par trenzado.

![Tarjetas ethernet con 4 conectores ](imgs/TarjetaRed4P.png#Width60){width=50%}

Tipos de cable de par trenzado: [![Cables de red de par trenzado](imgs/CablesRedTrenzados.png#Width70){width=50%}](https://www.tele-pc.es/tipos-de-cable-de-red-de-datos-utp-ftp-stp-cat5-cat5e-cat6-cat6a/)  

**Antes** se utilizaban los conectores **BNC** para el tipo de cable coaxial pero su uso está obsoleto. Existen tarjetas de red híbridas que permiten los dos sistemas de conexión.  

![Tarjeta de Red Ethernet con conector RJ-45 y BNC](imgs/TarjetaRed_1.png#Width50){width=50%}

Cable BNC: 

![Cable Red coaxial](imgs/CableBNC.png#Width60){width=50%}

Disponen de LEDs que se iluminan según la actividad de la tarjeta  
![](imgs/TarjetasRedLeds.png#Width60)  

### Dirección MAC (Media Control Address)

Se trata de un **código identificador de 48 bits (6 bytes)** individual que corresponde de forma única a una tarjeta.
Cada dispositivo tiene su propia **MAC** determinada y configurada por el IEEE (los últimos 24 bits) y el fabricante (los primeros 24 bits).
Se codifican en hexadecimal: son 12 números en hexadecimal agrupados de 2 en 2. Por ejemplo: **00-16-E6-5E-7B-74**. 

[![Composición de una dirección MAC](imgs/DireccionMAC.png#Width60{width=50%})](http://standards-oui.ieee.org/oui/oui.txt)

Las direcciones MAC o direcciones físicas son únicas a nivel mundial son escritas en el hardware en el momento de su fabricación de forma binaria.

### Velocidad

Una tarjeta de red puede trabajar a distintas velocidades, en función de la tecnología y los estándares que soporte.
Estándares más utilizados:  

- **Ethernet** 10 Mb/s.
- **Fast Ethernet** 100 Mb/s.
- **Gigabit Ethernet** 1000 Mb/s.

Es común que las tarjetas de red actuales soporten las 3 velocidades y se adapten a la velocidad del resto de los componentes de la red.

### Wake on LAN (WoL)

Estándar de redes de computadoras Ethernet que **permite encender remotamente** ordenadores apagados mediante el envío de un Magic Packet, paquete especial que recibe la tarjeta de red.
El soporte **WoL** está implementado en la **placa base del ordenador** y la mayoría de las placas base modernas cuentan con un controlador.
Ethernet que incorpora WoL sin necesidad de un cable externo. Las placas base antiguas necesitaban un conector WAKEUP-LINK que debía estar enchufado a la tarjeta a través de un cable de 3 pines especial. Debe estar habilitado en la sección administración de energía de la BIOS.

![BIOS. Wake On Lan](imgs/BIOSWakeOnLan.png#Width70){width=60%}

También es posible que sea necesario configurar el equipo para proveer energía a la tarjeta de red cuando el sistema está apagado.

Puede ser necesario activar la característica **WoL** en la tarjeta de red (cómo hacerlo dependerá del sistema operativo y de los drivers).  

![Software MagicPacket](imgs/WOLMagicPacket.png#Width40){width=35%}

En tarjetas con soporte **WoL** que necesiten cable para recibir alimentación: debe tener un conector de 3 pines y desde ese conector debemos conectar un cable a la placa base.
Tanto la tarjeta de red, como la placa base han de soportar esta tecnología.

### Tarjeta de red mediante adaptador USB

Este dispositivo consiste en un adaptador de red con un puerto USB y un puerto RJ-45 10/100/1000 Mb/s Fast/Giga Ethernet.

![Adaptador USB a RJ-48](imgs/ConversorUSB-RJ45.png#Width60){width=50%}

Se puede conectar a cualquier ordenador o portátil dotado de un puerto USB, convirtiendo así la interfaz USB en un puerto de red LAN tipo Ethernet o Fast/Giga Ethernet 10/100/1000 Mb/s.

Como la mayoría de dispositivos USB, se elimina la necesidad de instalar y utilizar tarjetas PCI para ofrecer conectividad LAN al ordenador.

## Tarjeta de Red WiFi

**Wi-Fi** es una marca de la _**Wi-Fi Alliance,**_ la organización comercial que adopta, prueba y certifica los estándares **802.11**.

Es un sistema de envío de datos para redes informáticas que usa ondas de radio en lugar de cables:

- Instalación rápida.
- Menos seguridad que con cable.
- Menor velocidad de transmisión de datos que con cable.

Transmite la información mediante tarjetas de red con una o varias antenas a través de routers o puntos de acceso. Los datos pueden ser enviados mediante algoritmos y procesos de cifrado para mejorar la seguridad.

![Dispositivos WiFI](imgs/WifiDispositivos.png#Width70){width=65%}

En el mercado se pueden encontrar tarjetas de expansión de red para Wi-Fi en formato PCIe pero se está imponiendo el uso de adaptadores red Wi-Fi en formato stickers USB por su facilidad de instalación y portabilidad.

![Tarjeta Wifi con antenas](imgs/WifiTarjeta.png#Width60){width=60%}

Las tarjetas de expansión de red Wi-Fi habilitan al equipo para acceder a este tipo de redes y **también tienen dirección MAC.**

### Clases de normas IEEE 802.11 para WLAN

Lo de **WMAN** y **WLAN** está muy bien, pero consideramos que no es un tema a tratar aquí, ya que estamos centrándonos en las **redes inalámbricas ámbito local**.

Entonces será importante conocer las **distintas versiones del estándar o nombra IEEE 802.11*- para así conocer las velocidades y características que aporta cada versión.

#### IEEE 802.11a/b/g

Estos estándares se consideran identificadores de **canales y frecuencias*- por donde se conectarán los hosts a la WLAN.

Con **802.11a**- opera sobre las bandas de **5 GHz a 20 MHz y 2,4 GHz**, las dos más utilizadas en Wi-Fi al menos en la zona de Europa. Además, en esta zona opera junto a **802.11h** que realiza ciertas modificaciones en el control dinámico de frecuencias y potencias de transmisión para que no existan interferencias con señales por satélite y sistemas de radar.

**802.11 b y g** están operando **solamente en la banda de 2,4 GHz** dotándola de 11 canales para Wi-Fi de los cuales normalmente se utilizan el 1, 6 y 11. En esta banda se opera a una frecuencia de **25 MHz** como ancho de banda. La **velocidad de transmisión** en la versión “b” es de **54 Mbps** sin capacidad de envío OFDM implementado en la última versión disponible.

#### IEEE 802.11n

Esta versión del estándar **empezó a operar en 2008*- aunque se definió en 2004. La velocidad asciende a los **600 Mbps en conexiones como máximo de 3×3*- (3 antenas). Utiliza de **forma simultánea las bandas de 2,4 GHz y 5 GHz**. Fue el primero en implementar la **tecnología MIMO*- (Multiple Input – Multiple Output) que permite usar varios canales a la vez para el envío y recepción de datos con hasta 3 antenas.

![IEEE 802.11g vs 802.11n](imgs/IEEE80211n.png#Width70){width=65%}

Aún no llegamos a tasas de velocidad comparables a cableado LAN, pero el poder utilizar ambas frecuencias con un mismo punto inalámbrico toda a los dispositivos de gran cobertura.

#### IEEE 802.11ac

También se denomina **WiFi 5** y fue implementado en el **año 2014** y a día de hoy la mayoría de aparatos trabajan sobre esta versión. En este caso es una versión que **solamente opera en la banda de 5 GHz** para proporcionarnos velocidades **de 433 Mbps en conexiones con una antena (1×1) y hasta 1,3 Gbps en 3×3**. Su máxima transferencia será de **3,39 Gbps utilizando 4 antenas a una frecuencia de 160 MHz o 6,77 Gbps con 8 antenas.**

Este estándar implementa **tecnología MU-MIMO** con hasta 8 flujos de datos con ancho de bandas de hasta **160 MHz y 256 QAM**. Normalmente opera junto a **802.11n** para los dispositivos que utilicen la banda de 2,4 GHz.

#### IEEE 802.11ax

![Logo Wifi 6](imgs/Wifi6Certified.png#Width60){width=50%}

Esta es la nueva versión también denominada **WiFi 6 y WiFi de 6ª generación** implementada en 2019 y que muchos equipos ya tienen soporte gracias al nuevo hardware. Además de MU-MIMO, se introduce la nueva **tecnología OFDMA** que mejora la eficiencia espectral de la red para WLAN en donde haya conectados gran cantidad de usuarios. Por ello es un estándar que sobre todo **aumenta sus prestaciones con grandes cargas de clientes** y transmisiones simultaneas.

Opera sobre las **frecuencias de 2,4 GHz y 5 GHz**, y soporta **conexiones 4×4 y 8×8** en ambos casos. La velocidad de transmisión aumenta hasta los **11 Gbps con la frecuencia de 160 MHz y 1024QAM.**

![Evolución tecnología Wi-Fi](imgs/WifiEvolucion.png#Width80){width=80%}

![Datos de las diferentes versiones del protocolo 802.11](imgs/WifiTabla.png#Width70){width=70%}

### Tarjetas de Red Wi-Fi USB

Actualmente están apareciendo en el mercado tarjetas de red Wi-Fi que se conectan a través de los puertos USB.

Hay varios tipos en función de las necesidades del usuario:

- **Nanowireless**: tarjetas de tamaño muy pequeño que se colocan en el conector USB para dotar al equipo de funcionalidad Wi-Fi. Apenas sobresalen, son muy baratas y de cómodo transporte.

![Nano Wireless](imgs/NanoWieless.png#Width30){width=30%}

![NAno Wireless](imgs/NanoWireless2.png#Width30){width=30%}

- **Tarjetas con antena externa**: tarjetas que disponen de un conector para acoplar una antena externa. Normalmente este conector es de tipo RP-SMA. El objetivo de este tipo de tarjeta+antena es el de potenciar la señal de emisión/recepción del equipo. Por ejemplo, una tarjeta de red Wi-Fi por USB como la Blueway alcanza 2W de potencia y dispone de una antena de 15 dB.

![Tarjeta Wifi con dos antenas](imgs/WifiTarjeta.png#Width60){width=50%}