---
layout: default
title: Slots de Expansión
permalink: /02_SlotsDeExpansion/
---


<!-- <link rel="stylesheet" type="text/css" href="/css/estilos.css"/> -->

# Slots de expansión

Los **Slots** son unas ranuras de expansión de la placa base donde se insertan las tarjetas.

Incorporan circuitos integrados para operar con diferentes periféricos o ampliar funcionalidades de un equipo

Los **Slots** principales son:  

## PCI (PERIPHERAL COMPONENTS INTERCONNECT)


- Ancho de bus de 32 bits o 64 bits (33 MHz)
- Tasa de transferencia máxima de 133 MB por segundo en el bus de 32 bits (33,33 MHz × 32 bits ÷ 8 bits / byte = 133 MB / s)
- Tasa de transferencia máxima de 266 MB / s en el bus de 64 bits
- 3,3 V o 5 V, dependiendo del dispositivo

![Tipos de Slots PCI](imgs/TiposSlotPCI.png#Width70){width=70%}

## AGP (ACCELERATED GRAPHICS PORT)

Uso exclusivo para tarjetas gráficas. En desuso actualmente.

- **Versión 4x**, tasa de transferencia máxima de 1 GB / s (266 MHz × 32 bits ÷ 8 bits / byte = 1.064 MB / s)
- **Versión 8x**, tasa de transferencia máxima de 1 GB / s (533 MHz × 32 bits ÷ 8 bits / byte = 2.132 MB / s  
    
- Tensiones:
  - 0,7 V o 1,5 V a la 8x
  - 1,5 o 3,3 V a la 4x
  
![Tipos Slots AGO](imgs/TiposSlotAGP.png#Width60){width=60%}

## PCI EXPRESS (PCI-E)
  
**PCI Express** (*Peripheral Component Interconnect Express*) es un bus seriado de datos de alta velocidad. Cuya función es la de comunicar entre sí los diferentes componentes de hardware de un PC. Estos componentes pueden tener todos sus controladores en la placa base. O bien pueden usar controladores externos, en el caso de tratarse de tarjetas de expansión.  
  
Este bus comenzó a introducirse en el año 2003. Y se desarrolló como sustituto del, ya extinto, bus PCI que empleaban las placas base hasta ese momento.

## Versiones del bus **PCIe** desde su creación

Actualmente, se han desarrollado 6 versiones diferentes del bus PCIe:  
  
- **PCIe 1.0**: presentado en el año 2003, tenía una capacidad de transferencia de datos de 2,5 GT/s (GigaTransfers por segundo) y de 250 MB/s por cada vía de datos.
- **PCIe 2.0**: del año 2007, doblaba la tasa de transferencia de datos a 5 GT/s y a 500 MB/s por cada vía de datos.
- **PCIe 3.0**: del año 2010, volvía a doblar las tasas de transferencia de archivos hasta los 8 GT/s y 984,6 MB/s por vía de datos. Precisamente por ello nunca hubo gran diferencia de rendimiento entre usar una tarjeta gráfica para este bus, en un bus PCIe 2.0.
- **PCIe 4.0:**  del año 2017, vuelve a doblar las tasas de transferencia hasta los 16 GT/s y 1.969 MB/s. Este bus de datos ha comenzado a verse recientemente en las placas base para los procesadores AMD Ryzen 3000 y Threadripper 3.
- **PCIe 5.0**: su especificación se ha finalizó el pasado año. Y, como es habitual, vuelve a doblar los datos de la anterior especificación hasta los 32 GT/S y 3.938 MB/s.
- **PCIe 6.0**: su especificación todavía no está finalizada (se la espera para el final del año 2022). Pero volverá a doblar las especificaciones anteriores, llegando hasta los 64 GT/s y 7.8777 MB/s por cada vía de datos.

[![Tabla versiones PCIe](imgs/TablaPCIe.png#Width90){width=90%}](https://es.wikipedia.org/wiki/PCI_Express)

Una particularidad del bus PCIe, es que es un bus modular. Es decir, que los conectores que se emplean en la placa base, no tienen todos las mismas características. En función del número de vías de datos PCI Express conectada a ellos, pueden ser conocidos como x1, x4, x8 o x 16.  
  
Esto quiere decir que físicamente cada conector tiene un número de pines de contacto determinado, donde por ejemplo el conector de mayor tamaño, el x16, puede tener todos los contactos habilitados en su longitud, o en cambio tener solo la mitad, lo que rebajaría su velocidad a x8 lógicamente.  

[![Tipos de placas PCIe](imgs/TiposSlotPCIe.png#Width70){width=60%}](https://hardzone.es/reportajes/que-es/pci-express-caracteristicas/)

![Tipos de placas PCIe](imgs/TiposSlotPCIe_2.png#Width70){width=60%}

## Factor de forma y tarjetas de expansión

Las tarjetas de expansión vienen preparadas para los diferentes factores de forma de las cajas de los equipos:

![Bracket perfil alto y bajo para tarjetas de expansión](imgs/BracketPCIe.png#Width60){width=50%}

Dependiendo del factor de forma, debemos utilizar un **bracket** de **perfil alto** o de **pefil bajo**