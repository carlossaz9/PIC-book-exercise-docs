# Gateway Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-GDA-* issues.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

La implementación establece las funciones básicas de monitoreo del Gateway Device Application (GDA) en un sistema IoT. Su objetivo principal es recopilar y registrar métricas de uso de CPU y memoria secundaria de manera automatizada. Para ello, implementa clases y métodos que permiten:

- Iniciar y detener el monitoreo del rendimiento del sistema.
- Registrar los datos de telemetría en logs para su posterior análisis.
- Ejecutar tareas de monitoreo en intervalos fijos mediante programación asíncrona.

Todo el sistema se lanza desde la GatewayDeviceApp, que actúa como el punto de entrada principal, coordinando la ejecución de las tareas de monitoreo.

How does your implementation work?

La implementación sigue un enfoque modular y jerárquico, estructurado en tres niveles principales:

- GatewayDeviceApp (Nivel superior):
    - Es el punto de entrada del sistema.
    - Se encarga de iniciar y detener el gestor de rendimiento (SystemPerformanceManager).
    - Registra eventos en logs, incluyendo errores y resultados.

- SystemPerformanceManager (Núcleo del sistema):
    - Es el encargado de la gestión de telemetría.
    - Inicia y detiene las tareas de monitoreo de CPU y memoria secundaria.
    - Registra las mediciones en logs.
    - Ejecuta las tareas de monitoreo en hilos separados mediante un ScheduledExecutorService, que permite programar tareas en intervalos fijos.
    - Cada intervalo ejecuta el método handleTelemetry(), que invoca las clases de medición.

- BaseSystemUtilTask y sus subclases (SystemCpuUtilTask y SystemMemUtilTask):
    - BaseSystemUtilTask es la clase base que proporciona la funcionalidad común a todas las tareas de monitoreo.
    - SystemCpuUtilTask obtiene métricas de uso de CPU.
    - SystemMemUtilTask obtiene métricas de uso de memoria secundaria.
    - Ambas implementan métodos para recuperar los datos del sistema y devolverlos a SystemPerformanceManager.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/carlossaz9/PIC-java-components/tree/P2


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest 

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- GatewayDeviceAppTest
- SystemPerformanceManagerTest 

EOF.
