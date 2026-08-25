# Insights Obtidos

## 1. Objetivo

Registrar os principais insights derivados da base analítica definitiva, distinguindo fatos observados, cálculos, interpretações e limitações.

## 2. Insight 1 — A deduplicação é necessária antes da consolidação

### Evidência

A `Updated_Anbernic_Sales_Data` possui 30 registros correspondentes por `invoice_id` a registros da `Meganium_Sales_Data`.

### Interpretação

As duas bases não representam 30 vendas adicionais. A quinta planilha é uma representação alternativa dos mesmos pedidos.

### Conclusão

A base analítica correta possui **110 transações únicas**, e não 140 registros físicos.

## 3. Insight 2 — O identificador de venda favorece a rastreabilidade

### Evidência

`invoice_id` permite identificar os 30 registros correspondentes entre a base geral e a `Updated_Anbernic_Sales_Data`.

### Conclusão

O identificador deve ser a chave prioritária para cruzamentos e deduplicação.

## 4. Insight 3 — A base analítica possui 323 unidades

### Evidência

As quatro bases operacionais totalizam:

- Base geral: 146 unidades;
- AliExpress: 58 unidades;
- Etsy: 55 unidades;
- Shopee: 64 unidades.

### Cálculo

**146 + 58 + 55 + 64 = 323 unidades.**

### Conclusão

O total oficial de unidades da consolidação é **323**.

## 5. Insight 4 — Etsy lidera em volume

### Evidência

Na base analítica:

- Etsy: 42 transações e 115 unidades;
- Shopee: 34 transações e 113 unidades;
- AliExpress: 34 transações e 95 unidades.

### Interpretação

Etsy apresenta o maior volume de transações e unidades.

### Limitação

Isso não demonstra que Etsy seja o canal mais rentável, porque as moedas são múltiplas e não há custos ou margem.

## 6. Insight 5 — A análise financeira precisa respeitar as moedas

### Evidência

A base utiliza EUR, GBP e USD.

### Conclusão

Valores monetários de moedas diferentes não devem ser somados diretamente. Qualquer conversão futura deve definir taxa e data de referência.

## 7. Insight 6 — O preço total apresenta consistência aritmética

### Evidência

A regra de validação é `total_price = quantity × unit_price` e os registros analisados apresentam consistência com essa relação.

### Conclusão

Os campos podem ser utilizados nas análises de volume e valor nominal, sem dispensar as demais regras de qualidade.

## 8. Insight 7 — Não é possível inferir lucro com os dados disponíveis

### Evidência

As bases não apresentam custos suficientes para cálculo de lucro ou margem.

### Conclusão

É possível analisar vendas e valores nominais por moeda, mas não rentabilidade.

## 9. Limitações

1. Não foi realizada conversão cambial.
2. Não foram calculados lucro ou margem.
3. A definição operacional de `discount_value` não permite tratá-lo automaticamente como desconto efetivo.
4. Novembro/2024 é um período parcial.
5. Os resultados agregados não devem reproduzir nomes ou datas de nascimento dos compradores.

## 10. Conclusão

O principal resultado metodológico do projeto é demonstrar que prompts de IA devem ser aplicados sobre dados previamente verificados. A auditoria estabeleceu uma base de **110 transações únicas e 323 unidades**, evitando a dupla contagem da `Updated_Anbernic_Sales_Data`.

A combinação entre auditoria, regras explícitas e análise crítica reduz o risco de duplicidades, somas monetárias incorretas e conclusões que não são sustentadas pelos dados.

## Rodapé

**Autora:** Nágyla Silva  
**Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.**