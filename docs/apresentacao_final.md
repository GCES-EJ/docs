


# 📝 Relatório Final – GCES 2025.2

**Disciplina:** Gerência de Configuração e Evolução de Software  
**Equipe:** Empurrando Juntas  
**Comunidade/Projeto de Software Livre:** Empurrando Juntas (EJ)  
**Período:** Agosto – Dezembro/2025

---

## 1. Resumo Geral do Projeto

### 1.1 Visão Quantitativa (a partir dos diários)

Com base **exclusivamente nos diários de bordo individuais da equipe**, foi possível identificar, ao longo das sprints:

- **Issues formais mencionadas com número:**  
  - Pelo menos **16 issues distintas**:  
    - `#45`, `#47`, `#50`, `#51`, `#52`, `#53`, `#54`, `#59`, `#60`, `#61`, `#64`, `#65`, `#67`, `#68`, `#69`, `#77`.   

- **Merge Requests (MRs) mencionados diretamente nos diários:**
  - Pelo menos **9 MRs** com número/link explícito:  
    - `MR #26`, `MR #27`, `MR #30`, `MR #33`, `MR #35`, `MR #36`, `MR #41`, `MR #42`, `MR #44`.   

> Essas quantidades são **mínimas**, pois muitos commits e revisões não aparecem com número detalhado nos diários. Ou seja: a equipe provavelmente fez **mais issues/MRs** do que as listadas aqui — mas estamos usando apenas o que está documentado oficialmente nos arquivos `.md`.

---

## 1.2 Resumo por Sprint

### Sprint 0 (25/08 – 10/09)

**Foco:** Ambientação, configuração de ambiente e estudo da documentação.

**Issues Planejadas:**
- Nenhuma issue formal com número foi registrada nos diários para esta sprint (fase predominantemente de estudo).
- Atividades principais:
  - Configuração de ambiente local (Docker, WSL, venv).
  - Leitura da documentação do projeto e guias de contribuição.
  - Estudos de arquitetura geral.   

**Issues Executadas:**
- Correções de ambiente e primeiros ajustes locais.
- Nenhuma issue numerada citada (trabalho preparatório).

**PRs/MRs Submetidos e Aceitos:**
- Nenhum MR numerado explicitamente para esta sprint.

---

### Sprint 1 (11/09 – 24/09)

**Foco:** Pipeline, primeiras contribuições, estabilização do projeto e documentação das rotas de users.

**Issues Planejadas:**
- Investigar e corrigir a falha do pipeline de CI/CD.
- Identificar primeiros pontos de contribuição (bugs simples, erros sintáticos, etc.).

**Issues Executadas (mínimo identificado):**
- **Issue #44 - Quality gate de cobertura no MR (job test-coverage, mínimo 85%)** – Implementação de cobertura de testes no pipeline (Victor Pontual)
- **Issue #50 – Falha no pipeline de CI/CD** (diagnosticada e detalhada por Yan e Felipe).   
- **Issue de erro sintático** (sem número nos diários, mas criada e corrigida por João Filipe). :contentReference[oaicite:4]{index=4}  
- **Issue #47 – Validação de senha forte** (implementação da regra de senha forte por Caio). :contentReference[oaicite:5]{index=5}
- **Issue #45 – Documentar endpoints do ej_users** (documentada por João Carvalho).   
- **Issue #48 – botão de visualizar senha na tela de login** (Implentado por Marco Tulio Soares).   

➡ **Pelo menos 5 issues trabalhadas na Sprint 1**, sendo 4 numeradas (#44, #45, #47, #50, #48).

**PRs/MRs Submetidos e Aceitos (mínimo identificado):**
- **MR #26** – Relacionado à documentação/rotas (Letícia). :contentReference[oaicite:6]{index=6}  
- **MR #27** – Implementação da validação de senha forte (Caio). :contentReference[oaicite:7]{index=7}
- **[MR #29](https://gitlab.com/gces-ej/ej-application/-/merge_requests/29)** – Implementação de test-coverage e correções de CI/CD (Victor Pontual)

➡ **Pelo menos 3 MRs aceitos na Sprint 1**.

---

### Sprint 2 (26/09 – 08/10)

**Foco:** Autenticação, documentação da API e correção de rotas.

**Issues Planejadas:**
- Revisão e melhoria do modelo de autenticação.
- Ajuste da documentação Swagger.
- Correção de rotas e endpoints ausentes.

**Issues Executadas (mínimo identificado):**
- **Issue #52** – Proposta detalhada de nova autenticação (criada por João Filipe). :contentReference[oaicite:8]{index=8}  
- **Issue #51** – Estudo e refino da nova arquitetura de autenticação (citada por Ana Joyce). :contentReference[oaicite:9]{index=9}  
- **Issue #53** – Registro de endpoints faltantes no router (Letícia). :contentReference[oaicite:10]{index=10}  
- **Issue #54** – Remoção de testes obsoletos de Kubernetes e correção de 28 testes (Victor Pontual). :contentReference[oaicite:11]{index=11}  
- **Issue #56** – Implementação CRUD foto de perfil (Marco Tulio Soares).
➡ **Pelo menos 4 issues formais (51, 52, 53, 54,56) trabalhadas na Sprint 2.**

**PRs/MRs Submetidos e Aceitos (mínimo identificado):**
- **MR #30** – Registro de endpoints faltantes (Letícia). :contentReference[oaicite:12]{index=12}  

➡ **Pelo menos 1 MR relacionado à Sprint 2** aparece explicitamente nos diários (há mais commits, mas não numerados como MR nos textos).

---

### Sprint 3 (09/10 – 22/10)

**Foco:** Definição da nova arquitetura de autenticação, CI/CD, início da federação de identidades e correção de rotas administrativas.

**Issues Planejadas:**
- Formalização da nova arquitetura de autenticação.
- Abertura de issues derivadas para implementação incremental.
- Evolução da cobertura e estabilidade do pipeline.

**Issues Executadas (mínimo identificado):**
- **Issue #54** – Continuação da remoção de testes obsoletos k8s (Victor Pontual)
- **Issue #59** – Início da implementação da nova autenticação (aberta por Ana Joyce). :contentReference[oaicite:13]{index=13}
- **Issue #60** – Correção de rotas duplicadas em `admin/administration` (João Carvalho). :contentReference[oaicite:21]{index=21}
- **Issue #61** – Documentação detalhada de endpoints críticos de autenticação e usuários (Letícia). :contentReference[oaicite:14]{index=14} 
- **Issue #62** – Implementação do modo escuro  (Marco Tulio Soares).

➡ **Pelo menos 4 issues formais (54, 59, 60, 61) ligadas à Sprint 3**.

**PRs/MRs Submetidos e Aceitos:**
- **MR #33** – Documentação dos endpoints de autenticação/usuarios (Letícia). :contentReference[oaicite:15]{index=15}  

---

### Sprint 4 (23/10 – 12/11)

**Foco:** Autenticação final, ClientPermission, ApiKeyService, rotas administrativas, testes e qualidade.

**Issues Executadas (mínimo identificado):**
- **Issue #67** – Implementação do modelo `ClientPermission` e interface administrativa (Uires). :contentReference[oaicite:16]{index=16}  
- **Issue #68** – Implementação do `ApiKeyService` e comando de criação de chaves (Uires). :contentReference[oaicite:17]{index=17}  
- **Issue #64** – Refatoração da lógica de clusterização com remoção de "magic numbers" (Victor Câmara). :contentReference[oaicite:18]{index=18}  
- **Issue #77** – Criação do `UserRegistrationService` e redução de “Fat Views” (Victor Câmara). :contentReference[oaicite:19]{index=19}  
- **Issue #69** – Continuidade da autenticação com middleware e unificação de usuários externos (citada em mais de um diário: Ana Joyce e João Filipe).   
- **Issue #65** – Correções de testes de `administration` ligadas às rotas (João Carvalho). :contentReference[oaicite:22]{index=22}
- **Issue #79** – Adicionar ordenação à listagem de conversas por data de criação (Caio Antonio).


➡ **Pelo menos 6 issues formais (64, 65, 67, 68, 69, 77) aparecem associadas à Sprint 4.**

**PRs/MRs Submetidos e Aceitos (mínimo identificado):**
- **MR #35** – Correção de queryset em `apply_board_filters` (João Carvalho). :contentReference[oaicite:23]{index=23}  
- **MR #36** – Finalização da issue de rotas e ajustes em testes (João Carvalho). :contentReference[oaicite:24]{index=24}  
- **MR #41** – Merge da nova arquitetura de autenticação (Ana Joyce / equipe de auth).   
- **MR #42** – Implementação da ordenação das conversas por data de criação (Caio Antonio).

➡ **Pelo menos 4 MRs diretamente associados à Sprint 4.**

---

### Sprint 5 (13/11 – 03/12)

**Foco:** Consolidação, estabilização final do develop, correção de pipeline e fechamento de MRs pendentes. Aumento de cobertura de testes.

**Issues Executadas (mínimo identificado):**
- **Issue #82** – Aumento de cobertura de código do projeto (Victor Pontual, Leticia Arisa)
- Revisão e validação de 100% das rotas da API. :contentReference[oaicite:26]{index=26}  
- Correção de inconsistências na branch `develop` causadas por MRs antigos. :contentReference[oaicite:27]{index=27}  

**PRs/MRs e Commits importantes:**
- Commits de padronização ampla com Black e Ruff e correções de pipeline (`ci: corrige pipeline`, remoção de stages de build e E2E). :contentReference[oaicite:28]{index=28}  
- Aprovação final dos MRs #35 e #36 (João Carvalho). :contentReference[oaicite:29]{index=29}
- **MR #44** – Implementação da funcionalidade de compartilhar link da conversa para área de transferência (Caio Antonio).  

---

## 2. Listagem de Commits, Issues e PRs/MRs por Integrante

> Como não utilizamos comandos Git para contagem exata, os números abaixo são **mínimos**, baseados no que aparece explicitamente nos diários (issues citadas, MRs citados e atividades em par). Os commits não foram contados numericamente nos diários, então a coluna de commits é qualitativa.

| Integrante | Issues trabalhadas (mínimo) | PRs/MRs mencionados (mínimo) | Observação |
|-----------|-----------------------------|------------------------------|-----------|
| **Ana Joyce** | ≥ 3 (`#51`, `#59`, `#69`) :contentReference[oaicite:30]{index=30} | ≥ 1 (`MR #41`) | Forte atuação em pipeline e nova arquitetura de autenticação. |
| **Caio Antonio** | ≥ 1 (`#47`, `#79`, `#83`) | ≥ 2 (`MR #44`, `MR #42`, `MR #31`, `MR #27`) | Melhorias gerais em diferentes áreas do projeto.
| **Danielle Rodrigues** | ≥ 5 (`#51`, `#63`, `#67`, `#68`, `#69`, `#81`) | ≥ 3 (`MR #41`, `MR #43`, MR relacionado a #63) | Arquitetura completa de Federação de Identidades especialmente na parte de APIClient, ClientPermission, ApiKeyService, FederationMiddleware, ExternalUserService e testes de integração. |
| **Felipe Matheus** | ≥ 1 (`#50`) :contentReference[oaicite:33]{index=33} | 0 mencionados diretamente | Diagnóstico da falha do pipeline em par com Yan. |
| **João Antonio Carvalho** | ≥ 3 (`#45`, `#60`, `#65`)  | ≥ 2 (`MR #35`, `MR #36`) | Correção de rotas, ajustes em testes e estabilização do pipeline. |
| **João Filipe** | ≥ 2 (issue de erro sintático sem número + `#51,#52,#59,#69`)  | 0 mencionados diretamente | Atuação na concepção da nova autenticação. |
| **Leticia Arisa** | ≥ 5 (`#46`, `#53`, `#61`, `#66`, `#82`)  | ≥ 5 ( `MR #26`, `MR #30`, `MR #33`, `MR #38`, `MR #45`) | Documentação Swagger, correção de endpoints, otimização de infraestrutura (Docker) e testes unitários. |
| **Marco Soares** | - | - | - |
| **Marco Tulio** | ≥ 3 (`#48`, `#56`, `#62`)| ≥ 3 (`#48`, `#56`, `#62`) | (dark mode, mostrar senha, foto de perfil) |
| **Uires Carlos** | ≥ 2 (`#67`, `#68`) :contentReference[oaicite:37]{index=37} | MRs implícitos ligados às issues, não numerados nos diários | ClientPermission, ApiKeyService, análise SonarQube e refatorações. |
| **Victor Augusto de Sousa Câmara** | ≥ 2 (`#64`, `#77`)  | MRs ligados a essas issues (links via issue, não por número) | Refatorações avançadas (Service Layer, magic numbers). |
| **Victor Pontual Guedes Arruda Nóbrega** | ≥ 3 (`#44`, `#54`, `#82`) | ≥ 3 ([`MR #29`](https://gitlab.com/gces-ej/ej-application/-/merge_requests/29), [`MR #37`](https://gitlab.com/gces-ej/ej-application/-/merge_requests/37), [`MR #45`](https://gitlab.com/gces-ej/ej-application/-/merge_requests/45)) | **Sprint 1**: Pipeline CI/CD completo com test-coverage, 58 erros Ruff corrigidos, 29 arquivos formatados. **Sprint 2-3**: Correção de 28 testes (+36 passando, 85.2%→91.5%), eliminação de 92.5% dos erros. **Sprint 4**: 28 testes FBV→CBV, decorator REST, namespace dinâmico. **Sprint 5**: +8% cobertura (67%→75%), 100% em 4 módulos, 710 linhas de testes. |
| **Yan Guimarães** | ≥ 1 (`#50`, em parceria com Felipe) :contentReference[oaicite:40]{index=40} | 0 MRs numerados nos diários | Diagnóstico de pipeline e apoio em testes. |

> Se a professora pedir **números exatos de commits**, esses dados podem ser obtidos facilmente com `git shortlog` rodando localmente, mas aqui optamos por usar apenas o que está registrado formalmente nos diários de bordo.

---

## 3. Relato das Tomadas de Decisão de Organização da Equipe

- Divisão da equipe em **frentes de trabalho**:
  - Pipeline e CI/CD  
  - Autenticação e segurança  
  - Documentação e Swagger  
  - Rotas/admin e refatoração de arquitetura  

- Decisões estratégicas:
  - Remover dependência de testes E2E que utilizavam infraestrutura externa obsoleta (Pencil). :contentReference[oaicite:41]{index=41}  
  - Adotar **drf-spectacular (Swagger)** como fonte de verdade da API. :contentReference[oaicite:42]{index=42}  
  - Criar um novo modelo de autenticação baseado em:
    - ClientPermission  
    - ApiKeyService  
    - Federação de Identidades / API Keys.   
  - Padronizar tudo com **Black + Ruff**, estabilizando o estilo em todo o projeto.   
  - Estabelecer regra de revisão de MRs (code review obrigatório).

---

## 4. Relato de Eventuais Dificuldades com o Projeto

Principais dificuldades relatadas nos diários:

- **Configuração de ambiente**:
  - Problemas com Python 3.12 vs 3.11.
  - Docker falhando em Windows e necessidade de migrar para WSL.   

- **Pipeline quebrado**:
  - Jobs de CI/CD falhando por:
    - tags de runners obsoletos,
    - `pull_policy` incorreta,
    - testes E2E dependentes de infra externa.   

- **Autenticação complexa e legada**:
  - Dificuldade em entender o modelo de autenticação antigo.
  - Necessidade de conciliar múltiplos padrões (login, tokens, API keys, federação).   

- **Testes automatizados**:
  - Grande volume de testes quebrados (ao menos 28 só na Issue #54). :contentReference[oaicite:48]{index=48}  
  - Complexidade dos erros, especialmente em rotas e migração de CBVs.   

- **Qualidade de código e arquitetura**:
  - Necessidade de refatorar "Fat Views" e remover magic numbers.
  - Ajustar arquitetura sem quebrar comportamento.   

---

## 5. Considerações Finais

Mesmo considerando apenas os dados documentados nos diários:

- Foram trabalhadas **pelo menos 16 issues formais** e **9 MRs numerados**, abrangendo:
  - Autenticação completa,
  - Documentação Swagger,
  - Correção de rotas e testes,
  - Refatoração de arquitetura e qualidade de código,
  - Estabilização do pipeline de CI/CD e da branch `develop`.

A partir de um projeto inicialmente com pipeline quebrado, testes falhando e documentação incompleta, a equipe conseguiu entregar uma base **mais estável, documentada e manutenível**, com melhorias claras em autenticação, qualidade de código e fluxo de contribuição.
