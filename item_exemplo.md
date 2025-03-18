# Item#002 - Tela de Cadastro

## **Descrição:**  
*A recepcionista cadastra os dados do aluno em um formulário. Ao finalizar o preenchimento, o sistema gera automaticamente um RA (login) e uma senha provisória, que são enviados para o e-mail do aluno. ***Em seguida, o aluno deve utilizar esses dados para acessar o sistema pela primeira vez e definir uma nova senha***.*  

## **Requisitos:**
Formulário contendo os dados pessoais do usuário (aluno), como listado abaixo:
- Identificação do paciente: Nome completo, data de nascimento, sexo/gênero, CPF, RG.
- Endereço e Contato: Endereço completo (rua, número, bairro, cidade, CEP, complemento), telefone, e-mail.
- Autorização para o uso de dados: Termo de consentimento informando sobre o uso dos dados pessoais, assinatura ou aceite digital, respeitando a Lei Geral de Proteção de Dados (LGPD) no Brasil (ou legislação equivalente).

## **Critérios de Aceitação:**
1. O sistema deve identificar automaticamente se a entrada fornecida pelo usuário é um CPF ou um endereço de e-mail e, a partir disso, aplicar regras de validação e tratamento específicas para cada tipo de dado.
2. Regras para o CPF.
   
    2.1. Deve conter 11 dígitos, todos numéricos.
   
    2.2. Gerar cálculo para validar a autenticidade do CPF.

3. Regras para o e-mail.		
   
    3.1. Seguir o padrão 'usuario@dominio' contendo pelo menos um @ e um domínio válido.
   
    3.2. Pode incluir checagem de TLD (top-level domain), por exemplo, .com, .br, .net e etc...
   
    3.3. Garantir que haja apenas números, pontos, sublinhados e alguns caracteres especiais antes do @.

4. Regras para a senha
   
    4.1. O tamanho mínimo será de 8 caracteres.
    4.2. Deverá conter letras minúsculas e pelo menos uma letra maiúscula, número e caractere especial (!@#$&'"%-).
   
    4.3. Impedir o uso de dados pessoais óbvios (nome, data de nascimento, CPF, etc.) dentro da senha, para dificultar adivinhações baseadas em informações públicas.
   
    4.4. Ao receber a senha, armazená-la usando algoritmos de hash seguros (bcrypt, argon2, scrypt) e não em texto puro.
   
    4.5. Política de ciclos de troca, a senha deverá ser alterada obrigatoriamente a cada 90 dias.
   
    4.6. Confirmar senha, a senha confirmada deve ser idêntica com a senha fornecida inicialmente.

5. Validar CEP.
   
    5.1. Garantir que o CEP utilizado é válido.

6. Permitir a criação da conta somente se o usuário concordar com os termos de uso do aplicativo.
7. Após concluir o cadastro, será atribuído a cada usuário um ID único. Esse ID será um número inteiro que começa em 1 e será incrementado automaticamente em 1 a cada novo usuário registrado.
8. Deve haver logs de erros e acertos.

9.  Ao finalizar o formulário, o sistema gera automaticamente um RA (login) e uma senha provisória, que são enviados para o e-mail do aluno cadastrado.
   	9.1. Ao logar pela primeira vez, o sistema deverá solicitar o login (RA e senha), digitar nova senha e confirmar nova senha, o sistema deve realizar a autenticação das senhas.

## **Protótipo / UI Design**:
**Link para o protótipo:** [Figma](https://www.figma.com/design/3IEKNX0N1ZoTbEZKxDIv6W/Giuseppe-Ferri's-team-library?t=cgAsHCThAqKPiv5w-1)

- Implementar todos os ***requisitos*** na tela de login.

## **Subtarefas**:
### 1. **Front-End**
- Desenvolver a tela conforme o **protótipo no Figma**.
- Implementar validações (campos vazios, botões desabilitados etc.).

### 2. **Back-End**
- Criar endpoint para autenticação do usuário.
- Integrar com o Front-End para verificar credenciais e retornar token de sessão.
- Implementar todos os ***Critérios de Aceitação*** (ex. bloqueio após 3 falhas).

### 3. **Integração com SQL Server**  
- Criar a tabela de **Usuários** com os campos necessários para autenticação.
- Garantir criptografia/salvamento seguro das senhas.
- Gravar dados de tentativas de login para permitir bloqueio temporário.

### 4. **Casos de Teste**
- Desenvolver os ***Casos de Teste***, nos quais serão criados cenários com base nos ***Critérios de Aceitação*** que deverão representar condições a serem validadas, sejam de sucesso (quando o comportamento está de acordo com o esperado) ou de falha (quando ocorre um erro ou exceção esperada).

## **Estimativa**:
- 3 story points

## **Prioridade**:
- Normal

## **Status**:
- Planejado

## **Referências e Anexos**:
- Documentação de segurança e boas práticas de autenticação.
