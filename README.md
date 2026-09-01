# **Sistema de Gestión y Control para Espacios de Estacionamiento**

## **Integrantes**

1. Jonathan Madriz Sánchez
2. Luis Enrique Carmona Villafaña
3. Evelin Cruz López
4. Enrique Cruz Jiménez
5. Josué Sebastián Navarrete Garcia

## **Descripción del proyecto**

El **Sistema de Gestión y Control para Espacios de Estacionamiento** utiliza tecnologías de IoT, sensores y/o visión artificial.

El cual permite identificar los espacios que se encuentran disponibles u ocupados por vehículos, lo cual proporciona información actualizada sobre la disponibilidad del estacionamiento.

## **Propósito**

El propósito principal del proyecto es proporcionar una administración de espacios disponibles que se encuentran dentro de un estacionamiento mediante un sistema automatizado.

En la actualidad, muchos conductores recorren diferentes áreas para encontrar un espacio disponible. Lo cual puede provocar una pérdida de tiempo, congestión y uso poco eficiente de los espacios.

Este proyecto permite solucionar este problema mediante la detección automática de vehículos y el procesamiento de la información obtenida por sensores y/o cámaras.

## **Problemas que resuelve**

1. Dificultad para localizar espacios disponibles.
2. Tiempo perdido buscando un lugar de estacionamiento.
3. Falta de información en tiempo real sobre los espacios disponibles.
4. Administración manual de los espacios.
5. Uso poco eficiente de las áreas disponibles.

## **Funcionamiento**

Dependiendo de la implementación final, la detección podrá realizarse mediante:

1. Sensores de distancia o presencia.
2. Cámara.
3. Visión artificial.
4. Procesamiento de imágenes.

Cuando el vehículo ha sido detectado dentro del espacio, el sistema lo mostrará como **OCUPADO**, pero si no se encuentra ningún vehículo, el espacio será marcado como **LIBRE**.

## **Flujo general del sistema**

El sistema funciona mediante el siguiente flujo:

~~~mermaid
flowchart TD
A[Vehículo] --> B[Sensor / Cámara]
B --> C[Detección de vehículo]
C --> D[ESP32 / Sistema de procesamiento]
D --> E[Clasificación del espacio]
E --> F{Estado del espacio}
F --> G[LIBRE]
F --> H[OCUPADO]
G --> I[Visualización de disponibilidad]
H --> I[Visualización de disponibilidad]
~~~

## **Objetivo general**
Diseñar un sistema IoT que sea capaz de detectar y administrar de forma autónoma la disponibilidad de los espacios de un estacionamiento, proporcionando información en tiempo real sobre los lugares disponibles y ocupados.

## **Objetivos especificos**

1. Detectar vehículos en los espacios de estacionamiento.
2. Identificar si existe un espacio disponible u ocupado.
3. Procesar la información mediante un sistema de control.
4. Mostrar disponibilidad de los espacios.
5. Reducir el tiempo para hallar un lugar disponible.
6. Implementar nuevas tecnologías relacionadas con IoT y automatización.


## **Componentes principales**

### Hardware

- **ESP32**
- **HC-SR04**
- **LEDs**
- **Resistencias**
- **Protoboard**
- **Cables Dupont**
- **Fuente de alimentación**

### Software

- **Arduino IDE**
- **Mosquitto**
- **Spring Boot**
- **PostgreSQL**
- **Frontend web**

### Tecnologías de comunicación

- **Wi-Fi**
- **MQTT**
- **HTTP/REST**

## **Resultado esperado**

Se espera en el prototipo logre mostrar en tiempo real estado de los espacios del estacionamiento.

```text
ESTACIONAMIENTO

Espacio 1 → LIBRE
Espacio 2 → OCUPADO
Espacio 3 → LIBRE
Espacio 4 → OCUPADO
Espacio 5 → LIBRE
```

1. Espacios disponibles: 3
2. Espacios ocupados: 2
