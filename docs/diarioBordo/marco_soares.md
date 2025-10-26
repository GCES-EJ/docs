# Diário de Bordo – Marco Tulio Soares

**Disciplina:** GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE  
**Equipe:** Empurrando Juntas  
**Comunidade/Projeto de Software Livre:** Empurrando Juntas  

---

## Sprint 0 – [25/08 – 10/09]

### Resumo da Sprint
Sprint com foco na aprendizagem do projeto e alinhamentos sobre próximos passos.

### Atividades Realizadas

| Data  | Atividade | Tipo | Link/Referência | Status |
|-------|------------|------|-----------------|---------|
| 08/08 | Inicialização do ambiente na máquina | Código | – | Concluído |
| 08/08 | Leitura da documentação | Documentação | [Documentação](https://gitlab.com/gces-ej/ej-application/-/tree/develop/docs?ref_type=heads) | Concluído |

### Maiores Avanços
- Ambiente rodando perfeitamente.  
- Compreensão do escopo do projeto.  
- Início da familiarização com as issues.  

### Maiores Dificuldades
- Entendimento completo da arquitetura.  
- Criação de máquina virtual Linux para rodar o projeto.  

### Aprendizados
- Escopo e parte da arquitetura do projeto aprendidos.  

### Plano Pessoal para a Próxima Sprint
- [ ] Focar nas issues abertas.  
- [ ] Conhecimento total da arquitetura do projeto.  
- [ ] Leitura completa da documentação.  

---

## Sprint 1 – [11/09 – 25/09]

### Resumo da Sprint
Implementada a funcionalidade de visualização da senha na tela de login para melhorar a usabilidade e a experiência do usuário.  

### Atividades Realizadas

| Data  | Atividade | Tipo | Link/Referência | Status |
|-------|------------|------|-----------------|---------|
| 25/09 | Criação de issue para implementar botão de visualizar senha | Issue | [#48](https://gitlab.com/gces-ej/ej-application/-/issues/48) | Concluído |
| 26/09 | Implementação do botão de visualização/ocultação de senha | Código | – | Concluído |
| 26/09 | Testes manuais de usabilidade | Teste | – | Concluído |
| 27/09 | Abertura de PR com a implementação | PR | [#48](https://gitlab.com/gces-ej/ej-application/-/issues/48) | Concluído |

### Maiores Avanços
- Inclusão do botão de visualizar/ocultar senha.  
- Melhoria da UX com ícones dinâmicos.  

### Maiores Dificuldades
- Manter o valor do campo sem recarregar a página.  
- Compatibilidade entre navegadores.  

### Aprendizados
- Manipulação de formulários no frontend.  
- Boas práticas de UX em autenticação.  

### Plano Pessoal para a Próxima Sprint
- [ ] Criar mensagens de erro mais claras.  
- [ ] Estudar segurança em formulários.  

---

## Sprint 2 – [26/09 – 08/10]

### Resumo da Sprint
Correções na funcionalidade de foto de usuário no perfil, permitindo agora substituir e remover imagens corretamente.  

### Atividades Realizadas

| Data  | Atividade | Tipo | Link/Referência | Status |
|-------|------------|------|-----------------|---------|
| 02/10 | Criação da issue para permitir excluir/alterar foto de usuário | Issue | [#56](https://gitlab.com/gces-ej/ej-application/-/issues/56) | Concluído |
| 07/10 | Implementação do fluxo de upload/atualização/remoção de foto | Código | – | Concluído |
| 07/10 | Ajustes no frontend para substituir/remover foto | Código | – | Concluído |
| 08/10 | Testes manuais e validação do comportamento | Teste | – | Concluído |

### Maiores Avanços
- Suporte completo para atualizar e excluir a foto de usuário.  
- Melhorias de UX na tela de perfil com estados claros.  

### Maiores Dificuldades
- Sincronização entre frontend e backend.  
- Tratamento de cache do navegador.  

### Aprendizados
- Manipulação de arquivos e tratamento de storage.  
- Padronização de endpoints e regras de autorização.  

### Plano Pessoal para a Próxima Sprint
- [ ] Documentar endpoints no Swagger.  
- [ ] Revisar limpeza de arquivos antigos no storage.  

---

## Sprint 3 – [09/10 – 26/10]

### Resumo da Sprint
Implementado o **modo escuro (dark mode)** na aplicação, ampliando a acessibilidade e oferecendo uma experiência mais agradável em ambientes com pouca luminosidade.  

### Atividades Realizadas

| Data  | Atividade | Tipo | Link/Referência | Status |
|-------|------------|------|-----------------|---------|
| 15/10 | Criação da issue para adicionar o modo escuro | Issue | [#62](https://gitlab.com/gces-ej/ej-application/-/issues/62) | Concluído |
| 18/10 | Implementação do modo escuro com alternância dinâmica (claro/escuro) | Código | – | Concluído |
| 20/10 | Ajustes de contraste e testes de acessibilidade | Teste | – | Concluído |
| 21/10 | Abertura de PR e revisão da implementação | PR | [#62](https://gitlab.com/gces-ej/ej-application/-/issues/62) | Concluído |

### Maiores Avanços
- Adição do modo escuro em toda a interface.  
- Alternância dinâmica entre temas via botão na interface.  
- Melhoria da experiência visual e conforto durante uso prolongado.  

### Maiores Dificuldades
- Ajuste de contraste em componentes do frontend.  
- Garantir consistência entre estilos claros e escuros.  

### Aprendizados
- Manipulação avançada de temas e variáveis CSS.  
- Boas práticas de acessibilidade e contraste em interfaces modernas.  

### Plano Pessoal para a Próxima Sprint
- [ ] Otimizar persistência do tema no navegador (localStorage).  
- [ ] Revisar responsividade com o novo tema ativo.  
