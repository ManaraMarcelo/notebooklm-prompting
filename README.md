<p align="center">
  <img src="https://github.com/ManaraMarcelo/notebooklm-prompoting/blob/main/img.png" width="600">
</p>


# [EN] - DIO Challenge: Generative Artificial Intelligence on AWS

Structured repository to demonstrate technical maturity, source curation, and prompt engineering applied to the GenAI ecosystem within Amazon Web Services (AWS). The main objective is to deepen knowledge in modern architectures requested by the job market.

---

## Context and Objectives

The context and object of this study is the practical use of Generative AI on AWS. The project aims to connect AI engineering to cloud infrastructure, generating productive and scalable value, focusing especially on agile implementations and serverless architectures.

**Main Objectives:**
* Know what is natively available in the AWS ecosystem.
* Understand the fundamental cloud infrastructure prerequisites before moving to the actual AI stage.
* Understand how to govern and use artificial intelligence inside the cloud correctly.
* Know the tools and architectures currently demanded by the market on AWS.

---

## Curated Sources

To compose the knowledge base of this study, strategic sources focused on cloud architecture and AI were selected:

1. https://www.youtube.com/watch?v=SiPbnW2ivlU
2. https://www.youtube.com/watch?v=qpEKtvfxseo
3. https://www.youtube.com/watch?v=55nzTrFfE2s
4. https://www.youtube.com/watch?v=nOZTyuhCU2k
5. https://aws.amazon.com/what-is/agentic-ai/?nc1=f_cc&trk=86c3abc1-a941-48dc-b313-118a1dfe0985&sc_channel=ps
6. https://aws.amazon.com/what-is-cloud-computing/?nc1=f_cc&trk=86c3abc1-a941-48dc-b313-118a1dfe0985&sc_channel=ps

---

## Prompt Engineering and "Scars" (Troubleshooting)

The fundamental premise of this project is that basic prompts do not deliver deep architectural value. The need for specific techniques must be evaluated on a case-by-case basis, but the logical structuring of the prompt is mandatory to avoid hallucinations.

### The Engineering Framework (6 Steps)
To extract knowledge accurately, a structural baseline was built:
1. **Initial instruction** (defining the role/persona).
2. **General context**.
3. **Examples (Few-Shotting)** of similar cases.
4. **Input data** to be analyzed.
5. **General rules and Guardrails** (output language, restrictions, and tone).
6. **Output preparation** (format, quantity, quality).

For use within **NotebookLM**, fully applying the 6 steps in every question would make the study exhausting. Therefore, the strategy was to adapt the framework: context and input data were already supplied by the uploaded documents on the platform, allowing the prompts to focus on instructions, a few vital rules, and output preparation.

### Practical Tests and Comparative Analysis (Execution Proofs)

Below is the real record of the approaches tested on the selected sources, highlighting the difference in output quality.

#### Approach 1: Basic Prompt (Zero-Shot)

**Prompt Tested:**
> "What Generative AI tools exist on AWS and what do I need to know before using them?"

**Output Obtained (Summary):**
AWS offers a robust ecosystem for Generative Artificial Intelligence. Sources highlight three pillars: Amazon Bedrock (model router and agent creation), Amazon Q (business and code assistant), and Amazon SageMaker (training from scratch). Before using, you need to know:
1. Technical Skills: Work with API calls and Python (Boto3).
2. Prompt Engineering: Surgical instructions.
3. Security: Shared Responsibility Model and Guardrails.
4. Observability: Implement logs and tracing.
5. Costs: Monitor token consumption.

**Analysis and Scar (Troubleshooting):**
The result was too broad. The AI generated a general list, but superficially, mixing basic cloud computing concepts with traditional AI, without delving into the actual infrastructure prerequisites or specific market demands.

#### Approach 2: Advanced Engineering (Roleplay + Few-Shot + Guardrails)

**Prompt Tested:**
> "Act as an AWS Solutions Architect specializing in Generative AI. Based on the provided sources, describe the AWS GenAI ecosystem (focusing on Amazon Bedrock and autonomous agents).
>
> Follow the example structure below for the response:
> Tool: [Name] -> Cloud Prerequisite: [What to know before] -> Market Focus: [Practical application].
>
> Restriction (Guardrail): Do not include legacy tools or traditional Machine Learning services (like pure SageMaker), focus strictly on Large Language Models (LLMs) and Agentic AI."

**Output Obtained:**
* **Tool: Amazon Bedrock** -> **Cloud Prerequisite:** Know how to make API calls (via Boto3 SDK for Python), configure identity and access permissions in AWS IAM, and manually enable model access in the AWS console. -> **Market Focus:** Act as a "router" that offers unified access to Foundation Models (FMs).
* **Tool: Agents for Amazon Bedrock** -> **Cloud Prerequisite:** Mastery of AWS Lambda, Knowledge Bases configuration (RAG), and observability implementation (logs and tracing). -> **Market Focus:** Development of autonomous Agentic AI that perceives, reasons, and acts.
* **Tool: Amazon Q (Business and Developer)** -> **Cloud Prerequisite:** Integration with code repositories or corporate data sources. -> **Market Focus:** Specialized productivity assistant for code generation and legacy application migration.
* **Tool: Amazon Q Developer CLI** -> **Cloud Prerequisite:** Local environment installation and session-level credentials configuration. -> **Market Focus:** Command-line interface for executing executive tasks in the terminal.
* **Tool: Amazon Bedrock Guardrails** -> **Cloud Prerequisite:** Knowledge about vulnerabilities like Prompt Injection and PII protection. -> **Market Focus:** Implementation of security layers that filter unwanted content.

**Analysis and Scar (Troubleshooting):**
The result generated a highly structured response, filtering out the noise from the sources and focusing exactly on the essential cloud computing prerequisites before implementing AI. The *Few-Shot* technique (providing the bracket format) guided the AI to the exact desired output, and the *Guardrails* technique prevented deviations towards older ML tools. Adding tone instructions (*Roleplay*) changed the AI's vocabulary to something more mature and professional.

---

## Study Mini-guide (Final Delivery)

This mini-guide was consolidated from the strategic questions submitted to NotebookLM, analyzing the material from the proposed sources.

### 1. Structured Subject Summaries

**Cloud Prerequisites for GenAI**
To correctly implement Generative AI on AWS, developers must master the infrastructure foundation. The entry point for AI systems that execute actions is **Serverless Computing (AWS Lambda)**, requiring mastery of the idempotency concept. Additionally, strict control in **AWS IAM** is critical to ensure applications invoke models securely, respecting the Shared Responsibility Model. Storage in **Amazon S3** and databases like **Amazon DynamoDB** sustain the memory and knowledge bases (RAG) of these models.

**Tools and Market Demand**
The most prominent tools are **Amazon Bedrock** (focused on building applications via API with models from providers like Anthropic and Meta) and **Amazon Q** (aimed at productivity and legacy code modernization). The market demands skills in Boto3 integration, surgical prompt engineering, Guardrails configuration for corporate data protection (which is not used for retraining on AWS), and the ability to architect complex workflows.

**The Agentic AI Paradigm**
Agentic AI represents the evolution from passive chatbots to proactive systems with "agency". Unlike a chatbot that merely returns text based on a prompt, an Autonomous Agent operates in a four-stage cycle: **Perceive** data from APIs, **Reason** by creating a logical plan via LLM, **Act** by executing tasks in third-party systems, and **Learn** from the results, being capable of decomposing complex requests into executable sub-tasks without constant human supervision.

### 2. Glossary of Learned Concepts

* **Amazon Bedrock:** Fully managed service that makes foundation models (FMs) available through a single API, ensuring corporate information isolation.
* **Agentic AI:** Autonomous AI system, capable of taking initiatives and using external tools (like Lambda functions) to achieve predetermined goals.
* **AWS IAM (Identity and Access Management):** Access and identity management service, essential for securely enabling and restricting calls to language models.
* **RAG (Retrieval-Augmented Generation):** Technique of providing additional and private context (via knowledge bases in S3) to the language model, increasing response accuracy.
* **Prompt Injection:** Vulnerability where the model is manipulated by malicious instructions hidden in the prompt to bypass original security rules.

### 3. Reusable Prompt Set

These templates consolidate the tested techniques and can support future reviews of the covered architectures:

**Prompt for Structuring Autonomous Agents**
```text
Act as a Senior Software Engineer. 
Based on the AWS technical documentation on Agentic AI, list the execution flow required to create an Agent in Amazon Bedrock that processes refunds.
Rules: Think step-by-step (Chain of Thought). Specify the AWS Lambda functions needed for the "Act" stage and the data required in DynamoDB for the "Perceive" stage.
Format: Present the plan in a technical numbered list.
```

**Prompt for Security Validation (Guardrails)**
```text
Analyze the following prompt structure that will be sent to an LLM via Amazon Bedrock.
Input Data: [INSERT YOUR BASE PROMPT HERE]
Your task is to act as a cybersecurity analyst and point out potential loopholes for 'Prompt Injection' or sensitive data leakage (PII).
Remember the initial instruction: focus exclusively on the prompt's structural security, do not evaluate the business logic.
```

---

# [PT] - Desafio DIO: Inteligência Artificial Generativa na AWS

Repositório estruturado para demonstrar maturidade técnica, curadoria de fontes e engenharia de prompts aplicadas ao ecossistema de GenAI dentro da Amazon Web Services (AWS). O objetivo principal é aprofundar os conhecimentos em arquiteturas modernas solicitadas pelo mercado de trabalho.

---

## Contexto e Objetivos

O contexto e objeto deste estudo é o uso prático de IA Generativa na AWS. O projeto visa conectar a engenharia de IA à infraestrutura de nuvem, gerando valor produtivo e escalável, especialmente focando em implementações ágeis e arquiteturas serverless.

**Objetivos Principais:**
* Saber o que está disponível nativamente no ecossistema AWS.
* Compreender os pré-requisitos fundamentais de infraestrutura de nuvem antes de ir para a etapa de IA de fato.
* Entender como usar a inteligência artificial lá dentro de maneira correta.
* Conhecer as ferramentas solicitadas pelo mercado na AWS.

---

## Curadoria de Fontes

Para compor a base deste estudo, foram selecionadas fontes estratégicas focadas em arquitetura de nuvem e IA:

1. https://www.youtube.com/watch?v=SiPbnW2ivlU
2. https://www.youtube.com/watch?v=qpEKtvfxseo
3. https://www.youtube.com/watch?v=55nzTrFfE2s
4. https://www.youtube.com/watch?v=nOZTyuhCU2k
5. https://aws.amazon.com/what-is/agentic-ai/?nc1=f_cc&trk=86c3abc1-a941-48dc-b313-118a1dfe0985&sc_channel=ps
6. https://aws.amazon.com/what-is-cloud-computing/?nc1=f_cc&trk=86c3abc1-a941-48dc-b313-118a1dfe0985&sc_channel=ps

---

## Engenharia de Prompts e "Cicatrizes"

A premissa fundamental deste projeto é que prompts básicos não entregam valor arquitetural profundo. O grau de necessidade de técnicas específicas deve ser avaliado caso a caso, mas a estruturação lógica do prompt é mandatória para evitar alucinações.

### O Framework de Engenharia (6 Passos)
Para extrair conhecimento com precisão, construiu-se uma base de estruturação:
1. **Instrução inicial** (definindo o papel).
2. **Contexto geral**.
3. **Exemplos (Few-Shotting)** de casos similares.
4. **Dados de entrada** a serem analisados.
5. **Regras gerais e Guardrails** (idioma de saída, restrições e tom).
6. **Preparo de saída** (formato, quantidade, qualidade).

Para o uso dentro do **NotebookLM**, aplicar os 6 passos integralmente em cada pergunta tornaria o estudo exaustivo. Portanto, a estratégia foi adaptar o framework: o contexto e os dados de entrada já estavam supridos pelos documentos carregados na plataforma, permitindo focar os prompts nas instruções, poucas regras vitais e no preparo de saída.

### Testes Práticos e Análise Comparativa (Provas de Execução)

Abaixo está o registro real das abordagens testadas nas fontes selecionadas, evidenciando a diferença de qualidade no retorno.

#### Abordagem 1: Prompt Básico (Zero-Shot)

**Prompt Testado:**
> "Quais ferramentas de IA Generativa existem na AWS e o que preciso saber antes de usar?"

**Saída Obtida (Resumo do Retorno):**
A AWS oferece um ecossistema robusto para Inteligência Artificial Generativa. As fontes destacam três pilares: Amazon Bedrock (roteador de modelos e criação de agentes), Amazon Q (assistente para código e negócios) e Amazon SageMaker (treinamento do zero). Antes de usar, é necessário saber:
1. Habilidades Técnicas: Trabalhar com chamadas de API e Python (Boto3).
2. Engenharia de Prompt: Instruções cirúrgicas.
3. Segurança: Modelo de Responsabilidade Compartilhada e Guardrails.
4. Observabilidade: Implementar logs e tracing.
5. Custos: Monitorar consumo de tokens.

**Análise e Cicatriz (Troubleshooting):**
O resultado ficou muito amplo. A IA gerou uma lista geral, mas de forma superficial, misturando conceitos básicos de computação em nuvem com IA, sem aprofundar nos pré-requisitos de infraestrutura reais ou nas demandas específicas de mercado.

#### Abordagem 2: Engenharia Avançada (Roleplay + Few-Shot + Guardrails)

**Prompt Testado:**
> "Atue como um Arquiteto de Soluções AWS especialista em IA Generativa. Com base nas fontes fornecidas, descreva o ecossistema de GenAI da AWS (focando em Amazon Bedrock e agentes autônomos).
>
> Siga a estrutura do exemplo abaixo para a resposta:
> Ferramenta: [Nome] -> Pré-requisito de Nuvem: [O que saber antes] -> Foco do Mercado: [Aplicação prática].
>
> Restrição (Guardrail): Não inclua ferramentas legadas ou serviços de Machine Learning tradicional (como SageMaker puro), foque estritamente em modelos de linguagem (LLMs) e IA Agêntica."

**Saída Obtida:**
* **Ferramenta: Amazon Bedrock** -> **Pré-requisito de Nuvem:** Saber realizar chamadas de API (via SDK Boto3 para Python), configurar permissões de identidade e acesso no AWS IAM e habilitar manualmente o acesso aos modelos no console da AWS. -> **Foco do Mercado:** Atuar como um "roteador" que oferece acesso unificado a Modelos Fundacionais (FMs).
* **Ferramenta: Agentes para Amazon Bedrock** -> **Pré-requisito de Nuvem:** Domínio de AWS Lambda, configuração de Bases de Conhecimento (RAG) e implementação de observabilidade (logs e tracing). -> **Foco do Mercado:** Desenvolvimento de IA Agêntica autônoma que percebe, raciocina e age.
* **Ferramenta: Amazon Q (Business e Developer)** -> **Pré-requisito de Nuvem:** Integração com repositórios de código ou fontes de dados corporativas. -> **Foco do Mercado:** Assistente especializado em produtividade na geração de código e migração de aplicações legadas.
* **Ferramenta: Amazon Q Developer CLI** -> **Pré-requisito de Nuvem:** Instalação em ambiente local e configuração de credenciais de nível de sessão. -> **Foco do Mercado:** Interface de linha de comando para realizar tarefas executivas no terminal.
* **Ferramenta: Amazon Bedrock Guardrails** -> **Pré-requisito de Nuvem:** Conhecimento sobre vulnerabilidades como Prompt Injection e proteção de PII. -> **Foco do Mercado:** Implementação de camadas de segurança que filtram conteúdos indesejados.

**Análise e Cicatriz (Troubleshooting):**
O resultado gerou uma resposta altamente estruturada, filtrando o ruído das fontes e focando exatamente nos pré-requisitos de computação em nuvem essenciais antes de implementar IA. A técnica de *Few-Shot* (fornecer o formato em colchetes) guiou a IA para a saída exata desejada, e a técnica de *Guardrails* evitou desvios para ferramentas de ML mais antigas. Adicionar instruções de tom (*Roleplay*) mudou o vocabulário da IA para algo mais maduro e profissional.

---

## Miniguia de Estudo (Entrega Final)

Este miniguia foi consolidado a partir das perguntas estratégicas submetidas ao NotebookLM, analisando o material das fontes propostas.

### 1. Resumos Estruturados do Assunto

**Pré-requisitos de Nuvem para GenAI**
Para implementar IA Generativa na AWS de forma correta, o desenvolvedor precisa dominar a base da infraestrutura. O ponto de entrada para sistemas de IA que executam ações é a **Computação Serverless (AWS Lambda)**, exigindo o domínio do conceito de idempotência. Além disso, o controle rigoroso no **AWS IAM** é fundamental para garantir que as aplicações invoquem modelos de forma segura, respeitando o Modelo de Responsabilidade Compartilhada. O armazenamento no **Amazon S3** e bancos como o **Amazon DynamoDB** sustentam a memória e as bases de conhecimento (RAG) desses modelos.

**Ferramentas e Demanda de Mercado**
As ferramentas de maior destaque são o **Amazon Bedrock** (focado na construção via API de aplicações com modelos de provedores como Anthropic e Meta) e o **Amazon Q** (voltado para produtividade e modernização de código legado). O mercado demanda habilidades de integração via Boto3, engenharia de prompt cirúrgica, configuração de Guardrails para proteção de dados corporativos (que não são usados para retreino na AWS) e a capacidade de arquitetar workflows complexos.

**O Paradigma da IA Agêntica**
A IA Agêntica representa a evolução dos chatbots passivos para sistemas proativos com "agency" (agência). Diferente de um chatbot que apenas retorna texto baseado em um prompt, um Agente Autônomo opera em um ciclo de quatro estágios: **Perceber** dados de APIs, **Raciocinar** criando um plano lógico via LLM, **Agir** executando tarefas em sistemas de terceiros e **Aprender** com os resultados, sendo capaz de decompor pedidos complexos em subtarefas executáveis sem supervisão humana constante.

### 2. Glossário de Conceitos Aprendidos

* **Amazon Bedrock:** Serviço totalmente gerenciado que disponibiliza modelos de fundação (FMs) por meio de uma única API, garantindo o isolamento das informações corporativas.
* **Agentic AI:** Sistema de IA autônomo, capaz de tomar iniciativas e utilizar ferramentas externas (como funções Lambda) para atingir objetivos pré-determinados.
* **AWS IAM (Identity and Access Management):** Serviço de gestão de acessos e identidades, essencial para habilitar e restringir chamadas aos modelos de linguagem de forma segura.
* **RAG (Retrieval-Augmented Generation):** Técnica de fornecer contexto adicional e privado (via bases de conhecimento no S3) para o modelo de linguagem, aumentando a precisão da resposta.
* **Prompt Injection:** Vulnerabilidade onde o modelo é manipulado por instruções maliciosas ocultas no prompt para burlar as regras originais de segurança.

### 3. Conjunto de Prompts Reutilizáveis

Estes templates consolidam as técnicas testadas e podem apoiar revisões futuras sobre as arquiteturas abordadas:

**Prompt para Estruturação de Agentes Autônomos**
```text
Atue como um Engenheiro de Software Sênior. 
Com base na documentação técnica da AWS sobre IA Agêntica, liste o fluxo de execução necessário para criar um Agente no Amazon Bedrock que processe reembolsos.
Regras: Pense passo a passo (Chain of Thought). Especifique as funções AWS Lambda necessárias para a etapa de "Agir" e os dados necessários no DynamoDB para a etapa de "Perceber".
Formato: Apresente o plano em uma lista numerada técnica.
```

**Prompt para Validação de Segurança (Guardrails)
```text
Analise a seguinte estrutura de prompt que será enviada para um LLM via Amazon Bedrock.
Dado de Entrada: [INSERIR SEU PROMPT BASE AQUI]
Sua tarefa é atuar como um analista de segurança cibernética e apontar possíveis brechas para 'Prompt Injection' ou vazamento de dados sensíveis (PII).
Lembre-se da instrução inicial: foque exclusivamente na segurança estrutural do prompt, não avalie a lógica de negócios.
```
