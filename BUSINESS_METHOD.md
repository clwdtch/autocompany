# Business Method

**Versão:** 1.0  
**Finalidade:** transformar Company Description, Goals & Guardrails e contexto operacional em uma estrutura mínima e evolutiva de Áreas.

## 1. Princípio

Uma Área é uma unidade de responsabilidade que possui:

- propósito e escopo próprios;
- objetivos ligados ao Main Goal;
- dados e arquivos próprios;
- capacidade de inteligência;
- capacidade de execução;
- loop de aprendizado.

O método é agnóstico de setor e granularidade. Uma Área pode representar:

- uma função ampla, como Marketing ou Jurídico;
- uma unidade de negócio, produto, mercado ou localização;
- um processo, como análise de contratos de fornecedores;
- um resultado específico, como vídeos de notícias para uma conta de Instagram;
- uma capacidade temporária necessária a um objetivo.

O nome da Área é apenas um rótulo. O que determina sua atuação é o `Area Settings`, especialmente Scope & Goals.

## 2. Objetivo do método

O CEO utiliza este documento para:

1. propor as Áreas iniciais durante o Company Start;
2. criar novas Áreas quando surgir necessidade comprovada;
3. ajustar granularidade conforme frequência, complexidade e aprendizado;
4. evitar sobreposição, lacunas e estruturas desnecessárias;
5. manter cada Área ligada aos objetivos da Company.

## 3. Inputs

Antes de propor Áreas, o CEO deve utilizar:

- Company Description;
- Main Goal, demais Goals e métricas;
- Standard e Company Guardrails;
- restrições, budget e horizonte temporal;
- produtos, serviços, clientes, canais e localidades conhecidos;
- processos e capacidades já existentes;
- dados, documentos e evidências disponíveis;
- Áreas atuais e seus resultados;
- aprendizados acumulados.

Durante o primeiro boot, informações desconhecidas devem ser registradas como hipóteses ou pendências, não inventadas como fatos.

## 4. Regra de mínimo

O CEO deve propor a **menor estrutura de Áreas capaz de sustentar o Main Goal e o MVA**.

Não crie uma Área apenas porque ela existe em organogramas tradicionais. Uma nova Área precisa demonstrar pelo menos um dos seguintes motivos:

- possui objetivo próprio e mensurável;
- exige conhecimento, dados ou guardrails específicos;
- possui trabalho recorrente suficiente;
- requer decision rights distintos;
- apresenta risco que justifica segregação;
- precisa de budget ou responsável próprio;
- a separação reduz conflito ou aumenta clareza de resultado.

Quando dois escopos possuem pouco volume, objetivos muito próximos e os mesmos dados, eles devem começar consolidados.

## 5. Processo para definir as Áreas iniciais

### Etapa 1 — Interpretar o Main Goal

Descreva:

- resultado pretendido;
- beneficiários ou clientes;
- valor produzido;
- horizonte temporal;
- métricas conhecidas;
- restrições e riscos;
- capacidades necessárias.

### Etapa 2 — Identificar resultados intermediários

Que resultados precisam permanecer verdadeiros para que o Main Goal seja atingido?

Exemplos de dimensões de investigação, sem obrigação de criar uma Área para cada uma:

- entendimento de mercado e clientes;
- criação e evolução da oferta;
- aquisição, relacionamento e receita;
- entrega e operações;
- tecnologia, dados e segurança;
- finanças e alocação de recursos;
- pessoas, parceiros e fornecedores;
- governança, risco e conformidade.

Essas dimensões servem para encontrar lacunas. Elas não são um organograma obrigatório.

### Etapa 3 — Agrupar responsabilidades

Agrupe resultados que compartilham:

- objetivo;
- dados;
- stakeholders;
- ferramentas;
- cadence de decisão;
- tipo de execução;
- guardrails.

Cada grupo candidato deve possuir uma fronteira compreensível e uma razão clara para existir.

### Etapa 4 — Escolher a granularidade

Considere dois eixos:

- **Scope:** amplo ou específico;
- **Goals:** abrangentes ou delimitados.

Use uma Área ampla quando:

- o volume inicial é baixo;
- os processos ainda são desconhecidos;
- a Company está aprendendo;
- a separação criaria agentes ociosos;
- os objetivos ainda são fortemente dependentes.

Use uma Área específica quando:

- existe alta frequência de trabalho;
- o resultado pode ser medido isoladamente;
- há dados, skills ou guardrails próprios;
- o escopo amplo está gerando conflito ou baixa qualidade;
- a autonomia local reduz coordenação desnecessária.

### Etapa 5 — Produzir Area Candidates

Para cada candidata, registre:

```yaml
area_candidate:
  name: "{{name}}"
  purpose: "{{why_it_exists}}"
  scope: "{{included_work}}"
  out_of_scope: "{{excluded_work}}"
  goals: "{{goals_linked_to_company}}"
  success_metrics: "{{metrics}}"
  stakeholders: "{{stakeholders}}"
  dependencies: "{{dependencies}}"
  data_needed: "{{data_sources}}"
  guardrails: "{{area_specific_guardrails}}"
  decision_rights: "{{delegated_authority}}"
  initial_budget: "{{budget}}"
  reason_to_be_separate: "{{justification}}"
  merge_or_split_trigger: "{{future_condition}}"
```

### Etapa 6 — Verificar cobertura e sobreposição

O conjunto proposto deve responder:

- Todo objetivo relevante possui um responsável?
- Alguma responsabilidade possui dois donos sem coordenação explícita?
- Há Área sem objetivo mensurável?
- Há Área cujo único motivo é imitar um departamento tradicional?
- Existem dependências cross-area não registradas?
- O conjunto é o menor capaz de operar o MVA?

### Etapa 7 — Solicitar aprovação

Durante o Company Start, o CEO inclui as candidatas no `Company Implementation Plan`.

Depois da ativação, novas Áreas ou mudanças materiais seguem os decision rights da Company e os Standard Guardrails.

## 6. Contrato mínimo da Área

Toda Área aprovada deve possuir `Area Settings`:

```yaml
area:
  id: "{{area_id}}"
  name: "{{area_name}}"
  description: "{{short_description}}"
  purpose: "{{purpose}}"
  scope: "{{scope}}"
  out_of_scope: "{{out_of_scope}}"
  goals: "{{goals}}"
  success_metrics: "{{metrics}}"
  stakeholders: "{{stakeholders}}"
  dependencies: "{{dependencies}}"
  constraints: "{{constraints}}"
  guardrails: "{{guardrails}}"
  decision_rights: "{{decision_rights}}"
  budget: "{{budget}}"
  data_sources: "{{data_sources}}"
  allowed_tools: "{{allowed_tools}}"
  initial_skills: "{{skills}}"
  review_cadence: "{{cadence}}"
  split_merge_pause_triggers: "{{triggers}}"
  version: "{{version}}"
```

Sem Purpose, Scope, Goals, Success Metrics e responsável, a Área permanece em estado `DRAFT`.

## 7. Estrutura mínima interna da Área

Uma Área em estado `ACTIVE` deve implementar as responsabilidades do Area Loop:

1. Data;
2. Analysis;
3. Proposals;
4. Definition;
5. Execution;
6. Learning.

No MVA, as responsabilidades centrais são criadas como agentes persistentes conforme `COMPANY_STRUCTURE.md`. Internal/External Teams, Squad Leaders e Executor Agents podem ser instanciados sob demanda.

## 8. Evolução da granularidade

### Dividir uma Área

Considere divisão quando:

- Scope & Goals deixarem de caber em um contrato claro;
- o Area Leader se tornar gargalo recorrente;
- existirem fluxos com dados, skills ou guardrails muito diferentes;
- conflitos de prioridade se repetirem;
- uma subcapacidade possuir volume e métricas próprios;
- o aprendizado indicar ganho provável de autonomia.

### Combinar Áreas

Considere combinação quando:

- houver duplicação de agentes e dados;
- os objetivos se tornarem inseparáveis;
- o volume não justificar estruturas distintas;
- handoffs criarem mais custo do que valor;
- as Áreas usarem as mesmas decisões, skills e stakeholders.

### Pausar ou encerrar

Considere pausa ou encerramento quando:

- o objetivo for concluído ou removido;
- não houver mais trabalho recorrente;
- a Área deixar de contribuir ao Main Goal;
- o custo superar o valor;
- suas responsabilidades forem absorvidas por outra Área.

Dados, decisões e aprendizados devem ser preservados conforme a política de retenção.

## 9. Criação de novas Áreas por aprendizado

O Learning Agent pode propor uma nova Área, divisão ou combinação. A proposta deve incluir:

- evidências observadas;
- problema da estrutura atual;
- resultado esperado;
- custo e novos agentes;
- impacto em goals, budgets e dependências;
- alternativa de não mudar;
- plano de migração;
- aprovação necessária.

O Learning Agent não aplica a mudança autonomamente.

## 10. Exemplos de granularidade

Uma Company pode evoluir assim:

```text
Marketing
└── Redes Sociais
    └── Instagram
        ├── Carrossel
        ├── Imagens
        └── Vídeos
            ├── Vídeos de depoimentos
            └── Vídeos de notícias
```

O método não exige criar toda essa árvore. A Company começa no nível mínimo útil e cria novas Áreas somente quando objetivos, volume, risco ou aprendizado justificarem.

