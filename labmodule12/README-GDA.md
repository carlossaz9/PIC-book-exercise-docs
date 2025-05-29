# Gateway Device Application (Connected Devices)

## Lab Module 12 - Semester Project - GDA Components

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación permite que el GDA reciba por MQTT o CoAP los nuevos datos generados en el CDA y los envíe a la nube, integrando estos sensores y actuadores nuevos con el sistema cloud existente.

How does your implementation work?

Mi implementación modifica el flujo de envío de datos para incluir los datos del sensor de gases y luz, que el GDA recibe del CDA y reenvía a la nube usando CloudClientConnector. Además, procesa comandos de actuadores recibidos vía MQTT, creando objetos ActuatorData que envía al CDA para controlar el ventilador. Se incluyen tests para validar estos nuevos dispositivos.


### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/carlossaz9/PIC-java-components/tree/P12



### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- Todos los de las partes 1,2,3 y 4

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- Todos los de las partes 1,2,3 y 4

EOF.
