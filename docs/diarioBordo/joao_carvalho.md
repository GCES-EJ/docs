# Diário de Bordo – João Antonio Ginuino Carvalho


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
| 08/08 | Leitura e estudo da documentação do projeto | Estudo                            | [Documentação](https://gitlab.com/gces-ej/ej-application/-/tree/develop/docs?ref_type=heads) | Concluído |

### Maiores Avanços

- Consegui rodar a aplicação localmente.
- Entendi o fluxo de contribuição do projeto através da [documentação de contribuição](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/contributing.rst?ref_type=heads).

### Maiores Dificuldades

- Utilização do inv. Solucionei esse problema dando o comando puro do Docker:

````bash
docker compose -f docker/docker-compose.yml build
docker compose -f docker/docker-compose.yml up
````


### Aprendizados

- Insights sobre a comunidade e compreensão da aplicação.
- Entendimento do fluxo de contribuição do projeto.

### Plano Pessoal para a Próxima Sprint

- [ ] Estudar o código-fonte em mais detalhes.
- [ ] Ler a documentação referente à arquitetura do projeto.  
- [ ] Estudar o inv. 

---

## Sprint 1 – \[11/09 – 25/09]

### Resumo da Sprint

O Empurrando Juntas está em processo de transformação para se tornar uma API independente do frontend. Para isso, é necessário mapear todas as rotas do projeto e documentá-las adequadamente. O grupo GCES anterior já mapeou algumas rotas, mas ainda falta documentar as realizadas e as pendentes. O objetivo desta sprint é finalizar esse mapeamento.

### Atividades Realizadas

| Data  | Atividade                                                          | Tipo    | Link/Referência                                                    | Status    |
|-------|--------------------------------------------------------------------|---------|--------------------------------------------------------------------|-----------|
| 19/09 | Mapeamento de rotas do projeto                                     | Revisão | -                                                                  | Concluído |
| 20/09 | Atualização da documentação no GitPage com o relatório da Sprint 1 | Doc     | https://gces-ej.github.io/docs/#/relatorios/sprint_1               | Concluído |
| 20/09 | Criação da issue e análise do guia de contribuição                 | Estudo  | [Issue #45](https://gitlab.com/gces-ej/ej-application/-/issues/45)             | Concluído |
| 21/09 | Documentação das rotas do `ej_users`                               | Doc     | [docs/api-ej-users-45](https://gitlab.com/gces-ej/ej-application/-/tree/docs/api-ej-users-45) | Concluído   |
| 22/09 | MR (Develop com pipeline quebrada, meu MR não será aceito pois minha branch é um fork da develop)                               | MR     | - | Pendente   |

### Maiores Avanços

- [x] Estudar o código-fonte em mais detalhes.
- [x] Ler a documentação referente à arquitetura do projeto.
- [x] Estudar o inv.

* Primeira issue criada na comunidade.

### Maiores Dificuldades

* Dificuldades com a ferramenta de documentação do EJ (rst).
* Pipeline quebrado dificuldade de realizar o MR.

### Aprendizados

* Aprofundamento no entendimento do código-fonte.
* Aprofundamento no guia de contribuição.
* Noções de boas práticas na documentação de rotas.

### Plano Pessoal para a Próxima Sprint

* [ ] Finalizar a documentação das rotas mapeadas.
* [ ] Iniciar a implementação das rotas pendentes.
* [ ] Corrigir o pipeline quebrado na develop.

---

## Sprint 2 – \[26/09 – 08/10]

### Resumo da Sprint

Seguindo a sugestão da professora Carla, abandonamos a ideia de documentar as rotas manualmente em um arquivo de documentação. Em vez disso, decidimos utilizar o Swagger, para facilitar a documentação das rotas de forma automática, melhorando a comunicação e a visualização das APIs.
### Atividades Realizadas


| Data  | Atividade                                                       | Tipo    | Link/Referência                                                        | Status    |
|-------|-----------------------------------------------------------------|---------|------------------------------------------------------------------------|-----------|
| 04/10 | Estudo sobre Swagger                                            | Estudo  | -                                                                      | Concluído |
| 05/10 | Análise da documentação do Swagger da ej                        | Revisão | -                                                                      | Concluído |
| 06/10 | Fechamento da issue e branch relacionadas a documentação de API | Revisão | -                                                                      | Concluído |
| 06/10 | Documentação de Swagger e como mapear rotas                     | Doc     | [Documentação Swagger](https://gces-ej.github.io/docs/#/notes/Swagger) | Concluído |


### Maiores Avanços

* Realização de um estudo sobre o Swagger.
* Análise da documentação Swagger já implementada no projeto.
* Documentação de como utilizar o Swagger para mapear rotas.

### Maiores Dificuldades

* Nunca havia trabalhado com Swagger antes, o que exigiu um aprendizado inicial sobre a ferramenta e suas funcionalidades.

### Aprendizados

* Criação de documentação automática de rotas com Swagger.
* Noções de boas práticas na documentação de rotas.

### Plano Pessoal para a Próxima Sprint

* [ ] Finalizar a documentação das rotas mapeadas.
* [ ] Iniciar a implementação das rotas pendentes.

---

## Sprint 3 – \[09/10 – 22/10]

### Resumo da Sprint

Esta sprint foi dedicada à análise do Swagger e à verificação das rotas da aplicação. Foram revisados os seguintes conjuntos de rotas:

* Profiles: 11 rotas verificadas
* Conversation: 15 rotas verificadas
* Admin: 10 rotas verificadas

Durante a análise, foram identificados erros e duplicações em 6 das 10 rotas do módulo admin.

> As demais rotas analisadas (profiles e conversation) não apresentaram problemas.

### Atividades Realizadas


| Data  | Atividade                                               | Tipo    | Link/Referência                                                                                                                                                           | Status    |
|-------|---------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| 20/10 | Análise das rotas de profiles                           | Revisão | -                                                                                                                                                                         | Concluído |
| 20/10 | Análise das rotas de conversation                       | Revisão | -                                                                                                                                                                         | Concluído |
| 20/10 | Análise das rotas de admin/administration               | Revisão | -                                                                                                                                                                         | Concluído |
| 21/10 | Correção das rotas duplicadas em admin e administration | Código  | [Issue #60](https://gitlab.com/gces-ej/ej-application/-/issues/60), [Commit](https://gitlab.com/gces-ej/ej-application/-/commit/8c8e78371162be6470f66ee4e4a942312678946f) | Concluído |

### Maiores Avanços

* Estudo do Django e identificação de rotas duplicadas.
* Identificação e correção de rotas duplicadas no módulo admin.

### Maiores Dificuldades

* Identificação e correção de rotas duplicadas no módulo admin.
* Varrer o código para encontrar as rotas duplicadas.

### Aprendizados

* Aprofundamento no funcionamento do Django REST Framework e da organização de rotas.
* Melhor compreensão do funcionamento e integração do módulo Admin com o restante da aplicação.

### Plano Pessoal para a Próxima Sprint

* [ ] Finalizar a análise das rotas de boards.
* [ ] Finalizar a análise das rotas de clusterizations.
* [ ] Finalizar a análise das rotas de comments.

---

## Sprint 4 – \[23/10 – 12/11]

### Resumo da Sprint

Durante esta sprint, o foco foi **finalizar o Merge Request pendente da sprint anterior**, garantindo que todas as modificações de rotas e ajustes de views não quebrassem a aplicação ou os testes existentes.  
Durante a validação, foi identificado um **erro nos testes de `administration`**, causado por inconsistêncis na comparações de usuários dentro dos querysets.

Após uma análise detalhada, as duplicidades foram removidas e as rotas foram unificadas, resultando em uma estrutura mais limpa, estável e coerente com o padrão da EJ.

Sendo assim, além da finalização da issue passada foi finalizado outro MR para as correções dos querysets, deixando o administration com todas as rotas padronizadas e os retornos totalmente corretos conforme os testes.

### Atividades Realizadas

| Data  | Atividade                                                                          | Tipo    | Link/Referência                                                         | Status    |
|-------|------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------|-----------|
| 09/11 | Finalização da issue da sprint anterior (verificação de rotas e ajustes em testes) | Código  | [MR #36](https://gitlab.com/gces-ej/ej-application/-/merge_requests/36) | Concluído |
| 09/11 | Identificação e análise de erro nos testes de `administration`                     | Revisão | [Issue #65](https://gitlab.com/gces-ej/ej-application/-/issues/65)      | Concluído |
| 09/11 | Correção da lógica de anotação no queryset (`apply_board_filters`)                 | Código  | [MR #35](https://gitlab.com/gces-ej/ej-application/-/merge_requests/35) | Concluído |

### Maiores Avanços

- Correção completa das **rotas duplicadas** e inconsistências na API administrativa.
- Revisão profunda da **integração entre Django Views, Templates (Jinja2)** e chamadas AJAX.
- Compreensão avançada da **estrutura de testes com Pytest** e execução dentro do ambiente Docker.
- Melhoria da **manutenibilidade e rastreabilidade** do código relacionado a URLs e views.

### Maiores Dificuldades

- Rastrear dependências entre templates Jinja2 e as rotas AJAX que os alimentam.
- Entender o impacto cruzado de alterações em rotas sobre os testes automatizados.
- Dificuldade inicial em interpretar as falhas de testes do módulo `administration`, especialmente por conta das comparações de objetos Django (`owner=user` vs `owner_id`).

### Aprendizados

- O Django compara objetos Python por **instância**, não por ID, exigindo uso de `owner_id` em anotações do ORM.
- A organização adequada das rotas evita duplicidade e inconsistência no Swagger.
- O uso correto de **Paginators e Querysets anotados** impacta diretamente a ordenação e os resultados exibidos na interface administrativa.
- Aprimoramento do entendimento de **Jinja2** e sua integração com JavaScript (AJAX).

### Plano Pessoal para a Próxima Sprint

- [ ] Finalizar a análise das rotas de **Boards**.
- [ ] Iniciar a análise e refatoração das rotas de **Clusterizations**.
- [ ] Realizar revisão das rotas e testes de **Comments**.
- [ ] Ampliar cobertura de testes nas views de administração.

---

## Sprint 5 – \[13/11 – 01/12]

### Resumo da Sprint

Nesta sprint final, foram revisadas e validadas todas as rotas restantes da aplicação, assegurando o funcionamento completo e correto de 100% da API. Além disso, dediquei-me à análise e aprovação dos merge requests pendentes, bem como à correção de inconsistências no pipeline e de erros provenientes de MRs antigos que impactavam a branch develop.

### Atividades Realizadas

| Data  | Atividade                                                                   | Tipo    | Link/Referência                                                                                                                                                                                                                                                                                                                                                     | Status    |
|-------|-----------------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| 26/11 | Corrige codigo não executando na develop                                    | Código  | [hotfix: corrigir conflito não resolvido em ej_users/admin.py](https://gitlab.com/gces-ej/ej-application/-/commit/3344f7b05710847ea38055a4808e8c057eeae189)                                                                                                                                                                                                         | Concluído |
| 26/11 | Padronização da indentação de todo o projeto                                | Código  | [fix: executa black](https://gitlab.com/gces-ej/ej-application/-/commit/b86d71c6aac7831d8dc23fe2acc99520adc12db4)                                                                                                                                                                                                                                                   | Concluído |
| 26/11 | Ajustes gerais reportados pelo Ruff (imports, warnings e formatação)        | Código  | [chore: ajustar imports e warnings reportados pelo ruff](https://gitlab.com/gces-ej/ej-application/-/commit/1c1dc0645e1ec6cdd494914cc911fd4325df8893)                                                                                                                                                                                                               | Concluído |
| 26/11 | Correção do pull policy inválido no pipeline, permitindo execução do pytest | Código  | [ci: corrige pull_policy inválido no job pytest](https://gitlab.com/gces-ej/ej-application/-/commit/b3a1957c31aa931a68170eb7bb865a136871bf96)                                                                                                                                                                                                                       | Concluído |
| 29/11 | Ajustes no pipeline: remoção de builds sem servidor e de testes E2E         | Código  | [ci: corrige pipeline](https://gitlab.com/gces-ej/ej-application/-/commit/83c4517c403c4304355bdd2b35a65dbf429b2cf4), [ci: remove o e2e](https://gitlab.com/gces-ej/ej-application/-/commit/9756f10b48971aaac9fe5a9539d2759264840d40), [ci: remove os stages de build ](https://gitlab.com/gces-ej/ej-application/-/commit/ba9fd13dcd306a0c4f6ffaca4d3fddfb4e89a5b5) | Concluído |
| 29/11 | Revisão completa das rotas restantes                                        | Revisão |                                                                                                                                                                                                                                                                                                                                                                     | Concluído |
| 29/11 | Aprovação dos Merge Requests #35 e #36                                      | Revisão | [MR #35](https://gitlab.com/gces-ej/ej-application/-/merge_requests/35), [MR #36](https://gitlab.com/gces-ej/ej-application/-/merge_requests/36)                                                                                                                                                                                                                    | Concluído |

### Maiores Avanços

- Validação integral das rotas da API e do Swagger.
- Correção de inconsistências na branch develop.
- Finalização e aprovação dos MRs pendentes.
- Estabilização do pipeline, garantindo sua execução correta.

### Maiores Dificuldades

- Correção de problemas oriundos de MRs antigos que impactavam o pipeline de forma indireta.
- Ajustes complexos em etapas do CI/CD que estavam bloqueando execuções.

### Aprendizados

- Aprofundamento no funcionamento do pipeline CI/CD do GitLab.
- Fortalecimento da habilidade de manutenção de projetos colaborativos.