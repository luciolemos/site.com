//VERSÃO DO LARAVEL
C:\wamp\www\site.com>php artisan list
Laravel Framework 7.16.1


//VERSÃO DO INSTALADOR DO LARAVEL
C:\wamp\www\site.com>laravel --version
Laravel Installer 3.1.0

//VERSÃO DO COMPOSER
C:\wamp\www\site.com>composer --version
Composer version 1.10.7 2020-06-03 10:03:56

//VERSÃO DO PHP
C:\wamp\www\site.com>php --version
PHP 7.4.0 (cli) (built: Nov 27 2019 10:14:18) ( ZTS Visual C++ 2017 x64 )
Copyright (c) The PHP Group
Zend Engine v3.4.0, Copyright (c) Zend Technologies

//LISTANDO COMANDOS
C:\wamp\www\site.com>php artisan list
Laravel Framework 7.16.1

//Voltando para o diretório "www", onde será criado o projeto "spima".
C:\wamp\www\site.com>cd ..

//Linha de comando para a criação do projeto "spima", dentro de "www".
C:\wamp\www>laravel new spima

//entrando em "spima".
C:\wamp\www>cd spima

//Executando p projeto "spima", no vscode.
C:\wamp\www\spima>code .
C:\wamp\www\spima>

//Criando a migration "pessoal".
C:\wamp\www\site.com>php artisan make:migration create_pessoal_table --create=pessoal
Created Migration: 2020_06_25_162146_create_pessoal_table

//"db:seed --database=laravel", informa qual base de dados queremos povoar, 
para o caso em que se está trabalhando com vários bancos
de dados simultaneamente.
C:\wamp\www\spima.com>php artisan db:seed --database=laravel
Database seeding completed successfully.

//EXECUTANDO A MIGRATION E CRIANDO NO BANCO DE DE DADOS LARAVEL, A TABLE "pessoal".
C:\wamp\www\spima.com>php artisan migrate
Migration table created successfully.                               //MIGRAÇÃO DA TABELA REALIZADA COM SUCESSO
Migrating: 2020_06_25_223533_create_pessoal_table                   //MIGRANDO
Migrated:  2020_06_25_223533_create_pessoal_table (0.17 seconds)    //MIGRADO/A

C:\wamp\www\site.com>php artisan serve
Laravel development server started: http://127.0.0.1:8000
[Thu Jun 25 12:24:13 2020] PHP 7.4.0 Development Server (http://127.0.0.1:8000) started

C:\wamp\www\spima.com>php artisan db:seed --database=laravel
Database seeding completed successfully.

//COMANDO REFRESH REVERTE TODAS AS MIGRAÇÕES
C:\wamp\www\spima.com>php artisan migrate:reset
Rolling back: 2020_06_25_223533_create_pessoal_table
Rolled back:  2020_06_25_223533_create_pessoal_table (0.35 seconds)

C:\wamp\www\spima.com>php artisan db:seed --database=laravel
Database seeding completed successfully.

//COMANDO "REFRESH" TAMBÉM FUNCIONOU. DESTRÓI O BANCO DE DADOS E RECRIA A "ESTRUTURA"
C:\wamp\www\spima.com>php artisan migrate:refresh
Rolling back: 2020_06_25_223533_create_pessoal_table
Rolled back:  2020_06_25_223533_create_pessoal_table (0.18 seconds)
Migrating: 2020_06_25_223533_create_pessoal_table
Migrated:  2020_06_25_223533_create_pessoal_table (0.3 seconds)

//USADO PARA CRIAR O ARQUIVO DE MIGRIÇÃO DA TABELA USERS
C:\wamp\www\spima.com>php artisan make:migration create_users_table
Created Migration: 2020_06_26_032955_create_users_table

//USADO PARA IMPLEMENTAR NOVA COLUNA À ESTRUTURA DA TABELA PESSOAL
C:\wamp\www\spima.com>php artisan make:migration add_votes_to_pessoal_table --table=pessoal


C:\wamp\www\spima.com>php artisan migrate:reset
Rolling back: 2020_06_26_051254_add_votes_to_pessoal_table
Rolled back:  2020_06_26_051254_add_votes_to_pessoal_table (0 seconds)
Rolling back: 2020_06_25_223533_create_pessoal_table
Rolled back:  2020_06_25_223533_create_pessoal_table (0.12 seconds)

C:\wamp\www\spima.com>php artisan migrate
Migrating: 2020_06_25_223533_create_pessoal_table
Migrated:  2020_06_25_223533_create_pessoal_table (0.12 seconds)
Migrating: 2020_06_26_051254_add_votes_to_pessoal_table
Migrated:  2020_06_26_051254_add_votes_to_pessoal_table (0.38 seconds)
