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
