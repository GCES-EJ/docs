# Diário de Bordo – João Antonio Ginuino Carvalho


*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

---

## Sprint 0 – \[25/08 – 10/09]

### Resumo da Sprint

Sprint dedicada à ambientação no projeto, com foco nos primeiros passos, leitura do guia de contribuição e estudo da documentação.

### Atividades Realizadas

| Data  | Atividade                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
|-------|---------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|-----------|
| 08/08 | Configuração inicial do ambiente            | Código                            | –                                                                                            | Concluído |
| 08/08 | Leitura e estudo da documentação do projeto | Estudo                            | [Documentação](https://gitlab.com/gces-ej/ej-application/-/tree/develop/docs?ref_type=heads) | Concluído |

### Maiores Avanços

- Consegui rodar a aplicação localmente.
- Entendi o fluxo de contribuição do projeto através da [documentação de contribuição](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/contributing.rst?ref_type=heads).

### Maiores Dificuldades

- Utilização do inv. Solucionei esse problema dando o comando puro do Docker:

````bash
docker compose -f docker/docker-compose.yml build
docker compose -f docker/docker-compose.yml up
````


### Aprendizados

- Insights sobre a comunidade e compreensão da aplicação.
- Entendimento do fluxo de contribuição do projeto.

### Plano Pessoal para a Próxima Sprint

- [ ] Estudar o código-fonte em mais detalhes.
- [ ] Ler a documentação referente à arquitetura do projeto.  
- [ ] Estudar o inv. 

---

## Sprint 1 – \[11/09 – 25/09]

### Resumo da Sprint

O Empurrando Juntas está em processo de transformação para se tornar uma API independente do frontend. Para isso, é necessário mapear todas as rotas do projeto e documentá-las adequadamente. O grupo GCES anterior já mapeou algumas rotas, mas ainda falta documentar as realizadas e as pendentes. O objetivo desta sprint é finalizar esse mapeamento.

### Atividades Realizadas

| Data  | Atividade                                                          | Tipo    | Link/Referência                                      | Status    |
|-------|--------------------------------------------------------------------|---------|------------------------------------------------------|-----------|
| 19/09 | Mapeamento de rotas do projeto                                     | Revisão | -                                                    | Concluído |
| 20/09 | Atualização da documentação no GitPage com o relatório da Sprint 1 | Doc     | https://gces-ej.github.io/docs/#/relatorios/sprint_1 | Concluído |
| 21/09 | Documentação das rotas mapeadas                                    | Doc     | \[link PR]                                           | Parcial   |

### Maiores Avanços

- [x] Estudar o código-fonte em mais detalhes.
- [x] Ler a documentação referente à arquitetura do projeto.
- [x] Estudar o inv.

* Primeira issue criada na comunidade.

### Maiores Dificuldades

* Dificuldades com as ferramentas para mapear as rotas.

### Aprendizados

* Aprofundamento no entendimento do código-fonte.
* Noções de boas práticas na documentação de rotas.

### Plano Pessoal para a Próxima Sprint

* [ ] Finalizar a documentação das rotas mapeadas.
* [ ] Iniciar a implementação das rotas pendentes.