# Diário de Bordo – Ana Joyce Guedes Amorim da Silva

*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

---

## Sprint 0 – [25/08 – 10/09]

### Resumo da Sprint

Esta sprint inicial foi focada na ambientação com o projeto. As principais atividades envolveram a configuração do ambiente de desenvolvimento, a leitura da documentação e o entendimento do fluxo de contribuição da comunidade.

### Atividades Realizadas

| Data  | Atividade                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
|-------|---------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|-----------|
| 09/09 | Configuração do ambiente local              | Código                            | –                                                                                            | Concluído |
| 09/09 | Leitura da documentação de contribuição     | Estudo                            | [Contributing.rst](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/contributing.rst?ref_type=heads) | Concluído |
| 10/09 | Contato com o monitor para agendar reunião  | Discussão                         | –                                                                                            | Concluído |
| 10/09 | Alinhamento com a professora sobre demandas | Discussão                         | –                                                                                            | Concluído |

### Maiores Avanços

- Ambiente de desenvolvimento configurado e aplicação rodando localmente.
- Compreensão inicial do processo para contribuir com o projeto.

### Maiores Dificuldades

- A configuração inicial do ambiente com Docker apresentou alguns desafios, mas foram resolvidos seguindo a documentação e dicas de outros membros.

### Aprendizados

- Noções sobre a arquitetura do projeto Empurrando Juntas.
- Familiarização com o fluxo de trabalho da comunidade (issues, branches, merge requests).

### Plano Pessoal para a Próxima Sprint

- [ ] Aprofundar o estudo sobre a arquitetura do projeto.
- [ ] Analisar as issues que serão abertas para identificar uma primeira contribuição.
- [ ] Reunião com o monitor para alinhamento.

----

## Sprint 1 – [11/09 – 23/09]

### Resumo da Sprint


Durante a Sprint 1, nosso objetivo principal foi dar início às contribuições no projeto. Após duas reuniões com o monitor Giovanni, a equipe foi dividida em duas frentes de trabalho: documentação e pipeline.

A frente de documentação assumiu a responsabilidade de mapear todos os endpoints da aplicação. Essa tarefa é crucial para identificarmos as rotas ausentes e garantirmos que o backend opere de maneira autônoma, visto que o projeto se destina a ser um Software as a Service (SaaS). Eu optei por integrar a frente de pipeline, que teve como meta refatorar a pipeline existente, pois a anterior estava desativada, o que tornava inviável a integração de novas contribuições ao código.

### Atividades Realizadas

| Data  | Atividade                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
|-------|---------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|-----------|
| 20/09 | Estudo da pipeline anterior | Estudo    | –  | Concluído |
| 21/09 | Identificação dos erros | Estudo    |  –  | Concluído |
| 22/09 | Contato com o monitor para verificar se era possível retirar os testes que dependiam do servidro da Pencil ou se migravamos para um servidor do Lappis  | Discussão  | – | Concluído |
| 23/09 | Refatoração da Pipeline | Código | –   | Concluído |

### Maiores Avanços

- Definição de teste para a pipeline, correção de testes unitários do pytest.
- Reestrutação da branch principal.
- Repositório contribuível novamente.

### Maiores Dificuldades

- A pipeline antiga contava com teste E2E que operavam em um servidor da Pencil, que já não está mais disponível, então nenhum push estava sendo aceito no projeto, decidir se a gente manteria estes testes, e o grupo anterior que contribuiu com o projeto subiu bastante código com erros de lint e sintaxe, foi bem difícil refatorar tantos arquivos para passaremk no Black no Ruff e no Pytest.

### Aprendizados

- Black
- Ruff
- teste E2E
- configuração de pipeline
- lint

### Plano Pessoal para a Próxima Sprint

- [ ] Divisão de tarefas.
- [ ] Terminar de refatorar os testes unitários.
- [ ] Abertura de novas issues.
- [ ] Aumentar a qualidade do código.

## Sprint 2 – [26/09 – 08/10]

### Resumo da Sprint

Durante a Sprint 2, o monitor Giovanni nos apresentou um novo desafio: refatorar a autenticação do projeto. Ele abriu uma issue com propostas para a equipe, focando inicialmente no estudo da documentação do modelo de autenticação atual.

### Atividades Realizadas

| Data  | Atividade                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
|-------|---------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|-----------|
| 29/09 | Monitor entra com a proposta | Estudo    |  –  | Concluído |
| 06/10 | Abertura da Issue | Estudo    | https://gitlab.com/gces-ej/ej-application/-/issues/51  | Concluído |
| 06/10 | Início dos estudos da autenticação  | Estudo  | – | Concluído |
| 07/10 | Reunião com os envolvidos na sprint para fechamento do novo padrão | Discussão | –   | Concluído |

### Maiores Avanços

- Estudo de como a comunicação da autemticação é feita hoje
- Estudo dos padrões e boas prática da autenticação
- Definição da arquitetura nova

### Maiores Dificuldades

- Entender o código antigo e o padrão utilizado, entender os diferentes padrões de autenticação disponíveis e o proposto pelo o monitor

### Aprendizados

- Auth 2.0
- Federação de Identidades com Mapeamento e Chaves de API

### Plano Pessoal para a Próxima Sprint

- [ ] Mandar a proposta para aprovação do Giovanni.
- [ ] Abrir as issue para o novo padrão de autenticação.
