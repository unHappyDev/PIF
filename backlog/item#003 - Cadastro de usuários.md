# Pagina de cadastro

- Importância: **Alta**
- Data limite para design no Figma: 07/04/2025
- Margem de erro para design: 3 dias (10/04/2025)
- Data limite de desenvolvimento: 14/04/2025
- Margem de erro: 1 semana (21/04/2025)

## Descrição

A pagina para cadastrar novos usuários de qualquer tipo no sistema.

## Requisitos

### Front-End

1. Deve haver um botão para selecionar o tipo de usuário que será cadastrado, *aluno*, *professor* ou *secretaria*.
   - Pode ser um Dropdown ou botões de seleção (radio buttons).
   - Dependendo da escolha, os campos adicionais para Aluno ou Professor devem aparecer dinamicamente.
2. Por padrão todos os tipos de usuários devem ter os campos *nome*, *email*, *data de nascimento*.
3. Os dados de todos os campos devem ser validados de acordo com os seus campos antes de serem enviados o Back-End.
4. Se o Back-End retornar que o usuário foi cadastrado com sucesso, exibir isso na tela e liberar para fazer um novo cadastro.

#### Aluno

- Deve conter também espaços para preencher os seguintes dados: *curso*, *semestre*, pode ser um Dropdown com os dados já guardados no banco de dados.
- O RA do aluno gera gerado automaticamente.

#### Professor

- Deve conter espaços para preencher os seguintes dados: *disciplinas*, pode ser um Dropdown com os dados já guardados no banco de dados.


### Back-End

1. Só usuários da secretaria podem acessa-la.
2. A senha dos novos usuários deve ser gerada automaticamente, usando seu *RA* e *data de nascimento*.
3. Não pode haver conflitos de *RA* e/ou *Email*.
4. Caso aconteça algum erro retornar erro informando a sua causa, caso contrario retornar que o usuário foi cadastrado com sucesso.
