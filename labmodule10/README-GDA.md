# Gateway Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación permite al GDA recibir y procesar de forma segura y asíncrona los datos del CDA vía MQTT con autenticación y TLS. Gestiona automáticamente las suscripciones a los temas del CDA y analiza la humedad recibida para enviar comandos de actuador cuando es necesario. Además, registra y transmite la información de sensores para su procesamiento.

How does your implementation work?

Mi implementación usa MqttAsyncClient para comunicación asíncrona y segura mediante TLS y autenticación. MqttClientConnector gestiona la conexión y suscripciones con listeners que reciben y validan mensajes, enviándolos a DeviceDataManager. Este analiza los datos (como la humedad) y genera comandos de actuador si detecta valores fuera de rango.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/carlossaz9/PIC-java-components/tree/P10



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
- DeviceDataManagerSimpleCdaActuationTest

EOF.

![QoS 0](https://github.com/user-attachments/assets/1ade485a-8f7d-4079-a798-729bdbec9939)

![QoS 1](https://github.com/user-attachments/assets/bea94cb8-7d11-45df-99e0-26ea66e61f4c)

![QoS 2](https://github.com/user-attachments/assets/8836b096-56ee-449c-936d-924d6e68b21c)

![POST-CON](https://github.com/user-attachments/assets/30de75ec-eee0-40ac-bd25-d4b3f82b7c55)

![POST-NON](https://github.com/user-attachments/assets/4885c318-2eb3-4e97-9d97-786a06cd02bb)

![PUT-CON](https://github.com/user-attachments/assets/55b206d7-d33f-4409-9818-95801915753c)

![PUT-NON](https://github.com/user-attachments/assets/f5254e43-7cb7-4413-9d96-b148cb0ed86e)



