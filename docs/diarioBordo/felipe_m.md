# Diário de Bordo – Felipe Matheus Ribeiro Lopes

*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

---

## Sprint 0 – \[25/08 – 10/09]

### Resumo da Sprint

O foco inicial desta sprint foi a imersão no projeto "Empurrando Juntas", buscando compreender seus objetivos, a comunidade envolvida e a arquitetura geral da aplicação. Dediquei tempo à configuração do ambiente de desenvolvimento, um processo que apresentou desafios inesperados, mas que foram superados após identificar um conflito de dependências na minha máquina local.

### Atividades Realizadas

| Data | Atividade | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status |
| :--- | :--- | :--- |:---|:---|
| 29/08 | Estudo da documentação principal do projeto | Estudo | [ejparticipe.org](https://www.ejparticipe.org/docs/index.html) | Concluído |
| 01/09 | Configuração do ambiente de desenvolvimento local | Código | – | Concluído |
| 03/09 | Análise do guia de contribuição e fluxo de trabalho | Estudo | [Contributing.rst](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/contributing.rst?ref_type=heads) | Concluído |
| 04/09 | Leitura inicial sobre a arquitetura do software | Estudo | [Architecture.rst](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/architecture.rst?ref_type=heads) | Concluído |

### Maiores Avanços

- Sucesso na configuração completa do ambiente, com o projeto rodando localmente.
- Compreensão clara do processo de contribuição, desde o fork até o merge request.
- Obtenção de uma visão geral da arquitetura do sistema e suas principais tecnologias.

### Maiores Dificuldades

- A principal barreira foi ao tentar construir a imagem Docker do projeto. O processo falhava repetidamente, e após alguma investigação, descobri que a versão do Python no meu sistema (3.12) era incompatível com a exigida pelo projeto (3.11). A solução foi configurar um ambiente virtual (venv) com a versão correta, isolando as dependências do projeto.

### Aprendizados

- Conhecimento fundamental sobre a proposta e o impacto do projeto "Empurrando Juntas".
- Entendimento prático sobre a importância de ambientes de desenvolvimento isolados.
- Familiarização com o fluxo de contribuição em um projeto de software livre consolidado.

### Plano Pessoal para a Próxima Sprint

- [x] Aprofundar o estudo na estrutura de diretórios e no código-fonte.
- [x] Selecionar uma *issue* de baixa complexidade para tentar uma primeira contribuição.
- [x] Participar das discussões da comunidade para entender as prioridades atuais.

## Sprint 1 – [11/09 a 23/09]

### Resumo da Sprint

Nesta sprint, o foco foi a saúde do projeto, especificamente o pipeline de CI/CD que apresentava falhas recorrentes. Em uma sessão de pair programming com o **Yan Lucas**, investigamos os logs e o código dos testes. Conseguimos diagnosticar com precisão a causa raiz do problema, que estava relacionada a uma verificação incorreta de status codes de autenticação/autorização. O trabalho culminou na criação de uma issue detalhada para guiar a correção.

### Atividades Executadas

| Data | Atividade | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status |
|---|---|---|---|---|
| 15/09 | Análise em par do pipeline de CI/CD para diagnóstico da falha | Análise/Diagnóstico | [Issue #50](https://gitlab.com/gces-ej/ej-application/-/issues/50) | Concluído |
| 21/09 | Discussão e revisão da issue criada pelo Yan | Discussão/Doc | [Issue #50](https://gitlab.com/gces-ej/ej-application/-/issues/50) | Concluído |

### Principais Conquistas

* **Diagnóstico preciso da falha**: Juntos, identificamos que um teste esperava o status `403 Forbidden` (acesso negado por falta de permissão) quando a API corretamente retornava `401 Unauthorized` (acesso negado por falta de credenciais de autenticação válidas).
* **Fortalecimento da colaboração em equipe**: O trabalho em par com o Yan foi eficaz, permitindo que combinássemos nossas observações para chegar à solução.

### Obstáculos Encontrados

* A dificuldade inicial foi interpretar os logs do GitLab CI, que eram verbosos. Foi preciso paciência e um olhar atento para isolar o teste exato que estava falhando e, a partir daí, analisar o código-fonte correspondente.

### Lições Aprendidas

* **O valor do Pair Programming**: Depurar problemas complexos em dupla é muito mais eficiente. Uma segunda perspectiva ajuda a identificar detalhes que poderiam passar despercebidos.
* **Diferença prática entre `401 Unauthorized` e `403 Forbidden`**: Embora já conhecesse a teoria, ver o impacto direto dessa diferença em um teste automatizado solidificou o conceito.
* Como documentar um bug de forma colaborativa, garantindo que todo o time tenha o mesmo entendimento do problema.

### Metas Pessoais para a Próxima Sprint

* [ ] Colaborar com o Yan na implementação da correção para a issue `Falha no teste de permissão da API`.
* [ ] Fazer o code review do Merge Request para garantir a qualidade e a eficácia da solução.
* [ ] Pesquisar e propor melhorias em outros testes de API para evitar inconsistências semelhantes.

