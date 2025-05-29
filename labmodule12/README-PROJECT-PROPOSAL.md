# Lab Module 12 - Semester Project Proposal

## Description

Describe your idea in 1 paragraph (at least 2 or 3 sentences).



## What - The Problem 

What problem are you trying to solve and why does it matter? Write 1 to 2 paragraphs in response.

Este proyecto busca abordar el riesgo asociado a la presencia de gases invisibles que pueden filtrarse en distintos entornos sin ser detectados de manera directa. Situaciones como esta pueden derivar en problemas graves si no se cuenta con un sistema que los identifique y actúe con rapidez.


## Why - Who Cares? 

Why do you care about this particular problem? Write 1 to 2 paragraphs in response.

En contextos como fábricas, almacenes o laboratorios, una fuga de gases puede representar un peligro real tanto para la infraestructura como para las personas. Por ello, desarrollar un sistema automatizado que detecte estas emisiones y reaccione apropiadamente puede ser una solución preventiva muy útil.


## How - Expected Technical Approach

How do you plan to tackle this problem technically?

Include a high-level design diagram depicting your planned technical approach - it does not need to be final, but it must include the CDA, GDA, and cloud services you plan to use, as well as the protocol(s) you will use for communicating between the devices and the cloud.

Write 1 to 2 paragraphs describing your diagram.

La solución técnica consiste en desarrollar un emulador de sensor de gases que produzca lecturas simuladas pero realistas, acompañado de un actuador que represente un ventilador. Este actuador se activa automáticamente cuando se detectan valores de gas por encima del umbral.

En el diseño planteado, el Constrained Device Application (CDA) será el encargado de generar y enviar los datos del sensor a través del protocolo MQTT al Gateway Device Application (GDA). El GDA evaluará estos datos y, en caso necesario, enviará comandos de activación al ventilador. Además, tanto los datos del sensor como las acciones del actuador se enviarán a la nube (Ubidots) para visualización y análisis. La comunicación se basará en protocolos seguros como MQTT sobre TLS.



## Results - Expected Outcomes 

If your project is successful, what outcome do you expect (e.g. what will happen if everything works)? Write 1 to 2 paragraphs describing your expected outcomes.

Si la implementación resulta exitosa, espero que el sistema sea capaz de generar datos de gases, evaluarlos correctamente, y activar el ventilador cuando sea necesario. Todo el flujo de información, desde el sensor hasta la nube, deberá funcionar de manera fluida.

Además, los datos deberían visualizarse en tiempo real en la nube, lo que permitiría monitorear remotamente la presencia de gases en el entorno y comprobar si el sistema de ventilación automatizada responde correctamente ante niveles peligrosos.



EOF.
