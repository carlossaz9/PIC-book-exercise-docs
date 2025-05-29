# Gateway Device Application (Connected Devices)

## Lab Module 07

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación habilita la comunicación bidireccional del GDA mediante MQTT. El cliente MQTT puede publicar datos y suscribirse a temas para recibir información en tiempo real. Para ello, se creó la clase MqttClientConnector, que configura la conexión, gestiona la publicación y suscripción de mensajes, y maneja los eventos del protocolo. Esta clase se integra en DeviceDataManager, activándose según la configuración.

How does your implementation work?

Mi implementación usa la librería Paho para manejar la comunicación MQTT de forma asincrónica. La clase MqttClientConnector configura y gestiona la conexión al broker, permitiendo publicar, suscribirse a temas y manejar eventos MQTT. Esta clase se integra en DeviceDataManager, activándose según la configuración. Verifiqué su funcionamiento con Wireshark.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/carlossaz9/PIC-java-components/tree/P7


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


EOF.
