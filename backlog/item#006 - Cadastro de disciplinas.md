# Cadastro de Disciplinas

- importância: **Alta**
- Data limite para design no Figma: 28/04/2025
- Margem de erro para design: 3 dias (01/05/2025)
- Data limite de desenvolvimento: 07/05/2025
- Margem de erro: 1 semana (14/05/2025)


## Descrição

Pagina para as pessoas da secretaria cadastrarem as disciplinas que terão no site e também a definição dos alunos que as farão e os professores que as lecionarão.

## Requisitos

### Front-End

1. Exibição da lista de disciplinas
   - Se houver disciplinas cadastradas, exibir uma tabela ou cards organizados com: Nome da disciplina, Professor(es) responsável(is)Quantidade de alunos matriculados, Botões de editar e apagar.
   - Se não houver disciplinas, exibir uma mensagem informativa e um botão centralizado para criar a primeira disciplina.
2. Campos obrigatórios a serem preenchidos para criação das disciplinas: 
   - *Nome da disciplina*;
   - *Descrição*.
3. Campos opcionais a serem preenchidos para criação das disciplinas: 
   - *Professor responsável*, pode ser mais de um;
   - *Alunos*, devem ter no mínimo 6 alunos.
4. Na lista de disciplinas já criadas devem ter as seguintes opções: *editar* e *apagar*.

### Back-End

1. Deve fornecer os dados das disciplinas já cadastradas.
2. Deve guardas as novas disciplinas e as alterações das já existentes no banco de dados.
