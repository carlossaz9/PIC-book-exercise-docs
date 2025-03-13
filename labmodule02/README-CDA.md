# Constrained Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación establece la base para la recopilación de datos de telemetría del sistema, específicamente el uso de memoria y CPU. Aunque por sí sola aún no realiza acciones avanzadas, sienta las bases para el monitoreo y la gestión eficiente del rendimiento en la plataforma de IoT.

How does your implementation work?

Se ha creado una clase base para las tareas de adquisición de telemetría, a partir de la cual se derivan dos clases específicas:

SystemCpuUtilTask → Obtiene métricas de uso de CPU.
SystemMemUtilTask → Obtiene métricas de uso de memoria.

Estas clases implementan métodos específicos para la recopilación de datos. Su ejecución es gestionada por el SystemPerformanceManager, que las activa y desactiva según sea necesario.

El SystemPerformanceManager:

- Llama a las tareas de telemetría a través del método handleTelemetry().
- Gestiona la frecuencia de muestreo (pollRate).
- Mantiene un registro de las mediciones en un log.
- Inicializa configuraciones clave del sistema, como el pollRate y el locationID.

De esta forma, la implementación permite el monitoreo continuo del sistema y prepara la infraestructura para futuras mejoras en la plataforma de IoT.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/carlossaz9/PIC-python-components.git

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest
- ConfigUtilTest

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- ConstrainedDeviceAppTest
- SystemPerformanceManagerTest

EOF.
