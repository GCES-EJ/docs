# Diário de Bordo – Marco Tulio Soares


*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

---

## Sprint 0 – \[25/08 – 10/09]

### Resumo da Sprint

Sprint com foco na aprendizagem do projeto e alinhamentos sobre prixmos passos.

### Atividades Realizadas

| Data  | Atividade                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                              | Status    |
|-------|---------------------------------------------|-----------------------------------|----------------------------------------------------------------------------------------------|-----------|
| 08/08 | Inicialização do ambiente na maquina           | Código                            | –                                                                                            | Concluído |
| 08/08 |  | Leitura da documentação                           | [Documentação](https://gitlab.com/gces-ej/ej-application/-/tree/develop/docs?ref_type=heads) | Concluído |


### Maiores Avanços

- Ambiente rodando perfeitamente.
- Compreensão do escopo do projeto.
- Comecei a entender mais a fundo com foco na resolução de issues.

### Maiores Dificuldades

- Compreensão da arquitetura.
- Criação de uma maquina virtual linux para rodar o projeto.


### Aprendizados

- Escopo aprendido.
- Arquitetura parcial do projeto aprendida.

### Plano Pessoal para a Próxima Sprint

- [ ] Ter um foco maior nas issues do projeto.
- [ ] Conhecimento total da aqrquitetura do projeto.
- [ ] Amplo conhecimento da documentação.

## Sprint 1 – \[11/09 – 25/09]

### Resumo da Sprint

Nesta sprint foi implementada a funcionalidade de visualização da senha na tela de login. A melhoria visa facilitar a usabilidade do sistema, permitindo que o usuário confira se digitou corretamente sua senha antes de realizar o login.  

### Atividades Realizadas

| Data  | Atividade                                                      | Tipo    | Link/Referência                                                    | Status    |
|-------|----------------------------------------------------------------|---------|--------------------------------------------------------------------|-----------|
| 25/09 | Criação de issue para implementar botão de visualizar senha na tela de login | Issue | https://gitlab.com/gces-ej/ej-application/-/issues/48  | Concluído |
| 26/09 | Implementação do botão de visualização/ocultação de senha no frontend | Código | - | Concluído |
| 26/09 | Testes manuais de usabilidade e validação do comportamento em navegadores | Teste  | - | Concluído |
| 27/09 | Abertura de PR com a implementação da feature | PRs | https://gitlab.com/gces-ej/ej-application/-/issues/48| Concluído |

### Maiores Avanços

- [x] Inclusão do botão de visualizar/ocultar senha na tela de login.  
- [x] Melhoria na experiência do usuário, que agora pode validar a senha digitada.  
- [x] Uso de ícones dinâmicos (olho aberto/fechado) para indicar o estado do campo.  

### Maiores Dificuldades

* Ajustar o comportamento do botão mantendo o valor do campo de senha sem recarregar a página.  
* Garantir compatibilidade do recurso em diferentes navegadores e dispositivos.  

### Aprendizados

* Prática em manipulação de formulários no frontend.  
* Melhor entendimento sobre boas práticas de UX em autenticação.  

### Plano Pessoal para a Próxima Sprint

* [ ] Criar mensagens de erro claras para senhas inválidas.  
* [ ] Estudar alternativas de segurança para formulários de autenticação.  
