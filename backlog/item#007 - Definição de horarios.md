# Pagina de notas

## Descrição

Onde a secretaria deve ter a opção de definir os horários e salas de cada disciplina cadastrada no sistema, para que os alunos e professores possam consultar.

## Prazos

- Data limite para design no Figma: 07/05/2025
- Margem de erro para design: 3 dias (10/05/2025)
- Data limite de desenvolvimento: 14/05/2025
- Margem de erro: 1 semana (21/05/2025)

## Prioridade

**Média**

## Requisitos

### Front-Eed

1. Deve haver uma lista de disciplinas, que quando selecionada, permite definir o professor que lecionará e qual será a sala.
2. Criar um calendário semanal interativo para facilitar a visualização dos horários.

### Back-End

1. Deve fornecer os dados necessários guardados em banco de dados.
2. Deve guardar os dados definidos pela secretaria no banco de dados para serem exibidas para os outros usuários.
3. Impedir que duas disciplinas diferentes sejam alocadas na mesma sala e horário.
4. Garantir que um professor não seja atribuído a duas disciplinas no mesmo horário.

### Banco de dados

1. Deve criar uma nova tabela para armazenar os horarios das disciplinas.
    - Deve ter colunas para armazenar os seguintes dados: *disciplina*, *horario da disciplina*, *Sala de aula da disciplina*.
    - A *disciplina* será uma chave estrangeira que liga a tebela de disciplinas.