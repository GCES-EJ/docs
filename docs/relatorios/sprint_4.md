# 📝 Relatório de Contribuição – Sprint 4

*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

*Período da Sprint:* 23/10 – 12/11

---

## 1. Objetivos da Sprint

- Finalizar e melhorar rotas `administration`.

---

## 2. Entregas Coletivas

| Entrega                                                      | Status (Concluído/Parcial/Pendente) | Link/Referência                                       | Observações                              |
|--------------------------------------------------------------|-------------------------------------|-------------------------------------------------------|------------------------------------------|
|                                                              |                                     |                                                       |                                          |

---

## 3. Contribuições Individuais


| Integrante                                | Contribuições                                                                                                                                                                                                                                            | Links (PRs, Issues, Docs)                                                                                                                                                                                            | Observações                                                                                                                                                                             |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ana Joyce Guedes Amorim da Silva**      |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **Caio Antonio Araújo Garcia de Almeida** |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **Danielle Rodrigues Silva**              |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **Felipe Matheus Ribeiro Lopes**          |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **João Antonio Ginuino Carvalho**         | Finalização da issue da sprint anterior, incluindo revisão das rotas e correção dos testes de administration. Análise e correção do erro nos querysets (apply_board_filters), eliminando duplicidades e unificando rotas para maior consistência da API. | [MR #36](https://gitlab.com/gces-ej/ej-application/-/merge_requests/36), [Issue #65](https://gitlab.com/gces-ej/ej-application/-/issues/65), [MR #35](https://gitlab.com/gces-ej/ej-application/-/merge_requests/35) | Conseguiu padronizar as rotas administrativas, corrigir falhas em testes e aprofundar o entendimento sobre comparações de instâncias Django e integração entre Views, Templates e AJAX. |
| **João Filipe de Oliveira Souza**         |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **Leticia Arisa Kobayashi Higa**          | Refatoração do Dockerfile para otimização de cache de camadas. Alteração da ordem de instruções para garantir que a instalação de dependências (`poetry install`) seja cacheada quando apenas o código fonte for alterado.                               | [Issue #66](https://gitlab.com/gces-ej/ej-application/-/issues/66), [MR #38](https://gitlab.com/gces-ej/ej-application/-/merge_requests/38)                                                                          |                                                                                                                                                                                         |
| **Marco Soares de Oliveira**              |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **Marco Tulio Soares de Deus**            |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **Uires Carlos de Oliveira**              |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **Victor Augusto de Sousa Câmara**        |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **Victor Pontual Guedes Arruda Nóbrega**  |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **Yan Guimarães**                         |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |


---

## 4. Maiores Avanços

### Qualidade e Estabilidade dos Testes
- **Testes de Administration**: Agora a rota além de ter todas as duplicatas removidas passa em todos os casos de teste.

### Arquitetura e Infraestrutura
- Remoção de rotas duplicadas em Administration, além da verificação das seguintes rotas:
  * Profiles: 11 rotas verificadas
  * Conversation: 15 rotas verificadas
  * Admin: 10 rotas verificadas

---

## 5. Maiores Dificuldades

- Rastrear dependências entre templates Jinja2 e as rotas AJAX que os alimentam.

---

## 6. Lições Aprendidas

### Django e Django REST Framework
- O Django compara objetos Python por **instância**, não por ID, exigindo uso de `owner_id` em anotações do ORM.
- O uso correto de **Paginators e Querysets anotados** impacta diretamente a ordenação e os resultados exibidos na interface administrativa.

---

## 7. Planejamento para a Próxima Sprint

* [ ] Corrigir os testes ainda falhando, visando atingir taxa de sucesso de 95%+
* [ ] Finalizar a verificação do restante das rotas

