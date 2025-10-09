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

