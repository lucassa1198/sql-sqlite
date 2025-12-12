# sql-sqlite
Aula sobre sql

  <h1>SQL</h1>

  <h2>SQL com SQLite</h2>

  <h3>Consultas</h3>

  <h4>Criar Tabela</h4>

  ~~~ sql
  CREATE TABLE aluno (
    id INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT,
    nome TEXT NOT NULL,
    telefone TEXT NOT NULL,
    curso TEXT NOT NULL,
    turma INTEGER NOT NULL,
    unidade TEXT NOT NULL,
    pcd BOOLEAN NOT NULL DEFAULT false
  );
  ~~~

  - `CREATE TABLE`: comando para criar uma tabela
  - `aluno`: nome da tabela
  - `id`, `nome`, `telefone`, `curso`, `turma`, `unidade`, `pcd`: colunas da tabela
  - `INTEGER`, `TEXT`, `BOOLEAN`: tipos de dados da coluna
  - `NOT NULL`: não permite ausência de valor na coluna
  - `DEFAULT`: insere um valor padrão na coluna

  <h4>Criar Nova Coluna na Tabela</h4>

  ~~~ sql
  ALTER TABLE aluno ADD turno TEXT NOT NULL DEFAULT 'não informado';
  ~~~

  - `ALTER TABLE`: comando para alterar coluna na tabela
  - `aluno`: nome da tabela
  - `ADD`: comando para adicionar
  - `TEXT`: tipo de dado da coluna
  - `NOT NULL`: não permite ausência de valor na coluna
  - `DEFAULT`: insere um valor padrão na coluna
  - `'não informado'`: valor padrão

  <h4>Renomear Coluna da Tabela</h4>

  ~~~ sql
  ALTER TABLE aluno RENAME COLUMN telefone TO contato;
  ~~~

  - `ALTER TABLE`: comando para alterar coluna na tabela
  - `aluno`: nome da tabela
  - `RENAME`: comando para renomear
  - `COLUMN`: especificação de campo
  - `telefone`: coluna a ser renomeada
  - `TO`: indica para qual
  - `contato`: novo nome setado

  <h4>Inserir Dado na Tabela</h4>

  ~~~ sql
  INSERT INTO aluno (nome, telefone, curso, turma, unidade)
  VALUES ('Alex', '(85) 992855525', 'Full Stack', 26, 'Sul');
  ~~~

  - `INSERT INTO`: comando para inserir dados na tabela
  - `aluno`: nome da tabela
  - `(nome, telefone, curso, turma, unidade)`: colunas da tabela que serão inseridos dados
  - `VALUES`: define valores a serem inseridos
  - `('Alex', '(85) 992855525', 'Full Stack', 26, 'Sul')`: valores para cada coluna da tabela referente a ordem especificada

  <h4>Selecionar Tabela</h4>

  ~~~ sql
  SELECT * FROM aluno;
  ~~~

  - `SELECT`: comando para selecionar a coluna da tabela
  - `*`: indica todas as colunas tabela
  - `FROM`: indica qual tabela será selecionada
  - `aluno`: nome da tabela

  <h4>Atualizar Valor na Tabela</h4>

  ~~~ sql
  UPDATE aluno SET turma = 11 WHERE id = 2;
  ~~~

  - `UPDATE`: comando para atualizar valor na tabela
  - `aluno`: nome da tabela
  - `SET`: comando para definir coluna e valor para atualização
  - `turma = 11`: coluna da tabela e novo valor
  - `WHERE`: comando para filtrar linha da tabela
  - `id = 2`: coluna e valor filtrado

  <h4>Deletar Valor na Tabela</h4>

  ~~~ sql
  DELETE FROM aluno WHERE id = 3;
  ~~~

  - `DELETE`: comando para deletar valor na tabela
  - `FROM`: indica qual tabela
  - `aluno`: nome da tabela
  - `WHERE`: comando para filtrar linha da tabela
  - `id = 3`: coluna e valor filtrado

