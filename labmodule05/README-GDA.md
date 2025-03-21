# Gateway Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación en el GDA gestiona los datos de los sensores y actuadores del CDA, procesando la información recibida y reenviándola a plataformas en la nube o sistemas de análisis. Además, maneja los comandos enviados desde sistemas externos hacia el CDA para ejecutar acciones en los actuadores. El componente principal, DeviceDataManager, gestiona las conexiones y el procesamiento de los datos, utilizando protocolos como MQTT y CoAP para una comunicación eficiente. También supervisa el rendimiento del sistema, incluyendo el uso de CPU y memoria, para asegurar una operación estable.

La implementación se centra en la generación y estructuración de datos en el gateway device, gestionando la telemetría de memoria, uso de disco y procesador del sistema. Esto sienta las bases para la gestión y transformación de los datos de los dispositivos conectados, preparándose para su envío y procesamiento adecuado.

How does your implementation work?

Mi implementación funciona mediante una arquitectura modular que gestiona los datos y las conexiones entre el GDA y el CDA. Al iniciarse el GDA, **DeviceDataManager** configura las conexiones necesarias utilizando protocolos como MQTT o CoAP. Luego, procesa los datos recibidos de los sensores y actuadores, y los reenvía a servicios en la nube o los almacena según sea necesario. Además, traduce los comandos recibidos en un formato comprensible y los envía al CDA para ejecutar las acciones en los actuadores.

DeviceDataManager también supervisa el rendimiento del sistema a través de SystemPerformanceManager, asegurando su funcionamiento óptimo. Se ha actualizado SystemPerformanceManager para manejar los datos de rendimiento del sistema, como CPU y memoria, generando la telemetría y enviándola a la nube. Además, se han desarrollado los módulos SensorData, ActuatorData, SystemPerformanceData y SystemStateData como contenedores de información, todos derivados de BaseIoTData.

En DataUtil, se han implementado métodos para convertir los datos de los módulos mencionados a JSON y viceversa. Los métodos de DeviceDataManager manejan la inicialización y detención de SystemPerformanceManager, y gestionan la comunicación y el procesamiento de datos mediante métodos específicos de la interfaz IDataMessageListener.

Finalmente, en GatewayDeviceApp se utiliza un wrapper que ejecuta la aplicación en bucle, con instancias de DeviceDataManager que se inician y detienen según corresponda, proporcionando una implementación básica pero funcional del sistema.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/carlossaz9/PIC-java-components.git


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

EOF.
