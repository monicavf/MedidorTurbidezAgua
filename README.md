# MEDIDOR DE TURBIDEZ DA ÁGUA

Este projeto utiliza um ESP32, um sensor de turbidez, um display OLED, um LED RGB e comunicação MQTT par monitorar a qualidade da água em tempo real. Os dados serão enviados para um broker MQTT (HiveMQ), exibidos em um display OLED e indicados visualmente com um LED RGB.

## MATERIAIS
- ESP32
- Protoboard 830 pinos
- Protoboard 400 pinos
- Sensor de turbidez da água
- Display OLED
- LED RGB
- 3 Resistores de 220 ohms
- 13 Jumpers

## PLATAFORMA DE DESENVOLVIMENTO
 - Arduino IDE

## CONEXÕES
| Componente        | Pino ESP32  |
|-------------------|-------------|
| Sensor de turbidez| GPIO 36     |
| OLED SDA          | GPIO 21     |
| OLED SCL          | GPIO 22     |
| LED Vermelho      | GPIO 25     |
| LED Verde         | GPIO 26     |
| LED Azul          | GPIO 27     |
 
## Montagem do protótipo
  ![image](https://github.com/user-attachments/assets/17005d3a-de07-41d3-a2f6-ac6f3cafcc24)

## MQTT 
- Broker -> broker.hivemq.com
- Porta -> 1883
- Tópicos publicados:
   sensor/turbidez -> valor da turbidez
   sensor/estado -> estado da água (Limpa, Moderada ou Suja)
   sensor/led -> cor do LED correspondente

## CLASSIFICAÇÃO DA TURBIDEZ
| Leitura Analógica | Estado da Água | Cor do LED |
|-------------------|----------------|------------|
| > 1500            | LIMPA          | Verde      |
| 1300–1500         | MODERADA       | Amarelo    |
| < 1300            | SUJA           | Vermelho   |




