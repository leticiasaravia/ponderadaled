# Projeto Arduino
### Por Letícia Saravia
Esse projeto contem o Blink Led Interno, a simulação com o TinkerCad do Blink Externo e o Blink Externo.

## Índice

- [Parte 1 - LED Interno](#parte-1---led-interno)
- [Parte 2 - LED Externo](#parte-2---led-externo)

## Parte 1 - LED Interno

## Objetivo

O objetivo desta atividade é realizar o primeiro experimento prático com o Arduino, utilizando o LED interno da placa para criar o efeito de piscar (“blink”).  

## Materiais e Ferramentas

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

 
