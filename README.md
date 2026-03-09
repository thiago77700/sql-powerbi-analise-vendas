# sql-powerbi-analise-vendas
Projeto de análise de vendas com banco de dados criado do zero em SQL e dashboard interativo desenvolvido no Power BI.

# 📊 Análise de Vendas — Banco de Dados & Dashboard (SQL + Power BI)

Projeto completo de **Análise de Dados**, envolvendo a **criação de um banco de dados relacional do zero em SQL (MySQL)** e o desenvolvimento de um **dashboard interativo no Power BI** para análise de vendas e geração de insights de negócio.

SQL · MySQL · Power BI · Modelagem de Dados · Business Intelligence

---

## 📌 Visão Geral do Projeto

Este projeto foi desenvolvido com o objetivo de demonstrar um **fluxo completo de dados**, desde a **modelagem e construção da base de dados**, até a **análise visual e interpretação dos resultados**.

Todo o banco de dados foi criado manualmente, seguindo boas práticas de **modelagem relacional**, garantindo **integridade referencial**, organização e confiabilidade das informações utilizadas no dashboard.

O resultado final é um **dashboard de vendas claro, visualmente organizado e orientado à tomada de decisão**.

---

## 🔄 Fluxo do Projeto

O projeto segue as seguintes etapas:

- Modelagem do banco de dados relacional
- Criação das tabelas utilizando SQL (DDL)
- Definição de Primary Keys e Foreign Keys
- Organização da base para consumo analítico
- Conexão do banco ao Power BI
- Criação de métricas e indicadores de vendas
- Desenvolvimento de dashboard interativo

---

## 🖼️ Dashboard de Vendas (Power BI)

![Dashboard de Vendas](imagens/dashboard.png)

O dashboard foi desenvolvido com foco em **clareza visual**, **padronização de cores** e **leitura rápida**, permitindo que usuários de negócio entendam rapidamente o desempenho das vendas.

---

## 📈 Análises e Indicadores do Dashboard

O dashboard responde às principais perguntas do negócio por meio das seguintes análises:

### 💰 Faturamento
- Faturamento total da empresa
- Valores apresentados em moeda (R$)
- Padronização em milhões para melhor leitura

### 📈 Evolução Temporal
- Evolução do faturamento por mês
- Identificação de tendências de crescimento ou queda
- Análise de sazonalidade

### 📦 Produtos Mais Vendidos
- Ranking dos produtos mais vendidos
- Identificação dos produtos com maior impacto na receita
- Apoio a decisões de estoque e mix de produtos

### 🍩 Faturamento por Categoria
- Distribuição do faturamento por categoria
- Comparação visual entre categorias
- Identificação das categorias mais relevantes para o negócio

### 👥 Clientes que Mais Compraram
- Ranking dos principais clientes por faturamento
- Identificação dos maiores geradores de receita
- Apoio a estratégias de relacionamento e fidelização

---

## 🧠 Narrativa Analítica

A análise inicia com uma visão geral do faturamento total, oferecendo um panorama rápido do desempenho do negócio.

Em seguida, a análise mensal permite identificar períodos de maior e menor desempenho, auxiliando no entendimento de padrões de venda ao longo do tempo.

Os gráficos de produtos e categorias evidenciam onde a empresa concentra sua receita, apoiando decisões estratégicas relacionadas a vendas, marketing e estoque.

Por fim, a análise de clientes destaca aqueles que mais contribuem para o faturamento, fornecendo insumos para ações comerciais mais direcionadas.

---

## 🧱 Modelagem do Banco de Dados

O banco de dados foi estruturado seguindo boas práticas de **modelagem relacional**, garantindo consistência, escalabilidade e facilidade de análise.

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

Essa estrutura permite análises detalhadas de vendas, produtos, clientes e categorias.

---

## 🛠️ Ferramentas e Tecnologias

| Ferramenta | Finalidade |
|-----------|------------|
| MySQL | Criação e modelagem do banco de dados |
| MySQL Workbench | Desenvolvimento das queries SQL |
| SQL | Definição da estrutura do banco (DDL) |
| Power BI | Análise e visualização de dados |
| GitHub | Documentação e portfólio |

---

## 📂 Arquivo com Todas as Queries SQL

Todas as queries utilizadas para criação do banco de dados estão disponíveis no arquivo abaixo:

[ecommerce_big_dataset.sql](queries/ecommerce_big_dataset.sql)

O arquivo contém:
- Criação das tabelas
- Definição de Primary Keys (PK)
- Definição de Foreign Keys (FK)
- Estruturação dos relacionamentos
- Organização da base para análise no Power BI

---

## 🎯 Objetivo do Projeto

- Criar um banco de dados relacional do zero
- Aplicar conceitos de modelagem de dados
- Utilizar SQL para estruturar e organizar informações
- Desenvolver um dashboard profissional no Power BI
- Demonstrar competências técnicas para portfólio profissional

---

## 🚀 Próximos Passos

- Implementar métricas avançadas (ticket médio, crescimento mensal)
- Criar páginas de drill-through no Power BI
- Otimizar consultas SQL
- Evoluir o projeto com novos cenários de negócio

---

## 📁 Estrutura do Projeto
sql-powerbi-analise-vendas
│
├── imagens
│ └── dashboard.png
│
├── queries
│ └── ecommerce_big_dataset.sql
│
└── README.md

---

## 🧪 Exemplos de Queries Utilizadas (Apêndice Técnico)

Abaixo estão **alguns exemplos** de queries utilizadas na criação do banco de dados.  
Todas as queries completas estão disponíveis no arquivo SQL do projeto.

### Criação da tabela clientes
```sql
CREATE TABLE clientes (
  id_cliente INT PRIMARY KEY,
  nome VARCHAR(100),
  email VARCHAR(100)
);
Criação da tabela pedidos
CREATE TABLE pedidos (
  id_pedido INT PRIMARY KEY,
  id_cliente INT,
  data_pedido DATE,
  status_pedido VARCHAR(20),
  FOREIGN KEY (id_cliente) REFERENCES clientes(id_cliente)
);
Criação da tabela item_pedido
CREATE TABLE item_pedido (
  id_item INT PRIMARY KEY,
  id_pedido INT,
  id_produto INT,
  quantidade INT,
  preco_unitario DECIMAL(10,2),
  FOREIGN KEY (id_pedido) REFERENCES pedidos(id_pedido),
  FOREIGN KEY (id_produto) REFERENCES produtos(id_produto)
);
👨‍💻 Autor

Seu nome

GitHub:

LinkedIn:

⭐ Se você achou este projeto interessante, considere dar uma estrela no repositório.
