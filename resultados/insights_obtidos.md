# Insights Obtidos

## 1. Objetivo

Registrar os principais insights derivados dos dados fornecidos, distinguindo fatos observados, interpretações e limitações.

## 2. Insight 1 — A auditoria é necessária antes da consolidação

### Evidência

A `Updated_Anbernic_Sales_Data` apresenta correspondência com registros da `Meganium_Sales_Data`.

### Interpretação

Somar as duas bases como fontes independentes poderia gerar dupla contagem.

### Conclusão

A deduplicação deve preceder qualquer cálculo consolidado.

## 3. Insight 2 — O identificador de venda favorece a rastreabilidade

### Evidência

As bases possuem `invoice_id`.

### Interpretação

Esse campo pode ser utilizado como chave prioritária para cruzamentos e identificação de registros correspondentes.

## 4. Insight 3 — O catálogo possui cinco produtos identificáveis

### Evidência

Foram identificados cinco modelos de produtos nas tabelas fornecidas.

### Conclusão

É possível estruturar análises por produto sem depender exclusivamente do nome, utilizando também o SKU quando disponível.

## 5. Insight 4 — O canal de venda é uma dimensão relevante

### Evidência

Foram identificados Etsy, Shopee e AliExpress.

### Conclusão

Os prompts podem comparar volume de unidades, quantidade de pedidos, produtos e distribuição geográfica por marketplace.

## 6. Insight 5 — A análise financeira precisa respeitar as moedas

### Evidência

Os registros utilizam EUR, GBP e USD.

### Conclusão

Valores monetários de moedas diferentes não devem ser somados diretamente. Uma consolidação financeira exige conversão cambial previamente definida.

## 7. Insight 6 — O preço total apresenta consistência aritmética

### Evidência

Nos registros fornecidos, `total_price` corresponde a `quantity × unit_price`.

### Conclusão

A consistência aritmética permite utilizar esses campos nas análises, sem dispensar outras validações de qualidade.

## 8. Insight 7 — Não é possível inferir lucro com os dados disponíveis

### Evidência

As tabelas fornecidas não apresentam custo de aquisição ou custo operacional.

### Conclusão

É possível analisar vendas e valores registrados, mas não calcular margem ou lucro de forma confiável.

## 9. Limitações

1. Os números consolidados referem-se somente aos registros fornecidos nesta etapa.
2. Não foi realizada conversão cambial.
3. Não foram calculados lucro ou margem.
4. A definição operacional de `discount_value` não foi fornecida.
5. A relação completa entre a base geral e todas as bases segmentadas deve ser confirmada com os arquivos completos antes de qualquer indicador definitivo de receita.

## 10. Conclusão

O principal resultado metodológico do projeto é demonstrar que prompts de IA devem ser aplicados sobre dados previamente verificados. A combinação entre auditoria, regras explícitas e análise crítica reduz o risco de duplicidades, somas monetárias incorretas e conclusões que não são sustentadas pelos dados.

## Rodapé

**Autora:** Nágyla Silva  
**Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.**