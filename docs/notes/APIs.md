# Documentação de Endpoints Pendentes da API

Este documento descreve os endpoints da API que foram identificados no código mas que ainda não constam na documentação oficial.

## Autenticação

### Efetuar Logout

    POST /api/v1/token/logout/

Este endpoint permite que um usuário autenticado invalide seu token de atualização (`refresh_token`), efetivamente encerrando sua sessão de forma segura.

## Gerenciamento de Usuários

### Registrar um Novo Usuário

    /api/v1/users/

Este endpoint público (AllowAny) é responsável pelo cadastro de novos usuários na plataforma. Ele recebe os dados do usuário, como nome, e-mail e senha, e, se o registro for bem-sucedido, já retorna os tokens de acesso e atualização, permitindo o login automático do novo usuário.

### Iniciar Recuperação de Senha

    /api/v1/users/recover-password/

Este endpoint inicia a primeira etapa do fluxo de recuperação de senha. Ele permite que qualquer usuário solicite um link de redefinição ao fornecer seu endereço de e-mail. Por motivos de segurança, a API sempre retornará uma resposta de sucesso genérica para não expor quais e-mails estão cadastrados no sistema.

### Listar todos os Usuários

    /api/v1/users/

Destinado a fins administrativos, este endpoint retorna uma lista paginada com todos os usuários cadastrados na plataforma. O acesso é restrito e exige que o usuário autenticado tenha permissões de administrador (IsAdminUser).

### Finalizar Registro com secret_id

    /api/v1/users/{secret_id}/

Este endpoint possui a finalidade específica de concluir um processo de cadastro que ocorre em múltiplas etapas. Ele utiliza um secret_id fornecido na URL para identificar um usuário temporário e, com os dados enviados no corpo da requisição, finaliza seu registro, transformando-o em um usuário completo.