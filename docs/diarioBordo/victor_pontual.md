# Diário de Bordo – Victor Pontual Guedes Arruda Nóbrega

**Disciplina:** Gerência de Configuração e Evolução de Software
**Equipe:** Empurrando Juntas
**Comunidade/Projeto de Software Livre:** Empurrando Juntas

---

## Sprint 0 – *25/08 a 10/09*

### Resumo da Sprint

Esta sprint foi voltada à ambientação inicial no projeto. O foco esteve na leitura do guia de contribuição, estudo da documentação e configuração do ambiente para execução da aplicação.

### Atividades Executadas

| Data  | Atividade                                    | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
| ----- | -------------------------------------------- | --------------------------------- | -------------------------------------------------------------------------------------------- | --------- |
| 09/08 | Configuração do ambiente local               | Código                            | –                                                                                            | Concluído |
| 09/08 | Leitura e análise da documentação do projeto | Estudo                            | [Documentação](https://gitlab.com/gces-ej/ej-application/-/tree/develop/docs?ref_type=heads) | Concluído |

### Principais Conquistas

* Aplicação executada corretamente em ambiente local.
* Familiarização com o processo de contribuição da comunidade, apoiado pela [documentação oficial de contribuição](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/contributing.rst?ref_type=heads).

### Obstáculos Encontrados

* Inicialmente houve dificuldade para rodar os serviços via *inv*. O problema foi contornado utilizando os comandos diretos do Docker:

```bash
docker compose -f docker/docker-compose.yml build
docker compose -f docker/docker-compose.yml up
```

* Posteriormente, a solução definitiva foi configurar o projeto dentro do **WSL (Windows Subsystem for Linux)**, permitindo manter o uso do **invoke** normalmente e garantindo maior praticidade no fluxo de trabalho.

### Lições Aprendidas

* Melhor compreensão do ecossistema da comunidade.
* Noções iniciais sobre a arquitetura e fluxo de contribuição do projeto.

### Metas Pessoais para a Próxima Sprint

* [ ] Aprofundar a análise do código-fonte.
* [ ] Estudar a documentação de arquitetura do sistema.

---

## Sprint 1 – *11/09 a 23/09*

### Resumo da Sprint

Esta sprint foi dedicada à implementação de verificação de cobertura de testes no pipeline de CI/CD, incluindo correções extensivas no GitLab CI e melhorias na qualidade do código. O trabalho envolveu configuração de runners, correção de linting, formatação de código e estabelecimento de políticas de cobertura.

### Atividades Executadas

| Data  | Atividade                                          | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                                    | Status    |
| ----- | -------------------------------------------------- | --------------------------------- | -------------------------------------------------------------------------------------------------- | --------- |
| 20/09 | Implementação do job test-coverage no GitLab CI   | Código                            | [Branch 44-test_coverage_pipeline](https://gitlab.com/gces-ej/ej-application/-/tree/44-test_coverage_pipeline) | Concluído |
| 20/09 | Correção de configuração de runners obsoletos     | Código                            | Commit: `fix: remove tags k8s obsoletas para usar runners compartilhados`                         | Concluído |
| 20/09 | Correção de pull policy no GitLab CI              | Código                            | Commit: `fix: alterar pull_policy para always conforme requerido`                                 | Concluído |
| 20/09 | Correção de erro de sintaxe em src/ej_admin/api.py| Código                            | Commit: `fix: corrigir erro de sintaxe e reformatar arquivos com black`                          | Concluído |
| 23/09 | Correção de 58 erros do linter Ruff               | Código                            | Commit: `fix: corrigir todos os erros do linter Ruff`                                            | Concluído |
| 23/09 | Reformatação de código com Black                  | Código                            | Commit: `fix: reformatar src/ej_users/tests/test_api.py com black`                               | Concluído |
| 23/09 | Correção de caminhos incorretos no pipeline       | Código                            | Commit: `fix: corrigir caminhos incorretos no GitLab CI`                                         | Concluído |
| 23/09 | Adição de dependência pytest-cov                  | Código                            | Atualização do pyproject.toml                                                                    | Concluído |

### Principais Conquistas

* **Pipeline de cobertura funcional**: Implementado job `test-coverage` com threshold mínimo de 85% executado automaticamente em merge requests.
* **Correção completa do GitLab CI**: Pipeline totalmente funcional após correção de runners obsoletos, pull policies e caminhos incorretos.
* **Melhoria significativa na qualidade de código**: 
  - 29 arquivos reformatados com Black
  - 58 erros de linting corrigidos automaticamente
  - Imports não utilizados removidos
  - Comparações booleanas simplificadas
* **Configuração de artefatos**: Relatórios de cobertura em XML integrados à interface do GitLab.

### Obstáculos Encontrados

* **Runners obsoletos**: Pipeline inicialmente falhava devido a runners k8s inativos. Solucionado removendo as tags e utilizando runners compartilhados.
* **Configuração de pull policy**: Runners compartilhados do GitLab.com requerem `pull_policy: always` em vez de `if-not-present`.
* **Erros de linting extensivos**: 58 erros de qualidade de código que exigiram correção manual e automática.
* **Caminhos hardcoded**: Comandos `cd` com caminhos absolutos incorretos causavam falhas nos jobs.

### Lições Aprendidas

* Importância da configuração adequada de runners no GitLab CI para projetos open source.
* Valor das ferramentas automatizadas de qualidade de código (Black, Ruff) para manter padrões consistentes.
* Necessidade de ambientes de CI/CD bem configurados para garantir qualidade antes de merges.
* Benefícios da verificação automática de cobertura para manter qualidade de testes.

### Metas Pessoais para a Próxima Sprint

* [ ] Contribuir com melhorias na documentação do pipeline de CI/CD
* [ ] Investigar oportunidades de otimização nos testes existentes
* [ ] Estudar possíveis implementações de features relacionadas à área de cobertura

---

## Sprint 2 – *26/09 a 08/10*

### Resumo da Sprint

Nesta sprint concentrei meus esforços em estabilizar a base de testes automatizados e corrigir problemas estruturais que vinham causando falhas no pipeline de integração contínua. Trabalhei em ajustes de permissões, integração de rotas que precisavam ser expostas corretamente e manutenção/refatoração de testes para refletir o comportamento atual da aplicação.

### Atividades Executadas

| Data  | Atividade                                                      | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                 | Status    |
| ----- | -------------------------------------------------------------- | --------------------------------- | ------------------------------------------------------------------------------- | --------- |
| 07/09 | Correção e refatoração de testes que causavam quebras no CI     | Código                            | [Issue #54](https://gitlab.com/gces-ej/ej-application/-/issues/54)               | Concluído |
| 07/09 | Ajustes de permissões e integração de novas rotas na API       | Código                            | [Issue #54](https://gitlab.com/gces-ej/ej-application/-/issues/54)               | Concluído |
| 07/10 | Manutenção contínua dos testes automatizados e estabilidade CI | Código                            | -                                                                               | Concluído |

### Principais Conquistas

* Estabilização de testes que estavam provocando falhas recorrentes no pipeline.
* Correções estruturais e de permissões que permitiram a integração de novas rotas na API.
* Manutenção preventiva da suíte de testes para reduzir falsos positivos e melhorar a confiança no CI.

### Obstáculos Encontrados

* A necessidade de refatorar testes legados para refletir mudanças no comportamento das funções testadas — isso demandou análise cuidadosa e tempo.
* Dependências entre testes e mudanças de estado compartilhado causaram intermitência em alguns casos, exigindo isolamento e ajustes nos fixtures.

### Lições Aprendidas

* Testes precisam acompanhar a evolução do código; refatorações pequenas no código frequentemente exigem ajustes correspondentes nos testes.
* Ajustes de permissão e exposição de rotas têm impacto direto na cobertura e estabilidade dos testes de integração.
* Melhor comunicação entre quem altera rotas/permissions e quem mantém os testes reduz retrabalho.

### Metas Pessoais para a Próxima Sprint

* [ ] Continuar a refatoração dos testes restantes para eliminar flakiness.
* [ ] Documentar padrões de testes e fixtures usados no projeto.
* [ ] Apoiar a implementação das mudanças de autenticação propostas (quando aprovadas) para garantir compatibilidade dos testes.

---

## Sprint 3 – *09/10 a 22/10*

### Resumo da Sprint

Esta sprint foi dedicada à correção sistemática de testes que falhavam devido à migração de infraestrutura e remoção de dependências obsoletas do servidor k8s. O trabalho envolveu identificação, análise e correção de múltiplos problemas estruturais nos testes, incluindo permissões, configurações de API, objetos de exemplo desatualizados e problemas de setup em testes de migração.

### Atividades Executadas

| Data  | Atividade                                                           | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                | Status    |
| ----- | ------------------------------------------------------------------- | --------------------------------- | ------------------------------------------------------------------------------ | --------- |
| 09/10 | Criação de Issue #54 para remoção de testes com dependências k8s   | Documentação                      | [Issue #54](https://gitlab.com/gces-ej/ej-application/-/issues/54)            | Concluído |
| 10/10 | Correção de permissões em test_searched_boards_api                  | Código                            | Commit: `fix: corrigir status code esperado em test_searched_boards_api`      | Concluído |
| 12/10 | Correção de permissões IsAdminUser em testes de API admin          | Código                            | Commit: `fix: Correct API test permissions to use IsAdminUser`                | Concluído |
| 15/10 | Registro do StereotypeRootViewSet na API principal                  | Código                            | Commit: `fix: Register StereotypeRootViewSet in API router`                   | Concluído |
| 18/10 | Atualização do objeto CONVERSATION em examples.py                  | Código                            | Commit: `fix: Update CONVERSATION test example to match current API`          | Concluído |
| 19/10 | Correção de comparações de timestamp em testes de conversação       | Código                            | Commit: `fix: Remove modified field from conversation test comparisons`       | Concluído |
| 20/10 | Correção de uso de fixture em test_update_conversation              | Código                            | Commit: `fix: Use existing conversation fixture in test_update_conversation`  | Concluído |
| 21/10 | Correção de método HTTP (PATCH vs PUT) em teste de update          | Código                            | Commit: `fix: Use PATCH instead of PUT in test_update_conversation`           | Concluído |
| 22/10 | Correção massiva de testes CBV (migration e permissions)           | Código                            | Branch: `54-remove-k8s-obsolete-tests`                                        | Concluído |

### Principais Conquistas

* **Eliminação de 92.5% dos erros**: Reduziu de 53 errors para 4 errors (eliminados 49 AttributeErrors)
* **Aumento significativo de testes passando**: De 479 para 515 testes passando (+36 testes, aumento de 7.5%)
* **Melhoria da taxa de sucesso**: De 85.2% para 91.5% (+6.3 pontos percentuais)
* **Correções sistemáticas aplicadas**:
  - 3 testes de permissões API admin corrigidos (status codes 401/403)
  - StereotypeRootViewSet registrado habilitando rotas de API de estereótipos
  - Objeto CONVERSATION atualizado com 12 campos novos da API
  - Testes de timestamp corrigidos para não falhar em valores dinâmicos
  - Método HTTP correto (PATCH) aplicado em testes de update parcial
  - 49 AttributeErrors eliminados em testes CBV (migration, permissions, url_migration)
  - 100% dos testes de CBV permissions passando (10/10)

### Obstáculos Encontrados

* **Permissões desalinhadas**: Testes esperavam permissões customizadas mas API usava `IsAdminUser`
* **API routes não registradas**: `StereotypeRootViewSet` não estava no router principal causando `NoReverseMatch`
* **Objetos de teste desatualizados**: Estrutura de serializers havia evoluído mas objetos de exemplo não
* **Timestamps dinâmicos**: Campos `created` e `modified` causavam falhas por valores não-determinísticos
* **Métodos inexistentes**: Uso de `self.make_user()` que não existe nas classes base de receitas
* **Acesso ao banco sem decorator**: Testes usando recipes sem `@pytest.mark.django_db`
* **Método HTTP incorreto**: Uso de PUT com dados parciais causando erro 400 em vez de 403

### Lições Aprendidas

* Importância de manter objetos de teste sincronizados com mudanças na API (serializers)
* Status codes HTTP têm significados específicos: 401 (não autenticado) vs 403 (sem permissão) vs 400 (validação)
* PUT vs PATCH: PUT requer todos os campos (partial=False), PATCH permite update parcial
* Necessidade de decorar classes/métodos com `@pytest.mark.django_db` quando usam ORM do Django
* Fixtures do pytest são preferíveis a criação manual de objetos em testes
* ViewSets precisam ser explicitamente registrados no router para gerar URLs corretas
* Campos dinâmicos (timestamps) devem ser excluídos de comparações de igualdade em testes

### Metas Pessoais para a Próxima Sprint

* [ ] Corrigir os 43 testes ainda falhando para aumentar taxa de sucesso para 95%+
* [ ] Documentar padrões identificados de correção de testes para facilitar manutenção futura
* [ ] Criar guia de boas práticas para escrita de testes no projeto
* [ ] Investigar e corrigir os 4 errors remanescentes em test_api.py do ej_dataviz