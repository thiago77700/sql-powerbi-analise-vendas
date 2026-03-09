# sql-powerbi-analise-vendas
Projeto de análise de vendas com banco de dados criado do zero em SQL e dashboard interativo desenvolvido no Power BI.

# Análise de Vendas — Banco de Dados & Dashboard

Projeto de análise de dados com **banco de dados criado do zero em SQL** e **dashboard interativo desenvolvido no Power BI**.

SQL · MySQL · Power BI · Modelagem de Dados · Business Intelligence

---

## Visão Geral do Projeto

Este projeto apresenta um fluxo completo de **Análise de Dados**, desde a **modelagem e criação de um banco de dados relacional do zero**, até a **construção de um dashboard analítico no Power BI**.

O objetivo é demonstrar habilidades práticas em **SQL, modelagem de dados e visualização**, transformando dados brutos em **insights estratégicos para tomada de decisão**.

O projeto segue um fluxo completo:

- Modelagem do banco de dados  
- Criação de tabelas com Primary Keys e Foreign Keys  
- Validação da estrutura dos dados  
- Organização dos dados para análise  
- Criação de métricas de vendas  
- Desenvolvimento de dashboard interativo  

---

## Pré-visualização do Dashboard

![Dashboard de Vendas](imagens/dashboard.png)

---

## Modelagem do Banco de Dados

O banco de dados foi estruturado seguindo boas práticas de **modelagem relacional**, garantindo integridade referencial e facilidade de análise.

### Tabelas criadas

- clientes  
- pedidos  
- item_pedido  
- produtos  
- categorias  

### Relacionamentos

- clientes → pedidos (1:N)  
- pedidos → item_pedido (1:N)  
- produtos → item_pedido (1:N)  
- categorias → produtos (1:N)  

---

## Ferramentas e Tecnologias

| Ferramenta | Finalidade |
|----------|-----------|
| MySQL | Criação e modelagem do banco de dados |
| MySQL Workbench | Desenvolvimento das queries SQL |
| SQL | Definição de tabelas, PK e FK |
| Power BI | Análise e visualização de dados |
| GitHub | Documentação e portfólio |

---

## Criação do Banco de Dados (SQL)

### Tabela clientes

```sql
CREATE TABLE clientes (
  id_cliente INT PRIMARY KEY,
  nome VARCHAR(100),
  email VARCHAR(100)
);
