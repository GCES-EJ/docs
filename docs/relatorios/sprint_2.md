# 📝 Relatório de Contribuição – Sprint 2

*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

*Período da Sprint:* 26/09 – 08/10

---

## 1. Objetivos da Sprint

Nesta sprint, o foco da equipe foi consolidar a documentação automática da API utilizando o Swagger, corrigir e validar a documentação existente para garantir completude e precisão. Além disso, foram implementadas melhorias significativas na experiência do usuário, com correção de funcionalidades essenciais como upload e remoção de fotos de perfil. A sprint também priorizou a correção de falhas em testes automatizados que estavam impactando o pipeline de CI/CD, garantindo maior estabilidade no processo de integração contínua. Por fim, foi realizado um estudo aprofundado sobre unificação de usuários com APIs externas, visando resolver o problema de gestão complexa de contas e senhas quando outras aplicações utilizam o EJ como API, propondo soluções com API Key e middleware customizado para facilitar essa integração.

---

## 2. Entregas Coletivas

| Entrega | Status (Concluído/Parcial/Pendente) | Link/Referência | Observações |
| ------- | ----------------------------------- | --------------- | ----------- |
| Documentação do Swagger | Concluído | [Documentação Swagger](https://gces-ej.github.io/docs/#/notes/Swagger) | Guia completo de uso da ferramenta |
| Estudo para Unificação de Usuários com APIs Externas | Concluído | [Arquivo do Estudo e Arquitetura](https://docs.google.com/document/d/1hSZnsbmtp1tcPWlt86P06GGv0V_nu3yQ3xxwJTOXjZ0/edit?tab=t.0) | Estudo de boas práticas para comunicação entre APIs externas e EJ, incluindo proposta de solução com API Key e middleware customizado |


---

## 3. Contribuições Individuais

| Integrante                       | Contribuições | Links (PRs, Issues, Docs) | Observações |
| -------------------------------- | ------------- | ------------------------- | ----------- |
| Ana Joyce Guedes Amorim da Silva |               |                           |             |
| Caio Antonio de Oliveira         |               |                           |             |
| Danielle Rodrigues Silva         | Estudo do fluxo de autenticação atual do EJ e boas práticas com API Key e federação de identidades. Elaboração do estudo e da proposta de arquitetura para o problema. | [Issue #51](https://gitlab.com/gces-ej/ej-application/-/issues/51), [Arquivo do Estudo e Arquitetura](https://docs.google.com/document/d/1hSZnsbmtp1tcPWlt86P06GGv0V_nu3yQ3xxwJTOXjZ0/edit?tab=t.0)  | Estudei a estrutura de autenticação atual do sistema e propus uma nova arquitetura mais segura e flexível para integrações externas. Essa proposta e estudo ainda serão avaliados pelo monitor Giovanni Giampauli para então serem implementados nas próximas sprints. |
| Felipe Matheus Ribeiro Lopes     |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |
| João Antonio Ginuino Carvalho    | Estudo do Swagger, documentação inicial do relatório 2, documentação de como utilziar o Swagger.                                         | [Documentação Swagger](https://gces-ej.github.io/docs/#/notes/Swagger)                                                              | Estudei o Swagger para entender como ele pode ser usado para documentar as rotas automaticamente. Como nunca tinha trabalhado com essa ferramenta antes, foi um desafio inicial, mas consegui aprender seus recursos e como aplicá-los no projeto. Além disso, documentei os aprendizados no pages da disciplina. |
| João Filipe de Oliveira Silva    |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |
| Leticia Arisa Kobayashi Higa     | Análise, estudo e correção da documentação da API (Swagger), registrando ViewSets que estavam ausentes. Criação da issue e MR da tarefa. | [Issue](https://gitlab.com/gces-ej/ej-application/-/issues/53), [MR](https://gitlab.com/gces-ej/ej-application/-/merge_requests/30) | Analisei a documentação da API e identifiquei que ViewSets (ClusterViewSet, StereotypeRootViewSet) estavam ausentes por não serem registrados no urls.py. Corrigi o router principal para expor as rotas faltantes e formalizei a tarefa criando a issue e o commit correspondentes.                              |
| Marco Soares de Oliveira         |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |
| Marco Tulio Soares de Deus       | Correcao: usuarios agora podem excluir e alterar a foto de perfil (antes nao era possivel).                                             | [Issue 56](https://gitlab.com/gces-ej/ej-application/-/issues/56)                                                                   | Ajustei o fluxo de upload para permitir atualizacao e remocao da foto de usuario, cobrindo os cenarios de adicionar, substituir e excluir a imagem.                                                                                                                                                               |
| Uires Carlos de Oliveira         |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |
| Victor Augusto Câmara de Oliveira |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |
| Victor Pontual Guedes Arruda Nóbrega |                                                                                                                                          |                                                                                                                                     |                                                                                                                                                                                                                                                                                                                   |
| Yan Guimarães                    | Correção de testes de API de conversas e ajustes de permissões. Fechamento da issue sobre falha no teste de permissão da API. | [Issue #50](https://gitlab.com/gces-ej/ej-application/-/issues/50), [Commit](https://gitlab.com/gces-ej/ej-application/-/commit/3e9f1558d4a049700a47c224878bc7fde8ec3340) | Corrigiu múltiplos testes de API que falhavam, incluindo permissões, autenticação e validações. Trabalho técnico detalhado com foco em estabilizar o pipeline CI/CD. |

---

## 4. Maiores Avanços

  * Swagger implementado e documentado: Equipe dominou a ferramenta e criou documentação completa de uso.
  * API mais completa: ViewSets ausentes foram identificados e registrados, tornando a API mais consistente.
  * Melhoria na experiência do usuário : Funcionalidades como upload/remoção de foto de perfil foram corrigidas.
  * Estabilização dos testes : Correção de múltiplos testes de API que estavam causando falhas no pipeline.
  * Estudos de arquitetura avançados: Proposta detalhada para modernização do sistema de autenticação com API Keys e federação de identidades.

---

## 5. Maiores Dificuldades

  * Complexidade da estrutura de URLs: Navegar na estrutura de URLs do projeto (API vs. Django tradicional) para identificar rotas faltantes.
  * Depuração de testes complexos: Entender falhas sutis em testes de permissão e autorização que exigiam análise detalhada do código.
  * Aprendizado de novas ferramentas: Membros que nunca trabalharam com Swagger precisaram de tempo para dominar a ferramenta.
  * Consistência entre frontend e backend: Garantir comportamento correto em funcionalidades como upload de fotos, especialmente relacionado a cache do navegador.


---

## 6. Lições Aprendidas

* Swagger como ferramenta de documentação: Criação e manutenção de documentação automática de rotas, eliminando a necessidade de documentação manual.
* Importância do registro correto de ViewSets: Um ViewSet só é exposto na API se for explicitamente registrado no router do urls.py.
* Diferenças entre códigos HTTP 401 e 403: Compreensão prática da diferença entre "Unauthorized" (sem credenciais) e "Forbidden" (sem permissão).
* Testes de API requerem configuração precisa: Fixtures, permissões e estado dos objetos devem estar alinhados para validar corretamente as funcionalidades.
* Segurança em integrações externas: Importância de usar API Keys em vez de credenciais de usuário para integrações service-to-service.
* Arquitetura de autenticação: Separação entre autenticação (quem você é) e autorização (o que você pode fazer).

---

## 7. Planejamento para a Próxima Sprint

* [ ] Implementar a proposta de arquitetura de autenticação via API Key e federação de identidades

