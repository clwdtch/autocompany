# Expansion Rules

**Versão:** 2.0  
**Finalidade:** definir quando e como o CEO pode propor a criação de novos Loops conforme a Company evolui.

## 1. Fronteira dos documentos

- `LOOP_LIBRARY.md` contém somente o catálogo de Loops disponíveis.
- `EXPANSION_RULES.md` define quando um Loop do catálogo deve ser criado, adiado, absorvido ou descartado.
- `COMPANY_STRUCTURE.md` define como um Loop aprovado é formado, opera, evolui e se relaciona com a Company.

Este documento não descreve a operação interna dos Loops e não duplica o catálogo.

## 2. Princípio de expansão progressiva

A Company deve começar com a menor quantidade de Loops capaz de sustentar o Main Goal e o MVA.

O CEO não deve:

- transformar toda a Loop Library em organograma;
- criar um Loop apenas porque ele representa a próxima etapa aparente;
- antecipar Project, Goal, agentes, budget ou heartbeat para capacidade futura;
- duplicar responsabilidade já coberta por um Loop ativo;
- interpretar a ordem da biblioteca como sequência rígida.

O CEO deve expandir a estrutura somente quando Goals, evidências, volume, risco ou especialização demonstrarem necessidade atual.

## 3. Momentos de avaliação

O CEO avalia a necessidade de novos Loops:

- durante o Company Start;
- quando um Goal é criado ou alterado;
- quando um Loop conclui seu objetivo;
- quando um aprendizado identifica uma capacidade ausente;
- quando a Company inicia uma nova etapa de descoberta, validação, estruturação ou escala;
- quando entra em novo produto, mercado, segmento, geografia ou canal;
- quando uma revisão periódica da estrutura é acionada.

A avaliação não autoriza criação automática. Ela produz um Loop Activation Plan sujeito aos approvals aplicáveis.

## 4. Inputs da avaliação

Antes de propor expansão, o CEO deve consultar:

- Company Description;
- Main Goal, Goal Tree e métricas;
- Goals & Guardrails;
- estado e Scope dos Loops atuais;
- Business Stage Assessment vigente;
- Loop Activation Plan vigente;
- evidências e aprendizados acumulados;
- produtos, clientes, mercados, canais e localidades conhecidos;
- capacidade operacional, budget e restrições;
- `LOOP_LIBRARY.md` na versão fixada pelo Source Manifest.

Informações desconhecidas devem ser registradas como hipóteses ou lacunas, não inventadas como fatos.

## 5. Business Stage Assessment

O CEO identifica o momento e o gargalo atuais antes de consultar candidatas.

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

Quando a confiança for `LOW`, o CEO propõe a menor estrutura capaz de produzir a evidência ausente. Não presume que a Company está pronta para uma etapa posterior.

Os momentos podem se sobrepor. Uma Company pode retornar à descoberta ao lançar um produto novo e pode crescer sem captar investimento.

## 6. Status de avaliação

Cada Loop da biblioteca recebe um status:

| Status | Significado | Efeito |
|---|---|---|
| `CREATE_NOW` | A capacidade é necessária no horizonte atual e não está coberta | Propor Loop no Company Implementation Plan |
| `PREPARE_NEXT` | A capacidade provavelmente será necessária em seguida | Registrar trigger e dependências; não criar estrutura |
| `ABSORBED` | Um Loop existente já cobre a capacidade | Registrar o Loop responsável |
| `COMPLETE` | O resultado necessário já existe e continua válido | Referenciar evidências; não recriar o Loop |
| `LATER` | O momento ainda não chegou ou faltam pré-condições | Manter no roadmap sem recursos operacionais |
| `SKIP` | A capacidade não se aplica ao modelo ou ao Goal | Registrar justificativa curta |
| `BLOCKED` | A capacidade é necessária agora, mas existe impedimento material | Registrar blocker e escalar |

Somente `CREATE_NOW` pode avançar para Loop Candidate.

## 7. Critérios para `CREATE_NOW`

Uma candidata só recebe `CREATE_NOW` quando todas as condições abaixo forem verdadeiras:

1. existe um Goal atual que exige seu resultado;
2. a capacidade é necessária no horizonte atual;
3. o resultado ainda não existe ou perdeu validade;
4. nenhum Loop ativo possui Scope suficiente para produzi-lo;
5. há volume, risco, especialização ou foco que justifique ownership próprio;
6. o resultado pode ser medido ou verificado;
7. existem autoridade e budget para iniciar;
8. dependências críticas estão disponíveis ou podem ser resolvidas no ciclo;
9. a separação satisfaz os critérios de formação de `COMPANY_STRUCTURE.md`.

Se a condição 4 for falsa, use `ABSORBED`. Se a capacidade for provável, mas ainda não atual, use `PREPARE_NEXT`. Se faltarem recursos ou dependências materiais, use `BLOCKED` ou `LATER` conforme urgência.

## 8. Loop Activation Plan

O CEO avalia todas as entradas da Loop Library sem instanciá-las automaticamente.

```yaml
loop_activation_plan:
  library_version: "{{version}}"
  assessment_id: "{{business_stage_assessment_id}}"
  evaluated_at: "{{timestamp}}"
  loops:
    - library_loop: "{{loop_name}}"
      status: "CREATE_NOW | PREPARE_NEXT | ABSORBED | COMPLETE | LATER | SKIP | BLOCKED"
      evidence: "{{evidence}}"
      linked_goal: "{{goal_id_or_none}}"
      covered_by: "{{existing_loop_or_none}}"
      dependencies: "{{dependencies}}"
      trigger_to_reassess: "{{event_or_condition}}"
      rationale: "{{short_reason}}"
```

O plano é armazenado em Company Data. Itens que não estejam em `CREATE_NOW` não recebem estrutura operacional.

## 9. Do candidato ao Loop aprovado

Para cada item `CREATE_NOW`, o CEO produz um Loop Candidate com:

- Loop da biblioteca ou justificativa de Loop customizado;
- evidências e trigger de ativação;
- Purpose;
- Scope e Out of Scope;
- Goals e métricas;
- dependências;
- guardrails e decision rights;
- dados, skills, ferramentas e budget necessários;
- responsável proposto;
- razão para existir separadamente;
- riscos e rollback;
- aprovação necessária.

O Loop Candidate é validado contra `COMPANY_STRUCTURE.md` e `STANDARD_GUARDRAILS.md`. Somente um Loop Candidate aprovado pode ser implementado.

## 10. Ordenação e dependências

O CEO prioriza candidatas por:

1. relação com o Main Goal;
2. urgência do gargalo;
3. redução de incerteza;
4. dependências desbloqueadas;
5. risco de não agir;
6. custo e reversibilidade;
7. capacidade disponível.

A posição de um Loop na biblioteca não supera essas condições. Loops podem ser ativados fora da ordem quando o contexto justificar e as dependências estiverem documentadas.

## 11. Reavaliação

O Loop Activation Plan deve ser revisto quando:

- o Business Stage Assessment mudar;
- um Goal for criado, alterado, concluído ou removido;
- um MVP ou Scale Cycle terminar;
- novas evidências alterarem mercado, valor, modelo ou capacidade;
- um Loop registrar lacuna recorrente fora de seu Scope;
- Learning propor mudança estrutural;
- budget, risco ou autoridade mudarem materialmente;
- ocorrer a cadência de revisão definida pela Company.

A revisão pode mudar o status de um candidato. Ela não cria, divide, combina, pausa ou encerra Loops sem decisão e aprovação registradas.

## 12. Loops fora da biblioteca

O CEO pode propor um Loop customizado quando uma capacidade necessária ao Main Goal não estiver representada em `LOOP_LIBRARY.md`.

A proposta deve explicar:

- por que nenhum Loop existente cobre a capacidade;
- qual Goal exige o novo Loop;
- evidências, Scope e resultado esperado;
- se a necessidade é específica da Company ou reutilizável;
- riscos de duplicação;
- approval necessário.

Um Loop customizado aprovado pode operar na Company sem alterar a biblioteca fonte.

## 13. Evolução da Loop Library

Adicionar uma nova entrada ao repo exige proposta versionada com:

- nome e descrição;
- grupo ou momento predominante;
- distinção em relação às entradas existentes;
- casos de uso observados em uma ou mais Companies;
- risco de sobreposição;
- aprovação do mantenedor do padrão.

Adicionar uma entrada à Loop Library não cria automaticamente um Loop em nenhuma Company existente.
