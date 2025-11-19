# 📝 Relatório de Contribuição – Sprint 1

*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

*Período da Sprint:* 11/09 – 24/09

---

## 1. Objetivos da Sprint

- [x] Mapear rotas da API.
- [x] Reconfigurar a pipeline atual.

---

## 2. Entregas Coletivas

| Entrega                            | Status (Concluído/Parcial/Pendente) | Link/Referência                           | Observações           |
|------------------------------------|-------------------------------------|-------------------------------------------|-----------------------|
| Atualização do Gitpages            | Concluído                           | https://gces-ej.github.io/docs/#/         | Organização da Equipe |
| Issues e PR em atividades iniciais | Concluído                           | https://gitlab.com/gces-ej/ej-application | -                     |
| Nova Pipeline definidade com etapa de black, ruff e pytest | Concluído   | Em produção | aguardando a refatoração de alguns códigos da branch principal |

---

## 3. Contribuições Individuais

| Integrante                        | Contribuições                                                                                                        | Links (PRs, Issues, Docs)                                                                             | Observações                                                           |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| Ana Joyce Guedes Amorim da Silva  | Estudo da pipeline antiga, entender como os testes antigos funcionavam e motivo dela não estar mais funcionando, identificação do erro, entrar em contato com o monitor para a discussão de possibilidades, definição do novo fluxo da pipeline   | Em produção | Aguardando a refatoração de arquivos da branch principal |
| Caio Antonio de Oliveira          | –                                                                                                                    | –                                                                                                     | –                                                                     |
| Felipe Matheus Ribeiro Lopes              | Em colaboração com Yan Lucas, realizamos uma análise da falha no pipeline de CI/CD e criação de issue para a correção.| [Issue #50](https://gitlab.com/gces-ej/ej-application/-/issues/50) |Contribuição focada em QA e documentação de erros na pipeline |
| João Antonio Ginuino Carvalho     | Documentação das rotas do `ej_users`, documentação inicial do relatório 1 e mapeamento inicial das rotas do projeto. | https://gces-ej.github.io/docs/#/, [Issue #45](https://gitlab.com/gces-ej/ej-application/-/issues/45) | Estudo e aplicação das boas práticas seguindo o guia de contribuição. |
| João Filipe de Oliveira Silva     | Criação e desenvolvimento da Issue 49                                                                                                                   | [issues 49](gces-ej/ej-application#49)                                                                                                    | –                                                                     |
| Leticia Arisa Kobayashi Higa      | Criação de um documento listando as APIs ainda não documentadas no projeto.  | [Documento](https://gces-ej.github.io/docs/#/notes/APIs)                                                                                                     | -                                                                     |
| Marco Soares de Oliveira          | -                                                                                                                    | -                                                                                                     | -                                                                     |
| Marco Tulio Soares de Deus        | Criação do botão de visualizar senha na tela de login                                                                                                                    | [Issue #48](https://gitlab.com/gces-ej/ej-application/-/issues/48)-                                                                                                     | -                                                                     |
| Uires Carlos de Oliveira          | Planejamento de pontos para documentação	–                                                                                                                    | –                                                                                                     | –                                                                     |
| Victor Augusto Câmara de Oliveira | –                                                                                                                    | –                                                                                                     | –                                                                     |
| Victor Pontual Guedes Arruda Nóbrega| Implementação do job test-coverage no GitLab CI, Correção de configuração de runners obsoletos, Correção de 58 erros do linter Ruff, Reformatação de código com Black | [Merge Request 29](https://gitlab.com/gces-ej/ej-application/-/merge_requests/29), [Issue #44](https://gitlab.com/gces-ej/ej-application/-/issues/44)                                                                                                     | –                                                                     |
| Yan Guimarães         | Em colaboração com Felipe Matheus, realizamos uma análise da falha no pipeline de CI/CD e criação de issue para a correção.| [Issue #50](https://gitlab.com/gces-ej/ej-application/-/issues/50) |Contribuição focada em QA e documentação de erros na pipeline |

---

## 4. Maiores Avanços

* [x] Inclusão dos contribuintes ao fork mais atualizado do projeto.
* [x] Ampliar a documentação, incluindo os procedimentos adotados e os aprendizados obtidos nesta sprint.
* [x] Refatoração da pipeline.
* [x] Mapeamento das rotas da API.
* [x] Configuração inicial da pipeline de CI/CD.

---

## 5. Maiores Dificuldades

- Mapear rotas da API, fluxo de dados e endpoints.
- Documentação utilizando o rst.
- Pipeline em desuso
- Servidor utilizado na pipeline em desuso
- Códigos antigos com muito erros de sintaxe e lint
- Teste com erro (pytest)
- Sem a pipeline o repositório não estava aceitando push

---

## 6. Lições Aprendidas

* Criação de issues e merge requests na comunidade.
* Importância do planejamento coletivo para reduzir retrabalho e melhorar a comunicação entre os membros da equipe
* Importãncia de uma pipeline manutenível
* Garantir a qualidade dos códigos que chegam a branch principal

---

## 7. Planejamento para a Próxima Sprint

* [ ] Criação de novas issues para documentação.
* [ ] Analise de rotas pendentes na API.
* [ ] Correção dos testes unitários.
* [ ] Criação de issues para revisão de qualidade do código.
