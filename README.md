# Atividades de Linguagem Ladder

Repositório com atividades práticas de Linguagem Ladder desenvolvidas no software PC03 (Ver. 3.28). Os programas abordam situações reais da automação industrial, desde o acionamento simples de motores até o controle de sistemas de transporte com intertravamento de segurança.

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
| `Contadores.cli` | Contagem de peças com CTU, reset e controle de saída por LED |

---

## 🔍 Detalhamento das Atividades

### MotorTrifasico

Programa de partida e parada de um motor trifásico por meio de botões de pulso. Implementa o circuito clássico de comando com botão de liga (NA), botão de desliga (NF) e contato auxiliar de selo, garantindo que o motor permaneça acionado após soltar o botão liga.

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

### Contadores

Programa desenvolvido no software PC03 que implementa a lógica de contagem de peças em uma esteira transportadora utilizando o contador crescente (CTU). A lógica é composta por três rungs principais:

- **Rung 002:** Circuito de acionamento da esteira (`MT ESTEI`) com botão de partida `S1` (I01), contato auxiliar de selo `Q01`, contato NF do contador `CONTADOR` (C01) e contato NA da mesma saída `Q01`. Enquanto o contador não atingir o valor predefinido, o contato NF (C01) permanece fechado, permitindo o acionamento da esteira.
- **Rung 005:** Sensor de presença `SENSOR` (I03) que alimenta a bobina do contador `CONTADOR` (C01). A cada peça detectada pelo sensor, o contador é incrementado em uma unidade.
- **Rung 007:** Quando o contador `CONTADOR` (C01) atinge o valor acumulado (preset), seu contato NA fecha, acionando a saída `LED – 1` (Q02), que sinaliza visualmente que a quantidade programada de peças foi atingida e a esteira é interrompida.

**Funcionamento geral:** A esteira permanece em operação enquanto o contador não alcança o valor preset. Ao atingir a contagem definida, o contato NF de C01 no rung de acionamento abre, desligando a esteira, e simultaneamente o contato NA de C01 no rung do LED fecha, acendendo o indicador luminoso. Para reiniciar o ciclo, é necessário efetuar o reset do contador.

**Conceitos:** contador crescente (CTU), preset, contato auxiliar NF de contador, sinalização por LED, reset de contador, lógica de parada automática por contagem.

---

## 🛠️ Como abrir os arquivos

Os arquivos `.cli` são projetos do software PC03 Ver. 3.28. Para abrir e simular:

1. Instale o PC03 (disponibilizado pelo professor ou instituição)
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
- Sinalização por saída digital (LED)
- Lógica de parada automática por contagem

---

*Linguagem Ladder — Automação Industrial*
