# TODO: Metodologias e Tópicos Arquiteturais Avançados (Enterprise/Missão Crítica)

Este arquivo consolida a lista de melhorias e tópicos avançados que podem ser adicionados futuramente às metodologias da Skill para elevar o nível da documentação gerada para projetos de grande porte.

## 1. Domain-Driven Design (DDD)
- [ ] **Classificação de Subdomínios (Domain Types):**
  - Mapear explicitamente se cada Bounded Context é *Core Domain* (coração do negócio/customizado), *Supporting Domain* (auxiliar/customizado) ou *Generic Domain* (genérico/pronto para uso/SaaS).
- [ ] **Tipagem de Relacionamento (Context Mapping):**
  - Definir e detalhar padrões de integração de comunicação entre contextos (ex: *Shared Kernel*, *Customer-Supplier*, *Conformist*, *Anti-Corruption Layer (ACL)*).

## 2. CQRS & Modelagem de Dados
- [ ] **Estratégia de Migração de Dados (Schema Migrations):**
  - Detalhar a estratégia de atualização estrutural e migração física do banco de dados (ex: migrações seguras, compatibilidade retroativa e planos de rollback/zero-downtime).

## 3. SDD & Clean Architecture
- [ ] **Aspectos Transversais (Cross-Cutting Concerns):**
  - Adicionar seções para padronizar o comportamento de segurança/autenticação, logs/auditoria, e métricas/observabilidade (telemetria) atravessando as camadas físicas da aplicação.

## 4. EDD (Event-Driven Design)
- [ ] **Resiliência e Idempotência:**
  - Definir tratamentos para entrega de mensagens *at-least-once*, controle de idempotência nos consumidores, retry loops e gerenciamento de falhas via *Dead Letter Queues (DLQ)*.
- [ ] **Serialização de Eventos e Contratos:**
  - Especificar os formatos de transmissão e protocolos de serialização dos eventos (ex: Avro, Protobuf, JSON Schema) e o respectivo versionamento de contratos para evitar quebras.

## 5. SEO & Marketing (Fase 13 - Sumário Executivo & Pitch)
- [ ] **Especificação de SEO e Metadados (SEO & Metadata Plan):**
  - Criar um artefato bônus automático (ex: `98.03_seo_metadata_plan.md`) gerado opcionalmente na Fase 13. Ele definirá a estratégia de indexabilidade do produto, mapeando meta tags (Title, Description, OpenGraph), dados estruturados (JSON-LD/Schema.org), hierarquia semântica de headings (H1-H3) e diretivas de rastreamento (sitemaps, robots.txt) caso a plataforma alvo seja voltada para a web pública.

## 6. Observabilidade Distribuída (Fase 08 - EDD)
- [ ] **Rastreabilidade e Correlation IDs:**
  - Adicionar o desenho de tracing distribuído nos fluxos lógicos assíncronos, especificando como os Correlation IDs serão propagados entre microsserviços/workers para auditoria e depuração de erros.

## 7. Ideias Futuras / Possibilidades (Talvez)
> [!NOTE]
> Os tópicos abaixo descem a um nível de detalhe e granularidade técnica muito alto. Devem ser considerados com cautela (Backlog "Icebox") para não sobrecarregar ou engessar o fluxo de planejamento de alto nível da Skill.

- [ ] **Estratégia de Multi-Tenancy (CQRS/Data):** Mapear se a solução isolará inquilinos (tenants) via coluna (ID), schemas lógicos segregados ou bancos de dados físicos independentes.
- [ ] **Testes de Mutação e SLAs de Latência (TDD):** Adicionar diretrizes conceituais para testar a eficácia real dos asserts dos testes de unidade e regras para falhar a suíte se limiares de throughput/latência forem estourados.
- [ ] **Testes de A11y Automatizados (TDD/UI):** Integrar checagens automáticas de acessibilidade (ex: axe-core) à suíte de testes do frontend para conformidade legal (WCAG).
- [ ] **Continuidade e Tolerância a Desastres (SDD/Legal):** Planejar e documentar metas de RTO (Recovery Time Objective) e RPO (Recovery Point Objective) para infraestrutura e banco.

