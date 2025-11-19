# Diário de Bordo – João FIlipe de Oliveira SOuza 


*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

---

## Sprint 0 – \[25/08 – 10/09]

### Resumo da Sprint

Essa primeira etapa foi mais de exploração e reconhecimento do terreno. Montei o ambiente, li a documentação e comecei a me familiarizar com como o projeto funciona por dentro. Foi um sprint de adaptação e muitos "primeiros contatos".
### Atividades Realizadas

| Data  | Atividade                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
|-------|---------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|-----------|
| 01/09 | Configuração inicial do ambiente            | Código                            | –                                                                                            | Concluído |
| 02/09 | Leitura e estudo do documento contributing.rst do projeto | Estudo                            | [Contributing.rst](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/contributing.rst?ref_type=heads) | Concluído |
| 02/09 | Leitura do documento arquitetura.rst do projeto | Estudo                            | [Architecture.rst](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/architecture.rst?ref_type=heads) | Concluído |

### Maiores Avanços

- Configuração completa do ambiente local e execução do projeto.
- entendimento do fluxo de contribuição do projeto.
- Primeiro contato com a arquitetura do projeto (ainda superficial, mas já abriu caminho).

### Maiores Dificuldades

- Entender a DOcumentacao ja existente


### Aprendizados

- Noção Inicial do projeto
- Fluxo de contribuição do projeto.

### Plano Pessoal para a Próxima Sprint

- [ ] Estudar detalhadamente a estrutura de pastas do projeto.
- [ ] Observar e acompanhar as Issues abertas no repositório.

      
---

## Sprint 1 – \[11/09 – 23/09]

### Resumo da Sprint

Nesta sprint, avancei da fase de exploração para a prática efetiva no projeto. Criei e executei a Issue do erro sintático em um dos arquivos, que estava impedindo o projeto de rodar corretamente. Além disso, identifiquei um problema na pipeline, que bloqueava a passagem de qualquer commit, e iniciei a criação e execução de outras Issues, dando início ao processo de contribuição prática.

### Atividades Realizadas

| Data  | Atividade                                       | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status       |
| ----- | ----------------------------------------------- | --------------------------------- | --------------- | ------------ |
| 14/09 | Criação e execução da Issue do erro sintático   | Código/Issue                      | –               | Concluído    |
| 22/09 | Identificação e análise de problema na pipeline | Código/Discussão                  | –               | Em andamento |


### Maiores Avanços

- Criei e executei a Issue que corrigiu o erro sintático e liberou a execução correta do projeto.
- Identifiquei a falha na pipeline que impactava os commits.
- Ganhei maior familiaridade com a dinâmica prática do projeto.


### Maiores Dificuldades

- Ajustar o ambiente às falhas da pipeline.

### Aprendizados

- Entendi na prática como funciona a contribuição via Issues.
- Tive minha primeira experiência com erros em pipeline e percebi sua importância no fluxo.
- Dominei melhor a execução do projeto localmente.

### Plano Pessoal para a Próxima Sprint

- [ ] Dar continuidade na execução das Issues em aberto.
- [ ] Trabalhar na solução definitiva do problema da pipeline.
- [ ] Aprofundar o entendimento da arquitetura do projeto.


## Sprint 2 – [26/09 – 08/10]

### Resumo da Sprint

Na Sprint 2, o monitor Giovanni apresentou um novo desafio à equipe: aprimorar o sistema de autenticação do projeto. Ele registrou uma issue com diferentes sugestões e orientações, destacando como primeiro passo o estudo detalhado da documentação do modelo de autenticação atual.
### Atividades Realizadas

| Data  | Atividade                                                                 | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status       |
|-------|---------------------------------------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|--------------|
| 30/09 | Giovanni apresenta a necessidade de melhorias na autenticação             | Estudo                            | –                                                                                            | Concluído    |
| 02/10 | Criação da issue com detalhes da proposta                                 | Doc                               | https://gitlab.com/gces-ej/ej-application/-/issues/52                                        | Concluído    |
| 03/10 | Análise do fluxo atual de login e tokens de acesso                        | Estudo                            | –                                                                                            | Concluído    |
| 05/10 | Reunião da equipe para definir o novo modelo de autenticação              | Discussão                         | –                                                                                            | Concluído    |
| 08/10 | Documentação das decisões e próximos passos para implementação            | Doc                               | –                                                                                            | Em andamento |


### Maiores Avanços

- Análise do funcionamento atual do processo de autenticação
- Pesquisa sobre padrões e boas práticas de autenticação
- Planejamento e definição da nova arquitetura de autenticação

### Maiores Dificuldades

- Analisar o código existente e o modelo atual de autenticação, explorando diferentes padrões disponíveis e compreendendo em detalhe a proposta apresentada pelo monitor.

### Aprendizados

- Auth 2.0
- Federação de Identidades com Mapeamento e Chaves de API

### Plano Pessoal para a Próxima Sprint

- [ ] Enviar a proposta ao Giovanni para validação.
- [ ] Criar as issues relacionadas à implementação do novo modelo de autenticação.

## Sprint 4 – [10/10 – 19/11]

### Resumo da Sprint

Na sprint 4 demos continuidade a implementação da nova arquitetura de autenticação com a update do middleware de autenticação e unificação de usuários externos

### Atividades Realizadas

| Data  | Atividade                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
|-------|---------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|-----------|
| 15/10 | Identificação do que já havia sido implmentado e o que estava pendente | Discussão | - | Concluído |
| 20/10 | Começo dos estudos de como adequadar a arquiteura antiga a nova| Outro | -  | Concluído |
| 17/11 | Abertura de issue para começar implementação  | Código  | https://gitlab.com/gces-ej/ej-application/-/issues/69 | Concluído |
| 19/11 | Abertura de Merge Request | Código | https://gitlab.com/gces-ej/ej-application/-/merge_requests/41 | Concluído |

### Maiores Avanços

- Middleware de autenticação e unificação de usuários externos

## Maiores Dificuldades

- Adequar o código antigo ao novo padrão

### Aprendizados

- Middleware

### Plano Pessoal para a Próxima Sprint

- [ ] Finalizar a autenticação