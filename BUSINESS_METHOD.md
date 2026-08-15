# Business Method

**Versão:** 2.0  
**Finalidade:** fornecer ao CEO uma biblioteca de Areas de negócio, indicando quando cada uma pode ser criada, quais condições devem existir e qual resultado ela deve produzir.

## 1. Papel deste documento

Este documento responde a duas perguntas:

1. **Qual Area de negócio pode ser útil agora?**
2. **Em qual momento ela deve ser criada?**

Ele não define como uma Area funciona internamente. Organograma, Area Settings, Area Data, agentes, Area Loop, granularidade, divisão, combinação, pausa e encerramento são definidos em `COMPANY_STRUCTURE.md`.

O CEO consulta esta biblioteca:

- durante o Company Start;
- quando um Goal novo exigir uma capacidade inexistente;
- quando um aprendizado indicar uma lacuna organizacional;
- quando a Company entrar em uma nova etapa de descoberta, validação, estruturação ou escala.

## 2. Princípio de ativação progressiva

A lista representa uma progressão possível do negócio, não um organograma obrigatório nem uma sequência rígida.

O CEO deve:

- identificar o estágio e o gargalo atuais por evidência;
- selecionar somente as Areas necessárias ao horizonte atual;
- reutilizar uma Area existente quando ela já cobrir a responsabilidade;
- manter como candidatas as Areas de etapas futuras;
- não criar agentes, budgets ou estruturas para uma Area marcada como futura;
- revisar a seleção quando Goals, evidências ou condições do negócio mudarem.

Uma Company não precisa possuir todas as Areas desta biblioteca. Algumas podem ser:

- desnecessárias para o tipo de negócio;
- absorvidas por outra Area;
- temporárias;
- recorrentes;
- ativadas fora da ordem apresentada.

## 3. Status de avaliação

Ao avaliar cada template, o CEO atribui um status:

| Status | Significado | Efeito |
|---|---|---|
| `CREATE_NOW` | A capacidade é necessária no horizonte atual e não está coberta | Propor Area no Company Implementation Plan |
| `PREPARE_NEXT` | A capacidade provavelmente será necessária em seguida | Registrar trigger e dependências; não criar estrutura ainda |
| `ABSORBED` | Uma Area existente já cobre a capacidade | Registrar a Area responsável |
| `COMPLETE` | O resultado necessário já existe e continua válido | Referenciar evidências e não recriar a Area |
| `LATER` | O momento ainda não chegou ou faltam pré-condições | Manter no roadmap sem agentes ou budget |
| `SKIP` | Não se aplica ao modelo ou ao Goal da Company | Registrar justificativa curta |
| `BLOCKED` | É necessária agora, mas existe impedimento material | Registrar blocker e escalar |

`PREPARE_NEXT` e `LATER` não autorizam criação de Project, Goal, agentes, heartbeat ou budget operacional.

## 4. Etapas do negócio

Para orientar a avaliação, a biblioteca agrupa as Areas em quatro momentos:

| Momento | Pergunta dominante | Areas mais comuns |
|---|---|---|
| Fundação | O sistema sabe para onde vai e consegue operar? | Agents Setup, Goals |
| Descoberta | Qual problema, mercado e referência justificam o negócio? | Concepts, Market, Benchmarking |
| Construção e validação | O que gera valor, como testar e como medir? | Software, Value, MVP, Branding, Metrics, Model |
| Escala e capital | O que é repetível, financiável e capaz de crescer? | Scale Cycles, Fundraise Model, Investment, Growth |

Os momentos podem se sobrepor. Uma Company pode retornar a Concepts ou Market ao lançar um produto novo e pode crescer sem captar investimento.

## 5. Biblioteca de Areas

### 5.1 Agents Setup

**Propósito:** implantar ou evoluir a capacidade agêntica necessária para o negócio operar.

**Criar quando:**

- o MVA ainda precisa de trabalho técnico ou operacional além do Company Start;
- integrações, modelos, canais, skills, segurança ou observabilidade precisam ser implantados;
- o crescimento do número de agentes exige uma capacidade recorrente de Agent Operations.

**Não criar separadamente quando:** o Company Start consegue implementar todo o setup inicial e não existe backlog recorrente. Nesse caso, classifique como `ABSORBED` pelo bootstrap.

**Resultados esperados:** baseline operacional dos agentes, integrações autorizadas, catálogo de skills, controles de acesso, observabilidade e readiness report.

**Forma típica:** temporária no boot; recorrente quando a infraestrutura agêntica se torna capacidade contínua.

### 5.2 Goals

**Propósito:** estruturar Goals, métricas, prioridades e relações entre objetivos.

**Criar quando:**

- o Main Goal existe, mas precisa ser decomposto em uma Goal Tree;
- objetivos são ambíguos, conflitantes ou não mensuráveis;
- a revisão de portfólio e prioridades se tornou trabalho recorrente.

**Não criar separadamente quando:** CEO e humano responsável conseguem definir e manter Goals diretamente na governança da Company.

**Resultados esperados:** Goal Tree, métricas, horizontes, dependências, critérios de conclusão e decisões reservadas ao humano.

**Limite:** a Area não substitui a autoridade humana sobre Main Goal e mudanças estratégicas materiais.

### 5.3 Concepts

**Propósito:** transformar uma intenção, problema ou oportunidade em conceitos de negócio investigáveis.

**Criar quando:**

- existe uma ideia ampla, mas a proposta ainda não está claramente formulada;
- há múltiplos conceitos concorrentes;
- premissas fundamentais ainda precisam ser explicitadas.

**Pré-condição mínima:** problema, oportunidade ou intenção inicial identificável.

**Resultados esperados:** Concept Briefs, problema-alvo, beneficiários, hipóteses centrais, alternativas e critérios para avançar, combinar ou descartar conceitos.

**Forma típica:** temporária ou reativada para novas teses, produtos e mercados.

### 5.4 Market

**Propósito:** compreender mercado, segmentos, clientes, contexto e evidências de demanda.

**Criar quando:**

- mercado ou segmento prioritário ainda é desconhecido;
- o conceito depende de premissas de demanda não validadas;
- a Company considera nova geografia, vertical ou perfil de cliente.

**Pré-condição mínima:** conceito ou problema a investigar.

**Resultados esperados:** Market Map, segmentação, ICPs, necessidades, tamanho e dinâmica do mercado, sinais de demanda, riscos e questões em aberto.

**Forma típica:** ativa na descoberta e reativada em expansões.

### 5.5 Benchmarking

**Propósito:** comparar concorrentes, alternativas, referências e práticas relevantes para uma decisão.

**Criar quando:**

- uma decisão material depende de comparação estruturada;
- posicionamento, produto, processo ou meta precisa de referências externas;
- existe risco de repetir solução já disponível ou ignorar um padrão relevante.

**Pré-condição mínima:** objeto e critérios de comparação definidos.

**Resultados esperados:** Benchmark Matrix, diferenças, lacunas, padrões, implicações e recomendações.

**Forma típica:** on-demand ou temporária. Só deve ser persistente quando comparação contínua for parte central do negócio.

### 5.6 Software

**Propósito:** conceber, construir, operar ou evoluir software necessário à oferta ou à operação.

**Criar quando:**

- software é parte da solução vendida;
- uma capacidade interna essencial precisa ser construída;
- existe backlog técnico recorrente com resultado próprio;
- confiabilidade, segurança e manutenção exigem ownership dedicado.

**Não criar quando:** o negócio não depende de software próprio e ferramentas existentes atendem ao Goal.

**Pré-condições:** necessidade identificada, usuário ou processo beneficiado e limite inicial de investimento.

**Resultados esperados:** Product/Software Scope, arquitetura e restrições, roadmap, releases, qualidade operacional e dívida técnica visível.

**Forma típica:** recorrente quando existe produto ou plataforma própria; temporária para uma implantação delimitada.

### 5.7 Value

**Propósito:** definir e testar o valor produzido para clientes, usuários e demais stakeholders.

**Criar quando:**

- mercado e público estão razoavelmente identificados, mas a proposta de valor ainda é incerta;
- benefícios, diferenciação ou disposição a adotar/pagar precisam de evidência;
- sinais do MVP exigem revisão da proposta de valor.

**Pré-condições:** conceito e segmento ou beneficiário identificados.

**Resultados esperados:** Value Proposition, jobs/pains/gains, promessas testáveis, diferenciação, evidências e hipóteses de valor.

**Forma típica:** temporária, com revisões quando mercado ou oferta mudarem.

### 5.8 MVP

**Propósito:** produzir o menor teste integrado capaz de reduzir as incertezas críticas do negócio.

**Criar quando:**

- existe hipótese de valor falsificável;
- público e problema do teste estão definidos;
- é possível medir um comportamento ou resultado relevante;
- aprender com uma entrega real é mais útil que continuar planejando.

**Pré-condições:** hipótese, público, métrica, budget, prazo e guardrails do experimento.

**Resultados esperados:** MVP Scope, Test Plan, entrega controlada, evidências, decisão de iterar, pivotar, avançar ou encerrar.

**Forma típica:** temporária por ciclo. Não deve virar nome permanente para uma operação já madura.

### 5.9 Branding

**Propósito:** construir posicionamento, narrativa e identidade coerentes com público e valor.

**Criar quando:**

- conceito, público e proposta de valor possuem estabilidade suficiente;
- a Company precisa se apresentar, lançar ou unificar comunicação;
- inconsistência de marca prejudica aquisição, confiança ou execução.

**Evitar antecipação:** identidade detalhada antes de evidência mínima de público e valor pode gerar retrabalho. Nesse caso, use identidade provisória e mantenha a Area como `LATER`.

**Resultados esperados:** positioning, narrativa, mensagens, identidade, princípios de aplicação e ativos mínimos.

**Forma típica:** temporária na criação e recorrente quando gestão de marca possuir volume próprio.

### 5.10 Metrics

**Propósito:** definir, instrumentar e manter as métricas que permitem decidir e aprender.

**Criar quando:**

- experimentos ou operação já exigem mensuração confiável;
- métricas estão dispersas, contraditórias ou sem owner;
- a Company pretende validar, comparar ou escalar resultados.

**Momento limite:** deve existir antes de declarar MVP validado, modelo repetível ou prontidão para escala.

**Resultados esperados:** Metric Tree, definições, fontes, baselines, instrumentação, dashboards, qualidade e cadência de revisão.

**Forma típica:** recorrente quando dados de performance se tornam capacidade compartilhada; absorvida por outra Area em operações pequenas.

### 5.11 Model

**Propósito:** estruturar como a Company cria, entrega e captura valor de forma operacional e economicamente sustentável.

**Criar quando:**

- há evidência inicial de valor e é necessário definir receita, custos e operação;
- alternativas de pricing, canal, parceria ou entrega precisam ser comparadas;
- o modelo atual não sustenta os Goals ou a escala pretendida.

**Pré-condições:** evidências de Market, Value/MVP e Metrics suficientes para evitar um modelo puramente imaginado.

**Resultados esperados:** Business Model, revenue model, pricing hypotheses, unit economics, cadeia de entrega, recursos, parceiros e riscos.

**Forma típica:** temporária na estruturação, com revisões materiais ao longo da vida da Company.

### 5.12 Scale Cycles

**Propósito:** executar ciclos controlados para testar e ampliar repetibilidade, capacidade e eficiência.

**Criar quando:**

- existe um baseline medido;
- valor e entrega apresentam repetibilidade inicial;
- o principal problema mudou de descoberta para aumento controlado de volume;
- gargalos de capacidade, canal, qualidade ou custo podem ser testados.

**Pré-condições:** métricas confiáveis, stop conditions, capacidade operacional e guardrails de risco/custo.

**Resultados esperados:** Scale Hypotheses, planos de ciclo, capacity constraints, resultados comparáveis e decisões de ampliar, estabilizar ou recuar.

**Forma típica:** ciclos temporários e repetidos; não equivale a crescimento irrestrito.

### 5.13 Fundraise Model

**Propósito:** determinar se capital externo é necessário e, se for, qual tese de captação sustenta os próximos marcos.

**Criar quando:**

- existe uma oportunidade ou plano cuja execução requer capital além do disponível;
- a Company precisa comparar bootstrap, receita, dívida, grants e equity;
- valor, uso dos recursos e marcos financiáveis podem ser explicitados.

**Não criar automaticamente:** captação não é etapa obrigatória de todo negócio.

**Resultados esperados:** Capital Need Assessment, funding strategy, montante, runway, uso de recursos, marcos, cenários, riscos e impactos de governança/diluição.

**Forma típica:** temporária e sujeita a aprovação humana.

### 5.14 Investment

**Propósito:** executar um processo aprovado de obtenção e formalização de investimento.

**Criar quando:**

- Fundraise Model foi aprovado;
- métricas, narrativa, documentos e responsáveis estão prontos;
- existe autorização humana para abordar investidores e negociar dentro de limites definidos.

**Pré-condições:** tese de captação, data room, target investors, decision rights, limites de negociação e compliance.

**Resultados esperados:** investor pipeline, materiais, interações registradas, diligência, propostas, decisões e fechamento ou encerramento do processo.

**Forma típica:** temporária. Comunicação, negociação e compromissos financeiros seguem approvals obrigatórias.

### 5.15 Growth

**Propósito:** construir mecanismos recorrentes de aquisição, ativação, retenção, expansão e receita.

**Criar quando:**

- público, valor, entrega e métricas possuem repetibilidade suficiente;
- a Company consegue atender crescimento sem degradar resultados críticos;
- existe capacidade de testar canais e loops com unit economics observáveis.

**Não depende de investimento:** Growth pode começar antes, durante ou sem uma rodada, desde que as condições operacionais existam.

**Resultados esperados:** Growth Model, channel portfolio, loops, experiment backlog, métricas de aquisição/retenção/receita e limites de escala.

**Forma típica:** recorrente quando crescimento se torna responsabilidade contínua.

## 6. Regras para decidir `CREATE_NOW`

Uma Area desta biblioteca só pode ser proposta como `CREATE_NOW` quando todas as condições abaixo forem verdadeiras:

1. existe um Goal atual que exige seu resultado;
2. o trigger do template está presente;
3. o resultado ainda não existe ou perdeu validade;
4. nenhuma Area ativa possui Scope suficiente para produzi-lo;
5. há volume, risco, especialização ou foco que justifique ownership próprio;
6. existem budget e autoridade para iniciar;
7. as dependências críticas estão disponíveis ou podem ser resolvidas no ciclo;
8. a criação respeita os critérios estruturais de `COMPANY_STRUCTURE.md`.

Se o item 4 for falso, use `ABSORBED`. Se os itens 6 ou 7 forem falsos, use `BLOCKED` ou `PREPARE_NEXT`. Se o resultado já existir e estiver válido, use `COMPLETE`.

## 7. Uso durante o Company Start

O CEO deve produzir dois artefatos antes de propor Areas.

### 7.1 Business Stage Assessment

```yaml
business_stage_assessment:
  evidence_cutoff: "{{timestamp}}"
  main_goal: "{{goal_id}}"
  current_moment: "FOUNDATION | DISCOVERY | VALIDATION | SCALE | MIXED"
  current_bottleneck: "{{bottleneck}}"
  capabilities_already_present: "{{capabilities_and_evidence}}"
  active_uncertainties: "{{uncertainties}}"
  constraints: "{{constraints}}"
  confidence: "LOW | MEDIUM | HIGH"
```

Quando faltarem dados, declare `LOW` confidence e proponha a menor Area capaz de produzir evidência. Não simule precisão.

### 7.2 Area Activation Plan

Avalie todos os templates sem criar todos eles:

```yaml
area_activation_plan:
  - template: "{{template_name}}"
    status: "CREATE_NOW | PREPARE_NEXT | ABSORBED | COMPLETE | LATER | SKIP | BLOCKED"
    evidence: "{{evidence}}"
    linked_goal: "{{goal_id_or_none}}"
    covered_by: "{{existing_area_or_none}}"
    trigger_to_reassess: "{{event_or_condition}}"
    dependencies: "{{dependencies}}"
    rationale: "{{short_reason}}"
```

Somente itens `CREATE_NOW` avançam para Area Candidates no Company Implementation Plan. Os demais ficam registrados em Company Data para revisão futura.

## 8. Revisão contínua

O CEO reavalia a biblioteca quando:

- um Goal é criado, alterado, concluído ou removido;
- um MVP ou Scale Cycle termina;
- evidências alteram a confiança em mercado, valor ou modelo;
- surge nova geografia, produto, segmento ou canal;
- uma Area registra lacuna recorrente fora de seu Scope;
- Learning propõe mudança estrutural;
- budget, risco ou autoridade mudam materialmente;
- ocorre revisão periódica definida pela Company.

A reavaliação produz um novo Area Activation Plan. Ela não cria, divide, combina, pausa ou encerra Areas sem o processo de decisão e aprovação definido em `COMPANY_STRUCTURE.md` e `STANDARD_GUARDRAILS.md`.

## 9. Extensão da biblioteca

A Company pode propor novos templates além dos quinze iniciais quando existir uma capacidade de negócio recorrente não representada.

Um novo template deve declarar:

- nome e propósito;
- momento de uso;
- triggers de criação;
- pré-condições;
- resultados esperados;
- forma típica;
- critérios para não criar;
- relação com templates existentes;
- evidências que justificam sua inclusão;
- aprovação e versão.

Adicionar um template à biblioteca não cria automaticamente uma Area em nenhuma Company.
