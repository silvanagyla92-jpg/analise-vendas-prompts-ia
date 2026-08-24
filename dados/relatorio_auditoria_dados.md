# Relatório de Auditoria dos Dados

## 1. Objetivo

Documentar a verificação inicial das bases de vendas antes da consolidação e da geração dos insights do projeto.

## 2. Bases Auditadas

Foram identificados cinco arquivos na pasta `dados/planilhas/`:

- `Meganium_Sales_Data.csv`;
- `Meganium_Sales_Data_-_AliExpress.csv`;
- `Meganium_Sales_Data_-_Etsy.csv`;
- `Meganium_Sales_Data_-_Shopee.csv`;
- `Updated_Anbernic_Sales_Data.csv`.

## 3. Achados Estruturais

### 3.1 Base derivada

`Updated_Anbernic_Sales_Data.csv` apresenta correspondência de registros com a base principal por `invoice_id`, além de alterações nos nomes dos produtos e na organização das colunas. Portanto, deve ser tratada como uma versão derivada e não adicionada à base principal.

### 3.2 Bases por canal

Os arquivos de AliExpress, Etsy e Shopee devem ser comparados com a base principal antes de qualquer consolidação. A existência de arquivos separados por canal não é suficiente para concluir que são conjuntos independentes.

### 3.3 Moedas

As bases possuem registros em diferentes moedas. Valores monetários de moedas distintas não devem ser somados diretamente. A análise financeira deverá preservar a moeda ou utilizar uma taxa de conversão explicitamente documentada.

### 3.4 Dados pessoais

Existem campos relacionados ao comprador, incluindo nome e data de nascimento. Esses campos não devem ser publicados nos resultados. As análises de clientes devem utilizar agregações ou identificadores não identificáveis.

## 4. Critério para a Análise

Antes da geração dos resultados finais, será definida uma base analítica sem dupla contagem. A escolha deverá considerar a cobertura dos dados, a sobreposição entre arquivos e a finalidade de cada base.

## 5. Próxima Verificação

A próxima etapa é comparar quantitativamente os cinco arquivos por `invoice_id`, data, produto, canal e demais campos relevantes para determinar quais registros são complementares e quais representam versões ou duplicações.

## 6. Conclusão Preliminar

As bases estão disponíveis e são adequadas para prosseguir com a auditoria quantitativa. Entretanto, ainda não é metodologicamente correto consolidar todos os arquivos em um único conjunto nem apresentar um faturamento global antes da verificação de sobreposição e do tratamento das moedas.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.