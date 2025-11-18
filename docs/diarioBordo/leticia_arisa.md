# Diário de Bordo – Leticia Arisa Kobayashi Higa


*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

---

## Sprint 0 – \[25/08 – 10/09]

### Resumo da Sprint

Sprint dedicada à ambientação no projeto, com foco nos primeiros passos, leitura do guia de contribuição e estudo da documentação.

### Atividades Realizadas

| Data  | Atividade                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
|-------|---------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|-----------|
| 08/08 | Configuração inicial do ambiente            | Código                            | –                                                                                            | Concluído |
| 09/08 | Leitura e estudo do documento contributing.rst do projeto | Estudo                            | [Contributing.rst](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/contributing.rst?ref_type=heads) | Concluído |
| 09/08 | Leitura do documento arquitetura.rst do projeto | Estudo                            | [Architecture.rst](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/architecture.rst?ref_type=heads) | Concluído |

### Maiores Avanços

- Configuração completa do ambiente local e execução do projeto com sucesso.
- Compreensão do fluxo de contribuição do projeto.
- Início do estudo da arquitetura do projeto.

### Maiores Dificuldades

- Compreensão do fluxo do projeto e da arquitetura.
- Compatibilidade de versões do Python (projeto escrito para 3.11, minha máquina tinha 3.12).


### Aprendizados

- Compreensão inicial da arquitetura do projeto.
- Fluxo de contribuição do projeto.

### Plano Pessoal para a Próxima Sprint

- [ ] Estudar detalhadamente a estrutura de pastas do projeto.
- [ ] Aprofundar o conhecimento sobre a arquitetura do projeto.
- [ ] Analisar e acompanhar as Issues abertas no repositório.


## Sprint 1 – \[11/09 – 25/09]

### Resumo da Sprint

Esta sprint foi dedicada à análise das APIs, identificando aquelas que ainda não estavam documentadas no documento oficial. Como atividade extra, foi adicionado ao README o passo a passo para executar o projeto no Windows.

### Atividades Realizadas

| Data  | Atividade                                                          | Tipo    | Link/Referência                                                    | Status    |
|-------|--------------------------------------------------------------------|---------|--------------------------------------------------------------------|-----------|
| 21/09 | Criação de issue para adicionar o passo a passo de execução do projeto no Windows windows | Issue | https://gitlab.com/gces-ej/ej-application/-/issues/46   | Concluído |
| 21/09 | Abertura de PR para incluir o passo a passo de execução do projeto no Windows | PRs | https://gitlab.com/gces-ej/ej-application/-/merge_requests/26              | Concluído |
| 23/09 | Estudo das APIs do projeto | Estudo  |      -        | Concluído |
| 23/09 | Criação de documento de anotações listando endpoints ainda não documentados  | Documento | https://gces-ej.github.io/docs/#/notes/APIs | Concluído |

### Maiores Avanços

- [x] Estudar o código das APIs.
- [x] Ler a documentação de APIs.


### Maiores Dificuldades

* Dificuldades com a ferramenta de documentação do EJ (rst).
* Pipeline quebrado dificuldade de realizar o PR.
* Entender o código.

### Aprendizados

* Aprofundamento no entendimento das APIs.
* Melhor entendimento em como funciona o guia de contribuição.

### Plano Pessoal para a Próxima Sprint

* [ ] Ajudar na documentação das rotas mapeadas.
* [ ] Abrir nova issue.
* [ ] Entender melhor outras partes do código-fonte.

---

## Sprint 2 – \[26/09 – 08/10]

### Resumo da Sprint

Nesta sprint, o meu foco foi a validação e correção da documentação automática da API gerada pelo Swagger. O objetivo era garantir que a documentação refletisse de forma completa o código-fonte. Foi realizada uma análise que resultou na identificação e correção de ViewSets inteiros que não estavam sendo expostos na API por falta de registro no router principal.

### Atividades Realizadas


| Data  | Atividade                                                       | Tipo    | Link/Referência                                                        | Status    |
|-------|-----------------------------------------------------------------|---------|------------------------------------------------------------------------|-----------|
| 05/10 | Análise da documentação Swagger e comparação com os ViewSets do código.   | Estudo  | - | Concluído |
| 06/10 | Correção do api_router para registrar os ViewSets ClusterViewSet e StereotypeRootViewSet.   | Código | - | Concluído |
| 07/10 | Criação da issue para formalizar a tarefa de registrar os endpoints faltantes. | Issue | [Issue](https://gitlab.com/gces-ej/ej-application/-/issues/53)| Concluído |
| 07/10 | Criação da MR para registrar os endpoints faltantes.   | MR | [MR](https://gitlab.com/gces-ej/ej-application/-/merge_requests/30) | Concluído |


### Maiores Avanços

* Aprofundamento técnico no sistema de roteamento do Django REST Framework e sua integração com a ferramenta drf-spectacular (Swagger).
* Contribuição direta no código-fonte para garantir a completude da API.

### Maiores Dificuldades

* A principal dificuldade foi entender por que alguns endpoints não apareciam na documentação, o que exigiu uma depuração na complexa estrutura de URLs do projeto para diferenciar as rotas da API REST das rotas do Django tradicional.

### Aprendizados

* Um ViewSet só é exposto na API se for explicitamente registrado no router do urls.py; sua simples existência no código não é suficiente.

### Plano Pessoal para a Próxima Sprint

* [ ] Ajudar na implementação das rotas pendentes.



## Sprint 3 – \[09/10 – 22/10]

### Resumo da Sprint

Esta sprint foi focada em corrigir a documentação dos endpoints mais críticos da API: autenticação e gerenciamento de usuários. A documentação automática existente no Swagger estava incompleta e não refletia a lógica de negócio customizada (ex: secret_id para update, respostas de login com token), o que dificultava o uso da API. O objetivo foi detalhar todos esses endpoints no ej_users/api.py para garantir que a documentação seja precisa e útil.

### Atividades Realizadas


| Data  | Atividade                                               | Tipo    | Link/Referência                                                                                                                                                           | Status    |
|-------|---------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| 21/10 | Análise da lógica customizada nos endpoints de ej_users/api.py  | Revisão | -                                                                                                                                                                 | Concluído |
| 22/10 | Criação de issue e MR para a tarefa de documentação dos endpoints.| Código | [Issue](https://gitlab.com/gces-ej/ej-application/-/issues/61), [MR](https://gitlab.com/gces-ej/ej-application/-/merge_requests/33)                              | Concluído |

### Maiores Avanços

* Estudo do Django e identificação de rotas duplicadas.
* Identificação e correção de rotas duplicadas no módulo admin.

### Maiores Dificuldades

* Documentação completa e precisa de toda a API de autenticação e gerenciamento de usuários (ej_users), incluindo login, cadastro, logout e os dois fluxos de recuperação de senha.
* Varrer o código para encontrar as rotas duplicadas.

### Aprendizados

* Como usar o decorador @extend_schema do drf-spectacular para documentar detalhes complexos da API, como parâmetros, request bodies, múltiplas responses e lógicas não-padrão.

### Plano Pessoal para a Próxima Sprint

* [ ] Ajudar o grupo responsável pela issue #51.

# Sprint 4 – [23/10 – 12/11]

## Resumo da Sprint

Durante esta sprint, o foco foi **otimizar o ambiente de desenvolvimento e o pipeline de construção (build)** do projeto. Foi identificado que o `Dockerfile` atual não estava aproveitando corretamente o mecanismo de **cache de camadas** do Docker, o que tornava o processo de build lento e redundante a cada alteração de código.

Após estudo sobre o funcionamento do Docker e do Poetry, realizei a refatoração do arquivo de configuração para isolar a instalação das dependências.

O resultado foi uma redução no tempo de *rebuild* incremental, garantindo que a instalação de pacotes pesados só ocorra quando realmente necessário. Essa melhoria impacta positivamente tanto a produtividade local quanto a eficiência da esteira de CI/CD.

## Atividades Realizadas

| Data  | Atividade                                                        | Tipo    | Link/Referência                | Status    |
| :--- | :--------------------------------------------------------------- | :------ | :----------------------------- | :-------- |
| 18/11 | Análise do `Dockerfile` atual e identificação de gargalo no build | Análise | [Issue #66](https://gitlab.com/gces-ej/ej-application/-/issues/66) | Concluído |
| 18/11 | Refatoração do Dockerfile (alteração da ordem de `COPY` e `RUN`)  | Infra   | [MR #38](https://gitlab.com/gces-ej/ej-application/-/merge_requests/38)       | Concluído |

## Maiores Avanços

* Implementação correta de **Layer Caching** no Dockerfile.
* Redução do tempo de instalação de dependências de minutos para **0.0s (Cached)** em builds incrementais.
* Compreensão prática do ciclo de vida de construção de containers e gerenciamento de dependências com **Poetry**.

## Maiores Dificuldades

* Compreender inicialmente a distinção entre o **Hot Reload** (usado no desenvolvimento local com Volumes) e o processo de **Build da Imagem** (usado para adicionar bibliotecas e no CI/CD).
* Entender como o Docker invalida o cache baseado na ordem das instruções (`COPY` vs `RUN`).

## Aprendizados

* A ordem das instruções no Dockerfile é crítica: arquivos que mudam muito devem ser copiados por último.
* O **Poetry** possui arquivos de bloqueio (`poetry.lock`) que devem ser copiados isoladamente antes do código para garantir a integridade e performance do build.
* Otimização de infraestrutura é tão importante quanto features, pois economiza tempo de computação e espera da equipe.
