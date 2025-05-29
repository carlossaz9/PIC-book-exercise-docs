# Constrained Device Application (Connected Devices)

## Lab Module 12 - Semester Project - CDA Components

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación añade soporte para un sensor de gases y un ventilador actuador en el CDA, generando datos realistas que se envían por MQTT. También incluye un sensor de luz simulado cuyo ventilador se activa o desactiva según comandos recibidos desde el GDA.

How does your implementation work?

Mi implementación funciona creando tareas emuladoras para el sensor de gas y el ventilador, así como para el sensor de luz. Estos simuladores generan datos y envían la información al GDA mediante MQTT o CoAP, siguiendo la misma lógica e integración que los demás dispositivos simulados.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/carlossaz9/PIC-python-components/tree/P12


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- Todos los de las partes 1,2 y 3

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- Todos los de las partes 1,2 y 3

EOF.
