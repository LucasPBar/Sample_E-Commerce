

<h1 align="center">🛍️ Sample E-Commerce</h1>

---

![Image](https://github.com/user-attachments/assets/ab167193-f44d-42ef-806b-5e232439eba7)

---

## 🧾 Contextualização do Projeto

Este projeto foi desenvolvido com o objetivo de construir um **modelo dimensional em estrela (Star Schema)** a partir da base **Financial Sample**, fornecida diretamente pelo Power BI.  
A proposta faz parte do desafio do bootcamp **Klabin - Excel e Power BI Dashboards**, em parceria com a **DIO** e a **Klabin**, e tem como foco aplicar conceitos de modelagem de dados, criação de tabelas fato e dimensão, além do uso de funções DAX para enriquecer as análises.

Durante o processo, foi feita a importação, limpeza, transformação e modelagem dos dados, organizando-os em um formato adequado para análise e criação de dashboards no Power BI.

---

## 🧩 Estrutura do Projeto  

| Tipo | Nome da Tabela | Descrição |
|------|----------------|------------|
| 🗂️ Backup | **Financials_origem** | Tabela original, mantida oculta para referência e integridade dos dados. |
| 📦 Dimensão | **D_Produtos** | Informações agregadas por produto (médias, máximos, mínimos e mediana). |
| 🧾 Dimensão | **D_Produtos_Detalhes** | Detalhes de produtos: faixa de desconto, preço de venda e fabricação. |
| 💸 Dimensão | **D_Descontos** | Colunas de desconto e faixas por produto. |
| 🌍 Dimensão | **D_Detalhes** | Informações complementares como Segment, Country, Sales e Profit. |
| 📅 Dimensão | **D_Calendário** | Criada via DAX com `CALENDAR()` para análises temporais. |
| 📊 Fato | **F_Vendas** | Base central do modelo, conectada às dimensões. |
---

## 🌟 Modelo Estrela

<img width="1106" height="721" alt="Image" src="https://github.com/user-attachments/assets/d3d6eef1-b0f2-4a37-943e-4918420b6210" />

---

## 📊 Dashboard Desenvolvido

Além da modelagem, foi criado um **dashboard interativo no Power BI** para representar os resultados do modelo de forma visual e intuitiva.

<img width="1273" height="713" alt="Image" src="https://github.com/user-attachments/assets/ca6959e7-9084-4179-8356-b2ad73df321c" />

🔗 **Link do dashboard no Power BI Desktop:** [Acesse aqui](https://app.powerbi.com/view?r=eyJrIjoiM2RkMzUzODUtZTg1Yi00OWRlLTk2OTgtZmU2NWNkYzVlYjhlIiwidCI6IjI2YmYyOTYxLWM4NGQtNDg2Zi1hYWJiLTQxZGQwMzkwYTRiOCJ9)

---

## ⚙️ Etapas de Desenvolvimento do Projeto

### 1. 📥 Importação e Backup da Tabela Original
- A tabela **Financial Sample** foi importada para o Power BI.  
- Renomeada como `Financials_origem` e marcada como oculta, servindo como backup e referência original.

### 2. 🧹 Limpeza Inicial dos Dados
- Ajuste de tipos de dados (datas, números e textos).  
- Padronização de nomes de colunas para facilitar o uso em fórmulas DAX e relacionamentos.

### 3. 🧩 Criação das Tabelas Dimensão (via Power Query)
#### 🔹 D_Produtos
- Agrupamento por **Product**.  
- Cálculo de métricas: média, mediana, máximo e mínimo de vendas.  
- Criação da coluna **ID_Produto (SK)** como chave substituta.

#### 🔹 D_Produtos_Detalhes
- Seleção de colunas: Product, Discount Band, Sale Price, Units Sold, Manufacturing Price.  
- Inclusão de **ID_Produto** para relacionamento com D_Produtos.

#### 🔹 D_Descontos
- Extração de colunas relacionadas a descontos: Product, Discount, Discount Band.  
- Inclusão de **ID_Produto** como chave de relacionamento.

#### 🔹 D_Detalhes
- Tabela complementar com Segment, Country, Salers, Profit.  
- Inclusão de **ID_Produto** para manter a integridade referencial.

### 4. 📅 Criação da Tabela D_Calendário (via DAX)
- Utilização da função `CALENDAR()` ou `CALENDARAUTO()` com base na coluna **Date**.  
- Criação de colunas derivadas como Ano, Mês, Trimestre e Dia da Semana.

### 5. 📊 Criação da Tabela F_Vendas
- Seleção das colunas principais da Financial Sample.  
- Criação da chave primária **SK_ID** e inclusão da **ID_Produto** para relacionamento.

### 6. 🔗 Relacionamentos e Organização do Modelo
- Estabelecimento dos relacionamentos entre fato e dimensões usando **ID_Produto** e **Date**.  
- Organização visual do diagrama em estrela com **F_Vendas** no centro.

### 7. 🧠 Colunas Calculadas e Índices
- Criação de colunas condicionais como o **Índice de Produtos**, para categorizar produtos por volume ou lucratividade.  
- Reorganização das colunas para melhor leitura e análise.

---

## 🧰 Ferramentas Utilizadas  

| Ferramenta | Descrição |
|-------------|------------|
| 🟡 **Power BI Desktop** | Utilizado para construção do modelo dimensional, criação de medidas DAX e desenvolvimento do dashboard final. |
| ⚙️ **Power Query** | Responsável pelas etapas de transformação, limpeza e criação das tabelas dimensão a partir da base original. |
| 🧮 **DAX (Data Analysis Expressions)** | Linguagem utilizada para criar colunas calculadas, medidas e a tabela de calendário. |
| 📋 **Financial Sample (Power BI)** | Base de dados fornecida pelo Power BI, utilizada como fonte para o desenvolvimento do modelo. |


---

## 📬 Contato

| | | |
| :--- | :--- | :--- |
| **👤 Nome:** | Lucas Pimenta Barretto | |
| **<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" alt="LinkedIn" width="24" style="vertical-align:middle; margin-right:8px;"> LinkedIn:** | [linkedin.com/in/lucaspimentabarretto](https://www.linkedin.com/in/lucaspimentabarretto) | |
| **📧 Email:** | lucaspimenta1805@gmail.com | |
| **💼 Portfólio**  | [Data Science Portfolio](https://www.datascienceportfol.io/lucaspimenta1805) |
