# Diário de Bordo – Uires Carlos de Oliveira


*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

---

## Sprint 0 – \[25/08 – 10/09]

### Resumo da Sprint

Sprint com foco na aprendizagem do projeto e alinhamentos sobre prixmos passos.

### Atividades Realizadas

| Data  | Atividade                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
|-------|---------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|-----------|
| 08/08 | Inicialização do ambiente na maquina           | Código                            | –                                                                                            | Concluído |
| 08/08 |  | Leitura da documentação                           | [Documentação](https://gitlab.com/gces-ej/ej-application/-/tree/develop/docs?ref_type=heads) | Concluído |


### Maiores Avanços

- Ambiente rodando perfeitamente no Windows e Linux .
- Compreensão do escopo do projeto leitura.
- Em verificação e estudo de problemas já solucionados e aguardando novas issues, de de forma proativa.

### Maiores Dificuldades

- Compreensão da arquitetura.
- Subir o sistema no Windows.


### Aprendizados

- Escopo aprendido.
- Arquitetura parcial do projeto aprendida.

### Plano Pessoal para a Próxima Sprint

- [ ] Ter um foco maior nas issues do projeto.
- [ ] Conhecimento total da aqrquitetura do projeto.
- [ ] Amplo conhecimento da documentação leitura e interpretação.

----

## Sprint 1 – [11/09 – 23/09]

### Resumo da Sprint


A Sprint 1 teve o objetivo de contribuições de cada inegrante. Tivemos reuniões com monitor Giovanni as sextas-feiras, tiramos dúvidas e a equipe esta em duas frentes a de documentação e de pipeline.

Cada conjuto de equipe esta responsável uma para mapear os endpoints, sendo essencial para a identificação das rotas. Estou na documentação.

### Atividades Realizadas

| Data  | Atividade                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
|-------|---------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|-----------|
| 20/09 | Viabilização de uma documentação | Em Estudo    | –  | Concluído |
| 21/09 | Planejamento de pontos para documentação | feito    |  –  | Concluído |

### Maiores Avanços

- Definição de criação de uma documentação.

### Maiores Dificuldades

- Leitura do sistema antigo, entendimento qual a sua operação de entrada e saída.

### Aprendizados

- planejamento para uma documentação

### Plano Pessoal para a Próxima Sprint

- [ ] Divisão de tarefas.
- [ ] Abertura de nova issue.

## Sprint 2 - [26/09 - 08/10]

### Resumo da Sprint

Melhorias no formulário de perfil de usuário
Correções e aprimoramentos nos campos do perfil:
Data de nascimento: agora o campo reconhece automaticamente o formato numérico (01011981) e aplica a máscara padrão dd/mm/aaaa, facilitando o preenchimento e evitando erros de digitação.

Cidade, País e Etnia: antes eram campos de texto livre, sem padronização. Agora possuem listas e autocomplete, permitindo seleção padronizada e acessível, garantindo consistência e melhor experiência de usuário.

Essas melhorias aumentam a usabilidade do formulário, padronizam os dados e seguem boas práticas de acessibilidade (WCAG e ABNT NBR 17225)..

### Atividades Realizadas

| Data  | Atividade                                                                 | Tipo    | Link/Referencia                                                                 | Status    |
|-------|---------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------|-----------|
| 09/10 | Criação da issue para padronização dos campos Cidade, País e Etnia no perfil           | Issue   | https://gitlab.com/gces-ej/ej-application/-/issues/58                            | Concluido |
| 09/10 | Criação da issue para máscara e validação automática da Data de Nascimento no perfil           | Issue   | https://gitlab.com/gces-ej/ej-application/-/work_items/57                            | Concluido |
| 09/10 | Documentação das melhorias no formulário de perfil (máscara de data, listas padronizadas e acessibilidade)                      | Codigo  | -                                                                                | Concluido |

### Maiores Avancos

- SImplementação de máscara automática e validação no campo Data de Nascimento (dd/mm/aaaa).
- Adição de listas padronizadas e autocomplete para os campos Cidade, País e Etnia, garantindo consistência e melhor experiência de usuário.
- Melhorias de UX e acessibilidade no formulário de perfil, com campos mais claros, padronizados e compatíveis com as diretrizes WCAG e ABNT NBR 17225.

### Maiores Dificuldades

- Tratar corretamente a validação da data de nascimento em diferentes formatos (01011981, 01/01/1981, etc.).
- Criar listas padronizadas de Cidade, País e Etnia sem afetar dados antigos dos usuários.
- Garantir que o frontend e backend permaneçam sincronizados após as mudanças nos campos do perfil.

### Aprendizados

- Manipulação e validação de formulários complexos no Django com foco em acessibilidade e usabilidade.
- Uso de máscaras automáticas e normalização de dados para campos sensíveis como datas.
- Padronização de dados de perfil com listas e autocomplete, melhorando a coerência das informações.
- Importância da internacionalização e acessibilidade digital nos sistemas de cadastro de usuário.

### Plano Pessoal para a Proxima Sprint

- [ ] Documentar os novos campos e fluxos de perfil no Swagger / API Docs.
- [ ] Implementar testes automatizados para as validações de data, cidade, país e etnia.
- [ ] Revisar e refatorar componentes de formulário para melhorar a acessibilidade (WCAG 2.2).
- [ ] Propor melhorias adicionais na interface de edição de perfil com foco em UX.

---

## Sprint 3 – [09/10 – 22/10]

### Resumo da Sprint

Nesta sprint, foquei na integração do projeto com o **SonarQube** e na análise completa da qualidade do código. A partir dessa análise, identifiquei bugs, *code smells*, duplicações e pontos de alta complexidade. Com base nos resultados, realizei refatorações essenciais e melhorias estruturais que aumentaram a manutenibilidade e a confiabilidade do sistema.

### Atividades Realizadas

| Data   | Atividade                                                                                     | Tipo       | Link/Referência                                                                 | Status      |
|--------|-----------------------------------------------------------------------------------------------|------------|----------------------------------------------------------------------------------|-------------|
| 10/10  | Configuração e inicialização do SonarQube localmente (Ubuntu)                                 | Ambiente   | —                                                                                | Concluído   |
| 11/10  | Execução da primeira análise estática do projeto usando SonarScanner                          | Ferramenta | —                                                                                | Concluído   |
| 12/10  | Revisão dos relatórios de qualidade: Bugs, Code Smells, Duplicações e Hotspots                | Análise    | —                                                                                | Concluído   |
| 14/10  | Refatorações gerais no código com base nos pontos críticos apontados pelo SonarQube           | Código     | —                                                                                | Concluído   |
| 16/10  | Redução de duplicações, simplificação de funções complexas e melhora de legibilidade          | Código     | —                                                                                | Concluído   |
| 20/10  | Revisão final da qualidade e nova análise para validar as correções                           | Análise    | —                                                                                | Concluído   |

### Maiores Avanços

* Configuração e execução do SonarQube com sucesso no ambiente local.
* Identificação de métricas críticas que afetavam a qualidade do projeto.
* Redução significativa de **code smells** e duplicações.
* Correção dos **bugs** detectados na análise estática.
* Simplificação de métodos com alta complexidade ciclomática.
* Melhoria da organização e manutenibilidade do código.

### Maiores Dificuldades

* Ajustar dependências e permissões até o SonarQube rodar corretamente no Ubuntu.
* Compreender o impacto das métricas e priorizar o que corrigir primeiro.
* Reduzir duplicações sem quebrar partes importantes do sistema.
* Refatorar funções complexas mantendo o comportamento original.

### Aprendizados

* Entendimento aprofundado das métricas de qualidade: Bugs, Code Smells, Duplication, Coverage e Complexity.
* Uso prático do SonarScanner e interpretação dos relatórios gerados.
* Importância da análise estática para detectar problemas ocultos.
* Como pequenas refatorações aumentam significativamente a manutenibilidade.
* Boas práticas de código limpo e sustentável.

### Plano Pessoal para a Próxima Sprint

* [ ] Integrar o SonarQube ao pipeline de CI/CD para análise automática a cada push.
* [ ] Aumentar a cobertura de testes automatizados.
* [ ] Tratar os últimos *Security Hotspots* identificados.
* [ ] Definir e aplicar metas de qualidade contínua (Quality Gate).

---

## Fase 4 – Análise de Qualidade com SonarQube (Resultados Reais do Projeto EJ-Application)

### Visão Geral

Nesta fase, realizei a análise completa do projeto **ej-application** utilizando o **SonarQube Community**, avaliando as principais características de qualidade: Segurança, Confiabilidade, Manutenibilidade, Cobertura de Testes e Duplicação de Código.  
A partir do relatório gerado, foi possível identificar problemas críticos, mensurar o estado atual da base de código e definir prioridades de melhoria para as próximas sprints.

---

### Métricas Gerais do Projeto (Overall Code)

| Categoria            | Valor / Status                | Interpretação |
|---------------------|-------------------------------|---------------|
| **Security**        | 1 issue aberto • Nota: **—**   | Baixo número de falhas diretas de segurança. |
| **Security Hotspots** | **140 hotspots** • Nota: **E** | Pontos sensíveis que exigem revisão manual e auditoria contínua. |
| **Reliability**     | **104 issues** • Nota: **B**   | Boa confiabilidade, mas ainda com problemas lógicos a revisar. |
| **Maintainability** | **372 issues** • Nota: **E**   | Alto acúmulo de code smells e pontos de manutenção complexa. |
| **Coverage**        | **0%** (16k linhas a cobrir)   | Ausência de testes automatizados no repositório. |
| **Duplications**    | **4.1%** (em 51k linhas)       | Nível moderado de duplicação; há espaço para refatoração. |

---

### Análise Detalhada

#### Segurança (Security)
- Apenas **1 issue direta de segurança**, o que indica que não há vulnerabilidades críticas explícitas.
- Porém, existem **140 Security Hotspots**, classificados como nota **E**, exigindo revisão manual:
  - Uso de funções potencialmente inseguras,
  - Falta de validação explícita em alguns fluxos,
  - Trechos que podem expor superfícies de ataque se não forem tratados corretamente.

#### Confiabilidade (Reliability)
- O projeto apresenta **104 issues de confiabilidade**, nota **B**.
- A maioria envolve:
  - Possíveis exceções não tratadas,
  - Falhas de fluxo de controle,
  - Lógicas duplicadas.

#### Manutenibilidade (Maintainability)
- O ponto mais crítico do relatório: **372 code smells**, nota **E**.
- Problemas mais comuns:
  - Funções muito longas,
  - Nomes pouco descritivos,
  - Complexidade ciclomática elevada,
  - Estruturas condicionais aninhadas,
  - Duplicação de lógica em múltiplos arquivos.

#### Cobertura de Código (Coverage)
- Cobertura **0%** em **16.000 linhas analisadas**.
- Não há testes automatizados detectados.
- Isso afeta diretamente:
  - Confiabilidade,
  - Manutenibilidade,
  - Qualidade geral do projeto.

#### Duplicação de Código (Duplications)
- **4.1% de duplicação**, dentro de um nível aceitável.
- No entanto:
  - Existem blocos repetidos que aumentam o risco de falhas.
  - Refatorações podem reduzir complexidade e esforço de manutenção.

---

### Conclusões da Fase 4

A análise indica que o projeto precisa de atenção especialmente em:

1. **Manutenibilidade (nota E)** – ponto mais crítico, com alto volume de code smells.  
2. **Security Hotspots (nota E)** – pontos sensíveis que exigem auditoria manual.  
3. **Cobertura de Testes (0%)** – inexistência de testes automatizados.  

Apesar disso, alguns pontos positivos são observados:

✔ Poucas falhas diretas de segurança  
✔ Duplicação moderada (4.1%)  
✔ Confiabilidade razoável (nota B)

---

### Ações Recomendadas (Backlog Técnico)

- [ ] Criar primeiro pacote de testes automatizados (unitários e integração).  
- [ ] Reduzir complexidade ciclomatica em módulos apontados como críticos pelo SonarQube.  
- [ ] Revisar 30–50 Security Hotspots prioritários.  
- [ ] Refatorar trechos duplicados (4.1%).  
- [ ] Introduzir CI/CD com análise automática do Sonar.  
- [ ] Aplicar padrões de código (PEP8 / Clean Code / Django Best Practices).  

---

### Pontos que devo apresentar na disciplina

- O SonarQube foi usado para medir objetivamente a **qualidade do código**.  
- Os **números reais** evidenciam onde o projeto deve melhorar (manutenibilidade e segurança).  
- A análise estática ajuda a definir **prioridades de melhoria nas Sprints seguintes**.  
- O relatório serve como parte da justificativa técnica para refatorações e criação de testes.

---