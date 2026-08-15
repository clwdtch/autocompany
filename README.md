# Autocompany

Blueprint genérico para iniciar uma empresa com **Minimum Viable Autonomy (MVA)** no Paperclip.

O repositório contém o padrão-fonte da organização. Cada Company criada a partir dele mantém seu próprio estado, dados, objetivos, guardrails, agentes e aprendizados.

## Minimum Viable Autonomy

MVA é a composição mínima necessária para que uma empresa possua um grau inicial de autonomia e autoaprendizado. O modelo exige quatro capacidades:

1. **Orientação a objetivos:** objetivos e guardrails deixam de existir apenas na cabeça do founder e passam a estar registrados e acessíveis aos agentes.
2. **Base de conhecimento e agentes unificados:** documentos, dados, instruções e skills possuem fontes conhecidas e compartilhadas.
3. **Inteligência separada de execução:** a empresa distingue coleta, análise, propostas e definição do trabalho que executa as decisões.
4. **Loop de aprendizado:** os resultados da execução são avaliados e transformados em aprendizados que alimentam os ciclos seguintes.

O MVA é um ponto de partida. O usuário pode posteriormente adicionar Áreas, agentes especializados, automações, skills, integrações, squads e controles mais sofisticados.

## Documentos do padrão

| Documento | Função |
|---|---|
| [`COMPANY_START.md`](./COMPANY_START.md) | Entry point executado pelo CEO para planejar, implementar, validar e ativar a Company |
| [`COMPANY_STRUCTURE.md`](./COMPANY_STRUCTURE.md) | Estrutura organizacional, dados, agentes, fluxos e critérios do MVA |
| [`AGENTS_CREATION_INSTRUCTIONS.md`](./AGENTS_CREATION_INSTRUCTIONS.md) | Regras e templates para criar instruções enxutas para cada agente |
| [`STANDARD_GUARDRAILS.md`](./STANDARD_GUARDRAILS.md) | Proteções mínimas aplicáveis à Company e aos agentes |
| [`EXPANSION_RULES.md`](./EXPANSION_RULES.md) | Regras usadas pelo CEO para decidir quando propor e ativar novas Areas |
| [`AREA_LIBRARY.md`](./AREA_LIBRARY.md) | Catálogo das Areas de negócio disponíveis |

`Plugin Base` e outras integrações são extensões opcionais. A implantação inicial do MVA não pode depender delas.

## Estado-fonte versus estado da Company

- **Repo:** contém o padrão reutilizável.
- **Company Data:** contém documentos e configurações exclusivos da Company.
- **Area Data:** contém configurações, dados, arquivos, resultados e aprendizados exclusivos de uma Área.

Uma Company deve registrar a URL, branch, commit e versão do padrão utilizado. Atualizações do repo não alteram silenciosamente Companies já implantadas.

## Como iniciar no Paperclip

1. Crie uma Company no Paperclip.
2. Informe nome, descrição inicial e Main Goal.
3. Crie ou conecte um CEO genérico com acesso de leitura ao commit aprovado deste repo.
4. Atribua ao CEO uma task em modo de planejamento.
5. Use uma instrução semelhante à abaixo:

```markdown
# Start Company

Inicialize esta Company seguindo integralmente o documento:

https://github.com/clwdtch/autocompany/blob/<COMMIT>/COMPANY_START.md

Use exclusivamente o commit informado.
Comece em modo PLAN.
Não aplique mudanças antes da aprovação do Company Implementation Plan.
Após a aprovação, implemente e valide o Minimum Viable Autonomy descrito no padrão.
```

Substitua `<COMMIT>` por um SHA aprovado. Não use automaticamente a versão mais recente de `main` em uma Company operacional.

## Inputs mínimos do usuário

O CEO pode gerar os demais documentos durante o boot, mas precisa receber ou localizar:

- nome da Company;
- descrição inicial do que ela faz ou pretende fazer;
- Main Goal e, quando disponíveis, métricas de sucesso;
- identidade da autoridade humana responsável;
- orçamento inicial ou limite de custo;
- restrições e aprovações adicionais conhecidas.

Se nome, descrição, Main Goal ou autoridade humana estiverem ausentes, o CEO deve interromper o boot e solicitá-los. Os demais campos podem começar com defaults conservadores documentados e sujeitos à aprovação.

## Resultado esperado

Ao final do boot, a Company deve possuir:

- Goals & Guardrails acessíveis aos agentes;
- Company Data instanciado;
- CEO com instruções operacionais enxutas;
- Business Stage Assessment e Area Activation Plan;
- pelo menos uma Área necessária ao Main Goal;
- Area Data para cada Área;
- times mínimos de inteligência e execução;
- um Area Loop rastreável;
- humano no circuito de aprovação;
- budgets, permissões e heartbeats definidos;
- Company Start Report;
- estado `OPERATIONAL` ou bloqueio claramente registrado.

## Princípio de implementação

> O CEO não inventa uma empresa a partir de um prompt vago. Ele instancia um padrão, propõe a configuração específica, obtém as aprovações necessárias, implementa o estado aprovado e valida o resultado.
