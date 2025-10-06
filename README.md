# Gryphix - E-commerce de Jogos Digitais

Bem-vindo ao Gryphix! Este é o repositório do nosso projeto de e-commerce para venda de chaves digitais de jogos, desenvolvido com uma API em Laravel e um frontend em React. Este projeto e totalmente para fins de aprendizado.

## Tecnologias Utilizadas

* **Backend**: PHP 8.1+ / Laravel 10+
* **Frontend**: JavaScript / React 18+ (Vite)
* **Banco de Dados**: PostgreSQL
* **Gerenciador de Pacotes**: Composer 2+ / NPM 10+

## Pré-requisitos

Antes de começar, garanta que você tenha o seguinte software instalado e configurado em sua máquina:

1.  **Git**: Para versionamento de código.
2.  **PHP**: Versão 8.1 ou superior.
3.  **Composer**: Para gerenciar as dependências do PHP.
4.  **Node.js e NPM**: Versão 18 (LTS) ou superior.
5.  **PostgreSQL**: O servidor de banco de dados.

---

## 🚀 Instalação Rápida (Passo a Passo)

Siga estes blocos de comando para configurar o ambiente de desenvolvimento.

### Passo 1: Clonar o Repositório

```bash
git@github.com:RaayaneCustodio/Gryphix.git
cd Gryphix
```

### Passo 2: Configurar o Backend (Parte 1)

```bash
# Acessando a pasta do backend
cd backend

# Instalando dependências do PHP com Composer
composer install

# Criando o arquivo de ambiente .env
# (No Linux/Mac, troque 'copy' por 'cp')
copy .env.example .env
```

### 🛑 AÇÃO MANUAL OBRIGATÓRIA: Configurar o Banco de Dados

Antes de continuar, você **PRECISA** editar o arquivo `.env` que acabou de ser criado.

1.  Abra o projeto no seu editor de código (VS Code, etc.).
2.  Navegue até a pasta `backend` e abra o arquivo `.env`.
3.  **Crie um banco de dados vazio no seu PostgreSQL** (ex: com o nome `gryphix`).
4.  Configure as credenciais de acesso ao banco:

    ```env
    DB_CONNECTION=pgsql
    DB_HOST=127.0.0.1
    DB_PORT=5432
    DB_DATABASE=gryphix
    DB_USERNAME=postgres
    DB_PASSWORD=sua_senha_secreta
    ```
5.  Salve o arquivo e volte para o terminal.

### Passo 3: Finalizar a Configuração do Backend

```bash
# Gerando a chave da aplicação Laravel
php artisan key:generate

# Criando todas as tabelas no banco de dados
php artisan migrate
```

### Passo 4: Configurar o Frontend

```bash
# Voltando para a raiz e acessando a pasta do frontend
cd ../frontend

# Instalando as dependências do JavaScript com NPM
npm install
```

---

## 🔥 Executando a Aplicação

A instalação está concluída! Para rodar o projeto, você sempre precisará de **dois terminais abertos** simultaneamente.

### Terminal 1: Servidor do Backend (API)

```bash
# 1. Navegue até a pasta do backend
cd backend

# 2. Inicie o servidor
php artisan serve
```
> A API estará rodando em `http://localhost:8000`.
> *Se a porta 8000 estiver ocupada, use `php artisan serve --port=8888`.*

### Terminal 2: Servidor do Frontend (React)

```bash
# 1. Abra um NOVO terminal e navegue até a pasta do frontend
cd frontend

# 2. Inicie o servidor de desenvolvimento
npm run dev
```
> O site estará acessível em `http://localhost:5173` (ou a porta que o Vite indicar).
