# Documentação Swagger – *EJ Application*

> Este guia explica como visualizar a **documentação da API** no **Swagger**, adicionar novas rotas e testá-las diretamente pela interface web interativa.

---

## 1. O que é o Swagger

O **Swagger UI** é uma interface gráfica que permite **visualizar, testar e documentar** endpoints de uma API REST de forma interativa. Ele é gerado automaticamente a partir das configurações e anotações do código, proporcionando uma visão clara da estrutura da aplicação e das rotas disponíveis.

---

## 2. Como visualizar o Swagger

1. **Execute a aplicação Django** normalmente.
2. Acesse o endpoint do Swagger no navegador:

```http request
http://localhost:8000/api/v1/swagger/
```

> Substitua `localhost` e `8000` conforme o host e porta configurados no seu ambiente.

**Código relacionado à configuração do Swagger:**  

````txt
https://gitlab.com/gces-ej/ej-application/-/blob/develop/src/ej/urls.py?ref_type=heads
````

> Alterações nele modificam automaticamente o swagger.

---

## 3. Módulos de Rotas da Aplicação

Abaixo estão os principais módulos responsáveis por gerenciar as **URLs** da aplicação **EJ Application**, com links diretos para os arquivos no repositório oficial.

| Módulo / App                | Caminho do Arquivo                                                                                                                                                         | Descrição                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| **Usuários**                | [ej_users/urls/user.py](https://gitlab.com/gces-ej/ej-application/-/blob/develop/src/ej_users/urls/user.py?ref_type=heads)                                                 | Rotas relacionadas às operações de usuários (perfil, listagem, etc). |
| **Contas / Autenticação**   | [ej_users/urls/account.py](https://gitlab.com/gces-ej/ej-application/-/blob/develop/src/ej_users/urls/account.py?ref_type=heads)                                           | Rotas de login, logout, registro e autenticação.                     |
| **Administração**           | [ej_admin/urls.py](https://gitlab.com/gces-ej/ej-application/-/blob/develop/src/ej_admin/urls.py?ref_type=heads)                                                           | Rotas administrativas (painel, gerenciamento e API administrativa).  |
| **Admin API**               | [ej_admin/api_urls.py](https://gitlab.com/gces-ej/ej-application/-/blob/develop/src/ej_admin/api_urls.py?ref_type=heads)                                                   | Endpoints REST voltados ao módulo administrativo.                    |
| **Quadros (Boards)**        | [ej_boards/urls.py](https://gitlab.com/gces-ej/ej-application/-/blob/develop/src/ej_boards/urls.py?ref_type=heads)                                                         | Rotas de criação, edição e visualização de quadros.                  |
| **Conversas Públicas**      | [ej_conversations/urls/public_conversations.py](https://gitlab.com/gces-ej/ej-application/-/blob/develop/src/ej_conversations/urls/public_conversations.py?ref_type=heads) | Endpoints para conversas acessíveis publicamente.                    |
| **Conversas Privadas**      | [ej_conversations/urls/conversations.py](https://gitlab.com/gces-ej/ej-application/-/blob/develop/src/ej_conversations/urls/conversations.py?ref_type=heads)               | Rotas de threads e mensagens privadas.                               |
| **Comentários**             | [ej_conversations/urls/comments.py](https://gitlab.com/gces-ej/ej-application/-/blob/develop/src/ej_conversations/urls/comments.py?ref_type=heads)                         | Rotas de criação, edição e exclusão de comentários.                  |
| **DataViz (Visualizações)** | [ej_dataviz/urls.py](https://gitlab.com/gces-ej/ej-application/-/blob/develop/src/ej_dataviz/urls.py?ref_type=heads)                                                       | Rotas que geram gráficos e visualizações de dados.                   |
| **Integrações**             | [ej_integrations/urls.py](https://gitlab.com/gces-ej/ej-application/-/blob/develop/src/ej_integrations/urls.py?ref_type=heads)                                             | Rotas voltadas para integrações externas (APIs de terceiros).        |
| **Perfis**                  | [ej_profiles/urls.py](https://gitlab.com/gces-ej/ej-application/-/blob/develop/src/ej_profiles/urls.py?ref_type=heads)                                                     | Rotas de exibição e edição de perfis de usuários.                    |

---

<center>

## Histórico de Versão

</center>

<div style="margin: 0 auto; width: fit-content;">

| Data       | Versão | Descrição               | Autores                                  |
|------------|--------|-------------------------|------------------------------------------|
| 06/10/2025 | `1.0`  | Criação do documento    | [João Ginuino](https://github.com/i-JSS) |
| 07/10/2025 | `1.1`  | Adiciona link das rotas | [João Ginuino](https://github.com/i-JSS) |

</div>