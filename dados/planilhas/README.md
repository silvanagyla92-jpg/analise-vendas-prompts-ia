# Planilhas

Esta pasta reúne os arquivos de dados utilizados no projeto de análise de vendas.

## 1. Arquivos Disponíveis

### 1.1 Base principal

- `Meganium_Sales_Data.csv`

### 1.2 Bases por canal

- `Meganium_Sales_Data_-_AliExpress.csv`
- `Meganium_Sales_Data_-_Etsy.csv`
- `Meganium_Sales_Data_-_Shopee.csv`

### 1.3 Base derivada

- `Updated_Anbernic_Sales_Data.csv`

A base derivada possui registros correspondentes à base principal por `invoice_id`, com alterações nos nomes dos produtos. Ela deve ser tratada como versão derivada e não como fonte adicional para soma dos resultados.

## 2. Critérios Aplicados na Auditoria

A auditoria das planilhas considerou:

1. estrutura e tipos de dados;
2. duplicidades por `invoice_id`;
3. sobreposição entre as bases;
4. moedas e unidades monetárias;
5. consistência entre quantidade, preço unitário e preço total;
6. definição da base de referência;
7. transformações relevantes.

A consolidação resultante estabelece **110 transações únicas e 323 unidades**. Os 30 registros da `Updated_Anbernic_Sales_Data.csv` correspondentes por `invoice_id` não são somados novamente.

## 3. Cuidados com os Dados

Os arquivos contêm campos de identificação e informações pessoais dos compradores. Esses dados devem ser utilizados somente quando necessários à análise e não devem ser reproduzidos nos resultados, gráficos ou exemplos públicos.

Como existem registros em diferentes moedas, valores monetários de moedas distintas não devem ser agregados diretamente sem conversão documentada.

## 4. Status

**Auditoria das planilhas: CONCLUÍDA.**

A base analítica oficial utilizada nos resultados consolidados é composta por **110 transações únicas e 323 unidades vendidas**.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.