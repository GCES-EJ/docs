# 📝 Relatório de Contribuição – Sprint 3

*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

*Período da Sprint:* 09/10 – 22/10

---

## 1. Objetivos da Sprint

Esta sprint teve como objetivo principal estabilizar a base de testes do projeto após a migração de infraestrutura e remoção de dependências do servidor Kubernetes obsoleto. As metas específicas incluíram:

- Identificar e corrigir testes que falhavam devido a mudanças na infraestrutura
- Atualizar objetos de exemplo e configurações de API desatualizadas
- Corrigir problemas de permissões e autenticação nos testes
- Melhorar a documentação automática da API com Swagger
- Dar continuidade à implementação da nova arquitetura de autenticação do EJ
- Implementar o modelo APIClient para autenticação via API Key
- Aumentar a taxa de sucesso da suíte de testes automatizados

---

## 2. Entregas Coletivas

| Entrega                                                      | Status (Concluído/Parcial/Pendente) | Link/Referência                                       | Observações                              |
|--------------------------------------------------------------|-------------------------------------|-------------------------------------------------------|------------------------------------------|
|                                                              |                                     |                                                       |                                          |

---

## 3. Contribuições Individuais



| Integrante                            | Contribuições                                                                                                                                                               | Links (PRs, Issues, Docs)                                                                                                                                                 | Observações                                                                                                                                                                                                               |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ana Joyce Guedes Amorim da Silva**      | [ej-users] Estender Modelo User para Federação de Identidades.                                                                                                              | [Issue #59](https://gitlab.com/gces-ej/ej-application/-/issues/59)                                                                                                        | Início da implementação da nova arquitetura de autenticação do EJ, dando seguimento à proposta do Giovanni.                                                                                                              |
| **João Filipe de Oliveira Souza**         |                                                                                                                                                                             |                                                                                                                                                                           |                                                                                                                                                                                                                           |
| **Caio Antonio Araújo Garcia de Almeida** |                                                                                                                                                                             |                                                                                                                                                                           |                                                                                                                                                                                                                           |
| **Danielle Rodrigues Silva**              | Implementação completa do modelo `APIClient` com interface administrativa, validações customizadas, métodos auxiliares e migrações de banco de dados para autenticação via API Key. | [Issue #63](https://gitlab.com/gces-ej/ej-application/-/issues/63)                                                                                                        | Implementação prática da arquitetura de autenticação via API Key proposta na sprint anterior, incluindo geração automática de `kid` único, controle de ativação/desativação e proteções na interface administrativa. |
| **Felipe Matheus Ribeiro Lopes**          |                                                                                                                                                                             |                                                                                                                                                                           |                                                                                                                                                                                                                           |
| **João Antonio Ginuino Carvalho**         | Análise e verificação das rotas **profiles**, **conversation** e **admin/administration**, com identificação e correção de endpoints duplicados no módulo *administration*. | [Issue #60](https://gitlab.com/gces-ej/ej-application/-/issues/60), [Commit](https://gitlab.com/gces-ej/ej-application/-/commit/8c8e78371162be6470f66ee4e4a942312678946f) | As demais rotas foram revisadas e não apresentaram inconsistências. O principal entregável da sprint foi a correção do bug de duplicação no módulo *administration*, garantindo maior integridade das rotas da aplicação. |
| **Leticia Arisa Kobayashi Higa**          | Documentação detalhada (@extend_schema) de todos os endpoints críticos no `ej_users/api.py` (autenticação, cadastro, recuperação de senha).                                | [Issue #61](https://gitlab.com/gces-ej/ej-application/-/issues/61), [MR #33](https://gitlab.com/gces-ej/ej-application/-/merge_requests/33)                              |                                                                                                                                                                                                                           |
| **Marco Soares de Oliveira**              |                                                                                                                                                                             |                                                                                                                                                                           |                                                                                                                                                                                                                           |
| **Marco Tulio Soares de Deus**            | Implementação do **modo escuro (dark mode)** na aplicação, com alternância dinâmica entre tema claro e escuro, ajustes de contraste e testes de acessibilidade.             | [Issue #62](https://gitlab.com/gces-ej/ej-application/-/issues/62), [PR #62](https://gitlab.com/gces-ej/ej-application/-/issues/62)                                      | A funcionalidade trouxe uma interface mais agradável e acessível, com persistência de tema e melhoria da experiência visual para o usuário.                                                                               |
| **Uires Carlos de Oliveira**              |                                                                                                                                                                             |                                                                                                                                                                           |                                                                                                                                                                                                                           |
| **Victor Augusto de Sousa Câmara**     |   Investigar e Remover o Módulo Experimental                                                                                                                                                                           |  [Issue #64](https://gitlab.com/gces-ej/ej-application/-/issues/64)                                                                                                                                                                         |   Remover código obsoleto e experimental melhora a manutenibilidade, reduz o débito técnico e foca o desenvolvimento em módulos de produção. É uma contribuição de baixo risco e alto impacto na qualidade do código.                                                                                                                                                                                                                        |
| **Victor Pontual Guedes Arruda Nóbrega**  | Correção sistemática de testes com dependências k8s obsoletas. Eliminação de 49 `AttributeErrors` em testes CBV, correção de permissões API, registro de ViewSets, atualização de objetos de teste e correção de métodos HTTP. | [Issue #54](https://gitlab.com/gces-ej/ej-application/-/issues/54), [Branch 54-remove-k8s-obsolete-tests](https://gitlab.com/gces-ej/ej-application/-/tree/54-remove-k8s-obsolete-tests) | Trabalho técnico detalhado com foco em estabilizar o pipeline CI/CD. Reduziu de 53 erros para 4 (92,5% de eliminação), aumentou testes passando de 479 para 515 (+36), melhorou taxa de sucesso de 85,2% para 91,5%. Incluiu correções em permissões, timestamps e métodos HTTP. |
| **Yan Guimarães**                         | Corrigiu o tratamento do campo `tags` no serializador da API, estabilizando o teste `test_create_conversation_success`. Atualizou o teste para validar o status da API.     | [Commit](https://gitlab.com/gces-ej/ej-application/-/commit/86372fc38bdcc30b4e6347fbabe4bc5d7b147d79)                              | Impacto direto na estabilidade da API e nos testes automatizados.                                                                                                                  |


---

## 4. Maiores Avanços

### Qualidade e Estabilidade dos Testes
- **Redução massiva de erros**: Eliminação de 92.5% dos erros (de 53 para 4 errors)
- **Aumento de testes bem-sucedidos**: Crescimento de 479 para 515 testes passando (+36 testes)
- **Melhoria da confiabilidade**: Taxa de sucesso aumentou de 85.2% para 91.5% (+6.3 pontos percentuais)

### Correções Técnicas Específicas
- **Testes CBV (Class-Based Views)**: Eliminados 49 AttributeErrors em testes de migração e permissões
- **Permissões de API**: Correção completa dos testes de autenticação (100% de sucesso em CBV permissions)
- **Rotas de API**: Registro do StereotypeRootViewSet, habilitando endpoints de votação de estereótipos
- **Documentação Swagger**: Correção de rotas duplicadas e melhoria na completude da documentação

### Arquitetura e Infraestrutura
- Início da implementação da nova arquitetura de autenticação federada
- Implementação completa do modelo APIClient com interface administrativa e validações customizadas
- Criação de migrações de banco de dados com índices para consultas de API Key
- Atualização de objetos de teste com 12 novos campos da API
- Padronização de métodos HTTP em testes (PATCH vs PUT)
- Melhoria na gestão de timestamps dinâmicos em comparações de testes

---

## 5. Maiores Dificuldades

### Desalinhamento entre Testes e Implementação
- **Permissões desatualizadas**: Testes esperavam permissões customizadas enquanto a API usava `IsAdminUser`, necessitando refatoração completa
- **Objetos de exemplo obsoletos**: Estrutura dos serializers evoluiu sem atualização correspondente nos objetos de teste, causando falhas de validação
- **Rotas não registradas**: ViewSets importantes não estavam registrados no router principal, gerando erros de `NoReverseMatch`

### Problemas de Configuração de Testes
- **Decorators faltantes**: Testes usando ORM do Django sem `@pytest.mark.django_db`, causando erros de acesso ao banco de dados
- **Métodos inexistentes**: Uso incorreto de `self.make_user()` que não existe nas classes base de receitas (mommy_recipes)
- **Timestamps dinâmicos**: Campos `created` e `modified` causavam falhas intermitentes por valores não-determinísticos

### Questões de API REST
- **Métodos HTTP inadequados**: Uso de PUT com dados parciais gerando erro 400 (Bad Request) em vez de 403 (Forbidden) esperado - deveria usar PATCH para updates parciais

---

## 6. Lições Aprendidas

### Boas Práticas de Testes
- **Sincronização contínua**: Objetos de teste devem evoluir junto com a API (serializers) para evitar falhas de validação
- **Uso de fixtures**: Fixtures do pytest são preferíveis à criação manual de objetos, garantindo isolamento, reusabilidade e consistência
- **Exclusão de valores dinâmicos**: Campos com valores não-determinísticos (timestamps, IDs gerados) devem ser excluídos das comparações de igualdade

### Arquitetura de Autenticação
- **Modelos Django com validações customizadas**: Implementação de campos UUIDField e CharField com validações específicas para garantir integridade dos dados
- **Interface administrativa robusta**: Criação de interfaces com proteções contra operações perigosas e filtros para facilitar gestão
- **Otimização de consultas**: Criação de índices compostos para melhorar performance em consultas frequentes de autenticação

### Conhecimentos Técnicos de API REST
- **Semântica de status codes HTTP**: 
  - 401 Unauthorized = usuário não autenticado
  - 403 Forbidden = usuário autenticado mas sem permissão
  - 400 Bad Request = erro de validação dos dados
- **PUT vs PATCH**: PUT exige todos os campos obrigatórios (update completo), PATCH permite atualização parcial de recursos

### Django e Django REST Framework
- **Decorators necessários**: Classes de teste que usam ORM do Django precisam do decorator `@pytest.mark.django_db`
- **Registro de ViewSets**: ViewSets devem ser explicitamente registrados no router para gerar URLs corretas e documentação adequada
- **Abordagem sistemática**: Correções metódicas e documentadas aceleram a identificação de padrões e problemas similares no projeto
- **Geração segura de chaves**: Uso de bibliotecas `secrets` para geração de API keys criptograficamente seguras e `uuid` para identificadores únicos
- **Migrações otimizadas**: Criação automática de índices de banco de dados durante migrações para otimizar consultas de autenticação

---

## 7. Planejamento para a Próxima Sprint

### Prioridade Alta
* [ ] Corrigir os 43 testes ainda falhando, visando atingir taxa de sucesso de 95%+
* [ ] Investigar e resolver os 4 errors remanescentes no módulo ej_dataviz (test_api.py)

### Melhoria Contínua
* [ ] Documentar padrões identificados de correção de testes para facilitar manutenção futura
* [ ] Criar guia de boas práticas para escrita de testes no projeto
* [ ] Estabelecer processo de revisão de testes ao modificar APIs e serializers
* [ ] Documentar arquitetura de autenticação via API Key para facilitar futuras implementações

