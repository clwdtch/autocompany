# Area Library

**Versão:** 2.0  
**Finalidade:** catálogo de Areas disponíveis para criação pela Company.

## Business Foundation and Evolution

| Title | Scope | Prerequisite |
|---|---|---|
| Agents Setup | Implantação e evolução da infraestrutura, modelos, ferramentas, skills, integrações, segurança e observabilidade dos agentes. | Nenhuma Area. Iniciar durante o bootstrap, antes da criação dos demais agentes operacionais. |
| Goals | Definição e manutenção do Main Goal, subgoals, prioridades, métricas e horizontes da Company. | CEO configurado, Company Description, Main Goal inicial e responsável humano definidos. |
| Concepts | Transformação de problemas, oportunidades e intenções em conceitos de negócio investigáveis. | `Goals`. Iniciar quando existir uma oportunidade ou problema ainda não estruturado. |
| Market | Investigação de mercados, segmentos, clientes, demanda, canais e contexto competitivo. | `Concepts`. Iniciar quando existir pelo menos um conceito a ser avaliado. |
| Benchmarking | Análise de concorrentes, alternativas, referências e práticas comparáveis. | `Concepts` e delimitação inicial de `Market`. |
| Customer Research | Coleta e análise de evidências diretamente com clientes e usuários potenciais. | `Market`. Iniciar quando segmentos estiverem identificados e ainda houver hipóteses críticas sobre necessidades ou comportamentos. |
| Value | Definição e validação do valor produzido para clientes, usuários e demais stakeholders. | `Market` e evidências de `Customer Research` ou fontes equivalentes. |
| Metrics | Definição, instrumentação e manutenção das métricas utilizadas para decidir e aprender. | `Goals`. Iniciar antes do primeiro experimento ou operação cujo resultado precise ser medido. |
| MVP | Criação da menor solução ou experimento capaz de reduzir as principais incertezas do negócio. | `Value`, segmento-alvo e critérios de sucesso definidos em `Metrics`. |
| Model | Estruturação de como a Company cria, entrega e captura valor de forma sustentável. | `Value` com evidência suficiente para formular hipóteses de receita, custos e entrega. |
| Software | Construção e evolução de software necessário ao produto ou à operação. | Necessidade validada por `MVP` ou por processo operacional recorrente; iniciar quando software for a resposta justificada. |
| Branding | Construção de posicionamento, narrativa, identidade e princípios de aplicação da marca. | `Value` e público-alvo definidos; iniciar antes de comunicação externa recorrente. |
| Scale Cycles | Execução de ciclos controlados para testar repetibilidade, capacidade, eficiência e unit economics. | `MVP` ou produto entregando valor, com `Model` e `Metrics` ativos. |
| Fundraise Model | Definição da necessidade de capital, montante, estratégia, instrumento, uso dos recursos e marcos financiáveis. | `Model`, `Metrics` e uma necessidade de capital documentada. |
| Investment | Execução do processo aprovado de obtenção e formalização de investimento. | `Fundraise Model` aprovado, materiais preparados e governança autorizada. |
| Growth | Construção de mecanismos recorrentes de aquisição, ativação, retenção, expansão e receita. | `Scale Cycles` com pelo menos um ciclo bem-sucedido, capacidade operacional e unit economics aceitáveis. |

## Product and Technology

| Title | Scope | Prerequisite |
|---|---|---|
| Product | Evolução contínua da oferta, experiência, roadmap e resultados do produto. | `MVP` validado e existência de usuários, operação ou roadmap recorrente. |
| Product Discovery | Investigação contínua de necessidades, problemas, oportunidades e soluções para o produto. | `Product` ou `MVP` ativo, com incertezas recorrentes sobre o que desenvolver. |
| Product Delivery | Planejamento e entrega contínua das evoluções aprovadas do produto. | `Product` ativo e volume recorrente de releases ou mudanças que justifique um loop próprio. |
| Data & Analytics | Organização de dados, modelos analíticos, dashboards e evidências para decisões. | `Metrics` ativo e múltiplas fontes ou decisões recorrentes dependentes de dados. |
| AI Systems | Desenvolvimento e evolução dos sistemas de IA utilizados pelo produto ou pela operação. | `Agents Setup`, `Software` ou `Product`; iniciar quando IA for uma capacidade central, recorrente e mensurável. |
| Reliability & Infrastructure | Disponibilidade, desempenho, infraestrutura, incidentes e continuidade dos sistemas. | `Software` em produção e impacto material de falhas, custos ou indisponibilidade. |

## Marketing

| Title | Scope | Prerequisite |
|---|---|---|
| Marketing | Estratégia e operação geral de posicionamento, comunicação, demanda e aquisição. | `Market`, `Value` e goals comerciais definidos. |
| Content Marketing | Produção e distribuição de conteúdo para educação, autoridade, descoberta e conversão. | Estratégia de `Marketing` definida e conteúdo identificado como canal recorrente. |
| Social Media | Estratégia e operação da presença da Company em redes sociais. | Estratégia de `Marketing`, público presente em redes sociais e objetivos específicos para esses canais. |
| Instagram | Crescimento, relacionamento e conversão por meio do Instagram. | Estratégia de `Social Media` ou `Marketing` seleciona Instagram e o canal possui volume suficiente para goals próprios. |
| Instagram Carousels | Produção, publicação e otimização de carrosséis no Instagram. | `Instagram` ativo e carrosséis com demanda recorrente, métricas próprias ou volume que justifique separação. |
| Instagram Images | Produção e otimização de publicações estáticas com imagens no Instagram. | `Instagram` ativo e publicações estáticas representando uma operação recorrente e mensurável. |
| Instagram Videos | Produção, publicação e otimização de vídeos no Instagram. | `Instagram` ativo e vídeo escolhido como formato recorrente e mensurável. |
| Instagram Testimonial Videos | Produção de vídeos com depoimentos, casos e evidências de clientes. | `Instagram Videos`, clientes com resultados comprováveis, autorização de uso e volume recorrente. |
| Instagram News Videos | Curadoria, produção e publicação de vídeos de notícias relevantes para o público da Company. | `Instagram Videos`, tese editorial, fontes confiáveis, frequência definida e relevância estratégica. |
| Paid Acquisition | Aquisição de clientes por mídia paga em diferentes plataformas. | Oferta validada, destino de conversão, tracking, orçamento e capacidade de atendimento. |
| Meta Ads | Planejamento e otimização de campanhas pagas no ecossistema Meta. | `Paid Acquisition` aprovado e Meta selecionada como canal com orçamento e volume próprios. |
| Landing Page Optimization | Experimentação contínua para melhorar conversão em páginas de aquisição. | Tráfego recorrente, conversões instrumentadas e volume suficiente para experimentos. |

## Sales and Customer

| Title | Scope | Prerequisite |
|---|---|---|
| Sales | Estruturação e operação geral da conversão de oportunidades em clientes. | `Value`, ICP, oferta e condições comerciais minimamente definidos. |
| Inbound Sales | Conversão de leads originados por marketing, conteúdo, indicações ou demanda espontânea. | `Sales` e entrada recorrente de leads inbound. |
| Outbound Sales | Prospecção ativa, qualificação e conversão de potenciais clientes. | `Sales`, ICP, fonte de contatos, abordagem e oferta testável. |
| Revenue Operations | Integração entre Marketing, Sales e Customer Success, incluindo processos, dados e handoffs. | Marketing, Sales e Customer Success operando com volume e complexidade suficientes para exigir coordenação própria. |
| Customer Onboarding | Ativação inicial e condução dos clientes até o primeiro resultado relevante. | Primeiros clientes e processo de entrada repetido mais de uma vez. |
| Customer Support | Resolução de dúvidas, solicitações, problemas e incidentes dos clientes. | Base ativa de clientes e demanda recorrente de atendimento. |
| Customer Success | Acompanhamento dos resultados, adoção, satisfação, renovação e expansão dos clientes. | Relação contínua com clientes e resultado posterior à venda relevante para receita ou retenção. |
| Retention | Investigação e melhoria contínua de recorrência, engajamento, renovação e churn. | `Metrics`, coortes de clientes e evidência de que retenção afeta materialmente os Goals. |

## Operations and Expansion

| Title | Scope | Prerequisite |
|---|---|---|
| Business Operations | Processos operacionais, handoffs, capacidade, eficiência e coordenação entre Areas. | Processos recorrentes atravessando duas ou mais Areas ou criando gargalos operacionais. |
| Finance | Fluxo financeiro, orçamento, caixa, pagamentos, recebimentos, contabilidade e relatórios. | Movimentações financeiras recorrentes ou obrigações fiscais e contábeis. |
| Legal & Compliance | Contratos, obrigações regulatórias, propriedade intelectual e conformidade. | Exposição contratual, regulatória, trabalhista, societária ou de dados material. |
| Security & Privacy | Proteção de sistemas, informações, acessos, dados pessoais e resposta a incidentes. | Tratamento de dados sensíveis, sistemas em produção, integrações críticas ou exigência de clientes e reguladores. |
| People Operations | Contratação, integração, desenvolvimento, desempenho e administração de pessoas. | Existência ou contratação planejada de trabalhadores humanos recorrentes. |
| Geographic Expansion | Entrada e adaptação da operação para novas cidades, regiões ou países. | `Scale Cycles` concluídos no mercado atual, operação estável e evidência de oportunidade no novo território. |
