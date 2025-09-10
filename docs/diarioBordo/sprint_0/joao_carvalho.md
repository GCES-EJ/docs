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

- Utilização do inv, solucionei esse problema dando o comando puro do docker:
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