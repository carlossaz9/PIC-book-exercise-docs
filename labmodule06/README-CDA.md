# Constrained Device Application (Connected Devices)

## Lab Module 06

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
La implementación añade soporte para MQTT, lo que permite que los dispositivos IoT se comuniquen entre sí mediante la publicación y suscripción a tópicos. Esto facilita el intercambio de datos en tiempo real entre los diferentes componentes del sistema.

How does your implementation work?
Mi implementación funciona configurando un cliente MQTT que se conecta automáticamente a un broker. Este cliente permite publicar mensajes en tópicos específicos y suscribirse a ellos, lo que facilita el envío y la recepción de datos entre dispositivos. Además, se han implementado callbacks que procesan los mensajes entrantes y gestionan eventos como reconexiones o errores. Gracias a esto, los dispositivos pueden compartir información de forma eficiente en tiempo real. 
También se realizaron pruebas para asegurar la compatibilidad y correcto funcionamiento con el resto de los componentes del sistema.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/carlossaz9/PIC-python-components/tree/labmodule06


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- Todos los de la unidad 1 y 2 

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- Todos los de la unidad 1 y 2
- MqttClientConnectorTest
- MqttClientControlPacketTest

EOF.
