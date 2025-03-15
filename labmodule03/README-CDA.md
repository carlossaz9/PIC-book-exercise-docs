# Constrained Device Application (Connected Devices)

## Lab Module 03

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do?

Mi implementación simula el funcionamiento de sensores y actuadores en un entorno IoT a través de la aplicación ConstrainedDeviceApp. Utiliza una estructura de clases basada en la clase BaseIotData, de la que derivan otras clases como SensorData, ActuatorData y SystemPerformanceData, para gestionar de manera organizada la información relacionada con los dispositivos.

Los sensores implementados incluyen sensores de humedad, temperatura y presión, que generan telemetría en tiempo real. Por otro lado, los actuadores, como el humidificador y el sistema HVAC (calefacción, ventilación y aire acondicionado), responden a comandos según las condiciones del entorno, simulando su activación y desactivación.

La implementación también incluye gestores como SensorAdapterManager y ActuatorAdapterManager, que centralizan la administración de los sensores y actuadores, coordinando sus interacciones para lograr un control eficiente del dispositivo IoT. Además, se gestiona la información relacionada con el rendimiento del sistema a través de la clase SystemPerformanceData, que permite monitorear el estado global del dispositivo.

How does your implementation work?

1.- BaseIotData: El sistema comienza con la creación de la clase BaseIotData, que contiene los atributos básicos para representar los datos de los dispositivos IoT, tales como tipo, ID, estado, nombre y valor. A partir de esta clase base, se derivan SensorData, ActuatorData y SystemPerformanceData, cada una con atributos específicos para representar sensores, actuadores y el rendimiento del sistema.

2.- Simulación de Sensores: Para la simulación de sensores, se implementa la clase BaseSensorSimTask, que genera los valores de telemetría de los sensores, ya sea de forma aleatoria o utilizando un conjunto de datos predefinido. De esta clase base, se derivan las clases HumiditySensorSimTask, PressureSensorSimTask y TemperatureSensorSimTask, que están especializadas en la captura de datos para humedad, presión y temperatura, respectivamente.

3.- Simulación de Actuadores: De manera similar, los actuadores son gestionados por la clase BaseActuatorSimTask, que permite simular la activación y desactivación de dispositivos físicos a partir de comandos. Las clases HumidifierActuatorSimTask y HvacActuatorSimTask heredan de esta clase base y simulan el comportamiento de un humidificador y un sistema HVAC, respectivamente.

4.- Gestión de Sensores y Actuadores: Se crean los gestores SensorAdapterManager y ActuatorAdapterManager, que son responsables de controlar la ejecución y el monitoreo de los sensores y actuadores. Estos gestores aseguran que los datos se procesen correctamente, gestionando las actualizaciones de los sensores y enviando comandos a los actuadores según corresponda.

5.- Coordinación Global: El DeviceDataManager actúa como el coordinador global del sistema, integrando la gestión de los sensores, actuadores y el monitoreo del rendimiento del sistema. Este gestor centraliza las funcionalidades de los otros dos gestores, y además incluye métodos para gestionar el rendimiento del sistema a través del SystemPerformanceManager.

6.- Ejecución en ConstrainedDeviceApp: El punto de entrada de la aplicación es ConstrainedDeviceApp, que instancia DeviceDataManager y coordina la ejecución de todo el sistema. A través de métodos como start y stop, se inicializa y detiene la gestión de sensores, actuadores y el rendimiento del sistema. Un bucle en el main asegura que el sistema funcione de manera continua.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/carlossaz9/PIC-python-components.git


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ActuatorDataTest
- SensorDataTest
- SystemPerformanceDataTest
- HumiditySensorSimTaskTest
- PressureSensorSimTaskTest
- TemperatureSensorSimTaskTest
- HumidifierActuatorSimTaskTest
- HvacActuatorSimTaskTest
- BaseIotDataTest


### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- SensorAdapterManagerTest
- ActuatorAdapterManagerTest
- DeviceDataManagerNoCommsTest
- ConstrainedDeviceAppTest
- SystemPerformanceManagerTest


EOF.
