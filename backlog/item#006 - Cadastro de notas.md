# Pagina de notas

## Descrição

Onde o professor postara as notas e lançara as faltas dos alunos das disciplinas que ele está lecionando.

## Prazos

- Data limite para design no Figma: 21/04/2025
- Margem de erro para design: 3 dias (24/04/2025)
- Data limite de desenvolvimento: 30/04/2025
- Margem de erro: 1 semana (07/05/2025)

## Prioridade

**Alta**

## Requisitos

### Front-Eed

- Deve ter um campo para selecionar uma aluno disciplina que o professor lecione e exibir uma lista com os alunos matriculados nela, onde ele possa adicionar as notas e faltas de cada um.

### Back-End

1. Deve fornecer os dados necessários guardados em banco de dados.
2. Deve guardar as notas e presenças lançadas pelo professor no banco de dados.

### Banco de dados

1. Deve criar uma nova tabela para armazenar as notas dos alunos.
    -Deve conter colunas para armazenar os seguintes dados: *nota do primeiro bimestre*, *nota de recuperação do primeiro bimestre*, *nota do primeiro trabalho*, *nota do segundo bimestre*, *nota de recuperação do segundo bimestre*, *nota do segundo trabalho*, *media final*, *id do aluno*.
    - O campo aluno deve ser uma chave estrangeira que liga a tabela aluno.
2. Deve ser criado uma tabela para armazenar as presenças dos alunos.
    -Deve conter colunas para armazenar os seguintes dados: *data da presença*, *um bool indicando se teve ou não presença nessa data*, *id do aluno*
    - O campo aluno deve ser uma chave estrangeira que liga a tabela aluno.
3. Deve ser criada uma tabela para armazenar disciplinas.
    - Deve conter colunas para armazenar os seguintes dados: *nome da disciplima*, *descrição*.
4. Deve ser criado também uma tabela para armazenar as aulas(turmas):
    - Deve conter colunas para armazenar os seguintes dados: *disciplina*, *professor responsavel* **e mais uma coisa que eu ainda não decidi como vai ser**
