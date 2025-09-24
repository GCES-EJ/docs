# Diário de Bordo – Caio Antonio

*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

---

## Sprint 0 – [25/08 – 10/09]

### Resumo da Sprint

Sprint com foco na aprendizagem do projeto e alinhamentos sobre próximos passos.

### Atividades Realizadas

| Data  | Atividade                                 | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
|-------|-------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|-----------|
| 05/09 | Inicialização do ambiente na máquina      | Código                            | –                                                                                            | Concluído |
| 05/09 | Leitura e estudo da documentação do projeto | Doc/Estudo                        | [Documentação](https://gitlab.com/gces-ej/ej-application/-/tree/develop/docs?ref_type=heads) | Concluído |

### Maiores Avanços

- Ambiente rodando corretamente localmente.
- Compreensão inicial do escopo do projeto.
- Entendimento do fluxo para começar a atuar em issues.

### Maiores Dificuldades

- Compreensão da arquitetura geral do sistema.
- Ajustes de ambiente e dependências para execução local.

### Aprendizados

- Visão do escopo e das principais áreas do projeto.
- Noções iniciais da arquitetura e da documentação.

### Plano Pessoal para a Próxima Sprint

- [ ] Focar na resolução de issues iniciais do projeto.
- [ ] Aprofundar no entendimento da arquitetura do sistema.
- [ ] Revisar e consolidar o estudo da documentação.



## Sprint 1 – [11/09 – 24/09]

### Resumo da Sprint

Evolução prática no projeto com foco na criação de issue e implementação de validação de senha forte.

### Atividades Realizadas

| Data  | Atividade                                                                 | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status    |
|-------|---------------------------------------------------------------------------|-----------------------------------|-----------------|-----------|
| 23/09 | Criação de issue para validação de senha forte                            | Discussão                         | https://gitlab.com/gces-ej/ej-application/-/issues/47               | Concluído |
| 23/09 | Implementação da validação de senha forte (>= 8 caract., letra maiúscula e número) | Código                            | https://gitlab.com/gces-ej/ej-application/-/merge_requests/27               | Concluído |

### Maiores Avanços

- Definição clara dos critérios de senha forte no projeto.
- Implementação válida cobrindo tamanho mínimo, presença de maiúscula e número.

### Maiores Dificuldades

- Ajustar a validação para contemplar diferentes cenários de entrada sem falsos positivos.

### Aprendizados

- Boas práticas de validação e mensagens de erro para UX.

### Plano Pessoal para a Próxima Sprint

- [ ] Criar testes adicionais para casos-limite de validação de senha.
- [ ] Documentar os critérios de senha no guia do usuário.
- [ ] Analisar feedback da equipe e ajustar a regra se necessário.
