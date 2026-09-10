# 📊 PrimeCommerce BI — Análise Comercial e Dashboard de Vendas

## 🎯 Problema de negócio

A gestão da PrimeCommerce precisa acompanhar o desempenho comercial e entender como o faturamento se distribui entre canais de venda, categorias de produtos e vendedores.

O objetivo do projeto é transformar dados operacionais de um e-commerce de pequeno porte em indicadores e análises visuais que apoiem o acompanhamento do desempenho comercial e a tomada de decisões.

## 🗂️ Sobre os dados

- **Fonte:** Dados simulados para fins de estudo e portfólio
- **Segmento:** E-commerce
- **Período:** Janeiro/2026 a Agosto/2026
- **Registros:** 1.492
- **Formato:** CSV
- **Ferramenta principal:** Microsoft Power BI

### Tabelas utilizadas

- `clientes`
- `produtos`
- `vendedores`
- `pedidos`
- `itens_pedido`
- `pagamentos`
- `entregas`

## 🛠️ Ferramentas utilizadas

- **Power BI Desktop**
- **Power Query (M)** — preparação e transformação dos dados
- **DAX** — criação de medidas e indicadores
- **Modelagem de dados** — estruturação do modelo analítico

## 🔍 Etapas do projeto

### 1. Perfilamento e qualidade dos dados

Foram realizadas verificações de:

- quantidade de registros;
- tipos de dados;
- valores nulos;
- valores inválidos;
- espaços extras em textos;
- unicidade das chaves;
- integridade referencial entre tabelas.

Durante essa etapa foram identificadas ocorrências como:

- valores nulos em campos categóricos e de status;
- quantidade de item igual a zero;
- preço unitário negativo;
- data de entrega inconsistente;
- espaços extras em valores textuais;
- registros sem correspondência em algumas chaves de relacionamento.

### 2. Tratamento dos dados

Os problemas identificados foram tratados no Power Query, incluindo:

- preenchimento controlado de valores nulos com `Não informado`;
- correção de quantidade inválida;
- correção de preço unitário inválido com referência ao cadastro de produtos;
- correção de data de entrega inconsistente;
- remoção de espaços extras em campos textuais;
- criação de consultas de QA para validação de registros sem correspondência.

### 3. Modelagem

Foi construído um modelo de dados relacionando:

- clientes → pedidos;
- vendedores → pedidos;
- pedidos → itens do pedido;
- produtos → itens do pedido;
- pedidos → pagamentos;
- pedidos → entregas.

### 4. Indicadores e métricas

Foram criados indicadores utilizando DAX:

- Faturamento Total
- Pedidos Totais
- Quantidade de Itens
- Ticket Médio
- Faturamento Concluído
- Custo Total
- Lucro Bruto

Também foi criada a coluna calculada `Custo_Total` para calcular o custo dos itens a partir da quantidade e do custo unitário dos produtos.

### 5. Visualização

Foi desenvolvido um dashboard com duas páginas:

**01 — Visão Geral Comercial**

- Faturamento Total
- Pedidos Totais
- Quantidade de Itens
- Ticket Médio
- Lucro Bruto
- Faturamento por Categoria
- Faturamento por Vendedor
- Faturamento por Canal de Venda

**02 — Análise de Vendas**

- Evolução do Faturamento Mensal
- Evolução dos Pedidos Mensais
- Evolução do Ticket Médio Mensal
- Pedidos por Canal de Venda
- Faturamento por Canal de Venda
- Ticket Médio por Canal de Venda

## 📈 Principais insights

- O **Site** apresenta o maior faturamento e o maior volume de pedidos entre os canais analisados.
- **Escritório** é a categoria com maior faturamento.
- **Março** apresenta o menor faturamento do período.
- Em março, o volume de pedidos permanece elevado, mas o ticket médio é o menor do período, contribuindo para o menor faturamento mensal observado.
- **Maio** apresenta o maior faturamento e o maior ticket médio mensal.
- **Marketplace** apresenta o maior ticket médio entre os canais de venda.

## 🖼️ Prévia do dashboard

### Visão Geral Comercial

![PrimeCommerce BI — Visão Geral](images/dashboard_visao_geral.png)

### Análise de Vendas

![PrimeCommerce BI — Análise de Vendas](images/dashboard_analise_vendas.png)

## ✅ Conclusão e recomendação

O PrimeCommerce BI demonstra um fluxo completo de análise de dados utilizando Power BI, desde o perfilamento e tratamento dos dados até a modelagem, criação de indicadores e desenvolvimento de dashboards.

Os resultados mostram a relevância do **Site** para o faturamento e volume de pedidos e evidenciam diferenças de desempenho entre os canais. Recomenda-se acompanhar principalmente a evolução do ticket médio e do faturamento por canal e período, utilizando esses indicadores como apoio à gestão comercial.

## 📁 Estrutura do projeto

```text
PrimeCommerce_BI/
│
├── 01_Dados_Raw/
│   ├── clientes.csv
│   ├── produtos.csv
│   ├── vendedores.csv
│   ├── pedidos.csv
│   ├── itens_pedido.csv
│   ├── pagamentos.csv
│   └── entregas.csv
│
├── 02_Power_BI/
│   └── PrimeCommerce_BI.pbix
│
├── 03_Documentacao/
│
├── 04_Exportacoes/
│
├── images/
│   ├── dashboard_visao_geral.png
│   └── dashboard_analise_vendas.png
│
└── README.md
```

## 🚀 Como reproduzir

1. Baixe ou clone o projeto.
2. Abra o arquivo `PrimeCommerce_BI.pbix` no Power BI Desktop.
3. Verifique os caminhos das fontes de dados, caso necessário.
4. Atualize os dados utilizando **Atualizar** no Power BI.
5. Navegue pelas páginas do dashboard.

---

## 📌 Projeto de portfólio

Projeto desenvolvido para prática e demonstração de competências em **Análise de Dados, Business Intelligence, Power Query, Modelagem de Dados, DAX e Power BI**.
