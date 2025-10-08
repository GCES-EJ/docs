# Diário de Bordo – Danielle Rodrigues Silva

*Disciplina:* GERÊNCIA DE CONFIGURAÇÃO E EVOLUÇÃO DE SOFTWARE

*Equipe:* Empurrando Juntas

*Comunidade/Projeto de Software Livre:* Empurrando Juntas

---

## Sprint 0 – \[25/08 – 10/09]

### Resumo da Sprint

Durante a Sprint 0, foquei na configuração inicial do ambiente de desenvolvimento e no estudo das tecnologias e documentações necessárias para contribuir com o projeto EJ Application. Estudei sobre Docker e containers, li a documentação de contribuição e arquitetura do projeto, e consegui configurar todo o ambiente usando WSL no Windows, apesar das dificuldades iniciais.

### Atividades Realizadas

| Data  | Atividade                        | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                                                                              | Status    |
| ----- | -------------------------------- | --------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| 07/09 | Estudo sobre Docker              | Estudo                            | [Playlist Docker](https://www.youtube.com/watch?v=OERbOJZwGAU&list=PLViOsriojeLrdw5VByn96gphHFxqH3O_N)                                       | Concluído |
| 07/09 | Estudo da Guia para contribuição | Estudo                            | [Contributing Guide](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/contributing.rst?ref_type=heads) | Concluído |
| 07/09 | Estudo da arquitetura do projeto | Estudo                            | [Architecture Guide](https://gitlab.com/gces-ej/ej-application/-/blob/develop/docs/development-guides/pt-br/architecture.rst?ref_type=heads) | Concluído |
| 08/09 | Configuração do ambiente         | Código                            | [EJ Application Docs](https://gitlab.com/gces-ej/ej-application#documentation)                                                               | Concluído |

### Maiores Avanços

* Ambiente de desenvolvimento configurado e aplicação rodando localmente usando WSL.
* Compreensão inicial do processo para contribuir com o projeto através da documentação oficial.
* Familiarização com Docker e containers.

### Maiores Dificuldades

* Rodar a aplicação no computador Windows sem familiaridade com WSL.
* A configuração do ambiente com Docker demorou aproximadamente 1 hora para ser concluída.

### Aprendizados

* Noções sobre Docker e containers.
* Familiarização com WSL e sua integração com Windows.
* Compreensão da arquitetura do projeto EJ Application.
* Entendimento do fluxo de contribuição da comunidade.

### Plano Pessoal para a Próxima Sprint

- [x] Contribuir com pelo menos 1 PR.
- [x] Aprofundar o estudo sobre a arquitetura do projeto.
- [x] Analisar as issues disponíveis para identificar uma primeira contribuição.

---

## Sprint 1 – \[11/09 – 25/09]

### Resumo da Sprint

Breve descrição.

### Atividades Realizadas

| Data  | Atividade                   | Tipo    | Link/Referência | Status    |
| ----- | --------------------------- | ------- | --------------- | --------- |
| 03/09 | Implementação da função Y   | Código  | [link PR]       | Concluído |
| 05/09 | Revisão de PR de colega     | Revisão | [link PR]       | Concluído |
| 08/09 | Atualização de documentação | Doc     | [link wiki]     | Parcial   |

### Maiores Avanços

* [Exemplo] Primeiro PR aceito pela comunidade.

### Maiores Dificuldades

* Dificuldade com testes automatizados.

### Aprendizados

* Melhoria no uso de Git (branches, rebase).
* Importância de escrever commits claros.

### Plano Pessoal para a Próxima Sprint

* [ ] Melhorar conhecimento em testes.
* [ ] Aprofundar em Docker para rodar ambiente completo.

---


## Sprint 2 – \[26/09 – 08/10]

### Resumo da Sprint

Nesta sprint, meu foco foi estudar como é feita atualmente a comunicação e autenticação de aplicações externas com a API do EJ, além de levantar boas práticas para esse tipo de integração. A partir disso, elaborar a proposta de arquitetura que visa substituir o modelo atual de autenticação baseado em credenciais de usuário por uma abordagem de Federação de Identidades com acesso via API Key, mais segura e escalável para integrações com sistemas externos.



### Atividades Realizadas

| Data   | Atividade                                                                                     | Tipo     | Link/Referência                                                                 | Status     |
|--------|-----------------------------------------------------------------------------------------------|----------|----------------------------------------------------------------------------------|------------|
| 04/10  | Estudo do fluxo atual de autenticação do EJ (JWT, SimpleJWT, riscos e estrutura atual).       | Estudo   | [Issue #51](https://gitlab.com/gces-ej/ej-application/-/issues/51)              | Concluído  |
| 05/10  | Estudo de boas práticas para integrações via API Key, UUIDv7 e federação de identidades.      | Estudo   | [Issue #51](https://gitlab.com/gces-ej/ej-application/-/issues/51)              | Concluído  |
| 07/10  | Construção do documento de arquitetura com definição das camadas de dados e lógica.           | Documento| [Issue #51](https://gitlab.com/gces-ej/ej-application/-/issues/51)  [Arquivo do Estudo](https://docs.google.com/document/d/1hSZnsbmtp1tcPWlt86P06GGv0V_nu3yQ3xxwJTOXjZ0/edit?tab=t.0)            | Concluído  |
| 08/10  | Elaboração e entrega dos diagramas (ASCII e .drawio) explicando a arquitetura proposta.       | Documento | [Arquivo do Estudo](https://docs.google.com/document/d/1hSZnsbmtp1tcPWlt86P06GGv0V_nu3yQ3xxwJTOXjZ0/edit?tab=t.0) | Concluído  |


### Maiores Avanços

* Compreensão completa do fluxo atual de autenticação do EJ usando JWT e os riscos associados à exposição de credenciais em integrações externas.
* Elaboração de uma proposta de arquitetura para federação de identidades com API Key, envolvendo a criação dos modelos `APIClient`, `ClientPermission` e o fluxo via middleware.


### Maiores Dificuldades

* A principal dificuldade foi encontrar um modelo que mantivesse a solução simples, sem recorrer a OAuth, mas que ainda garantisse segurança, rastreabilidade e controle de permissões por cliente.


### Aprendizados

### Aprendizados

* A autenticação atual do EJ é baseada em JWT (access/refresh token via SimpleJWT), exigindo credenciais de usuário para aplicações externas.
* Esse modelo apresenta riscos como acoplamento de senha, fragilidade em mudanças de senha e exposição em sistemas terceiros.
* O uso de API Key como autenticação de sistemas é uma alternativa mais segura para integrações service-to-service.
* A Federação de Identidades permite associar um `external_uuid` de outra aplicação a um `User` interno, sem depender de e-mail ou senha.
* O UUIDv7 é recomendado por ser único e ordenável no tempo, facilitando auditoria e rastreabilidade.
* A separação entre autenticação (API Key) e autorização (`ClientPermission`) é fundamental para garantir segurança e controle por cliente.


### Plano Pessoal para a Próxima Sprint

* [ ] Criar issues para implementar essa solução 
* [ ] Implementar solução.
---