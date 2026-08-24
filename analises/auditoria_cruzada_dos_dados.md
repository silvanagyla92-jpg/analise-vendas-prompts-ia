# Auditoria Cruzada dos Dados

## 1. Objetivo

Esta auditoria verifica a consistência estrutural e a relação entre as bases de vendas utilizadas no projeto, com foco em duplicidades, correspondência de produtos, integridade dos valores e critérios necessários para a geração de insights por meio de prompts de IA.

## 2. Bases analisadas

Foram consideradas cinco planilhas:

1. `Meganium_Sales_Data`
2. `Meganium_Sales_Data_-_AliExpress`
3. Base de vendas do Etsy
4. `Meganium_Sales_Data_-_Shopee`
5. `Updated_Anbernic_Sales_Data`

## 3. Relação entre as bases

A primeira base apresenta registros gerais de vendas. As bases 2, 3 e 4 apresentam registros associados a canais específicos: AliExpress, Etsy e Shopee.

A quinta base possui os mesmos registros identificáveis da primeira base, mantendo campos como data, quantidade, preço, moeda, canal, cupom, desconto, comprador, país de entrega e `invoice_id`. A principal alteração observada é a nomenclatura dos produtos, que passa de MEGANIUM para ANBERNIC.

Dessa forma, a quinta base deve ser tratada como uma versão transformada ou atualizada dos registros da primeira base, e não como uma nova fonte independente de vendas.

## 4. Correspondência de produtos e SKUs

As bases que possuem a coluna `SKU` apresentam correspondência consistente entre SKU e produto:

| SKU | Produto |
|---|---|
| `SKU-35XX01` | NEW MEGANIUM RG35XX |
| `SKU-40XXV01` | NEW MEGANIUM RG 40XXV |
| `SKU-28XX01` | NEW MEGANIUM RG28XX |
| `SKU-CUBEXX01` | NEW MEGANIUM RG CubeXX |
| `SKU-353M01` | MEGANIUM RG353M |

A ausência de SKU nas bases 1 e 5 não impede a análise, mas representa uma diferença estrutural que deve ser considerada na consolidação.

## 5. Validação dos valores

Nos registros fornecidos, a relação entre quantidade, preço unitário e preço total apresenta consistência:

`total_price = quantity × unit_price`

Exemplos observados incluem 2 × 90 = 180, 5 × 100 = 500, 4 × 80 = 320 e 3 × 110 = 330.

O campo `discount_value` deve ser analisado separadamente. A estrutura disponível não permite concluir, sem documentação adicional, se `total_price` representa valor bruto ou valor após desconto. Portanto, não se deve assumir automaticamente que `total_price - discount_value` corresponde à receita líquida.

## 6. Auditoria de duplicidades

O campo `invoice_id` é um identificador relevante para cruzamento dos registros. A correspondência entre as bases 1 e 5 demonstra que os mesmos pedidos podem aparecer em duas representações diferentes.

Consequentemente, a base 5 não deve ser somada à base 1 sem uma regra explícita de deduplicação.

Para futuras consolidações, recomenda-se verificar, em conjunto, `invoice_id`, data, produto, quantidade, preço total e canal.

## 7. Auditoria das moedas

Foram identificadas as moedas EUR, GBP e USD.

Valores de moedas diferentes não devem ser somados diretamente. Uma análise financeira consolidada exige uma taxa de conversão e uma data de referência definidas previamente.

Na ausência dessas informações, recomenda-se apresentar os resultados financeiros separados por moeda.

## 8. Auditoria dos canais

Os canais identificados são:

- Etsy
- Shopee
- AliExpress

Essa dimensão permite análises comparativas de vendas, quantidade, produtos, descontos e distribuição geográfica.

Antes de comparar totais entre bases, deve-se verificar se a base geral contém registros dos mesmos canais já representados nas bases específicas.

## 9. Regras para análise com IA

Os prompts utilizados no projeto devem incorporar as seguintes regras:

1. Verificar duplicidades antes de calcular totais consolidados.
2. Usar `invoice_id` como identificador prioritário no cruzamento.
3. Não contabilizar duas vezes registros que sejam versões da mesma venda.
4. Não somar diretamente valores em moedas diferentes.
5. Não interpretar `discount_value` como receita ou desconto efetivamente aplicado sem confirmar sua definição.
6. Diferenciar fatos observados, cálculos, inferências e recomendações.
7. Informar limitações quando os dados não permitirem uma conclusão segura.

## 10. Conclusão

As bases apresentam estrutura adequada para exploração de dados de vendas e geração de insights com prompts de IA. A principal questão de integridade identificada é a relação entre `Meganium_Sales_Data` e `Updated_Anbernic_Sales_Data`, que não devem ser tratadas como conjuntos independentes.

A análise também deve considerar a presença de múltiplas moedas e a diferença estrutural relacionada à coluna `SKU`.

Esses critérios serão utilizados como premissas para as próximas etapas de análise e para a avaliação da qualidade dos insights produzidos pela IA.

## Rodapé

**Autora:** Nágyla Silva  
**Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.**