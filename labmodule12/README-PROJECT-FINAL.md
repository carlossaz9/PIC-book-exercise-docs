# Lab Module 12 - Semester Project - Final Write-up

NOTE: Be sure to implement all the Lab Module 12 requirements listed at Lab Module 12.


## Description

Describe your idea in 1 paragraph (at least 2 or 3 sentences).



## What - The Problem 

What problem did you tackle and why does it matter? Write 1 to 2 paragraphs in response.

Este proyecto busca abordar el riesgo asociado a la presencia de gases invisibles que pueden filtrarse en distintos entornos sin ser detectados de manera directa. Situaciones como esta pueden derivar en problemas graves si no se cuenta con un sistema que los identifique y actúe con rapidez.

## Why - Who Cares? 

Why do you care about this particular problem? Write 1 to 2 paragraphs in response.

En contextos como fábricas, almacenes o laboratorios, una fuga de gases puede representar un peligro real tanto para la infraestructura como para las personas. Por ello, desarrollar un sistema automatizado que detecte estas emisiones y reaccione apropiadamente puede ser una solución preventiva muy útil.


## How - Expected Technical Approach

Write 1 to 2 paragraphs describing the outcomes you achieved.

Logré desarrollar un emulador que simula lecturas provenientes de un sensor de gas, con valores realistas que representan concentraciones variables. Estos datos son enviados desde el CDA al GDA mediante MQTT, donde se procesan y reenvían hacia la nube para su posterior uso, como almacenamiento o visualización en dashboards. Además, incorporé la emulación de un ventilador como actuador, capaz de recibir órdenes para activarse o desactivarse en función de los niveles detectados.


### System Diagram

Embed a block diagram depicting your overall design, including the CDA, GDA, and Cloud Services interactions.
Be sure to include arrows depicting data flow from one application / service to the next.



Write 1 to 2 paragraphs describing your design.

CDA ↔ GDA ↔ Cloud

En este esquema, el CDA actúa como fuente de datos, generando información de sensores simulados que es transmitida al GDA. Este último se encarga de procesar los datos recibidos y realizar dos tareas clave: enviar información relevante a la nube para su análisis, y, si corresponde, generar comandos de actuador que vuelven al CDA para activar el ventilador.



### What THREE (3) sensors and ONE (1) actuator did you use (add more if you wish)?

- CDA Sensor 1: Presión

- CDA Sensor 2: Temperatura

- CDA Sensor 3: Humedad

- CDA Actuator 1: Ventilador 



### What ONE (1) CDA protocol and TWO (2) GDA protocols did you implement (add more if you wish)?

- CDA to GDA Protocol: MQTT

- GDA to CDA Protocol: MQTT

- GDA to Cloud Protocol: MQTT

- Cloud to GDA Protocol: MQTT


 
### What TWO (2) cloud services / capabilities did you use (add more if you wish)?

- Cloud Service 1 (data ingress - all inputs):

- Cloud Service 2 (data egress - all actuation events):



## Screen Shots Representing Cloud Services



### Screen Shots Representing Visualized Data

NOTE: Include (at least) TWO (2) screen shots - one showing at least 1 hour
of time-series data from the CDA, and one showing an event being triggered
that results in an actuation event sent to your GDA and then to your CDA.



EOF.
