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

Esta sprint foi dedicada à análise do pipeline de CI/CD do projeto. Fui capaz de identificar uma falha crítica em um teste de API e, em resposta, documentei o problema de forma detalhada, criando uma issue para rastreamento e planejamento da correção. O trabalho envolveu a leitura de logs de pipeline e a compreensão do fluxo de autenticação da aplicação. Este trabalho foi realizado em parceria com o **Felipe Matheus**.

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

* [x] Realizar a correção da issue `Falha no teste de permissão da API`.
* [x] Explorar e refatorar outros testes de autenticação e permissão para garantir consistência.

## Sprint 2 – *24/09 a 08/10*

### Resumo da Sprint

Nesta sprint, o foco foi a análise e correção de falhas em testes automatizados da API de conversas do projeto, além de ajustes na camada de permissões da API. Foram realizados diagnósticos para identificar causas raiz das falhas, correções nos testes para usar os fixtures adequados, inclusão de campos obrigatórios em payloads e atualização das permissões para métodos restritos. Essas ações resultaram em estabilidade das validações no pipeline CI/CD e consistência no comportamento da API.

### Atividades Executada

| Data   | Atividade                                                                  | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                                                    | Status    |
|--------|----------------------------------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------|-----------|
| 26/09  | Correção do teste `test_update_conversation` para uso de usuário não autor | Código                            | [Fix conversation API tests](https://gitlab.com/gces-ej/ej-application/-/commit/3e9f1558d4a049700a47c224878bc7fde8ec3340) | Concluído |
| 27/09  | Ajuste em `test_patch_conversation_unauthenticated` com cliente correto    | Código                            | [Fix conversation API tests](https://gitlab.com/gces-ej/ej-application/-/commit/3e9f1558d4a049700a47c224878bc7fde8ec3340) | Concluído |
| 29/09  | Inclusão do campo obrigatório `board` no teste de PUT                      | Código                            | [Fix conversation API tests](https://gitlab.com/gces-ej/ej-application/-/commit/3e9f1558d4a049700a47c224878bc7fde8ec3340) | Concluído |
| 01/10  | Adição da permissão `IsOwnerOrSuperUser` para ação `destroy` na API       | Código                            | [Fix conversation API tests](https://gitlab.com/gces-ej/ej-application/-/commit/3e9f1558d4a049700a47c224878bc7fde8ec3340)  | Concluído |
| 03/10  | Garantia da autoria correta em teste de exclusão                           | Código                            | [Fix conversation API tests](https://gitlab.com/gces-ej/ej-application/-/commit/3e9f1558d4a049700a47c224878bc7fde8ec3340) | Concluído |
| 07/10  | Fechamento da issue sobre falha no teste de permissão da API criada na Sprint 1 | Planejamento/Doc | [Issue #50](https://gitlab.com/gces-ej/ej-application/-/issues/50)                                                                                      | Concluído   |

### Principais Conquistas

- Ajuste preciso do teste `test_update_conversation` para refletir a lógica de autorização real: uso do fixture `other_user` como não autor para validar retorno 403, alinhando com a permissão `IsOwnerOrSuperUser`.
- Correção do cliente utilizado no teste `test_patch_conversation_unauthenticated`, substituindo `api` (sem método PATCH) pelo cliente DRF `api_client`, garantindo resposta 401 para requisições não autenticadas.
- Inclusão do campo obrigatório `board` no payload do teste `test_put_conversation_full_update`, obedecendo validação do modelo `Conversation` com relação FK para `Board`.
- Atualização do método `ConversationViewSet.get_permissions()` para reconhecer explicitamente a ação `destroy`, atribuindo a permissão `IsOwnerOrSuperUser` para permitir exclusão apenas a autores ou superusuários.
- Garantia da autoria correta no teste `test_delete_conversation_by_author_succeeds`, atribuindo explicitamente `conversation.author = user` para satisfazer a verificação de permissão durante a deleção.

### Obstáculos Encontrados

- O método `ConversationViewSet.get_permissions()` originalmente não processava a ação `destroy`, aplicando permissões padrão (`IsAuthenticatedOnlyGetView`) que permitem apenas requisições GET. Isso fazia com que requisições DELETE retornassem erro 403, bloqueando a exclusão mesmo para usuários autorizados.

- No teste de exclusão `test_delete_conversation_by_author_succeeds`, mesmo após ajustar a permissão no ViewSet, o teste falhava porque o objeto `conversation` não tinha o `user` como autor. A permissão `IsOwnerOrSuperUser` exige que `request.user` seja exatamente o autor do objeto para permitir a ação, o que não estava assegurado no fixture de teste. Foi necessário atribuir explicitamente `conversation.author = user` para que o teste validasse corretamente a autorização e aprovasse a exclusão.

### Lições Aprendidas

- É fundamental que `get_permissions()` do ViewSet trate explicitamente todas as ações REST, principalmente `destroy`, para garantir segurança e evitar gaps de autorização.
- Fixtures devem ser cuidadosamente escolhidos e configurados; clientes de teste sem a implementação necessária podem gerar falhas difíceis de detectar.
- Compreender a diferença semântica entre códigos HTTP 401 e 403 é essencial para implementar respostas API corretas e evitar ambiguidades nos testes.
- Testes de atualização completas via PUT precisam respeitar todas as restrições de modelo, incluindo campos obrigatórios e relações de banco de dados.
- Testes de autorização demandam que o estado do objeto testado (exemplo: autoria) esteja alinhado para validar corretamente as permissões de acesso.

  ### Metas Pessoais para a Próxima Sprint

- [ ] Expandir a cobertura dos testes automatizados para outras rotas da API, garantindo casos completos de autenticação e autorização.
- [ ] Documentar detalhadamente todas as alterações na API e testes para facilitar futuras manutenções.
- [ ] Propor melhorias no pipeline CI/CD para automação e monitoramento de testes relacionados a permissões e segurança.


