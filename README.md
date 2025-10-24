# 🚗 Projeto de Sistemas Embarcados — Carrinho Controlado por Bluetooth

## 🧠 Visão Geral

Este projeto foi desenvolvido na disciplina de **Sistemas Embarcados** da **Universidade Tecnológica Federal do Paraná (UTFPR)**.  
O objetivo foi criar um sistema embarcado funcional que integrasse **hardware, software e controle em tempo real**, aplicando conceitos de **interrupções, multitarefas e comunicação sem fio via Bluetooth**.

O resultado foi um **carrinho controlado por celular**, capaz de se mover, desviar de obstáculos e emitir alertas sonoros — tudo coordenado pelo microcontrolador **ESP-32**.

---

## 🎯 Objetivos do Projeto

- Projetar e montar um sistema embarcado funcional.  
- Desenvolver uma **PCB (Placa de Circuito Impresso)** para os componentes.  
- Integrar **dois ou mais periféricos** ao sistema.  
- Implementar **interação homem-máquina** via Bluetooth.  
- Utilizar **tarefas e semáforos com FreeRTOS**.  
- Incorporar uma **interrupção** para controle de eventos em tempo real.

---

## ⚙️ Componentes Utilizados

| Componente | Função |
|-------------|--------|
| **ESP-32** | Microcontrolador principal com Bluetooth integrado |
| **Ponte H Dupla L298N** | Controle do sentido de rotação dos motores |
| **Motor DC** | Movimento do carrinho |
| **Servo motor** | Controle da direção |
| **Sensor ultrassônico (sonar)** | Medição de distância para evitar colisões |
| **Buzzer ativo** | Sinalização sonora de alerta |
| **Resistores e capacitores** | Estabilização e redução de ruídos |
| **Placa universal (7x5)** | Montagem dos componentes eletrônicos |
| **Aplicativo “Arduino Bluetooth Control”** | Controle remoto via smartphone (Android) |

---

## 🧩 Estrutura do Projeto

### 🛠️ Montagem Física
- A estrutura do carrinho foi montada manualmente, com o motor DC acoplado na parte traseira e o **servo motor** responsável pela direção na parte frontal.  
- O circuito foi montado em uma **placa universal**, fixando o ESP-32, o buzzer, resistores, capacitores e fios de interligação.  
- Todos os componentes foram fixados com cola ou fita isolante para estabilidade.

### 💻 Montagem do Código
- O software foi desenvolvido em **C/C++** na IDE do **Arduino**.  
- Foram importadas as bibliotecas:
  ```cpp
  #include "BluetoothSerial.h"
  #include "ESP32Servo.h"
