# Decisões técnicas — Data Desk

## 1. Interface conversacional

A linguagem natural foi escolhida para reduzir a complexidade de utilização do Jira por usuários não técnicos.

## 2. Skill estruturada

A evolução de agente para skill permitiu consolidar instruções, regras de negócio, classificações e fluxos de execução em uma estrutura organizada.

## 3. Integração via conector Atlassian

A utilização do conector permitiu disponibilizar operações do Jira sem precisar desenvolver uma integração própria para cada ação.

## 4. Classificação automatizada

As regras de negócio foram estruturadas para interpretar o contexto da solicitação e identificar atributos como frente, tipo de trabalho e prioridade.

## 5. Human-in-the-loop

A confirmação explícita antes de operações de criação e alteração foi adotada para permitir a validação das informações pelo solicitante.

## 6. Padronização e rastreabilidade

As informações são estruturadas em um formato padronizado e o usuário recebe o link direto para acompanhar a demanda.

## Consideração

As decisões descritas representam os princípios de implementação da solução, sem expor configurações internas ou identificadores do ambiente original.
