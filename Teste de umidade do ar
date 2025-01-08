#include <dht.h>

#define pinoDHT11 7

dht sensorDHT11;

void setup () {
  Serial.begin(9600);
  delay(2000);
}

void loop () {
  sensorDHT11.read11(pinoDHT11);
  Serial.print("UMIDADE: ");
  Serial.println(sensorDHT11.humidity);
  Serial.print("TEMPERATURA: ");
  Serial.print(sensorDHT11.temperature);
  delay(200); 
}
