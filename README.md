# data-desk-ai-jira
AI-powered demand management solution integrated with Jira.
# Data Desk | AI-Powered Demand Management

**Agente de IA para gestão inteligente de demandas, integrado ao Jira, que transforma solicitações em linguagem natural em operações estruturadas e rastreáveis.**


## Sobre o projeto

O Data Desk é uma solução de inteligência artificial desenvolvida para simplificar a comunicação entre stakeholders e um time de dados, automatizando diferentes etapas do ciclo de vida das demandas.

A solução permite que usuários solicitem serviços, consultem demandas existentes, acompanhem solicitações e realizem atualizações no Jira por meio de conversas em linguagem natural, sem precisar conhecer a estrutura técnica da plataforma.

O projeto nasceu de uma necessidade operacional: organizar e centralizar o backlog de um time de dados que atendia quatro projetos distintos, cada um com um volume significativo de solicitações.

Para resolver esse problema, o Jira foi adotado como ferramenta de gestão. Entretanto, sua utilização direta exigia conhecimento sobre campos, classificações e processos internos, tornando a abertura de demandas pouco intuitiva para as áreas de negócio.

A partir desse cenário, desenvolvi o Data Desk para funcionar como uma camada inteligente de interação entre os usuários e o sistema de gestão.

## O problema de negócio

Antes da solução, o processo de abertura de demandas apresentava alguns desafios:

- Necessidade de conhecimento técnico para preencher corretamente os campos do Jira.
- Tempo elevado para registrar uma nova solicitação.
- Risco de demandas incompletas ou com informações pouco estruturadas.
- Dificuldade de utilização da ferramenta por stakeholders não familiarizados com o Jira.
- Necessidade de padronizar as informações para melhorar a organização e priorização do backlog.

O preenchimento manual de uma demanda levava aproximadamente 5 a 10 minutos.

## A solução

Desenvolvi o Data Desk, inicialmente como um agente conversacional de IA, posteriormente substituído por uma arquitetura baseada em skill.

A solução funciona como um analista virtual que interpreta solicitações em linguagem natural, conduz perguntas para complementar informações, aplica regras de negócio e executa operações no Jira por meio do conector Atlassian.

Em vez de preencher formulários técnicos, o stakeholder simplesmente descreve o que precisa.

O Data Desk interpreta a solicitação, identifica as informações necessárias e apresenta um resumo da operação planejada. A execução só acontece após a confirmação explícita do usuário.

Após a operação, o sistema retorna o resultado e o link direto para acompanhamento da demanda no Jira.

## Principais funcionalidades

### 1. Criação inteligente de demandas

- Recebe solicitações em linguagem natural.
- Conduz perguntas para identificar contexto, objetivo, prazo e formato esperado de entrega.
- Identifica automaticamente a frente responsável.
- Classifica o tipo de trabalho.
- Infere a prioridade com base no contexto e na urgência declarada.
- Estrutura as informações no padrão definido para o time de dados.
- Solicita confirmação antes de executar a criação.
- Retorna o identificador e o link da demanda criada.

### 2. Consulta e acompanhamento

- Consulta demandas por frente.
- Pesquisa solicitações por palavras-chave.
- Utiliza filtros e consultas JQL.
- Apresenta informações de status e prioridade.
- Traduz os status técnicos do Jira para uma linguagem compreensível pelos stakeholders.
- Retorna links diretos para acompanhamento.

### 3. Atualização e gestão de demandas

- Atualiza prioridades.
- Modifica campos permitidos.
- Atualiza responsáveis e datas.
- Adiciona comentários e informações complementares.
- Inclui links de referência.
- Realiza movimentações entre etapas do workflow.
- Solicita confirmação antes de executar operações de alteração.

### 4. Consultoria e validação

- Orienta sobre como estruturar uma solicitação.
- Identifica informações ausentes.
- Sugere melhorias na descrição das demandas.
- Ajuda a dividir solicitações complexas.
- Aplica regras de negócio para melhorar a qualidade dos registros.

## Arquitetura da solução

A arquitetura foi estruturada para separar a interpretação das solicitações da execução das operações no Jira.

O fluxo geral funciona da seguinte maneira:

1. **Entrada:** o stakeholder descreve sua necessidade em linguagem natural.
2. **Interpretação:** a skill identifica a intenção e extrai as informações relevantes.
3. **Orquestração:** as instruções e regras de negócio determinam quais ferramentas devem ser utilizadas.
4. **Validação:** a solução estrutura a operação e apresenta um resumo ao usuário.
5. **Confirmação:** o usuário autoriza explicitamente a execução.
6. **Integração:** o conector Atlassian executa a operação no Jira.
7. **Retorno:** o Data Desk apresenta o resultado e disponibiliza o link da demanda.

### Componentes tecnológicos

| Componente | Tecnologia / recurso |
|---|---|
| Plataforma de desenvolvimento | Toqan |
| Modelos de IA | Claude e Gemini |
| Sistema de gestão | Jira |
| Integração | Conector Atlassian |
| Interface | Conversacional |
| Linguagem de interação | Português brasileiro |
| Inteligência | Engenharia de prompts e regras de negócio |
| Execução | Orquestração de ferramentas |

## Evolução: de agente para skill

O Data Desk começou como um agente conversacional desenvolvido para automatizar a abertura de demandas no Jira.

Com a evolução do projeto, a solução foi substituída por uma arquitetura baseada em skill.

Essa mudança consolidou o conhecimento necessário para executar as operações em uma estrutura organizada, contendo:

- Instruções de comportamento.
- Regras de negócio.
- Mapeamentos de classificações e prioridades.
- Critérios de validação.
- Fluxos específicos por tipo de solicitação.
- Definição das ferramentas disponíveis.
- Tratamento de exceções e casos de borda.

A evolução ampliou a capacidade da solução, permitindo que ela deixasse de atuar apenas na criação de solicitações e passasse a apoiar diferentes operações de gestão do backlog.

## Controle e confiabilidade

Um dos princípios da solução é evitar alterações no Jira sem conhecimento e autorização do solicitante.

Para operações de criação ou atualização, o Data Desk apresenta previamente um resumo da ação planejada e solicita confirmação explícita.

Esse mecanismo de human-in-the-loop permite que o usuário valide as informações antes da execução.

Outros mecanismos utilizados:

- Validação de informações obrigatórias.
- Padronização das descrições.
- Mapeamento de classificações técnicas.
- Tradução de termos internos para linguagem de negócio.
- Tratamento de solicitações ambíguas.
- Retorno do resultado da operação com link para rastreabilidade.

## Resultados e impacto

A solução trouxe melhorias para a experiência de abertura e gestão de demandas.

| Indicador | Antes | Depois |
|---|---:|---:|
| Tempo de abertura de demanda | 5–10 minutos | Aproximadamente 2 minutos |
| Necessidade de conhecimento técnico do Jira | Sim | Não |
| Estruturação das informações | Manual | Assistida por IA |
| Classificação da demanda | Manual | Automatizada |

**Redução estimada de 60% a 80% no tempo de abertura de demandas.**

Além do ganho de velocidade, a solução contribuiu para:

- Melhor padronização dos pedidos.
- Maior completude das informações.
- Menor barreira de entrada para os stakeholders.
- Melhor rastreabilidade das solicitações.
- Maior facilidade de consulta e acompanhamento do backlog.

## Meu papel no projeto

Atuei na concepção e desenvolvimento da solução, desde a identificação do problema operacional até a estruturação dos fluxos de inteligência e integração.

Minhas principais responsabilidades envolveram:

- Identificação e entendimento do problema de negócio.
- Desenho da experiência conversacional.
- Estruturação dos fluxos de interação.
- Engenharia de prompts e definição de instruções.
- Desenvolvimento das regras de negócio e classificações.
- Configuração e orquestração das ferramentas do conector Atlassian.
- Definição de mecanismos de validação e confirmação.
- Evolução da solução de agente conversacional para skill.

## Aprendizados técnicos

O projeto envolveu desafios importantes relacionados a:

- Transformação de linguagem natural em operações estruturadas.
- Orquestração de ferramentas externas.
- Integração de modelos de linguagem com sistemas corporativos.
- Construção de fluxos conversacionais com validação.
- Redução de alucinações por meio de regras e instruções.
- Desenvolvimento de soluções de IA orientadas a problemas reais de negócio.

## Demonstração

A demonstração deste repositório utiliza cenários fictícios e informações ilustrativas para apresentar o funcionamento da solução sem expor dados ou configurações internas

https://github.com/user-attachments/assets/567150fb-be10-49b9-affa-db3518ad7764



## Observações

Este projeto foi desenvolvido em ambiente corporativo. O repositório apresenta uma documentação demonstrativa e sanitizada.

Não são disponibilizados códigos proprietários, credenciais, identificadores internos, dados de usuários ou configurações confidenciais do ambiente original.

---

**Miller Souza | AI Builder & Data Professional**

[LinkedIn](https://linkedin.com/in/miller-souza-)
