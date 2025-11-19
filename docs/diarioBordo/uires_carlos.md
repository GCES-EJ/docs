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