# Constrained Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación recoge datos de telemetría de la CPU y la memoria, y habilita la conversión de datos de sensores, actuadores y rendimiento a JSON y viceversa. En el CDA, SensorDataManager y ActuatorDataManager son los encargados de la adquisición y transformación de datos, asegurando que la información del hardware del dispositivo se convierta en un formato estructurado antes de enviarla al GDA. Este sistema permite la serialización, deserialización, procesamiento y transmisión eficiente de los datos de los sensores, así como la recepción y ejecución de los comandos de los actuadores.

How does your implementation work?

Mi implementación funciona gestionando de manera estructurada los datos del dispositivo a través de clases específicas para sensores y actuadores. SensorDataManager recopila los datos de los sensores, los convierte a JSON y los transmite, mientras que ActuatorDataManager recibe los comandos, los deserializa y ejecuta las acciones en los actuadores. La comunicación entre el CDA y el GDA se realiza mediante MQTT o CoAP, enviando datos de sensores como temperatura, humedad o presión, y recibiendo comandos para los actuadores.

Se realizan modificaciones en SystemPerformanceManager para recopilar la telemetría de CPU y memoria, y se crea un setter para dataMessageListener. Además, DataUtil se adapta para convertir los datos de sensores, actuadores y rendimiento a JSON y viceversa.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/carlossaz9/PIC-python-components/tree/P5


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

EOF.
