# 📱 Sistema de Gerenciamento de Assistência Técnica

## 📌 Sobre o Projeto

Este projeto consiste no desenvolvimento de um sistema web para gerenciamento de uma assistência técnica de celulares, com o objetivo de organizar e facilitar o controle de clientes, aparelhos e agendamentos de reparos.

O sistema foi desenvolvido para solucionar problemas comuns em assistências técnicas que utilizam controles manuais, como perda de agendamentos, duplicidade de informações, dificuldade na localização de clientes e falta de segurança no armazenamento de dados pessoais.

A aplicação conta com autenticação de usuários, gerenciamento de informações e proteção dos dados dos clientes, seguindo os princípios de segurança da Lei Geral de Proteção de Dados (LGPD).

## 🎯 Objetivo

Desenvolver uma solução informatizada que permita controlar os atendimentos de uma assistência técnica, centralizando as informações em um banco de dados e proporcionando mais organização, segurança e praticidade no gerenciamento dos serviços.

## ⚙️ Funcionalidades

### 🔐 1. Login e autenticação
- Login com usuário e senha.
- Validação das credenciais informadas.
- Mensagem de erro em caso de autenticação inválida.
- Controle de sessão com tempo de expiração.
- Opção para sair do sistema (logout).

### 🏠 2. Página principal
- Exibição do nome do usuário autenticado.
- Acesso às funcionalidades do sistema.
- Navegação entre as páginas.
- Opção de encerramento da sessão.

### 👥 3. Gerenciamento de clientes
- Cadastro de clientes.
- Consulta e listagem de clientes.
- Busca por informações cadastradas.
- Edição dos dados de clientes.
- Armazenamento seguro do CPF por meio de criptografia.

### 📱 4. Gerenciamento de aparelhos
- Cadastro de aparelhos vinculados a clientes.
- Registro da marca e modelo.
- Armazenamento do IMEI.
- Registro do defeito relatado.
- Consulta dos aparelhos cadastrados.

### 📅 5. Gerenciamento de agendamentos
- Cadastro de agendamentos de reparos.
- Listagem dos reparos agendados.
- Organização dos agendamentos por data.
- Exibição das informações do cliente e do aparelho relacionado.
- Atualização da data de um agendamento existente.

## 🗄️ Banco de Dados

O sistema utiliza um banco de dados relacional para armazenar e organizar as informações.

As principais entidades são:

- **Usuários:** armazenam as informações necessárias para autenticação no sistema.
- **Clientes:** armazenam os dados pessoais dos clientes.
- **Aparelhos:** armazenam as informações dos celulares e seus respectivos defeitos.
- **Agendamentos:** armazenam as datas e informações dos reparos programados.

O banco de dados possui relacionamentos entre clientes, aparelhos e agendamentos, utilizando chaves primárias e estrangeiras para garantir a integridade das informações.

O script SQL também deve conter registros iniciais para popular as tabelas.

## 🔒 Segurança e LGPD

A segurança das informações é uma das prioridades do projeto.

Foram consideradas as seguintes medidas:

- Criptografia dos CPFs armazenados no banco de dados.
- Proteção das senhas dos usuários por meio de hash.
- Validação das credenciais durante o login.
- Controle de acesso por meio de sessões.
- Expiração automática da sessão após determinado período.
- Proteção das informações pessoais dos clientes.

Essas medidas ajudam a reduzir os riscos de acesso não autorizado e contribuem para o atendimento às exigências da LGPD.

## 🛠️ Tecnologias Utilizadas

As tecnologias utilizadas no desenvolvimento incluem:

- **Python:** desenvolvimento da aplicação e regras de negócio.
- **Flask:** criação das rotas e gerenciamento das funcionalidades web.
- **MySQL:** armazenamento e gerenciamento dos dados.
- **HTML:** estruturação das páginas.
- **CSS:** estilização e organização visual da interface.
- **JavaScript:** recursos de interação com o usuário.
- **Cryptography (Fernet):** criptografia dos dados sensíveis.
- **Werkzeug Security:** geração e validação de hash das senhas.

## 📂 Estrutura do Projeto

```text
assistencia-tecnica/
│
├── sistema/
│   ├── app.py
│   ├── banco.py
│   ├── rotas.py
│   ├── clientes.py
│   ├── aparelhos.py
│   ├── agendamentos.py
│   │
│   ├── templates/
│   │   ├── login.html
│   │   ├── index.html
│   │   ├── clientes.html
│   │   ├── aparelhos.html
│   │   └── agendamentos.html
│   │
│   └── static/
│       ├── css/
│       ├── js/
│       └── img/
│
├── assistencia_db.sql
├── documentacao.pdf
├── der.png
├── requirements.txt
└── README.md
```

*Observação: a estrutura pode variar conforme a organização final dos arquivos do projeto.*

## 🚀 Como Executar o Projeto

### 1. Pré-requisitos

Antes de executar o sistema, é necessário possuir:

- Python instalado.
- MySQL instalado e configurado.
- Navegador de internet.
- Editor de código, como Visual Studio Code.

### 2. Instalar as dependências

Abra o terminal na pasta do projeto e execute:

```bash
pip install -r requirements.txt
```

### 3. Configurar o banco de dados

1. Abra o MySQL ou MySQL Workbench.
2. Execute o arquivo `assistencia_db.sql`.
3. Configure as credenciais de acesso ao banco de dados no projeto.

### 4. Executar o sistema

No terminal, entre na pasta `sistema` e execute o arquivo principal da aplicação:

```bash
python app.py
```

### 5. Acessar o sistema

Abra o navegador e acesse:

```text
http://127.0.0.1:5000
```

## 📋 Entregas do Projeto

O projeto contempla os seguintes itens solicitados:

| Nº | Entrega | Arquivo |
|---|---|---|
| 1 | Documentação de software | `documentacao.pdf` |
| 2 | Diagrama entidade-relacionamento | `der.png` ou `der.pdf` |
| 3 | Script de criação e população do banco | `assistencia_db.sql` |
| 4 | Funcionalidade de login | Pasta `sistema` |
| 5 | Funcionalidade principal | Pasta `sistema` |
| 6 | Gerenciamento de clientes | Pasta `sistema` |
| 7 | Gerenciamento de aparelhos | Pasta `sistema` |
| 8 | Gerenciamento de agendamentos | Pasta `sistema` |

## 👨‍💻 Desenvolvedor

**Pedro Henrique Gonzaga Castro**

Estudante de Desenvolvimento de Sistemas.

Projeto desenvolvido como atividade prática do curso de Desenvolvimento de Sistemas.

---

**Sistema de Gerenciamento de Assistência Técnica de Celulares**

Organização, segurança e praticidade no gerenciamento de atendimentos.
