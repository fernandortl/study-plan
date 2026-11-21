# Formação em AI Engineering --- Currículo de 16 semanas

**Perfil de entrada:** desenvolvedor web experiente, com domínio de
HTML, CSS, JavaScript, PHP, SQL, Docker e TypeScript, experiência
aproximada de 10 anos e uso prévio de ChatGPT e Claude Code.

**Objetivo:** desenvolver competências práticas de AI Engineering para
projetar, implementar, avaliar e operar aplicações inteligentes,
compreendendo os componentes técnicos por trás dos modelos e sistemas de
IA.

## Visão geral

-   **Duração:** 16 semanas (4 meses).
-   **Dedicação:** 12 a 15 horas por semana.
-   **Carga horária total estimada:** 192 a 240 horas.
-   **Abordagem:** prática, com teoria suficiente para compreender as
    decisões técnicas.
-   **Entregas:** cinco projetos principais e um projeto final
    integrado.

Ao concluir o ciclo, a meta é conseguir:

1.  Entender os fundamentos dos LLMs e explicar como funcionam.
2.  Desenvolver aplicações que utilizam modelos de IA profissionalmente.
3.  Construir agentes que utilizam ferramentas e executam tarefas
    controladas.
4.  Implementar RAG para consultar conhecimento próprio.
5.  Executar modelos open source localmente.
6.  Avaliar qualidade, precisão, latência e custo das aplicações.
7.  Projetar arquiteturas de IA preparadas para produção.
8.  Escolher conscientemente entre API, modelo local, RAG, fine-tuning
    ou uma solução tradicional sem IA.

> O princípio central é aprender a construir e entender sistemas de IA,
> não apenas utilizar ferramentas de chat ou escrever prompts.

------------------------------------------------------------------------

# 1. Organização do estudo

## Distribuição semanal sugerida

  Atividade                            Horas por semana
  ---------------------------------- ------------------
  Estudar conceitos e documentação                   3h
  Acompanhar aulas e exemplos                        2h
  Implementar exercícios                             5h
  Desenvolver o projeto da etapa                     3h
  Revisar e documentar                               1h
  **Total de referência**                       **14h**

A rotina pode ser distribuída em quatro ou cinco sessões semanais. A
distribuição é uma referência flexível, desde que a dedicação total
fique entre 12 e 15 horas.

## Método de aprendizagem

Cada assunto será estudado em cinco passos:

1.  **Aula conceitual:** entender o conceito, como funciona internamente
    e por que existe.
2.  **Exemplo técnico:** analisar código e implementar uma versão
    pequena, evitando abstrações desnecessárias.
3.  **Desafio prático:** resolver um problema sem simplesmente copiar
    uma solução pronta.
4.  **Revisão técnica:** avaliar arquitetura, código, decisões e
    resultados.
5.  **Avaliação:** explicar o que foi construído e demonstrar que
    funciona.

O ChatGPT pode ser utilizado como tutor e revisor, e o Claude Code como
assistente de implementação. Porém, o código gerado deve ser
compreendido, testado e revisado. O objetivo é conseguir identificar
arquitetura inadequada, abstrações desnecessárias e implementações
incorretas.

------------------------------------------------------------------------

# 2. Stack tecnológica

A formação acrescenta tecnologias de IA ao conhecimento de
desenvolvimento web já existente.

  -----------------------------------------------------------------------
  Tecnologia              Utilização na formação  Situação
  ----------------------- ----------------------- -----------------------
  Python                  Linguagem principal     Aprender
                          para experimentos e     
                          desenvolvimento de IA   

  PyTorch                 Tensores, redes neurais Aprender
                          e execução de modelos   

  Hugging Face            Modelos, datasets,      Aprender
                          Transformers e          
                          fine-tuning             

  PostgreSQL + pgvector   Dados relacionais,      Complementar
                          embeddings e busca      
                          vetorial                

  Docker                  Ambientes reproduzíveis Conhecimento prévio;
                          e deploy                aplicar em IA

  Ollama                  Execução de modelos     Aprender
                          localmente              

  FastAPI                 APIs e serviços Python  Aprender
                          para IA                 

  LangGraph               Orquestração de agentes Aprender
                          e fluxos com estado     

  TypeScript              Frontend e integração   Conhecimento prévio
                          com os serviços de IA   

  PHP / SQL               Integração com sistemas Conhecimento prévio
                          existentes e regras de  
                          negócio                 
  -----------------------------------------------------------------------

**Estratégia:** não tentar aprender todos os frameworks existentes.
Primeiro dominar os fundamentos e implementar partes importantes sem
abstrações. Depois estudar ferramentas que simplificam o desenvolvimento
em produção.

------------------------------------------------------------------------

# 3. Currículo detalhado --- 16 semanas

## Etapa 1 --- Fundamentos e ambiente de desenvolvimento

**Semanas 1 e 2**

**Objetivo:** compreender a estrutura básica dos modelos e preparar o
ambiente de desenvolvimento.

### Semana 1 --- Entendendo os LLMs

**Conteúdo:**

-   Inteligência Artificial, Machine Learning, Deep Learning e LLMs.
-   Tokens, tokenização e janela de contexto.
-   Como funcionam Transformers e Attention.
-   Treinamento, inferência, pesos e parâmetros.
-   Temperature, Top-P, sampling e alucinações.

**Atividades:**

-   Comparar dois modelos diferentes executando as mesmas tarefas.
-   Registrar diferenças nas respostas.
-   Observar quantidade de tokens de entrada e saída.
-   Medir tempo de resposta.
-   Testar o comportamento diante de informações insuficientes.
-   Comparar respostas determinísticas e variáveis.
-   Documentar observações e conclusões.

Não basta observar qual resposta parece melhor. É necessário começar a
medir o comportamento dos modelos.

**Resultado esperado:** conseguir explicar, em nível introdutório, o que
são tokens, contexto, parâmetros, treinamento, inferência e por que um
LLM pode alucinar.

### Semana 2 --- Python para AI Engineering

O objetivo não é reaprender programação, mas aprender Python aplicado ao
ecossistema de IA.

**Conteúdo:**

-   Ambiente virtual e gerenciamento de dependências.
-   NumPy e operações com arrays.
-   Pandas para manipulação de dados.
-   Jupyter Notebook.
-   Requests e consumo de APIs.
-   Tipagem e validação com Pydantic.
-   FastAPI para criar serviços.
-   Introdução a tensores.

### Projeto 1 --- AI Model Playground

Criar uma aplicação que permita:

1.  Selecionar diferentes provedores de IA.
2.  Enviar prompts.
3.  Alterar parâmetros.
4.  Visualizar tokens de entrada e saída.
5.  Medir latência.
6.  Registrar custos quando disponíveis.
7.  Comparar resultados.

**Stack:** Python, FastAPI, TypeScript e o frontend habitual.

**Entrega:** aplicação funcional para experimentar e comparar modelos.

------------------------------------------------------------------------

## Etapa 2 --- Engenharia de aplicações com LLMs

**Semanas 3 e 4**

**Objetivo:** aprender a integrar modelos de forma confiável,
controlando entradas, saídas e execução de ferramentas.

### Semana 3 --- APIs e comunicação com LLMs

**Conteúdo:**

-   Como funcionam as APIs de LLMs.
-   Mensagens System, User e Assistant.
-   Context Window.
-   Streaming.
-   Structured Outputs.
-   JSON Schema.
-   Function Calling.
-   Tool Calling.
-   Tratamento de erros.
-   Retry, timeout e fallback.

**Exercício:** criar uma API que recebe uma solicitação e retorna uma
resposta estruturada.

Exemplo: o usuário escreve:

> Preciso cadastrar um cliente chamado João, telefone 41999999999 e
> interesse em tratamento odontológico.

O modelo deve transformar isso em uma estrutura semelhante a:

``` json
{
  "intent": "create_customer",
  "customer": {
    "name": "João",
    "phone": "41999999999",
    "interest": "tratamento odontológico"
  }
}
```

A aplicação valida os dados antes de executar qualquer operação.
Structured Outputs ajuda a garantir conformidade com um esquema
suportado, mas não garante que os dados sejam verdadeiros nem que as
regras comerciais estejam corretas.

### Semana 4 --- Tool Calling e integração com sistemas

**Conteúdo:**

-   Como o modelo identifica quando precisa de uma ferramenta.
-   Como definir ferramentas e seus parâmetros.
-   Como o backend executa ferramentas.
-   Como devolver resultados ao modelo.
-   Permissões e validações.
-   Operações com efeitos colaterais.
-   Separação entre decisão do modelo e execução do sistema.

### Projeto 2 --- Assistente inteligente para CRM

Criar um assistente com ferramentas reais:

-   Consultar leads.
-   Consultar pacientes.
-   Buscar histórico de atendimento.
-   Criar tarefas.
-   Atualizar informações autorizadas.
-   Gerar relatórios.

O modelo não terá acesso irrestrito ao banco de dados. Ele solicitará
operações por ferramentas específicas, e o backend fará as validações.

**Entrega:** assistente que interage com uma aplicação real, não apenas
um chatbot.

------------------------------------------------------------------------

## Etapa 3 --- RAG e conhecimento próprio

**Semanas 5 e 6**

**Objetivo:** aprender a construir aplicações que consultam conhecimento
externo sem precisar treinar um modelo.

### Semana 5 --- Embeddings e bancos vetoriais

**Conteúdo:**

-   O que são embeddings.
-   Como textos são convertidos em vetores.
-   Similaridade por cosseno.
-   Distância vetorial.
-   Dimensionalidade.
-   Modelos de embedding.
-   Chunking.
-   Indexação.
-   Busca semântica.
-   Busca híbrida.

**Conceito fundamental:** um embedding não é um resumo do texto. É uma
representação numérica que permite comparar relações semânticas.

**Fluxo conceitual:**

1.  Receber documentos originais (PDF, TXT, DOCX e outros).
2.  Extrair e dividir o conteúdo em chunks.
3.  Enviar os chunks para um modelo de embeddings.
4.  Armazenar os vetores e metadados em um banco vetorial.
5.  Recuperar os trechos relevantes quando uma pergunta for feita.

### Semana 6 --- RAG na prática

**Conteúdo:**

-   Arquitetura RAG.
-   Retrieval.
-   Context assembly.
-   Geração com contexto recuperado.
-   Metadata filtering.
-   Re-ranking.
-   Busca híbrida.
-   Citações e rastreabilidade.
-   Avaliação de recuperação.

### Projeto 3 --- Sistema de conhecimento inteligente

Criar uma aplicação que recebe documentos, indexa seu conteúdo e permite
fazer perguntas.

**Exemplo:** uma empresa disponibiliza manuais, contratos, procedimentos
e documentação interna. O usuário pergunta: "Qual é o procedimento para
cancelar um contrato?"

O sistema deve localizar os documentos relevantes, construir o contexto
e responder com referências às fontes.

**Critérios de aprovação:**

-   Respostas apoiadas em documentos recuperados.
-   Referências que apontem para as fontes corretas.
-   Capacidade de admitir quando não encontrou informação.
-   Testes com perguntas sem resposta na base.
-   Comparação entre busca textual e semântica.

**Tecnologias sugeridas:** PostgreSQL com pgvector; Qdrant como
alternativa para experimentar outro banco vetorial.

------------------------------------------------------------------------

## Etapa 4 --- Agentes de IA

**Semanas 7 e 8**

**Objetivo:** desenvolver sistemas capazes de planejar tarefas, utilizar
ferramentas e trabalhar com fluxos de execução.

### Semana 7 --- Fundamentos de agentes

**Conteúdo:**

-   Diferença entre chatbot, workflow e agente.
-   Ciclo de execução de agentes.
-   Planejamento.
-   Tool Calling.
-   Estado e memória.
-   Controle de execução.
-   Loops.
-   Limites de iteração.
-   Human-in-the-loop.

Começar construindo um agente sem framework, para compreender o
mecanismo:

1.  Receber o objetivo do usuário.
2.  Enviar objetivo e ferramentas disponíveis ao modelo.
3.  Interpretar a solicitação de ferramenta.
4.  Validar e executar a ferramenta no backend.
5.  Devolver o resultado ao modelo.
6.  Permitir que o modelo continue ou finalize.
7.  Impor limites de execução e permissões.

### Semana 8 --- Orquestração e MCP

**Conteúdo:**

-   LangGraph.
-   Estados e nós.
-   Grafos de execução.
-   Condições e ramificações.
-   Checkpoints.
-   Persistência de estado.
-   Subagentes.
-   MCP (Model Context Protocol).
-   Integração com servidores MCP.
-   Segurança de ferramentas.

### Projeto 4 --- Agente de análise empresarial

Criar um agente que recebe uma solicitação como:

> Analise os leads deste mês, identifique os que estão parados há mais
> de sete dias e prepare uma lista de ações.

O agente deverá:

1.  Interpretar a solicitação.
2.  Consultar os leads.
3.  Aplicar critérios.
4.  Analisar os resultados.
5.  Preparar recomendações.
6.  Solicitar aprovação antes de executar alterações.

**Entrega:** agente com ferramentas, estado, controle de execução e
aprovação humana para ações relevantes.

------------------------------------------------------------------------

## Etapa 5 --- Avaliação, segurança e qualidade

**Semanas 9 e 10**

**Objetivo:** aprender o que separa uma demonstração interessante de um
produto de IA confiável.

### Semana 9 --- Avaliação de modelos e aplicações

**Conteúdo:**

-   O que são LLM Evals.
-   Testes de qualidade.
-   Groundedness.
-   Faithfulness.
-   Relevância.
-   Precision e Recall.
-   Métricas de recuperação.
-   Testes de regressão.
-   Comparação de modelos.
-   Avaliação humana.

**Exercício:** montar um conjunto de pelo menos 100 perguntas e
respostas esperadas para testar o projeto RAG.

Investigar quantitativamente:

-   Qual modelo responde melhor?
-   Qual modelo custa menos?
-   Qual modelo alucina mais?
-   Qual configuração recupera os documentos corretos?
-   Qual mudança melhorou ou piorou o resultado?

### Semana 10 --- Segurança e observabilidade

**Conteúdo:**

-   Prompt Injection.
-   Data Leakage.
-   Controle de permissões.
-   Isolamento de dados.
-   Segurança de ferramentas.
-   Rate Limiting.
-   Logs.
-   Tracing.
-   Latência.
-   Monitoramento de custos.
-   Auditoria de ações.
-   Proteção contra execução indevida.

**Entrega:** adicionar testes, logs, rastreamento e controles de
segurança aos projetos anteriores.

------------------------------------------------------------------------

## Etapa 6 --- Modelos locais e infraestrutura

**Semanas 11 e 12**

**Objetivo:** executar modelos sem depender exclusivamente de serviços
externos.

### Semana 11 --- Modelos open source

**Conteúdo:**

-   Hugging Face Hub.
-   Transformers.
-   Modelos base e instruction-tuned.
-   Modelos quantizados.
-   GGUF.
-   Ollama.
-   Tokenizers.
-   Inferência local.
-   Uso de GPU.
-   Consumo de VRAM.

**Laboratório:** testar três alternativas:

-   Um modelo pequeno.
-   Um modelo intermediário quantizado.
-   Um modelo via API comercial.

Comparar velocidade, qualidade, consumo de memória e custo.

O ambiente disponível para os experimentos inclui uma GPU RTX 4080 com
16 GB de VRAM. Ela permite experimentar inferência local com modelos
quantizados e realizar experimentos menores, respeitando os limites de
memória.

### Semana 12 --- Servindo modelos em produção

**Conteúdo:**

-   Ollama.
-   vLLM.
-   FastAPI.
-   Model Serving.
-   Batching.
-   Throughput.
-   Latência.
-   Concorrência.
-   Quantização.
-   Docker para serviços de inferência.

### Projeto 5 --- Servidor local de IA

Criar um serviço local que disponibilize modelos por API.

A aplicação TypeScript ou PHP deverá conseguir consumir esse serviço sem
precisar saber qual modelo está sendo utilizado internamente.

**Entrega:** serviço local de inferência com interface de API,
permitindo trocar modelos sem reescrever toda a aplicação.

------------------------------------------------------------------------

## Etapa 7 --- Fine-tuning e especialização

**Semanas 13 e 14**

**Objetivo:** entender quando vale a pena adaptar um modelo em vez de
depender somente de prompts e RAG.

### Semana 13 --- Preparação de dados

**Conteúdo:**

-   Datasets.
-   Formatos de treinamento.
-   Curadoria de dados.
-   Dados sintéticos.
-   Instruction tuning.
-   Supervised Fine-Tuning.
-   Data quality.
-   Separação de treinamento e validação.

### Semana 14 --- Fine-tuning na prática

**Conteúdo:**

-   LoRA.
-   QLoRA.
-   PEFT.
-   Hugging Face Transformers.
-   TRL.
-   Treinamento supervisionado.
-   Avaliação antes e depois do treinamento.

**Projeto:** adaptar um modelo pequeno para executar uma tarefa
específica, como classificar solicitações e identificar intenções.

Comparar três abordagens:

1.  Prompt bem elaborado.
2.  RAG.
3.  Fine-tuning.

**Pergunta a responder:** qual abordagem realmente melhora o resultado
para aquela tarefa?

------------------------------------------------------------------------

## Etapa 8 --- Projeto final e arquitetura de produção

**Semanas 15 e 16**

**Objetivo:** integrar os conhecimentos e desenvolver uma aplicação
completa.

### Requisitos do projeto final

A aplicação deverá ter:

-   Interface web.
-   Backend Python.
-   Integração com LLMs.
-   Banco de dados.
-   RAG.
-   Agentes.
-   Tool Calling.
-   Autenticação.
-   Controle de permissões.
-   Observabilidade.
-   Avaliação automatizada.
-   Monitoramento de custos.
-   Docker e deploy.

### Arquitetura de referência

``` text
Frontend
  TypeScript / React ou stack atual
       |
       v
Backend
  FastAPI / autenticação / regras de negócio
       |
       v
Camada de AI Engineering
  - LLM Router
  - RAG
  - Agents
  - Evaluation
       |
       +--------------------+
       |                    |
       v                    v
PostgreSQL              Modelos
Dados e vetores         APIs e modelos locais
```

**Critério de conclusão:** outra pessoa deve conseguir executar o
projeto, testar suas funcionalidades, verificar sua qualidade e entender
como os componentes se comunicam.

------------------------------------------------------------------------

# 4. Materiais de estudo e referências

Priorizar materiais gratuitos, documentação oficial e cursos com
exercícios.

  ---------------------------------------------------------------------------------------------------------------
  Recurso                 Uso na formação         Link
  ----------------------- ----------------------- ---------------------------------------------------------------
  Hugging Face Learn      Transformers, agentes,  https://huggingface.co/learn
                          modelos e fine-tuning   

  PyTorch Tutorials       Tensores, redes         https://docs.pytorch.org/tutorials/beginner/basics/intro.html
                          neurais, treinamento e  
                          otimização              

  Full Stack Deep         Engenharia de           https://fullstackdeeplearning.com/course/
  Learning                aplicações de IA,       
                          implantação e operação  

  OpenAI Developer        APIs, ferramentas,      https://developers.openai.com/api/docs/
  Documentation           saídas estruturadas e   
                          avaliação               

  Anthropic Documentation Modelos, ferramentas e  https://docs.anthropic.com/
                          agentes                 

  3Blue1Brown             Matemática e redes      https://www.3blue1brown.com/
                          neurais com explicações 
                          visuais                 

  DeepLearning.AI         Fundamentos e           https://www.deeplearning.ai/
                          aplicações de IA        

  Karpathy                Materiais para entender https://karpathy.ai/
                          LLMs construindo-os     
  ---------------------------------------------------------------------------------------------------------------

**Observação:** alguns cursos e documentações evoluem com frequência.
Conferir a versão atual dos materiais e das bibliotecas antes de
implementar exemplos.

------------------------------------------------------------------------

# 5. Decisões pedagógicas importantes

1.  **Não aprofundar matemática excessivamente no início.** Aprender o
    necessário para entender algoritmos e trabalhar com eles. Aprofundar
    conforme a necessidade.
2.  **Não começar com frameworks de agentes.** Primeiro implementar um
    agente simples manualmente. Depois entender o que LangGraph e outras
    ferramentas abstraem.
3.  **Não fazer fine-tuning antes de dominar RAG e avaliação.** Muitas
    aplicações que parecem precisar de treinamento especializado podem
    ser resolvidas com recuperação de contexto e uma boa arquitetura.
4.  **Medir resultados.** Não aceitar apenas respostas que parecem boas.
    Criar conjuntos de testes, métricas e comparações.
5.  **Entender o código gerado.** Utilizar Claude Code como apoio, mas
    revisar arquitetura, segurança, comportamento e qualidade.

Este currículo é uma formação inicial sólida em AI Engineering, não uma
formação completa em pesquisa de IA. Depois dele, será possível avançar
para visão computacional, modelos multimodais, treinamento mais profundo
e sistemas distribuídos de inferência.

------------------------------------------------------------------------

# 6. Acompanhamento das 16 semanas

Utilizar esta lista para acompanhar a conclusão de cada etapa.

-   [ ] Semanas 1--2: Fundamentos e Python
-   [ ] Semanas 3--4: Engenharia de aplicações com LLMs
-   [ ] Semanas 5--6: Embeddings e RAG
-   [ ] Semanas 7--8: Agentes e MCP
-   [ ] Semanas 9--10: Avaliação e segurança
-   [ ] Semanas 11--12: Modelos locais e infraestrutura
-   [ ] Semanas 13--14: Fine-tuning
-   [ ] Semanas 15--16: Projeto final

## Critério geral de progresso

Uma etapa só deve ser considerada concluída quando:

-   Os conceitos principais puderem ser explicados sem depender de uma
    resposta pronta.
-   Os exercícios tiverem sido implementados e testados.
-   O projeto da etapa estiver funcional.
-   As decisões técnicas e limitações estiverem documentadas.
-   O resultado puder ser demonstrado.

------------------------------------------------------------------------

# 7. Primeiro assunto

**Semana 1 --- Aula 1: IA, Machine Learning, Deep Learning e LLMs.**

Seguir uma aula por vez, com explicação técnica, exemplos de código,
exercícios e avaliação. Avançar quando o assunto estiver dominado, não
apenas quando o conteúdo tiver sido lido.
