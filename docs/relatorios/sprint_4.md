# 📝 Relatório de Contribuição – Sprint 4

*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

*Período da Sprint:* 23/10 – 12/11

---

## 1. Objetivos da Sprint

- Finalizar e melhorar rotas `administration`.
- Implementar o modelo `ClientPermission` e o serviço `ApiKeyService` para a arquitetura de Federação de Identidades.
- Corrigir testes falhando relacionados à migração FBV→CBV e padronizar autenticação REST.
- Garantir que todos os testes unitários estejam funcionando e o pipeline de CI/CD estável.


---

## 2. Entregas Coletivas

| Entrega                                                      | Status (Concluído/Parcial/Pendente) | Link/Referência                                       | Observações                              |
|--------------------------------------------------------------|-------------------------------------|-------------------------------------------------------|------------------------------------------|
|                                                              |                                     |                                                       |                                          |

---

## 3. Contribuições Individuais


| Integrante                                | Contribuições                                                                                                                                                                                                                                            | Links (PRs, Issues, Docs)                                                                                                                                                                                            | Observações                                                                                                                                                                             |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ana Joyce Guedes Amorim da Silva**  |  [ej-users] Implementar Middleware de Autenticação + Unificação de Usuários Externos   |  [Issue #69](https://gitlab.com/gces-ej/ej-application/-/issues/69)    |  Continuidade da implementação da nova arquitetura de autenticação do EJ, dando seguimento à proposta do Giovanni.|
| **João Filipe de Oliveira Souza** | [ej-users] Implementar Middleware de Autenticação + Unificação de Usuários Externos | [Issue #69](https://gitlab.com/gces-ej/ej-application/-/issues/69) | Continuidade da implementação da nova arquitetura de autenticação do EJ, dando seguimento à proposta do Giovanni. |
| **Caio Antonio Araújo Garcia de Almeida** | Implementação da funcionalidade de ordenação das conversas por data de criação, melhorando a organização e usabilidade da interface de listagem. | https://gitlab.com/gces-ej/ej-application/-/merge_requests/42 | Melhoria na organização e usabilidade da interface de listagem de conversas através da ordenação por data de criação. |
| **Danielle Rodrigues Silva**              | Implementação do modelo `ClientPermission` com sistema de revogação e interface administrativa. Desenvolvimento do serviço `ApiKeyService` para gestão de chaves de API. | [Issue #67](https://gitlab.com/gces-ej/ej-application/-/issues/67), [Issue #68](https://gitlab.com/gces-ej/ej-application/-/issues/68)                                                                                      | Contribuições focadas na continuidade da arquitetura de Federação de Identidades, focado principalmente na segurança, usabilidade e integração com o Django Admin.                                                                 |
| **Felipe Matheus Ribeiro Lopes**          |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **João Antonio Ginuino Carvalho**         | Finalização da issue da sprint anterior, incluindo revisão das rotas e correção dos testes de administration. Análise e correção do erro nos querysets (apply_board_filters), eliminando duplicidades e unificando rotas para maior consistência da API. | [MR #36](https://gitlab.com/gces-ej/ej-application/-/merge_requests/36), [Issue #65](https://gitlab.com/gces-ej/ej-application/-/issues/65), [MR #35](https://gitlab.com/gces-ej/ej-application/-/merge_requests/35) | Conseguiu padronizar as rotas administrativas, corrigir falhas em testes e aprofundar o entendimento sobre comparações de instâncias Django e integração entre Views, Templates e AJAX. |
| **João Filipe de Oliveira Souza**         |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **Leticia Arisa Kobayashi Higa**          | Refatoração do Dockerfile para otimização de cache de camadas. Alteração da ordem de instruções para garantir que a instalação de dependências (`poetry install`) seja cacheada quando apenas o código fonte for alterado.                               | [Issue #66](https://gitlab.com/gces-ej/ej-application/-/issues/66), [MR #38](https://gitlab.com/gces-ej/ej-application/-/merge_requests/38)                                                                          |                                                                                                                                                                                         |
| **Marco Soares de Oliveira**              |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **Marco Tulio Soares de Deus**            |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **Uires Carlos de Oliveira**              |  Segunda análise estática completa utilizando SonarQube	                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                      |                                                                                                                                                                                         |
| **Victor Augusto de Sousa Câmara**        |      limpando o código das Views de usuário, movendo as regras de negócio para um Serviço dedicado para tornar o sistema mais organizado e testável.                                                                                                                                                                                                                                     |    [issue #77](https://gitlab.com/gces-ej/ej-application/-/issues/77)                                                                                                                                                                                                              |  A issue visa aplicar o padrão 'Skinny Views' no módulo de usuários, centralizando a orquestração de persistência e e-mails em um Service Layer.                                                                                                                                                                                       |
| **Victor Pontual Guedes Arruda Nóbrega**  | Correção completa de 28 testes falhando relacionados à migração FBV→CBV e padronização de autenticação REST. Implementação do decorator `@can_access_dataviz_api` para retornar códigos HTTP corretos (401/403) ao invés de redirects. Registro dinâmico do namespace `ej_integrations` via `get_app_urls()`. | [Issue #54](https://gitlab.com/gces-ej/ej-application/-/issues/54) | Corrigiu testes em ej_dataviz (12), ej_integrations (14), ej_users (1) e ej_boards (1). Todos os testes unitários agora passam, deixando o pipeline de CI/CD funcional. Padronizou comportamento de autenticação em APIs REST seguindo padrões HTTP corretos. |
| **Yan Guimarães**                         |                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                      |                                                                                                                                                                                         |


---

## 4. Maiores Avanços

### Qualidade e Estabilidade dos Testes
- **Testes de Administration**: Agora a rota além de ter todas as duplicatas removidas passa em todos os casos de teste.
- **Testes de Federação de Identidades**: Cobertura de testes para os modelos `ClientPermission` e `ApiKeyService`.
- **Correção de 28 testes**: Testes em ej_dataviz (12), ej_integrations (14), ej_users (1) e ej_boards (1) corrigidos e passando.
- **Padronização de Autenticação REST**: Implementação de códigos HTTP corretos (401/403) ao invés de redirects (302) em APIs.
- **Pipeline de CI/CD Funcional**: Todos os testes unitários passando, garantindo estabilidade do pipeline de integração contínua.

### Arquitetura e Infraestrutura
- Remoção de rotas duplicadas em Administration, além da verificação das seguintes rotas:
  * Profiles: 11 rotas verificadas
  * Conversation: 15 rotas verificadas
  * Admin: 10 rotas verificadas
- Implementação do modelo `ClientPermission` com sistema de revogação e interface administrativa.
- Desenvolvimento do serviço `ApiKeyService` para gestão de chaves de API com segurança avançada.
- Criação do decorator `@can_access_dataviz_api` para padronização de respostas REST.
- Registro dinâmico do namespace `ej_integrations` via método `get_app_urls()`.

### Autentição
- Implementação do Middleware de Autenticação e Unificação de Usuários Externos  

---

## 5. Maiores Dificuldades

- Rastrear dependências entre templates Jinja2 e as rotas AJAX que os alimentam.
- Garantir a validação de chaves de API em tempo constante para prevenir ataques de timing.
- Balancear segurança (uso de hash e salt) com performance em consultas frequentes.
- Implementar um padrão consistente de soft delete para os modelos `ClientPermission` e `ApiKeyService`.
- Identificar e corrigir diferenças entre clientes de teste (`logged_client` vs `api_client`) para APIs REST.
- Garantir compatibilidade entre FBVs e CBVs durante migração, especialmente em métodos `setup()` de views.

---

## 6. Lições Aprendidas

### Django e Django REST Framework
- O Django compara objetos Python por **instância**, não por ID, exigindo uso de `owner_id` em anotações do ORM.
- O uso correto de **Paginators e Querysets anotados** impacta diretamente a ordenação e os resultados exibidos na interface administrativa.
- Decorators para APIs REST devem retornar códigos HTTP apropriados (401/403/404) ao invés de redirects (302).
- Uso de `@pytest.mark.django_db` é essencial para testes que acessam o banco de dados.
- Diferença entre `Client` (sessões) e `APIClient` (tokens/autenticação REST) impacta testes de API.
### Segurança Criptográfica
- Uso de `secrets` para geração de tokens seguros e comparação em tempo constante.
- Importância de salt único para prevenir ataques de rainbow table.
### Django Admin
- Customização avançada com badges visuais e ações administrativas traduzidas.
- Controle de permissões e proteção contra operações perigosas.
### Arquitetura de Segurança
- Separação clara entre autenticação e autorização.
- Implementação de padrões de auditoria com timestamps detalhados.

### Testes e Qualidade de Código
- Registro dinâmico de URLs via `get_app_urls()` em AppConfig facilita modularização.
- Testes devem usar fixtures apropriadas (`api_client`, `board`, `conversation`) para evitar erros de integridade.
- Importância de manter pipeline de CI/CD funcional para detectar regressões rapidamente.
- Aplicação consistente de formatadores (Black, Ruff) facilita manutenção e revisão de código.

---

## 7. Planejamento para a Próxima Sprint
* [ ] Corrigir os testes ainda falhando, visando atingir taxa de sucesso de 95%+
* [ ] Finalizar a verificação do restante das rotas
* [ ] Desenvolver endpoints REST para gerenciamento de chaves
* [ ] Documentar o fluxo completo de autenticação com exemplos de uso
* [ ] Finalizar o novo modelo de autenticação
* [ ] Expandir cobertura de testes para novos endpoints criados
