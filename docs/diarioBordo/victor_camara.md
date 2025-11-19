# Diário de Bordo – Victor Augusto de Sousa Câmara


*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

---

## Sprint 0 – \[25/08 – 10/09]

### Resumo da Sprint

Sprint com objetivo de ambientar o projeto e entender a documentação

### Atividades Realizadas

| Data  | Atividade                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
|-------|---------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|-----------|
| 09/06 | Configuração inicial do ambiente            | Código                            | –                                                                                            | Concluído |
| 09/06 | Leitura e estudo do documento contributing.rst do projeto | Estudo                            | [Contributing.rst](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/contributing.rst?ref_type=heads) | Concluído |
| 09/07 | Leitura do documento arquitetura.rst do projeto | Estudo                            | [Architecture.rst](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/architecture.rst?ref_type=heads) | Concluído |

### Principais Avanços

* Ambiente local totalmente configurado, com o projeto executando corretamente e passando nos testes.
* Compreensão do fluxo de contribuição utilizado no projeto.
* Primeiro contato com a arquitetura e organização do sistema.

### Principais Dificuldades

* Enfrentei problemas ao tentar realizar o build do Docker, pois estava utilizando o Python 3.12 em vez da versão 3.11 exigida pelo projeto. Resolvi a questão criando um ambiente virtual (venv) para evitar conflitos com os pacotes globais da minha máquina.

### Conhecimentos Adquiridos

* Visão inicial sobre o funcionamento do projeto.
* Entendimento do processo de contribuição.
* Práticas de gerenciamento de versões de pacotes e dependências.

### Objetivos Pessoais para a Próxima Sprint

* [ ] Estudar com mais profundidade a estrutura do projeto.
* [ ] Acompanhar e analisar as Issues abertas no repositório.
Aqui está o Diário de Bordo formatado seguindo os exemplos fornecidos (`uires_carlos.md` e `victor_pontual.md`), incorporando as datas solicitadas e o conteúdo técnico discutido anteriormente (refatoração de views, issues de cluster e services).

-----


## Sprint 1 – *16/09 a 24/09*

### Resumo da Sprint

Esta sprint foi dedicada à análise do pipeline de CI/CD do projeto. Fui capaz de identificar uma falha crítica em um teste de API e, em resposta, documentei o problema de forma detalhada, criando uma issue para rastreamento e planejamento da correção. O trabalho envolveu a leitura de logs de pipeline e a compreensão do fluxo de autenticação da aplicação. Este trabalho foi realizado em parceria com o **Felipe Matheus**.

### Atividades Executadas

| Data  | Atividade                                         | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                                                   | Status    |
|-------|---------------------------------------------------|-----------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------|
| 18/09 | Análise da falha no pipeline de CI/CD             | Análise/Diagnóstico               | - | Concluído |
| 21/09 | Criação de issue para correção de teste (Issue 50) | Planejamento/Doc                  | [Issue \#50 - Falha no teste de permissão da API](https://gitlab.com/gces-ej/ej-application/-/issues/50)           | Concluído |

### Principais Conquistas

  * **Identificação da causa raiz da falha**: O problema no pipeline foi diagnosticado como um teste esperando um status de autenticação diferente do retornado pela API.
  * **Criação de uma issue detalhada**: Foi criado um item de trabalho completo, com contexto, objetivo, escopo e critérios de aceitação, demonstrando uma abordagem profissional para o gerenciamento de bugs.

### Obstáculos Encontrados

  * A principal dificuldade foi a inconsistência entre o comportamento esperado pelo teste (status **`403 Forbidden`**) e o comportamento real da API (status **`401 Unauthorized`**). Essa diferença sutil exigiu uma análise cuidadosa para ser identificada e entendida no contexto do Django REST Framework.

### Lições Aprendidas

  * A importância de uma análise minuciosa dos logs do pipeline para identificar a origem exata de uma falha.
  * Noções sobre o fluxo de autenticação e autorização em APIs, e a diferença semântica entre os status codes **`401`** e **`403`**.
  * Aprender a documentar bugs de maneira eficaz, com informações claras e acionáveis para facilitar o trabalho de correção.

### Metas Pessoais para a Próxima Sprint

  * [ ] Aprofundar-me na análise de performance das Views existentes.
  * [ ] Investigar gargalos de processamento síncrono no projeto.

-----

## Sprint 2 – *26/09 a 08/10*

### Resumo da Sprint

Nesta sprint, o foco mudou para a análise de performance e arquitetura do módulo `ej_clusters`. Identifiquei que o processamento estatístico dos clusters estava sendo realizado de forma síncrona dentro da View, o que representa um risco alto de *timeouts*. Documentei a necessidade de migração para processamento assíncrono e abri a Issue correspondente para refatoração arquitetural.

### Atividades Executadas

| Data  | Atividade                                                       | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                   | Status    |
|-------|-----------------------------------------------------------------|-----------------------------------|-------------------------------------------------------------------|-----------|
| 28/09 | Análise de código fonte em `src/ej_clusters/views.py`           | Análise                           | -                                                                 | Concluído |
| 02/10 | Identificação de gargalo de performance (cálculo síncrono)      | Diagnóstico                       | -                                                                 | Concluído |
| 05/10 | Abertura de Issue para migração de cálculo para tarefas assíncronas | Doc/Issue                         | [Issue - Otimização ej\_clusters](https://gitlab.com/gces-ej/ej-application/-/tree/develop/src/ej_clusters?ref_type=heads) (Ref) | Concluído |

### Principais Conquistas

  * **Diagnóstico de Arquitetura**: Identificação de um padrão de bloqueio de thread (cálculos matemáticos pesados na camada de View).
  * **Proposta de Solução Escalável**: Definição de uma arquitetura baseada em tarefas em segundo plano (Background Tasks com Celery) para resolver o problema de experiência do usuário.

### Obstáculos Encontrados

  * Compreender o fluxo de dados dentro do algoritmo de clusterização para garantir que a extração para uma tarefa assíncrona não quebraria a integridade dos dados.
  * Entender como o projeto gerencia dependências de tarefas assíncronas (se já existia configuração de Celery/Redis).

### Lições Aprendidas

  * **Sync vs Async**: A importância crítica de não bloquear o loop de requisição/resposta HTTP com processamento pesado.
  * **Arquitetura Django**: O papel das *Tasks* em complementar as *Views* em aplicações de ciência de dados.

### Metas Pessoais para a Próxima Sprint

  * [ ] Iniciar refatorações de qualidade de código (Linting/Code Smells).
  * [ ] Melhorar a legibilidade do módulo de clusters.

-----

## Sprint 3 – *09/10 a 22/10*

### Resumo da Sprint

Dando continuidade às melhorias no módulo `ej_clusters`, esta sprint foi dedicada à refatoração de código e qualidade ("Clean Code"). Trabalhei na Issue \#64, focando na remoção de "Magic Numbers" (números mágicos) e na parametrização dos algoritmos de clusterização. O objetivo foi tornar o código mais manutenível e facilitar testes futuros com diferentes configurações de dataset.

### Atividades Executadas

| Data  | Atividade                                                                 | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                      | Status    |
|-------|---------------------------------------------------------------------------|-----------------------------------|----------------------------------------------------------------------|-----------|
| 10/10 | Mapeamento de constantes hardcoded em `ej_clusters`                       | Análise                           | [Issue \#64](https://gitlab.com/gces-ej/ej-application/-/issues/64)   | Concluído |
| 15/10 | Criação de arquivo de constantes/configuração para o algoritmo            | Código                            | [Issue \#64](https://gitlab.com/gces-ej/ej-application/-/issues/64)   | Concluído |
| 20/10 | Refatoração da lógica para utilizar parâmetros nomeados                   | Código                            | [Issue \#64](https://gitlab.com/gces-ej/ej-application/-/issues/64)   | Concluído |

### Principais Conquistas

  * **Aumento da Manutenibilidade**: O código de clusterização agora depende de constantes nomeadas e explicativas, ao invés de números soltos no meio da lógica.
  * **Facilidade de Teste**: A parametrização permite que testes unitários rodem com configurações de "dataset pequeno" sem precisar alterar o código produtivo.

### Obstáculos Encontrados

  * Identificar o significado real de alguns valores numéricos sem documentação prévia (engenharia reversa da lógica matemática).
  * Garantir que a extração das constantes não alterasse o resultado final dos algoritmos.

### Lições Aprendidas

  * **Code Smells**: Como identificar e corrigir "Magic Numbers".
  * **Refatoração Segura**: A importância de manter o comportamento funcional inalterado enquanto se melhora a estrutura interna do código.

### Metas Pessoais para a Próxima Sprint

  * [ ] Aplicar padrões de arquitetura mais robustos (Service Layer) em outros módulos críticos, como `ej_users`.
  * [ ] Reduzir acoplamento nas Views de cadastro.

-----

## Sprint 4 – *23/10 a 12/11*

### Resumo da Sprint

Nesta sprint, abordei um problema de alta complexidade e acoplamento no módulo de usuários. Trabalhei na Issue \#77, que visava resolver o anti-padrão "Fat Views" no processo de registro de usuários. Implementei uma Camada de Serviço (*Service Layer*), extraindo a lógica de negócios, persistência e notificações (e-mails) da View para um serviço dedicado, facilitando testes e reutilização.

### Atividades Executadas

| Data  | Atividade                                                                 | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                      | Status    |
|-------|---------------------------------------------------------------------------|-----------------------------------|----------------------------------------------------------------------|-----------|
| 24/10 | Análise da complexidade da View de registro em `ej_users`                 | Análise                           | [Issue \#77](https://www.google.com/search?q=https://gitlab.com/gces-ej/ej-application/-/issues/77)   | Concluído |
| 28/10 | Criação do `UserRegistrationService` para isolar regras de negócio        | Código                            | [Issue \#77](https://www.google.com/search?q=https://gitlab.com/gces-ej/ej-application/-/issues/77)   | Concluído |
| 05/11 | Refatoração da View para delegar processamento ao Service                 | Código                            | [Issue \#77](https://www.google.com/search?q=https://gitlab.com/gces-ej/ej-application/-/issues/77)   | Concluído |
| 10/11 | Implementação de testes unitários focados apenas no novo serviço          | Testes                            | [Issue \#77](https://www.google.com/search?q=https://gitlab.com/gces-ej/ej-application/-/issues/77)   | Concluído |

### Principais Conquistas

  * **Desacoplamento**: Separação clara entre a camada HTTP (View) e a camada de Negócio (Service).
  * **Testabilidade**: Possibilidade de testar a criação de usuário e envio de e-mail sem precisar simular um request HTTP completo.
  * **Redução de Complexidade**: A View passou de um bloco monolítico de código para um orquestrador simples de chamadas.

### Obstáculos Encontrados

  * Lidar com transações de banco de dados (`transaction.atomic`) para garantir que o perfil só fosse criado se o usuário fosse salvo com sucesso.
  * Gerenciar os *side-effects* (envio de e-mail) de forma que pudessem ser "mockados" facilmente nos testes.

### Lições Aprendidas

  * **Padrão Service Layer**: Como e quando aplicar serviços no Django para evitar *Fat Views*.
  * **Princípio da Responsabilidade Única (SRP)**: Na prática, garantir que a View só cuide da interação HTTP e o Service cuide da regra de negócio.
  * **Injeção de Dependência**: Facilitando testes ao isolar componentes.

### Metas Pessoais para a Próxima Sprint

  * [ ] Consolidar a documentação dos novos serviços criados.
  * [ ] Avaliar a cobertura de testes global após as refatorações.
