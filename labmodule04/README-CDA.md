# Constrained Device Application (Connected Devices)

## Lab Module 04

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do?

Mi implementación permite la simulación y prueba de un sistema de IoT sin necesidad de hardware físico, utilizando el emulador Sense HAT de Raspberry Pi. Genera datos de sensores de temperatura, humedad y presión, y procesa comandos para controlar dispositivos como humidificadores y sistemas HVAC. Además, emplea la pantalla LED del emulador para visualizar mensajes, facilitando la validación del comportamiento del sistema.

How does your implementation work?

Mi implementación funciona mediante la interacción entre la CDA y el emulador Sense HAT. Los sensores simulados del emulador generan datos en tiempo real sobre temperatura, humedad y presión, que son recogidos por la CDA para su procesamiento y análisis.

Los sensores y actuadores simulados se implementan como clases que heredan de BaseSensorSimTask y BaseActuatorSimTask, respectivamente, sobrescribiendo el método generateTelemetry para devolver valores simulados.

Los sensores son gestionados por la clase SensorAdapterManager, que se encarga de manejarlos y generar sus datos, permitiendo la inicialización de tareas tanto para sensores simulados como reales. De manera similar, los actuadores son gestionados por la clase ActuatorAdapterManager, que permite controlar dispositivos como HVAC, humidificadores y pantallas LED.

Cuando se envía un comando a un actuador, la CDA ejecuta la acción correspondiente y actualiza la pantalla LED del emulador para visualizar los cambios. Dado que no se cuenta con una Raspberry Pi, no se han implementado las partes que dependen directamente del hardware real.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/carlossaz9/PIC-python-components/tree/P4


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- part01
- part02

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- SenseHatEmulatorQuickTest
- HumidityEmulatorTaskTest
- PressureEmulatorTaskTest
- TemperatureEmulatorTaskTest
- HumidifierEmulatorTaskTest
- HvacEmulatorTaskTest
- LedDisplayEmulatorTaskTest
- SensorEmulatorManagerTest
- ActuatorEmulatorManagerTest


EOF.
