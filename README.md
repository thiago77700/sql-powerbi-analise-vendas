# sql-powerbi-analise-vendas
Projeto de análise de vendas com banco de dados criado do zero em SQL e dashboard interativo desenvolvido no Power BI.
📊 Análise de Vendas — Banco de Dados & Dashboard

Projeto de análise de dados com banco de dados criado do zero em SQL e dashboard interativo desenvolvido no Power BI.

SQL · Power BI · MySQL · Modelagem de Dados · Business Intelligence

📌 Visão Geral do Projeto

Este projeto realiza uma análise de vendas de ponta a ponta, desde a modelagem e criação de um banco de dados relacional do zero, até a construção de um dashboard analítico no Power BI.

O foco do projeto é demonstrar habilidades práticas em SQL, modelagem de dados, organização de dados para BI e visualização, transformando dados brutos em insights estratégicos para o negócio.

O projeto segue um fluxo completo de análise de dados:

Modelagem do banco de dados

Criação de tabelas com PK e FK

Validação da estrutura dos dados

Organização dos dados para análise

Criação de métricas de vendas

Desenvolvimento de dashboard interativo

🖼️ Pré-visualização do Dashboard

📌 Dashboard de Vendas desenvolvido no Power BI

🧱 Modelagem do Banco de Dados

O banco de dados foi modelado seguindo boas práticas de modelagem relacional, garantindo integridade referencial, escalabilidade e facilidade de análise.

📌 Tabelas criadas

clientes

pedidos

item_pedido

produtos

categorias

🔗 Relacionamentos

clientes → pedidos (1:N)

pedidos → item_pedido (1:N)

produtos → item_pedido (1:N)

categorias → produtos (1:N)

Essa estrutura permite análises como faturamento, desempenho de produtos, comportamento de clientes e vendas por categoria.

🛠️ Ferramentas e Tecnologias
Ferramenta	Finalidade
MySQL	Criação e modelagem do banco de dados
MySQL Workbench	Desenvolvimento das queries SQL
SQL	Definição de tabelas, PK, FK e estrutura
Power BI	Análise e visualização de dados
GitHub	Documentação e portfólio
🗄️ Criação do Banco de Dados (SQL)

Exemplos de queries utilizadas para estruturar o banco de dados:

CREATE TABLE clientes (
  id_cliente INT PRIMARY KEY,
  nome VARCHAR(100),
  email VARCHAR(100)
);
CREATE TABLE pedidos (
  id_pedido INT PRIMARY KEY,
  id_cliente INT,
  data_pedido DATE,
  status_pedido VARCHAR(20),
  FOREIGN KEY (id_cliente) REFERENCES clientes(id_cliente)
);
CREATE TABLE item_pedido (
  id_item INT PRIMARY KEY,
  id_pedido INT,
  id_produto INT,
  quantidade INT,
  preco_unitario DECIMAL(10,2),
  FOREIGN KEY (id_pedido) REFERENCES pedidos(id_pedido),
  FOREIGN KEY (id_produto) REFERENCES produtos(id_produto)
);

📌 Todas as queries completas estão disponíveis no arquivo:

👉 ecommerce_big_dataset.sql

🎯 Perguntas de Negócio Respondidas

Este projeto responde a perguntas importantes para a área comercial, como:

1️⃣ Qual é o faturamento total da empresa?
2️⃣ Como o faturamento evolui ao longo do tempo?
3️⃣ Quais são os produtos mais vendidos?
4️⃣ Qual é o faturamento por categoria?
5️⃣ Quais clientes geram maior receita para o negócio?

📈 Indicadores Analisados no Power BI

O dashboard apresenta os seguintes KPIs e análises:

💰 Faturamento Total

📈 Evolução do Faturamento por Mês

📦 Produtos Mais Vendidos

🍩 Faturamento por Categoria

👥 Top Clientes por Faturamento

O layout foi desenvolvido com foco em clareza visual, padronização de cores e leitura rápida para tomada de decisão.

🧠 Narrativa Analítica

A análise inicia com a visualização do faturamento total e sua evolução mensal, permitindo identificar períodos de maior e menor desempenho.

Em seguida, é possível analisar quais produtos e categorias contribuem mais para a receita, auxiliando decisões estratégicas relacionadas a estoque, marketing e vendas.

Por fim, o ranking de clientes permite identificar os principais geradores de receita, apoiando estratégias de relacionamento e fidelização.

🚀 Próximos Passos

Implementar métricas avançadas (ticket médio, crescimento mês a mês)

Criar páginas de drill-through no Power BI

Otimizar consultas SQL

Evoluir o projeto com novos cenários de negócio

📁 Estrutura do Projeto
sql-powerbi-analise-vendas
│
├── imagens
│   └── dashboard.png
│
├── queries
│   └── ecommerce_big_dataset.sql
│
└── README.md
👨‍💻 Autor

Seu nome

GitHub:

LinkedIn:

⭐ Se você achou este projeto interessante, considere dar uma estrela no repositório!
