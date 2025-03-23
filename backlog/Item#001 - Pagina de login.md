# Pagina de Login

- Importância: **Alta**
- Data limite para design no Figma: 24/03/2025
- Margem de erro para design: 3 dias (27/03/2025)
- Data limite de desenvolvimento: 31/03/2025
- Margem de erro: 1 semana (07/04/2025)

## Descrição

A Tela de login será a primeira tela que todos os tipos de usuários terão que acessar.

## Requisitos

Deve ser simples e intuitiva, com apenas dois campos para serem preenchidos, login e senha, um botão de *entrar*, um para *esqueci minha senha* e outro para *alterar tipo de usuário*.

### Front-End

1. campos de entrada.
    - Independente o tipo de usuário, deve ser enviado ao Back-End, pelo body, uma variável chamada *login*, com RA ou email, e uma variável chamada *senha*, com a senha digitada pelo usuário.
    - O campo da senha deve ter seus caracteres mascarados.
    - Deve aparecer um botão no campo da senha, quando se passa o mouse sobre ele, que, quando **mantido** pressionado, exibe a senha.

2. Botão de esqueci minha senha.
    - O usuário será redirecionado para a pagina de alteração de senha.
    - Serão usados os mesmo critérios para a alteração de senha padrão.
3. Após o login ser aprovado pelo Back-End, deve guardar o Token JWT de acesso que será enviado como resposta.

### Back-End

1. Deve ser feita uma validação na variável *login*, recebida do Front-End, para reconhecer se é um **RA** ou **e-mail**.
2. No primeiro login de um usuário ele entrará com uma senha padrão, definida automaticamente no cadastro e o sistema deve obriga-lo a trocar essa senha redirecionando-o diretamente para a pagina de alteração de senha.
3. Após a confirmação que o login foi efetuado correntemente, deve retornar ao Front-End o Token JWT do usuário, onde pode ser armazenado o id  e o tipo do usuário.

