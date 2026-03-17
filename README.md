# 📚 Books API — Spring Boot CRUD

![Java](https://img.shields.io/badge/Java-17-orange)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-4.x-brightgreen)
![Maven](https://img.shields.io/badge/Maven-Build-red)
![License](https://img.shields.io/badge/license-MIT-blue)

API REST desenvolvida com **Spring Boot** para gerenciamento de livros.

O projeto implementa um **CRUD completo** utilizando arquitetura em camadas, com persistência usando **Spring Data JPA** e banco de dados em memória **H2**.

Este projeto foi desenvolvido com foco em **aprendizado de arquitetura backend Java moderna**.

---

# 🚀 Tecnologias

* Java 17
* Spring Boot
* Spring Data JPA
* Hibernate
* H2 Database
* Maven
* REST API

---

# 🏗️ Arquitetura do Projeto

A aplicação segue o padrão de arquitetura em camadas:

```
Controller
   ↓
Service
   ↓
Repository
   ↓
Database
```

### Estrutura de pacotes

```
com.livros.estudos
│
├── controller
│   └── LivroController
│
├── service
│   ├── LivroService
│   └── impl
│       └── LivroServiceImpl
│
├── repository
│   └── LivroRepository
│
├── entity
│   └── Livro
│
└── OlamundoApplication
```

---

# 🗄️ Banco de Dados

A aplicação utiliza **H2 Database**, um banco de dados em memória.

Isso significa que os dados são apagados quando a aplicação é finalizada.

### Console do banco

```
http://localhost:8080/h2-console
```

Configuração:

```
JDBC URL: jdbc:h2:mem:bootapp
User: sa
Password:
```

---

# 📡 Endpoints da API

## Listar livros

```
GET /livros
```

Resposta:

```json
[
  {
    "id": 1,
    "titulo": "Spring Boot"
  }
]
```

---

## Buscar livro por ID

```
GET /livro/{id}
```

Exemplo:

```
GET /livro/1
```

---

## Criar livro

```
POST /livro
```

Body:

```json
{
  "titulo": "Java Fundamentals"
}
```

---

## Atualizar livro

```
PUT /livro/{id}
```

Body:

```json
{
  "titulo": "Spring Boot Avançado"
}
```

---

## Deletar livro

```
DELETE /livro/{id}
```

---

# ▶️ Executando o Projeto

### 1️⃣ Clonar o repositório

```
git clone https://github.com/seuusuario/books-api.git
```

### 2️⃣ Entrar na pasta do projeto

```
cd books-api
```

### 3️⃣ Executar a aplicação

```
mvn spring-boot:run
```

ou executar a classe principal:

```
OlamundoApplication.java
```

---

# 🧪 Testando a API

A API pode ser testada usando:

* Postman
* Insomnia
* Curl

Exemplo usando **curl**:

Criar livro:

```
curl -X POST http://localhost:8080/livro \
-H "Content-Type: application/json" \
-d '{"titulo":"Spring Boot"}'
```

---

# 📊 Exemplo de Fluxo

```
HTTP Request
     ↓
Controller
     ↓
Service
     ↓
Repository
     ↓
Hibernate
     ↓
H2 Database
```

---

# 🎯 Objetivo do Projeto

Este projeto foi desenvolvido para estudo de:

* criação de **APIs REST com Spring Boot**
* arquitetura em camadas
* persistência de dados com JPA
* integração com banco de dados
* boas práticas de desenvolvimento backend Java

---

# 📌 Melhorias Futuras

* adicionar validação com Bean Validation
* implementar tratamento global de exceções
* adicionar Swagger/OpenAPI
* integrar banco PostgreSQL
* implementar testes automatizados

---


Projeto desenvolvido para estudos de **Java Backend e Spring Boot**.
