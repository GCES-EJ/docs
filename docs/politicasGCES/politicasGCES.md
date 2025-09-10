# Políticas de Contribuição – Projeto Empurrando Juntas (OSS)

## 1. Comunicação e integração
- Ponto de entrada para contribuições: [Grupo Telegram da comunidade](https://t.me/EJComum).  
- Para dúvidas técnicas ou problemas no desenvolvimento: contatar a equipe da [Pencillabs](https://pencillabs.tec.br/) e entrar no canal de comunicação do desenvolvimento.  
- Boas práticas de comunicação:
  - Ser educado(a) e paciente.
  - Descrever detalhadamente dúvidas, incluindo o que já foi tentado e logs de erros.
  - Priorizar comunicação em grupo, evitando mensagens privadas sem necessidade.

## 2. Estudo da aplicação
- Antes de contribuir, estudar:
  - [Guia de usuário](https://gitlab.com/gces-ej/ej-application/-/tree/develop/docs/user-guides?ref_type=heads) – conceitos básicos como conversa, jornada de participação e coleta de dados.  
  - [Guia de desenvolvimento/arquitetura](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/architecture.rst?ref_type=heads) – visão geral do código e funcionamento interno.

## 3. Escolhendo uma issue
- Ponto de partida: [Board de planejamento (Kanban)](https://gitlab.com/pencillabs/ej/ej-application/-/boards/5359092).  
- Tarefas priorizadas de acordo com [OKRs](https://rockcontent.com/br/blog/okr/) do projeto.  
- Discutir com o time qual issue começar primeiro.

## 4. Trabalhando na sua issue
- Branches principais:
  - **develop**: branch de desenvolvimento.
  - **prod**: branch de produção, atualizada a cada 15 dias.
- Para desenvolver:
  - Criar uma branch a partir da **develop**.
  - Nomear a branch com o ID da issue correspondente.
  - Desenvolver usando o ambiente configurado via [Docker](https://gitlab.com/pencillabs/ej/ej-application/-/blob/develop/README.md).

## 5. Testes e qualidade de código
- **Backend**: novos comportamentos devem ter testes unitários ([pytest](https://docs.pytest.org/en/8.0.x/)).  
- **Frontend**: alterações na jornada de participação devem ter testes de integração/aceitação ([Cypress](https://www.cypress.io/)).  
- Padrões de estilo:
  - **Python**: usar [Black](https://github.com/psf/black).  
  - **CSS/SASS**: metodologia [BEM](https://getbem.com/), flexbox/grid, medidas relativas (`rem`/`em`), cores via variáveis, media queries estruturadas.  
- Ferramentas adicionais:
  - **Ruff**: analisador estático ([Ruff](https://github.com/astral-sh/ruff)).  
  - **HTMX**: requisições assíncronas ([HTMX](https://htmx.org/)).  
- Garantir responsividade para telas ≥360px.

## 6. Boas práticas de programação
- Django segue arquitetura **MVT**:
  - **Models**: regras de negócio.
  - **Views**: conectar templates e models, alimentar templates.
  - **Templates**: mínima lógica, apenas exibir dados.
- Evitar overengineering e nomes genéricos como `utils` para código específico.  
- Uso de signals, decorators e middlewares deve ser criterioso.

## 7. Documentação e traduções
- Atualizar documentação com [Sphinx](https://www.sphinx-doc.org/en/master/) se a issue alterar funcionalidades ou fluxos.  
- Strings devem ser traduzíveis via internacionalização do Django (`locale/pt_BR/...`).

## 8. Merge requests
- Antes de solicitar revisão:
  - Faça auto-revisão do código e do MR (pode abrir como [draft](https://docs.gitlab.com/ee/user/project/merge_requests/drafts.html)).  
  - Garanta que todos os testes passaram.
- O MR será revisado por um revisor experiente.  
- Após aprovação, o **deploy contínuo** atualiza o ambiente de homologação e produção.
