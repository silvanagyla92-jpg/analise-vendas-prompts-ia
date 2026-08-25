# Relatório de Auditoria dos Dados

## 1. Objetivo

Documentar a verificação das bases de vendas, incluindo a identificação de sobreposições, duplicidades e critérios utilizados para estabelecer a base analítica definitiva do projeto.

## 2. Bases Auditadas

Foram identificados cinco arquivos na pasta `dados/planilhas/`:

- `Meganium_Sales_Data.csv`;
- `Meganium_Sales_Data_-_AliExpress.csv`;
- `Meganium_Sales_Data_-_Etsy.csv`;
- `Meganium_Sales_Data_-_Shopee.csv`;
- `Updated_Anbernic_Sales_Data.csv`.

## 3. Auditoria Quantitativa Concluída

As quatro bases operacionais apresentam:

- `Meganium_Sales_Data`: 50 registros;
- AliExpress: 20 registros;
- Etsy: 20 registros;
- Shopee: 20 registros.

Essas quatro bases totalizam **110 transações operacionais e 323 unidades**.

A `Updated_Anbernic_Sales_Data.csv` possui **30 registros correspondentes por `invoice_id`** à base geral. Ela representa uma versão derivada dos mesmos pedidos e, portanto, **não deve ser somada novamente**.

A base analítica definitiva é:

> **110 transações únicas — 323 unidades vendidas.**

## 4. Achados

### 4.1 Base derivada

A `Updated_Anbernic_Sales_Data.csv` apresenta correspondência com a base principal por `invoice_id`, além de alterações nos nomes dos produtos e na organização das colunas. Foi classificada como versão derivada.

### 4.2 Bases por canal

AliExpress, Etsy e Shopee foram consideradas bases operacionais do conjunto consolidado. A consolidação considera a sobreposição identificada e evita dupla contagem.

### 4.3 Moedas

As bases possuem registros em diferentes moedas. **EUR, GBP e USD permanecem separados**. Não foi aplicada conversão cambial.

### 4.4 Dados pessoais

Existem campos relacionados ao comprador, incluindo nome e data de nascimento. Esses campos não devem ser publicados nos resultados. Análises de clientes devem utilizar agregações ou identificadores não identificáveis.

### 4.5 Consistência

A validação considera, quando aplicável, `invoice_id`, data, produto, canal, quantidade, preço unitário, preço total, moeda e sobreposição entre arquivos.

## 5. Critério da Base Analítica

A base definitiva foi estabelecida evitando a dupla contagem da `Updated_Anbernic_Sales_Data.csv`. Os resultados consolidados devem utilizar exclusivamente as **110 transações únicas e 323 unidades**.

## 6. Conclusão

**Auditoria quantitativa de sobreposição e deduplicação: CONCLUÍDA.**

A definição da base analítica definitiva encerrou a principal pendência de integridade identificada na verificação inicial. Os resultados devem preservar a separação das moedas e não devem inferir lucro ou margem sem dados de custos suficientes.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.