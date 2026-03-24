# Atividades de Linguagem Ladder
 
Repositório com atividades práticas de **Linguagem Ladder** desenvolvidas no software **PC03 (Ver. 3.28)**. Os programas abordam situações reais da automação industrial, desde o acionamento simples de motores até o controle de sistemas de transporte com intertravamento de segurança.
 
---
 
## 📁 Atividades
 
| Arquivo | Descrição resumida |
|---|---|
| `MotorTrifasico.cli` | Acionamento básico de motor trifásico |
| `Intertravamento.cli` | Intertravamento simples entre dois acionamentos |
| `DoisMotoresIntertravados.cli` | Dois motores com intertravamento entre si |
| `VentiladorIndustrial.cli` | Controle de ventilador industrial |
| `EsteiraTransportadora.cli` | Acionamento de esteira transportadora |
| `PeçasEsteira.cli` | Controle de esteira com contagem/passagem de peças |
 
---
 
## 🔍 Detalhamento das Atividades
 
---
 
### MotorTrifasico
 
Programa de partida e parada de um motor trifásico por meio de botões de pulso. Implementa o circuito clássico de comando com botão de **liga (NA)**, botão de **desliga (NF)** e **contato auxiliar de selo**, garantindo que o motor permaneça acionado após soltar o botão liga.
 
**Conceitos:** contato NA, contato NF, bobina de saída, circuito autossustentado.
 
---
 
### Intertravamento
 
Implementa a lógica de intertravamento entre dois acionamentos, impedindo que ambos sejam habilitados simultaneamente. O contato auxiliar NF de cada saída bloqueia o acionamento da outra, garantindo segurança operacional.
 
**Conceitos:** intertravamento elétrico, contato auxiliar NF, segurança em comandos.
 
---
 
### DoisMotoresIntertravados
 
Evolução da atividade de intertravamento, aplicada a dois motores independentes com comandos de liga e desliga individuais. Nenhum dos motores pode ser ligado enquanto o outro estiver em operação.
 
**Conceitos:** intertravamento entre múltiplos atuadores, selos independentes, lógica combinacional com bobinas auxiliares.
 
---
 
### VentiladorIndustrial
 
Controle de um ventilador industrial com partida, parada e proteção contra acionamentos simultâneos indevidos. Pode incluir temporizador para desligamento automático após determinado período de operação.
 
**Conceitos:** comando de ventilador, partida temporizada, autossustentação.
 
---
 
### EsteiraTransportadora
 
Acionamento de uma esteira transportadora com lógica de partida, parada e condições de intertravamento com outros equipamentos da linha. Simula um trecho de linha de produção onde a esteira só pode operar sob condições específicas.
 
**Conceitos:** acionamento condicional, intertravamento de linha, comando de esteira.
 
---
 
### PeçasEsteira
 
Controle de esteira com detecção e contagem de peças por meio de sensores. A esteira pode ser interrompida ao atingir uma quantidade predefinida de peças ou mediante outros critérios lógicos definidos pelos sensores.
 
**Conceitos:** sensor de presença, contador (CTU), lógica de parada por contagem, reset de contador.
 
---
 
## 🛠️ Como abrir os arquivos
 
Os arquivos `.cli` são projetos do software **PC03 Ver. 3.28**. Para abrir e simular:
 
1. Instale o **PC03** (disponibilizado pelo professor ou instituição)
2. Abra o software e acesse **Arquivo > Abrir**
3. Selecione o arquivo `.cli` desejado
4. Utilize o modo de simulação para testar a lógica Ladder
 
---
 
## 📖 Conceitos Abordados
 
- Contatos normalmente abertos (NA) e normalmente fechados (NF)
- Bobinas de saída e bobinas auxiliares
- Circuito autossustentado (botão selo)
- Intertravamento elétrico entre acionamentos
- Temporizadores de retardo (TON/TOF)
- Contadores crescentes (CTU) com reset
 
---
 
*Linguagem Ladder — Automação Industrial*
