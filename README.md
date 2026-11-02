 
<div align="center">

# 📊 PrimeCommerce BI
### Análise Comercial e Dashboard de Vendas

**Projeto de Business Intelligence desenvolvido por Renato Leone**

[![Power BI](https://img.shields.io/badge/Power%20BI-Analytics-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Power Query](https://img.shields.io/badge/Power%20Query-ETL-217346?style=for-the-badge)](https://learn.microsoft.com/power-query/)
[![DAX](https://img.shields.io/badge/DAX-Data%20Analysis-0078D4?style=for-the-badge)](https://learn.microsoft.com/dax/)
[![Business Intelligence](https://img.shields.io/badge/Business-Intelligence-0F766E?style=for-the-badge)](https://)

</div>

---

## 🖼️ Visão geral do projeto

![PrimeCommerce BI — Capa do Projeto](05_Images/Capa_PrimeCommerce%20BI.png)

O **PrimeCommerce BI** é um projeto de Business Intelligence voltado à análise comercial de um e-commerce fictício.

O objetivo é transformar dados operacionais em indicadores, análises visuais e insights que contribuam para a compreensão do desempenho comercial e apoiem a tomada de decisões estratégicas.

O projeto contempla etapas de perfilamento, qualidade e tratamento dos dados, modelagem, criação de métricas e desenvolvimento de dashboards interativos no Power BI.

---

## 🎯 Problema de negócio e objetivos

A gestão da PrimeCommerce precisa acompanhar o desempenho comercial e compreender como o faturamento se distribui entre canais de venda, categorias de produtos, vendedores e clientes.

O projeto busca responder questões como:

- Qual é o faturamento total e como ele evolui ao longo do tempo?
- Quais canais de venda apresentam melhor desempenho?
- Quais categorias contribuem mais para o faturamento?
- Como o ticket médio se comporta entre os períodos e canais?
- Como se distribuem os clientes e suas compras?
- Existe concentração de faturamento em determinados clientes?
- Quais indicadores podem apoiar decisões comerciais?

### Objetivo principal

Desenvolver uma solução de BI que consolide indicadores comerciais e permita explorar os dados de forma interativa, facilitando a identificação de tendências, oportunidades e pontos de atenção.

---

## 📂 Dados utilizados

| Característica | Descrição |
|---|---|
| Fonte | Dados simulados para estudo e portfólio |
| Segmento | E-commerce |
| Período | Janeiro a agosto de 2026 |
| Registros | 1.492, conforme documentação da base de origem |
| Formato | CSV |
| Ferramenta principal | Microsoft Power BI |

### Tabelas utilizadas

- `clientes`
- `produtos`
- `vendedores`
- `pedidos`
- `itens_pedido`
- `pagamentos`
- `entregas`

As tabelas representam diferentes entidades do negócio e foram integradas para permitir análises comerciais e operacionais.

---

## 📊 Dashboards desenvolvidos

O relatório foi organizado em três páginas analíticas, cada uma com uma perspectiva específica do negócio.

### 01 — Visão Geral Comercial

Painel executivo para acompanhamento dos principais indicadores e do desempenho comercial.

**Indicadores e análises:**

- Faturamento Total
- Pedidos Totais
- Quantidade de Itens
- Ticket Médio
- Lucro Bruto
- Faturamento por Categoria
- Faturamento por Vendedor
- Faturamento por Canal de Venda

![PrimeCommerce BI — Visão Geral Comercial](05_Images/dashboard_visao_geral.png)

### 02 — Análise de Vendas

Página dedicada à evolução temporal dos indicadores e à comparação do desempenho entre canais.

**Indicadores e análises:**

- Evolução do Faturamento Mensal
- Evolução dos Pedidos Mensais
- Evolução do Ticket Médio Mensal
- Pedidos por Canal de Venda
- Faturamento por Canal de Venda
- Ticket Médio por Canal de Venda

![PrimeCommerce BI — Análise de Vendas](05_Images/dashboard_analise_vendas.png)

### 03 — Clientes e Canais

Análise do comportamento dos clientes, da recorrência de compras, da distribuição geográfica e do desempenho dos canais.

**Indicadores e análises:**

- Clientes Únicos
- Clientes Recorrentes
- Faturamento por Cliente
- Pedidos por Cliente
- Faturamento por Estado e Cidade
- Jornada de Recorrência dos Clientes
- Desempenho dos Canais de Venda
- Top 5 Clientes por Faturamento
- Clientes Únicos por Cidade
- Participação dos cinco principais clientes no faturamento

![PrimeCommerce BI — Clientes e Canais](05_Images/dashboard_clientes_canais.png)

---

## ⚙️ Metodologia analítica

O desenvolvimento foi conduzido seguindo um fluxo de trabalho de Business Intelligence.

### 1. Perfilamento e qualidade dos dados

Foram realizadas verificações para identificar inconsistências e avaliar a qualidade das informações:

- Quantidade de registros
- Tipos de dados
- Valores nulos
- Valores inválidos
- Espaços extras em textos
- Unicidade das chaves
- Integridade referencial entre tabelas

Durante o perfilamento foram identificadas ocorrências como valores nulos, quantidade de itens igual a zero, preço unitário negativo, datas de entrega inconsistentes, espaços extras em textos e registros sem correspondência em algumas chaves.

### 2. Tratamento e transformação dos dados

O tratamento foi realizado no Power Query, incluindo:

- Preenchimento controlado de valores nulos com `Não informado`
- Correção de quantidade inválida
- Correção de preço unitário inválido com referência ao cadastro de produtos
- Correção de data de entrega inconsistente
- Remoção de espaços extras em campos textuais
- Criação de consultas de QA para validação de registros sem correspondência

### 3. Modelagem de dados

Foi construído um modelo analítico com relacionamentos entre as entidades:

- Clientes → Pedidos
- Vendedores → Pedidos
- Pedidos → Itens do Pedido
- Produtos → Itens do Pedido
- Pedidos → Pagamentos
- Pedidos → Entregas

A modelagem permite integrar informações comerciais e explorar os dados de diferentes perspectivas.

### 4. Criação de indicadores com DAX

Foram desenvolvidas medidas para acompanhar os principais indicadores do negócio:

- `Faturamento Total`
- `Pedidos Totais`
- `Quantidade de Itens`
- `Ticket Médio`
- `Faturamento Concluído`
- `Custo Total`
- `Lucro Bruto`

Também foi criada a coluna calculada `Custo_Total`, utilizada para calcular o custo dos itens a partir da quantidade e do custo unitário dos produtos.

### 5. Desenvolvimento dos dashboards

As páginas foram estruturadas para facilitar:

- A leitura dos indicadores
- A comparação entre períodos
- A análise de canais e categorias
- A exploração do comportamento dos clientes
- A identificação de tendências e oportunidades comerciais

---

## 📈 Principais insights

As análises comerciais documentadas no projeto identificaram os seguintes resultados:

- **Site:** apresenta o maior faturamento e o maior volume de pedidos entre os canais analisados.
- **Categoria Escritório:** apresenta o maior faturamento.
- **Março:** registra o menor faturamento do período.
- **Março:** apesar de manter volume de pedidos elevado, apresenta o menor ticket médio, contribuindo para o menor faturamento mensal.
- **Maio:** apresenta o maior faturamento e o maior ticket médio mensal.
- **Marketplace:** apresenta o maior ticket médio entre os canais de venda.

A página Clientes e Canais complementa a análise com informações sobre recorrência de compras, concentração do faturamento, distribuição geográfica dos clientes e diferenças de desempenho entre os canais.

---

## 💡 Conclusão e recomendações

O PrimeCommerce BI demonstra a aplicação de conceitos de Business Intelligence em um processo que contempla qualidade dos dados, transformação, modelagem, criação de indicadores e visualização analítica.

Os resultados evidenciam diferenças de desempenho entre canais, categorias e períodos, permitindo identificar pontos de atenção e oportunidades de investigação.

### Recomendações analíticas

- Acompanhar a evolução do faturamento e do ticket médio por canal e período.
- Investigar os fatores associados aos meses de menor faturamento.
- Monitorar a recorrência de compras dos clientes.
- Avaliar a concentração de receita nos principais compradores.
- Comparar o desempenho dos canais para identificar oportunidades comerciais.
- Utilizar indicadores comerciais como apoio ao planejamento e à tomada de decisões.

As recomendações devem ser avaliadas em conjunto com o contexto operacional e comercial da empresa.

---

## 🛠️ Tecnologias e ferramentas

| Tecnologia | Aplicação no projeto |
|---|---|
| Microsoft Power BI | Desenvolvimento dos dashboards e relatórios |
| Power Query (M) | Perfilamento, limpeza e transformação dos dados |
| DAX | Criação de medidas e indicadores |
| Modelagem de Dados | Estruturação do modelo analítico |
| CSV | Formato das bases de dados |

---

## 📁 Estrutura do repositório

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
├── 05_Images/
│   ├── Capa_PrimeCommerce BI.png
│   ├── dashboard_visao_geral.png
│   ├── dashboard_analise_vendas.png
│   └── dashboard_clientes_canais.png
│
└── README.md
```

---

## 🚀 Como reproduzir o projeto

1. Clone ou baixe este repositório.
2. Acesse a pasta `02_Power_BI`.
3. Abra o arquivo `PrimeCommerce_BI.pbix` no Power BI Desktop.
4. Verifique os caminhos das fontes de dados, caso necessário.
5. Atualize os dados utilizando a opção **Atualizar** no Power BI.
6. Navegue pelas três páginas do relatório.

> **Observação:** os dados utilizados são simulados e destinados a fins de estudo, demonstração técnica e portfólio. A reprodução poderá exigir ajustes nos caminhos dos arquivos de origem.

---

## 👨‍💻 Autor

**Renato Leone**  
Analista de Dados | Business Intelligence

Projeto desenvolvido individualmente para demonstrar competências em análise de dados, qualidade de dados, transformação, modelagem, criação de indicadores e visualização de informações para apoio à tomada de decisões.

### Competências demonstradas

- Análise e interpretação de dados
- Data Quality e tratamento de dados
- Power Query (M)
- Modelagem de dados
- DAX e desenvolvimento de indicadores
- Business Intelligence
- Visualização e comunicação de insights

### Portfólio e contato profissional

- **GitHub:** [github.com/rrleone](https://github.com/rrleone)
- **Projeto:** [PrimeCommerce BI](https://github.com/rrleone/PrimeCommerce_BI)
- **Portfólio:** [renatoleone — Google Sites](https://sites.google.com/view/renatoleone/)

---

<div align="center">

**PrimeCommerce BI**

*Dados • Análise • Insights • Decisões*

Desenvolvido por **Renato Leone**

</div>
