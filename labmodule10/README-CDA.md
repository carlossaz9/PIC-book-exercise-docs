# Constrained Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación permite al CDA comunicarse de forma segura con el GDA usando MQTT con cifrado TLS. Soporta el envío de datos (sensores, rendimiento, actuadores) y la recepción de comandos remotos para controlar el humidificador. También incluye lógica local para activar el HVAC según la temperatura.

How does your implementation work?

Mi implementación usa `tls_set` y certificados generados con OpenSSL para establecer una conexión MQTT segura con TLS. Al recibir datos del GDA, el cliente MQTT los procesa, `DeviceDataManager` los convierte a objetos `ActuatorData`, y `ActuatorDataManager` actualiza el humidificador según las instrucciones. También se integró lógica local para activar el HVAC según la temperatura.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/carlossaz9/PIC-python-components/tree/P10


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ConfigUtilTest.py
- SystemCpuUtilTaskTest.py
- SystemMemUtilTaskTest.py
- ActuatorDataTest.py
- SensorDataTest.py
- SystemPerformanceDataTest.py
- HumiditySensorSimTaskTest.py
- PressureSensorSimTaskTest.py
- TemperatureSensorSimTaskTest.py
- HumidifierActuatorSimTaskTest.py
- HvacActuatorSimTaskTest.py
- All unit tests in part02


### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- ConstrainedDeviceAppTest.py
- SystemPerformanceManagerTest.py
- SensorAdapterManagerTest.py
- ActuatorAdapterManagerTest.py
- DeviceDataManagerNoCommsTest.py
- SenseHatEmulatorQuickTest.py
- HumidityEmulatorTaskTest.py
- PressureEmulatorTaskTest.py
- TemperatureEmulatorTaskTest.py
- HumidifierEmulatorTaskTest.py
- HvacEmulatorTaskTest.py
- LedDisplayEmulatorTaskTest.py
- SensorEmulatorManagerTest.py
- ActuatorEmulatorManagerTest.py
- DataIntegrationTest.py
- MqttClientConnectorTest.py
- CoapClientConnectorTest.py
- DeviceDataManagerIntegrationTest.py


EOF.
![QoS0](https://github.com/user-attachments/assets/bf396728-4d1d-4768-95ea-4c5bb3c6c5d7)

![QoS 1](https://github.com/user-attachments/assets/d50160e0-bd58-4a38-9bc7-4f92b380361a)

![QoS 2](https://github.com/user-attachments/assets/c9222695-eb24-4a72-87c4-0cde6db8e04a)



