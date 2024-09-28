Video: https://youtu.be/-2Mqif16hiE



# Sistema de Telemetria IoT para Carros de Fórmula-E

## Visão Geral do Projeto

Este projeto visa desenvolver um sistema de telemetria em tempo real utilizando tecnologias de IoT para carros de Fórmula-E. A solução proposta envolve a instalação de sensores nos carros para monitorar dados críticos como **velocidade**, **nível da bateria** e **temperatura dos motores elétricos**. Esses dados são transmitidos para um servidor central, processados e disponibilizados para visualização em tempo real por meio de uma interface web. O sistema fornece tanto uma experiência aprimorada para os espectadores quanto dados valiosos para as equipes de corrida.

## Arquitetura Proposta

### 1. **Dispositivos IoT**
   - **Sensores de Velocidade**: Capturam a velocidade do carro em tempo real e enviam os dados via um protocolo de comunicação sem fio (ex.: Wi-Fi, LoRa, ou Zigbee).
   - **Sensores de Nível de Bateria**: Monitoram a quantidade de energia restante na bateria do carro e enviam as leituras para o servidor.
   - **Sensores de Temperatura**: Verificam a temperatura dos motores elétricos para evitar superaquecimento e falhas durante a corrida.

### 2. **Servidor Back-end**
   - **Servidor Central (Edge Computing)**: Responsável por processar os dados recebidos dos sensores, realizar análises e calcular métricas adicionais, caso necessário.
   - **API Restful**: Expondo os dados de telemetria processados para a interface de usuário (UI) e para outros serviços de análise de dados.
   - **Banco de Dados**: Um banco de dados para armazenar dados históricos, permitindo análise pós-corrida e otimização de desempenho futuro.

### 3. **Front-end (Interface de Usuário)**
   - **Interface Web Responsiva**: Desenvolvida utilizando React.js para exibir os dados de telemetria em tempo real. Essa interface inclui gráficos dinâmicos, tabelas e dashboards que exibem a velocidade, a carga da bateria e a temperatura do motor.
   - **Atualização Automática**: A interface é projetada para atualizar os dados automaticamente conforme eles são processados pelo servidor, proporcionando uma experiência em tempo real para os espectadores e as equipes.

### 4. **Comunicação**
   - **Protocolo de Comunicação**: A comunicação entre os sensores e o servidor pode ser realizada via Wi-Fi, LoRa ou Zigbee, dependendo da infraestrutura e do alcance de transmissão necessário.
   - **MQTT**: Utilizado para uma comunicação eficiente e leve entre os sensores e o servidor central, ideal para envio de dados em tempo real com baixa latência.

## Recursos Necessários para Implementação

### **Dispositivos IoT**
   - **Sensores de Velocidade**: Medidores de velocidade instalados diretamente nos carros.
   - **Sensores de Nível de Bateria**: Dispositivos capazes de monitorar e transmitir a carga restante da bateria.
   - **Sensores de Temperatura**: Equipamentos instalados nos motores elétricos para monitorar a temperatura.
   - **Módulo de Comunicação**: Modem Wi-Fi ou LoRa para transmissão dos dados dos sensores para o servidor.

### **Back-end**
   - **Servidor de Aplicação**: Responsável por gerenciar a coleta e processamento dos dados dos sensores em tempo real.
   - **Banco de Dados**: Banco de dados NoSQL (ex: MongoDB) ou relacional (ex: MySQL) para armazenar os dados de telemetria e fornecer acesso aos dados históricos.
   - **API Restful**: Interface para fornecer os dados em tempo real à interface de usuário.

### **Front-end**
   - **React.js**: Para o desenvolvimento da interface de usuário, permitindo uma visualização fluida e responsiva dos dados de telemetria.
   - **Bibliotecas de Gráficos**: Bibliotecas como Chart.js ou D3.js para exibir gráficos dinâmicos que ilustram as métricas de velocidade, bateria e temperatura.

## Dependências do Projeto

- **Node.js**
- **Express.js**
- **MongoDB ou MySQL**
- **React.js**
- **Chart.js ou D3.js**
- **MQTT.js**: Para comunicação eficiente via protocolo MQTT.
- **Axios**: Para fazer requisições HTTP entre o front-end e o back-end.

## Exemplos de Uso

- **Visualização de Desempenho**: Durante uma corrida, os espectadores podem acompanhar em tempo real a velocidade de cada carro, o estado da bateria e a temperatura dos motores, proporcionando uma experiência interativa.
- **Análise Pós-corrida**: Equipes técnicas podem acessar os dados armazenados no banco de dados para avaliar o desempenho dos veículos e identificar áreas para melhorias.

## Desenvolvimento Futuro

- **Integração com Mais Sensores**: Possibilidade de monitorar outras variáveis, como pressão dos pneus, energia consumida e GPS.
- **Ferramentas de Análise Avançada**: Implementação de algoritmos de machine learning para prever o desempenho com base nos dados de telemetria.
- **API Pública**: Oferecer uma API pública para que outros desenvolvedores possam criar aplicativos baseados nos dados da telemetria.

---

## Códigos Fonte

Os códigos necessários para a implementação do servidor back-end, a interface front-end, e a comunicação com os sensores IoT estão incluídos neste repositório. Siga as instruções de instalação e configuração para replicar o sistema.

