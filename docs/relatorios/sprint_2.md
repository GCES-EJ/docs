# 📝 Relatório de Contribuição – Sprint 2

*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

*Período da Sprint:* 26/09 – 08/10

---

## 1. Objetivos da Sprint

- [x] tanana
- [x] Estudo do modelo antigo de autenticação

---

## 2. Entregas Coletivas

| Entrega                            | Status (Concluído/Parcial/Pendente) | Link/Referência                           | Observações           |
|------------------------------------|-------------------------------------|-------------------------------------------|-----------------------|
| Issue 51 - Permitir unificação de usuários com APIs externas  |  Parcial  |  https://gitlab.com/gces-ej/ej-application/-/issues/51 | Apresentar o modelo novo para o Giovanni |

---

## 3. Contribuições Individuais

| Integrante                           | Contribuições                                                                                                                            | Links (PRs, Issues, Docs)                                                                                                           | Observações                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ana Joyce Guedes Amorim da Silva     |  Estudo do modelo de autenticação antigo ou modelo de autenticação atual do EJ  |  https://gitlab.com/gces-ej/ej-application/-/issues/51  |   Apresentar o modelo novo para o Giovanni    |
| Caio Antonio de Oliveira             |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |
| Felipe Matheus Ribeiro Lopes         |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |
| João Antonio Ginuino Carvalho        | Estudo do Swagger, documentação inicial do relatório 2, documentação de como utilziar o Swagger.                                         | [Documentação Swagger](https://gces-ej.github.io/docs/#/notes/Swagger)                                                              | Estudei o Swagger para entender como ele pode ser usado para documentar as rotas automaticamente. Como nunca tinha trabalhado com essa ferramenta antes, foi um desafio inicial, mas consegui aprender seus recursos e como aplicá-los no projeto. Além disso, documentei os aprendizados no pages da disciplina. |
| João Filipe de Oliveira Silva        |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |
| Leticia Arisa Kobayashi Higa         | Análise, estudo e correção da documentação da API (Swagger), registrando ViewSets que estavam ausentes. Criação da issue e MR da tarefa. | [Issue](https://gitlab.com/gces-ej/ej-application/-/issues/53), [MR](https://gitlab.com/gces-ej/ej-application/-/merge_requests/30) | Analisei a documentação da API e identifiquei que ViewSets (ClusterViewSet, StereotypeRootViewSet) estavam ausentes por não serem registrados no urls.py. Corrigi o router principal para expor as rotas faltantes e formalizei a tarefa criando a issue e o commit correspondentes.                              |
| Marco Soares de Oliveira             |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |
| Uires Carlos de Oliveira             |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |
| Victor Augusto Câmara de Oliveira    |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |
| Victor Pontual Guedes Arruda Nóbrega |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |
| Yan Guimarães                        |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |

---

## 4. Maiores Avanços

- Estudo e entendimento do Swagger.
- Estudo da autenticação

---

## 5. Maiores Dificuldades

- Navegar na estrutura de URLs do projeto (API vs. Django tradicional).
- Entender a autenticação antiga.

---

## 6. Lições Aprendidas

* Criação de documentação automática de rotas com Swagger.
* A necessidade de registrar ViewSets no router para que sejam expostos na API e na documentação.
* Padrões e boa práticas de autenticação

---

## 7. Planejamento para a Próxima Sprint

* [ ] tanana
* [ ] Abertura das issues para implementação da nova arquitetura de autenticação
