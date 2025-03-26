# pagina de criação de posts

## Descrição

Onde os professores ou pessoas da secretaria vão criar e postar os avisos que aparecerão na pagina inicial para os alunos.

## Prazos

- Data limite para design no Figma: 14/04/2025
- Margem de erro para design: 3 dias (17/04/2025)
- Data limite de desenvolvimento: 21/04/2025
- Margem de erro: 1 semana (28/04/2025)

## Prioridade

**Média**

## Requisitos

### Front-End

1. Tem que ter espaços para, *titulo* e *corpo* do post.
   - O titulo deve ter um limite da caracteres.
2. O autor e a data da postagem devem ser registrados no post automaticamente.
3. Deve Haver opções para selecionar quem verá o post.
4. Os dados do post serão enviado ao Back-End para serem armazenados em banco de dados.
5. Deve haver uma pre-visualização do post antes de ser postado.

### Back-End

1. Só professores e pessoas da secretaria podem acessa-la.
2. Deve guardar as informações dos posts criados no banco de dados.

### Banco de dados

1. Deve ser criada uma tabela para armazenar os post do site.
   - Devem conter colunas para armazenar os seguintes dados: *titulo*, *corpo do post*, *Resposavel pe postagem*, *data de postagem*.
   - A coluna para o *Resposavel pe postagem*, deve ser uma chave estrangeira que o liga a um usuario do tipo secretaria ou professor.
