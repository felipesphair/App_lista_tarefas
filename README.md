# App_lista_tarefas

Aplicativo de TO DO LIST, visando aprimorar e exercitar esses conhecimentos: 
  - HMTL, 
  - CSS(bootstrap),
  - PHP com o uso de PDO,
  - Java Script.

Para rodar:

- Baixe as pastas,

- Abra onde instalou o XAMMP,

- Coloque app_lista_tarefas dentro da pasta XAMMP,

- Coloque app_lista_tarefas_public dentro de HTDOCS,
  
- inicie o XAMMP com apache e mysql
  
- abra o PHPMYADMIN e rode esse SQL:
  
      -- Cria o banco de dados pdo_com_mysql
      CREATE DATABASE IF NOT EXISTS pdo_com_mysql;
      
      -- Seleciona o banco de dados pdo_com_mysql
      USE pdo_com_mysql;
      
      -- Cria a tabela tb_status
      CREATE TABLE IF NOT EXISTS tb_status (
          id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
          status VARCHAR(25) NOT NULL
      );
      
      -- Insere os dados na tabela tb_status
      INSERT INTO tb_status (status) VALUES ('pendente');
      INSERT INTO tb_status (status) VALUES ('realizado');
      
      -- Cria a tabela tb_tarefas
      CREATE TABLE IF NOT EXISTS tb_tarefas (
          id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
          id_status INT NOT NULL DEFAULT 1,
          FOREIGN KEY (id_status) REFERENCES tb_status (id),
          tarefa TEXT NOT NULL,
          data_cadastrado DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP
      );

Telas:

![image](https://github.com/felipesphair/App_lista_tarefas/assets/107360437/9f848169-5962-4083-ae8d-cc41abdee054)

![image](https://github.com/felipesphair/App_lista_tarefas/assets/107360437/c58804dc-6099-4f61-ae41-856dca93db13)

![image](https://github.com/felipesphair/App_lista_tarefas/assets/107360437/bfa368e8-397d-4a76-b6f8-1d1856bc4c1b)

![image](https://github.com/felipesphair/App_lista_tarefas/assets/107360437/93243f5d-fe77-40ee-a360-61c666c564c9)



