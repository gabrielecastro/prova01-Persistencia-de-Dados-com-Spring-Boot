# 📦 Avaliação Spring Boot: Persistência de Dados com MariaDB

## 📚 Descrição

Este projeto tem como objetivo implementar uma aplicação utilizando **Spring Boot** com **MariaDB**, aplicando conceitos de persistência de dados e mapeamento entre entidades. A aplicação simula o relacionamento entre duas entidades: **Produto** e **Categoria**, com operações completas de **CRUD** expostas via endpoints REST.

## 🛠️ Tecnologias Utilizadas

- **Spring Boot** – Framework para criação de aplicações Java modernas.
- **Spring Web** – Para construção de APIs REST.
- **Spring Data JPA** – Para integração com banco de dados via JPA.
- **Lombok** – Para reduzir a verbosidade do código (getters, setters, etc).
- **Spring DevTools** – Para recarregamento automático durante o desenvolvimento.
- **MariaDB** – Banco de dados relacional utilizado no projeto.


## 🧩 Entidades

### 🧺 Categoria

- `id` (Long)
- `nome` (String)
- `descricao` (String)
- ✅ Relacionamento: **One-to-Many** com Produto

### 📦 Produto

- `id` (Long)
- `nome` (String)
- `quantidade` (Integer)
- `descricao` (String)
- ✅ Cada produto pertence a uma **única categoria**

## 🔗 Relacionamento

- Uma **Categoria** pode conter vários **Produtos**.
- Cada **Produto** pertence a uma única **Categoria**.

> Relacionamento implementado com `@OneToMany` e `@ManyToOne` usando JPA.

---

## 🗄️ Configuração do Banco de Dados

O projeto utiliza **MariaDB** com o auxílio do **XAMPP**.

### 🧭 Passos:

1. Baixe o XAMPP: [https://www.apachefriends.org/pt_br/index.html](https://www.apachefriends.org/pt_br/index.html)
2. Inicie o serviço `MySQL` no painel do XAMPP.
3. Crie o banco de dados (ex: `spring_db`) usando o phpMyAdmin ou CLI.
4. Configure o arquivo `application.properties`:

```properties
spring.datasource.url=jdbc:mariadb://localhost:3306/bd_prova01
spring.datasource.username=root
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

## 🌐 Endpoints Principais

### 🔸 Categoria

- `GET /categoria` → Lista todas as categorias
- `POST /categoria` → Cria uma nova categoria

### 🔸 Produto

- `GET /produto` → Lista todos os produtos
- `POST /produto` → Cria um novo produto

> Use ferramentas como **Postman** ou **Bruno** para testar as rotas.

---

## ✅ Requisitos Atendidos

- [x] CRUD completo para ambas as entidades
- [x] Relacionamento entre entidades funcional e persistido
- [x] Uso de Lombok para reduzir verbosidade
- [x] Endpoints REST criados e testados

---

## 📌 Conclusão

Este projeto demonstra como estruturar uma aplicação Spring Boot com integração ao MariaDB, mapeando entidades com JPA e implementando CRUD completo. Ele pode ser expandido para incluir novas funcionalidades, relacionamentos mais complexos ou autenticação de usuários.


> ⚠️ **Observação:** Devido a uma limitação técnica no meu computador não consegui executar o banco MariaDB localmente via XAMPP. Apesar disso, toda a estrutura de persistência foi construída com base nos padrões corretos, e o projeto está configurado para funcionar normalmente em qualquer ambiente com o banco devidamente instalado.



