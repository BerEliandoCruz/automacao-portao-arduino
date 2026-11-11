

# ⚙️ Automação de Portão com Arduino

<p align="center">
  <img src="https://img.shields.io/badge/Arduino-161B22?style=for-the-badge&logo=arduino&logoColor=00979D" />
  <img src="https://img.shields.io/badge/C%2B%2B-161B22?style=for-the-badge&logo=cplusplus&logoColor=00599C" />
  <img src="https://img.shields.io/badge/Embedded_Systems-161B22?style=for-the-badge&logoColor=58A6FF" />
</p>

## 📌 Sobre o projeto

Este projeto consiste no desenvolvimento de um sistema de controle de dois portões utilizando Arduino.

O sistema permite controlar individualmente a abertura e o fechamento dos portões por meio de botões. Também utiliza LEDs para indicar o estado de cada portão e um buzzer para emitir sinais sonoros durante as operações.

O projeto foi desenvolvido como atividade prática de Desenvolvimento de Sistemas, aplicando conceitos de programação, eletrônica e automação.

## 🚀 Funcionalidades

- Controle independente de dois portões.
- Abertura e fechamento por meio de botões.
- Acionamento de motores em diferentes sentidos.
- Indicação visual do estado dos portões utilizando LEDs.
- Sinalização sonora durante a movimentação.
- Controle do estado de abertura e fechamento por programação.

## 🔌 Componentes utilizados

- Arduino.
- 2 motores.
- Driver de motores ou ponte H compatível.
- 2 botões.
- 2 LEDs verdes.
- 2 LEDs vermelhos.
- Resistores para os LEDs e botões.
- 1 buzzer.
- Jumpers e protoboard.

## 📍 Mapeamento dos pinos

| Componente | Pino Arduino |
|---|---:|
| Motor interno positivo | 12 |
| Motor interno negativo | 13 |
| Motor externo positivo | 10 |
| Motor externo negativo | 11 |
| Botão interno | 8 |
| Botão externo | 7 |
| LED verde interno | 5 |
| LED vermelho interno | 4 |
| LED verde externo | 3 |
| LED vermelho externo | 2 |
| Buzzer | 6 |

## 💡 Funcionamento

O sistema utiliza dois estados para controlar cada portão:

- **Fechado (0):** LED vermelho aceso.
- **Aberto (1):** LED verde aceso.

Ao pressionar um botão, o programa verifica o estado atual do portão e executa a operação correspondente.

Durante a movimentação, o LED vermelho permanece aceso e o buzzer emite um sinal sonoro.

Após a abertura, o sistema aguarda um pequeno intervalo, acende o LED verde e emite um sinal de confirmação.

O fechamento também possui sinalização sonora e visual.

## 🛠️ Tecnologias e conceitos aplicados

- Programação para Arduino.
- Linguagem C++ utilizada no ambiente Arduino.
- Controle de entradas e saídas digitais.
- Estruturas condicionais (`if` e `else`).
- Funções para organização do código.
- Controle de motores.
- Sinalização com LEDs e buzzer.

## ▶️ Como executar

1. Instale a [Arduino IDE](https://www.arduino.cc/en/software).
2. Clone este repositório:

```bash
git clone https://github.com/SEU-USUARIO/automacao-portao-arduino.git
```

3. Abra a pasta do projeto.
4. Abra o arquivo `codigo/portao.ino`.
5. Conecte o Arduino ao computador.
6. Selecione a placa e a porta correta na Arduino IDE.
7. Carregue o código para a placa.

## ⚠️ Observações técnicas

- O tempo de movimentação dos motores está configurado em 3 segundos.
- O código atual utiliza temporização, sem sensores de fim de curso.
- Os botões estão configurados como entradas `INPUT`, exigindo resistores externos de pull-down para manter os sinais estáveis.
- Os motores devem ser conectados por meio de um driver apropriado, nunca diretamente aos pinos do Arduino.

Para utilização em um portão real, são necessários dispositivos adicionais de segurança, como sensores de fim de curso, detecção de obstáculos e parada de emergência.

## 🎯 Objetivo do projeto

Aplicar conhecimentos de programação e eletrônica na construção de um sistema de automação, desenvolvendo habilidades com Arduino, controle de motores, sensores e componentes eletrônicos.

---

⭐ Obrigado por conferir o projeto!

