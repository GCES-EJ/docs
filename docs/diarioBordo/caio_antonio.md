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

## Sprint 2 – [26/09 – 08/10]

### Resumo da Sprint

Foco na melhoria da qualidade da documentação através de correções de typos e ortografia.

### Atividades Realizadas

| Data  | Atividade                                 | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status    |
|-------|-------------------------------------------|-----------------------------------|-----------------|-----------|
| 07/10 | Correção de typos e erros ortográficos na documentação | Doc                               | –               | Concluído |
| 07/10 | Revisão e padronização de textos da documentação | Doc                               | –               | Concluído |

### Maiores Avanços

- Melhoria significativa na qualidade e legibilidade da documentação.
- Padronização da linguagem e correção de inconsistências textuais.

### Maiores Dificuldades

- Identificar e corrigir todos os erros de forma consistente em diferentes seções.
- Manter a coerência terminológica ao longo de toda a documentação.

### Aprendizados

- Importância da revisão textual para a qualidade da documentação.
- Impacto positivo das correções na experiência do usuário ao consultar a documentação.

### Plano Pessoal para a Próxima Sprint

- [ ] Continuar monitorando a qualidade textual da documentação.
- [ ] Estabelecer processo de revisão para futuras adições à documentação.
- [ ] Contribuir com outras melhorias na documentação do projeto.

## Sprint 4 – [23/10 – 12/11]

### Resumo da Sprint

Implementação da funcionalidade de ordenação das conversas por data de criação, melhorando a organização e usabilidade da interface de listagem.

### Atividades Realizadas

| Data | Atividade | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status |
|------|-----------|-----------------------------------|-----------------|--------|
|      | Implementação da ordenação das conversas por data de criação | Código | – | Concluído |

### Maiores Avanços

- Implementação da funcionalidade de ordenação das conversas por data de criação.
- Melhoria na organização e usabilidade da interface de listagem de conversas.

### Maiores Dificuldades

- Garantir que a ordenação funcione corretamente em diferentes cenários de uso.
- Manter a performance da consulta mesmo com a ordenação aplicada.

### Aprendizados

- Importância da organização visual para melhorar a experiência do usuário.
- Técnicas de ordenação de dados em consultas ao banco de dados.

### Plano Pessoal para a Próxima Sprint

- [ ] Testar a funcionalidade de ordenação em diferentes cenários.
- [ ] Verificar se há necessidade de melhorias adicionais na interface.
- [ ] Contribuir com outras melhorias na funcionalidade de conversas.

## Sprint 5 – [13/11 – 03/12]

### Resumo da Sprint

Implementação da funcionalidade de compartilhamento do link da conversa para a área de transferência, a partir da tela de listagem, facilitando o compartilhamento de conversas entre usuários.

### Atividades Realizadas

| Data | Atividade | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status |
|------|-----------|-----------------------------------|-----------------|--------|
|      | Implementação da funcionalidade de compartilhar link da conversa para área de transferência | Código | – | Concluído |

### Maiores Avanços

- Implementação da funcionalidade de compartilhamento do link da conversa.
- Melhoria na facilidade de compartilhamento de conversas entre usuários.
- Integração com a API de área de transferência do navegador.

### Maiores Dificuldades

- Garantir compatibilidade com diferentes navegadores para a funcionalidade de área de transferência.
- Implementar feedback visual adequado para o usuário após o compartilhamento.

### Aprendizados

- Uso de APIs do navegador para interação com a área de transferência.
- Importância de feedback visual para ações do usuário.
- Técnicas de geração e compartilhamento de links dinâmicos.

### Plano Pessoal para a Próxima Sprint

- [ ] Testar a funcionalidade de compartilhamento em diferentes navegadores.
- [ ] Verificar se há necessidade de melhorias adicionais na experiência de compartilhamento.
- [ ] Contribuir com outras melhorias na funcionalidade de conversas.
