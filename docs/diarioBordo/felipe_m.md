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

- [ ] Aprofundar o estudo na estrutura de diretórios e no código-fonte.
- [ ] Selecionar uma *issue* de baixa complexidade para tentar uma primeira contribuição.
- [ ] Participar das discussões da comunidade para entender as prioridades atuais.
