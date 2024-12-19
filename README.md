# DHT22


# Practica ESP32 con DHT22
Este repositorio muestra como podemos programar una ESP32 con el sensor DHT22 para que nos muestre la información recibida por el sensor DHT22.

## Introducción

### Descripción

La ```ESP32``` la utilizamos en un entorno de adquisición de datos, en esta práctica ocuparemos un sensor (```DTH22```) para adquirir los datos de temperatura y humedad del entorno.  Cabe aclarar que esta practica se usara un simulador llamado [WOKWI](https://https://wokwi.com/).


## Material Necesario

Para realizar esta practica necesitas lo siguiente

- [WOKWI](https://https://wokwi.com/)
- Tarjeta ESP 32
- Sensor DHT22



## Instrucciones

### Requisitos previos

Para poder usar este repositorio necesitas entrar a la plataforma [WOKWI](https://https://wokwi.com/).


### Instrucciones de preparación de entorno 

1. Abrir la terminal de programación y colocar la siguente programación:

```
#include "DHTesp.h"

const int DHT_PIN = 15;
DHTesp dhtSensor;

void setup() {

  Serial.begin(115200);
  dhtSensor.setup(DHT_PIN, DHTesp::DHT22);
}

void loop() {

  TempAndHumidity  data = dhtSensor.getTempAndHumidity();
  Serial.println("Temp: " + String(data.temperature, 1) + "°C");
  Serial.println("Humidity: " + String(data.humidity, 1) + "%");
  Serial.println("---");
  delay(1000);
}

```
2. Instalar la librería:
-  **DHT sensor library for ESPx**

![](https://github.com/Ricardoramosdelapaz/DHT22/blob/main/lib.PNG?raw=true).

3. Hacer la conexion de **DHT2** con la **ESP32** como se muestra en la siguiente imagen.

![](https://github.com/Ricardoramosdelapaz/DHT22/blob/main/cone.PNG?raw=true

### Instrucciónes de operación

1. Iniciar simulador.
2. Visualizar los datos en el monitor serial.
3. Colocar la temperatura y humedad dando *doble click* al sensor **DHT22** 

## Resultados

Al iniciar la simulacion, verás los valores dentro del monitor serial como se muestra en la siguente imagen.

![](https://github.com/Ricardoramosdelapaz/DHT22/blob/main/result.PNG?raw=true).



# Créditos

Desarrollado por Ing. Ricardo Ramos De la paz

- [GitHub](https://github.com/Ricardoramosdelapaz)
