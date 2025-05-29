# Gateway Device Application (Connected Devices)

## Lab Module 08

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación permite la comunicación entre dispositivos usando CoAP. Se desarrolló un servidor CoAP (CoapServerGateway) que registra dispositivos y procesa datos mediante handlers específicos para rendimiento del sistema y sensores. Además, se integró soporte para manejar datos de actuadores y añadir recursos dinámicamente.

How does your implementation work?

Mi implementación funciona mediante la clase `CoapServerGateway`, que inicia un servidor CoAP y organiza los recursos en rutas jerárquicas. Al arrancar, registra manejadores que procesan mensajes `POST`, `PUT` y `GET`, según el tipo de datos (sensores, rendimiento, actuadores). Se integra con `DeviceDataManager`, que permite activar o desactivar el servidor según la configuración, y se pueden añadir recursos dinámicamente para mayor flexibilidad.


### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/carlossaz9/PIC-java-components/tree/P8


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ConfigUtilTest
- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest
- ActuatorDataTest
- SensorDataTest
- SystemPerformanceDataTest
- SystemStateDataTest
- DataUtilTest


### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- GatewayDeviceAppTest
- SystemPerformanceManagerTest
- DataIntegrationTest
- DeviceDataManagerNoCommsTest
- MqttClientConnectorTest
- MqttClientControlPacketTest
- UpdateResourceHandlerTest
- GetActuatorCommandResourceHandlerTest
- CoapServerGatewayTest


EOF.
