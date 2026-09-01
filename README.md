# Sistema de Gestión y Control para Espacios de Estacionamiento

## Integrantes

1. Jonathan Madriz Sánchez
2. Luis Enrique Carmona Villafaña
3. Evelin Cruz López
4. Enrique Cruz Jiménez
5. Josué Sebastián Navarrete Garcia

## Descripción del proyecto

SmartPark es un sistema de estacionamiento inteligente que utiliza tecnologías IoT, sensores y microcontroladores ESP32 para identificar los espacios disponibles u ocupados por vehículos.

El sistema proporciona información actualizada sobre la disponibilidad del estacionamiento mediante una interfaz web.

## Propósito

El propósito principal del proyecto es administrar los espacios disponibles dentro de un estacionamiento mediante un sistema automatizado.

Muchos conductores recorren diferentes áreas para encontrar un espacio disponible. Esto puede provocar pérdida de tiempo, congestión y un uso poco eficiente de los espacios.

SmartPark busca solucionar este problema mediante la detección automática de vehículos y el procesamiento de la información obtenida por sensores.

## Problemas que resuelve

- Dificultad para localizar espacios disponibles.
- Tiempo perdido buscando un lugar de estacionamiento.
- Falta de información en tiempo real sobre los espacios disponibles.
- Administración manual de los espacios.
- Uso poco eficiente de las áreas disponibles.

## Funcionamiento

En el prototipo, el sensor HC-SR04 detecta la presencia de un vehículo en cada espacio de estacionamiento.

1. El sensor realiza una medición de distancia.
2. El ESP32 interpreta la medición y clasifica el espacio como **LIBRE** u **OCUPADO**.
3. El ESP32 transmite el estado mediante Wi-Fi y MQTT.
4. El broker Mosquitto distribuye el mensaje al backend.
5. Spring Boot procesa la información.
6. PostgreSQL almacena los datos.
7. El dashboard muestra la disponibilidad actualizada.

## Flujo general del sistema

Vehículo → HC-SR04 → ESP32 → Wi-Fi → MQTT/Mosquitto → Spring Boot → PostgreSQL → Dashboard

## Tecnologías utilizadas

### Hardware

- ESP32
- Sensor HC-SR04
- LEDs
- Resistencias
- Protoboard
- Cables Dupont
- Fuente de alimentación

### Software y comunicación

- Arduino IDE
- Mosquitto
- Spring Boot
- PostgreSQL
- Frontend web
- Wi-Fi
- MQTT
- HTTP/REST

## Documentación

La documentación detallada de los componentes y de la comunicación del sistema se encuentra en la [Wiki del proyecto](../../wiki).
