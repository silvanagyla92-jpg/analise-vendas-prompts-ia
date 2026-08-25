# Dados

Esta pasta concentra as bases de dados utilizadas no projeto de análise de vendas.

## 1. Fonte dos Dados

Os dados foram disponibilizados pela **Digital Innovation One (DIO)** como parte do laboratório **Como Utilizar Prompts para Gerar Insights de Relatórios de Vendas**.

## 2. Bases Disponíveis

### 2.1 Arquivos

- `Meganium_Sales_Data.csv` — base principal de vendas;
- `Meganium_Sales_Data_-_AliExpress.csv` — dados de vendas do canal AliExpress;
- `Meganium_Sales_Data_-_Etsy.csv` — dados de vendas do canal Etsy;
- `Meganium_Sales_Data_-_Shopee.csv` — dados de vendas do canal Shopee;
- `Updated_Anbernic_Sales_Data.csv` — versão derivada da base principal, com alteração dos nomes dos produtos e reorganização das colunas.

### 2.2 Sobreposição e Base Definitiva

A `Updated_Anbernic_Sales_Data.csv` contém registros correspondentes aos registros da base principal por `invoice_id`, com alterações nos nomes dos produtos. Por isso, **não deve ser somada à base principal como fonte independente**.

A auditoria quantitativa já foi concluída. As quatro bases operacionais totalizam **110 transações únicas e 323 unidades**. A base derivada possui 30 registros correspondentes e não deve ser contabilizada novamente.

## 3. Estrutura dos Dados

As bases contêm campos relacionados a:

- produto;
- data da venda;
- quantidade;
- preço unitário;
- preço total;
- moeda;
- canal/site;
- cupom e valor do desconto;
- data de nascimento do comprador;
- nome do comprador;
- país de entrega;
- identificador da venda.

## 4. Critérios de Verificação Aplicados

A auditoria considerou:

- estrutura e compatibilidade das colunas;
- tipos de dados;
- duplicidades por `invoice_id`;
- consistência entre `quantity`, `unit_price` e `total_price`;
- moedas utilizadas;
- período analisado;
- sobreposição entre arquivos;
- métricas disponíveis.

### 4.1 Cuidados analíticos

Os valores de `total_price` não devem ser somados entre moedas diferentes sem uma regra de conversão documentada. A análise financeira deve preservar a moeda ou aplicar uma conversão explícita e consistente.

Os campos `buyer_name` e `buyer_birth_date` não devem ser expostos nos resultados analíticos. Para análises de clientes, deve-se utilizar identificadores agregados ou métricas que não revelem dados pessoais.

## 5. Status

**Auditoria e definição da base analítica: CONCLUÍDAS.**

A referência quantitativa oficial do projeto é **110 transações únicas e 323 unidades vendidas**.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.