# Arquitetura — Data Desk

## Visão geral

O Data Desk utiliza uma arquitetura conversacional baseada em skill de IA, com integração a ferramentas externas por meio do conector Atlassian.

A solução separa três responsabilidades:

1. Interpretação da solicitação.
2. Aplicação das regras de negócio.
3. Execução da operação no sistema externo.

## Camada de interpretação

Responsável por compreender a intenção do usuário e extrair informações relevantes da conversa.

Exemplos:
- Criar uma demanda.
- Consultar uma solicitação.
- Atualizar uma prioridade.
- Adicionar contexto.
- Movimentar uma demanda no workflow.

## Camada de inteligência

Responsável por aplicar as regras de negócio e estruturar os dados.

Exemplos:
- Identificação da frente responsável.
- Classificação do tipo de trabalho.
- Inferência de prioridade.
- Conversão de datas relativas.
- Padronização das descrições.
- Identificação de informações obrigatórias ausentes.

## Camada de execução

Responsável por orquestrar as ferramentas disponibilizadas pelo conector Atlassian.

As operações podem envolver:
- Criação de demandas.
- Consulta de registros.
- Atualização de informações.
- Inclusão de comentários.
- Alteração de prioridades.
- Movimentação de status.

## Camada de controle

Antes de executar uma operação de criação ou alteração, a solução apresenta um resumo da ação planejada e solicita confirmação explícita do usuário.

Após a confirmação, a ferramenta correspondente é acionada.

## Fluxo simplificado

Stakeholder → Interpretação → Regras de negócio → Resumo da operação → Confirmação → Conector Atlassian → Jira → Retorno ao usuário.

## Considerações

Este documento representa uma visão conceitual e simplificada da arquitetura. Não representa a configuração proprietária do ambiente corporativo.
