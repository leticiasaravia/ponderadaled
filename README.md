# Projeto Arduino
### Por Letícia Saravia
Esse projeto contem o Blink Led Interno, a simulação com o TinkerCad do Blink Externo e o Blink Externo.

## Índice

- [Parte 1 - LED Interno](#parte-1---led-interno)
- [Parte 2 - LED Externo](#parte-2---led-externo)

## Parte 1 - LED Interno

## Objetivo

O objetivo desta atividade é realizar o primeiro experimento prático com o Arduino, utilizando o LED interno da placa para criar o efeito de piscar (“blink”).  

## Materiais

- Computador com a Arduino IDE
- Placa Arduino UNO 
- Cabo USB
- LED interno da placa

## Passo a passo

1. **Instalação da IDE**  
   - Instalar a Arduino IDE.  

2. **Criação do Código**  
   - Abrir um novo sketch.  
   - Inserir o código que faz o LED interno acender e apagar nos intervalos definidos.

    
```cpp
/*
  Blink LED Interno
  Autora: Letícia Saravia
  Data: 17 de outubro de 2025
  Descrição: Faz o LED interno do Arduino piscar com tempos de acendimento (X) e apagamento (Y).
*/

int led = LED_BUILTIN;   
int tempoAceso = 500;     // aceso por 0,5 segundo
int tempoApagado = 500;    // apagado por 0,5 segundo

void setup() {
  pinMode(led, OUTPUT);  
}

void loop() {
  digitalWrite(led, HIGH); // Acende o LED
  delay(tempoAceso);       // Espera 500 milissegundos
  digitalWrite(led, LOW);  // Apaga o LED
  delay(tempoApagado);     // Espera 500 milissegundos
}

3. **Upload para o Arduino**  
   - Conectar placa ao computador via USB.  
   - Compilar e enviar o código para a placa.
```
### Evidências


## Parte 2 – Simulando Blink Externo (TinkerCad)
## Objetivo

Nesta segunda parte, o objetivo é simular no TinkerCad um circuito externo que reproduza o comportamento do “pisca-pisca” realizado anteriormente com o LED interno.
Agora, o controle será feito sobre um LED físico conectado em um protoboard, utilizando uma porta digital do Arduino UNO, resistores e ligações elétricas adequadas.

## Materiais

Plataforma TinkerCad (modo de simulação de circuitos)

Arduino UNO virtual

Protoboard

LED externo (OFF_BOARD)

Resistor de 220 Ω

Fios de conexão

## Esquema de Ligação

Anodo (perna maior) do LED → pino digital 13 do Arduino (via fio jumper).

Catodo (perna menor) do LED → resistor de 220 Ω → linha GND da protoboard.

Linha GND da protoboard conectada ao GND do Arduino.

/*
  Blink LED Externo
  Autora: Letícia Saravia
  Data: 17 de outubro de 2025
  Descrição: Pisca um LED externo conectado ao pino 13 do Arduino UNO.
  ```
*/

int led = 13;           // LED conectado ao pino digital 13
int tempoAceso = 500;   // LED aceso por 0,5 segundo
int tempoApagado = 500; // LED apagado por 0,5 segundo

void setup() {
  pinMode(led, OUTPUT); // Define o pino como saída
}

void loop() {
  digitalWrite(led, HIGH); // Acende o LED
  delay(tempoAceso);       // Espera 500 ms
  digitalWrite(led, LOW);  // Apaga o LED
  delay(tempoApagado);     // Espera 500 ms
}
```

# Evidências
