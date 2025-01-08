#include <SoftwareSerial.h>
#include "DHT.h" 

#define DHTPIN 2  
#define DHTTYPE DHT11  

DHT dht(DHTPIN, DHTTYPE);
SoftwareSerial BTSerial(10, 11); 

void setup() {
  Serial.begin(9600);  
  BTSerial.begin(9600); 
  dht.begin();  
  Serial.println("Sistema Iniciado...");
}

void loop() {
  float humidity = dht.readHumidity();  

  if (isnan(humidity)) {  
    Serial.println("Falha ao ler o sensor de umidade!");
    return;
  }

  if (humidity < 60) {  
    BTSerial.println("Alerta: Umidade abaixo de 30%");
    Serial.println("Alerta enviado via Bluetooth.");
  }

  delay(2000);  
}
