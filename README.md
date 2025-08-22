# 📘 Projeto de Banco de Dados – Índices e Procedures  

Este repositório foi criado para organizar e documentar um projeto dividido em **duas partes principais**:  

1. **Criação de Índices em Banco de Dados**  
2. **Utilização de Procedures para manipulação de dados**  

A ideia é refinar conhecimentos de **SQL avançado** aplicando índices, consultas otimizadas e procedures para manipulação de dados em diferentes cenários, como *company*, *universidade* e *e-commerce*.  

---

## 📌 Parte 1 – Criando Índices em Banco de Dados  

Nesta primeira parte, vamos trabalhar com o cenário de **company**, onde precisaremos responder algumas perguntas através de queries SQL e otimizar o acesso aos dados com **índices bem definidos**.  

### 🔎 O que foi levado em consideração para a criação dos índices?  
- Quais os **dados mais acessados** nas queries.  
- Quais os **atributos mais relevantes** no contexto de pesquisa.  
- Lembrando sempre que índices **impactam diretamente na performance**:  
  - **Aceleram consultas**  
  - **Podem pesar em inserções/updates** se usados em excesso  
  - Por isso, só criamos aqueles **essenciais**  

### 📌 Perguntas (queries SQL a responder):  
1. **Qual o departamento com maior número de pessoas?**  
2. **Quais são os departamentos por cidade?**  
3. **Relação de empregados por departamento**  

### 🛠️ Exemplos de criação de índices:  
```sql
-- Índice único para emails de clientes
ALTER TABLE customer ADD UNIQUE index_email(email);

-- Índice hash para acelerar buscas por status de ativo
CREATE INDEX index_ativo_hash ON exemplo(ativo) USING HASH;


