# Diário de Bordo – Yan Lucas Souza Guimarães


*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

---

## Sprint 0 – \[25/08 – 10/09]

### Resumo da Sprint

Nesse início foquei em entender o que o projeto Empurrando juntas tinha como proposta e resolução, dando foco também em como funciona a arquitetura da API. Tive bastante dficuldade em configurar o ambiente na minha máquina mas, depois descobri que era por conta da versão do python.
Nesse início, concentrei meus esforços em compreender a proposta e os objetivos do projeto Empurrando Juntas, além de explorar a arquitetura da API Ej. Enfrentei dificuldades iniciais para configurar o ambiente de desenvolvimento na minha máquina, que foram solucionadas ao identificar incompatibilidades com a versão do Python instalada localmente.
### Atividades Realizadas

| Data  | Atividade                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
|-------|---------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|-----------|
| 01/09 | Tentativa de configuração inicial do ambiente            | Código                            | –                                                                                            | Concluído |
| 02/09 | Leitura e estudo do documento contributing.rst do projeto | Estudo                            | [Contributing.rst](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/contributing.rst?ref_type=heads) | Concluído |
| 02/09 | Leitura da página do projeto, para o entendimento do projeto | Estudo                            | [ejparticipe.org](https://www.ejparticipe.org/docs/index.html) | Concluído |

### Maiores Avanços

- Configuração completa do ambiente local, execução do projeto e testes.
- entendimento do fluxo de contribuição do projeto.
- Primeiro contato com a arquitetura do projeto.

### Maiores Dificuldades

- Tive dificuldade de buildar o docker do projeto, mas depois entendi que eu estava usando o python 3.12 ao invés do 3.11 que é o escolhido pelo projeto. Para resolução preferi criar um ambiente virtual (venv) para não confundir com os meus pacotes globais.


### Aprendizados

- Noção Inicial do projeto.
- Fluxo de contribuição do projeto.
- Gerenciamento de versões de pacotes e dependências.

### Plano Pessoal para a Próxima Sprint

- [x] Estudar detalhadamente a estrutura do projeto.
- [x] Observar e acompanhar as Issues abertas no repositório.
- [x] Identificar novas melhorias para criação de issue.

---

## Sprint 1 – *11/09 a 23/09*

### Resumo da Sprint

Esta sprint foi dedicada à análise do pipeline de CI/CD do projeto. Fui capaz de identificar uma falha crítica em um teste de API e, em resposta, documentei o problema de forma detalhada, criando uma issue para rastreamento e planejamento da correção. O trabalho envolveu a leitura de logs de pipeline e a compreensão do fluxo de autenticação da aplicação.

### Atividades Executadas

| Data | Atividade | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status |
|---|---|---|---|---|
| 15/09 | Análise da falha no pipeline de CI/CD | Análise/Diagnóstico | Imagem | Concluído |
| 21/09 | Criação de issue para correção de teste | Planejamento/Doc | [Issue sobre falha no teste de permissão da API](https://gitlab.com/gces-ej/ej-application/-/issues/50) | Concluído |

<img width="1514" height="204" alt="image" src="https://github.com/user-attachments/assets/61486406-4daf-4592-8ad7-293abbce855f" />

### Principais Conquistas

* **Identificação da causa raiz da falha**: O problema no pipeline foi diagnosticado como um teste esperando um status de autenticação diferente do retornado pela API.
* **Criação de uma issue detalhada**: Foi criado um item de trabalho completo, com contexto, objetivo, escopo e critérios de aceitação, demonstrando uma abordagem profissional para o gerenciamento de bugs.

### Obstáculos Encontrados

* A principal dificuldade foi a inconsistência entre o comportamento esperado pelo teste (status **`403 Forbidden`**) e o comportamento real da API (status **`401 Unauthorized`**). Essa diferença sutil exigiu uma análise cuidadosa para ser identificada.

### Lições Aprendidas

* A importância de uma análise minuciosa dos logs do pipeline para identificar a origem exata de uma falha.
* Noções sobre o fluxo de autenticação e autorização em APIs, e a diferença entre os status codes **`401`** e **`403`**.
* Aprender a documentar bugs de maneira eficaz, com informações claras e acionáveis para facilitar o trabalho de correção.

### Metas Pessoais para a Próxima Sprint

* [ ] Realizar a correção da issue `Falha no teste de permissão da API`.
* [ ] Submeter um Merge Request com a correção e garantir que o pipeline seja aprovado.
* [ ] Explorar e refatorar outros testes de autenticação e permissão para garantir consistência.
