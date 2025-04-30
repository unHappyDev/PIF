# Item#002 - Tela de Cadastro

## **Descrição:**  
*A recepcionista cadastra os dados do aluno em um formulário. Ao finalizar o preenchimento, o sistema gera automaticamente um RA (login) e uma senha provisória, que são enviados para o e-mail do aluno. Em seguida, o aluno deve utilizar esses dados para acessar o sistema pela primeira vez e definir uma nova senha.*

## **Prazos**:
- **Protótipo Figma:** dd/mm/yyyy  
- **Finalização do Item:** dd/mm/yyyy  

## **Prioridade**:
- Normal

## **Estimativa**:
- 3 story points

## **Status**:
- Planejado

## **Requisitos:**
- Formulário contendo os dados pessoais do usuário (aluno):
  - Nome completo, data de nascimento, sexo/gênero, CPF, RG.
  - Endereço completo (rua, número, bairro, cidade, CEP, complemento).
  - Telefone, e-mail.
- Autorização para o uso de dados conforme LGPD (ou legislação equivalente).
- Termo de consentimento com assinatura ou aceite digital.
- Validação automática de CPF ou e-mail conforme entrada.
- Geração de RA e senha provisória, enviados por e-mail.
- Criação de ID único incremental para cada usuário.
- Logs de erro e sucesso.

## **Critérios de Aceitação:**

### **Front-End**
1. Validar campos obrigatórios e entradas incorretas (ex: campos vazios, CEP inválido).
2. Aplicar máscaras e validações específicas para CPF e e-mail.
3. Desabilitar botão de envio até que todos os dados estejam válidos e o termo de consentimento aceito.

### **Back-End**
1. Gerar automaticamente RA e senha provisória, e enviar via e-mail.
2. Armazenar senha com algoritmo seguro (bcrypt, argon2, scrypt).
3. Aplicar políticas de segurança: 
   - Validação da senha (mín. 8 caracteres, 1 maiúscula, 1 número, 1 caractere especial).
   - Troca obrigatória da senha a cada 90 dias.
   - Proibição de uso de dados pessoais como senha.
   - Confirmação de senha idêntica.
4. Implementar login inicial com solicitação de troca de senha.
5. Bloqueio após 3 tentativas de login inválido.

### **Database**  
- **Criar a tabela:** `Usuarios`
- **Adicionar as colunas:** `id_usuario`, `nome`, `data_nascimento`, `genero`, `cpf`, `rg`, `endereco`, `cep`, `telefone`, `email`, `senha_hash`, `ra`, `senha_temporaria`, `termo_aceite`, `tentativas_login`, `data_ultima_troca_senha`, `criado_em`

### **Casos de Teste**
- Devem ser desenvolvidos testes automatizados conforme necessário, nos quais serão criados cenários com base nos ***Critérios de Aceitação*** que deverão representar condições a serem validadas, sejam de sucesso (quando o comportamento está de acordo com o esperado) ou de falha (quando ocorre um erro ou exceção esperada).

## **Referências e Anexos**:
