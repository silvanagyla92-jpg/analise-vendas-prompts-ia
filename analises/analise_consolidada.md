# Análise Consolidada dos Dados

## 1. Objetivo

Consolidar os registros fornecidos para o projeto após a auditoria cruzada, preservando a rastreabilidade das bases e evitando dupla contagem.

## 2. Bases consideradas

Foram analisadas quatro bases operacionais:

1. `Meganium_Sales_Data`
2. `Meganium_Sales_Data_-_AliExpress`
3. Base de vendas do Etsy
4. `Meganium_Sales_Data_-_Shopee`

A base `Updated_Anbernic_Sales_Data` não deve ser somada à base principal, pois os registros fornecidos demonstram correspondência com ela.

## 3. Escopo dos dados enviados

Nos registros efetivamente fornecidos para esta etapa, foram analisadas **110 linhas**, correspondentes a **323 unidades vendidas**.

Esses números representam somente os registros apresentados nesta etapa da conversa e não devem ser interpretados como o total de toda a base original caso existam outras linhas nos arquivos completos.

## 4. Produtos

Foram identificados cinco modelos:

1. NEW MEGANIUM RG35XX
2. NEW MEGANIUM RG 40XXV
3. NEW MEGANIUM RG28XX
4. NEW MEGANIUM RG CubeXX
5. MEGANIUM RG353M

Nas bases com SKU, os códigos permitem relacionar os produtos de maneira padronizada.

## 5. Canais

Os registros abrangem:

1. Etsy
2. Shopee
3. AliExpress

A separação por canal permite análises específicas de volume, produtos, descontos e distribuição geográfica.

## 6. Período observado

Nos dados fornecidos, as datas variam de **20/05/2024 a 10/11/2024**.

## 7. Moedas

Foram identificadas:

1. EUR
2. GBP
3. USD

Os valores financeiros não foram convertidos entre moedas. Portanto, não é metodologicamente correto apresentar um único total monetário somando diretamente EUR, GBP e USD.

## 8. Integridade dos valores

Nos registros apresentados, `total_price` é consistente com `quantity × unit_price`.

O campo `discount_value` foi mantido como uma dimensão separada. Não foi assumido que ele representa necessariamente o desconto efetivamente abatido da receita, pois sua definição operacional não foi fornecida.

## 9. Duplicidade

A `invoice_id` deve ser utilizada como identificador prioritário para cruzamentos. A `Updated_Anbernic_Sales_Data` contém registros correspondentes aos da base principal e, por isso, deve ser tratada como representação alternativa dos dados, não como uma quinta fonte independente.

## 10. Interpretação

Os dados permitem explorar desempenho por produto, canal, período, país e moeda. Entretanto, não permitem calcular lucro ou margem, pois não foram fornecidos custos dos produtos.

Também não é possível comparar receita total entre moedas sem definir uma taxa de câmbio e uma data de referência.

## 11. Conclusão

A consolidação deve priorizar rastreabilidade, deduplicação e separação monetária. Esses critérios serão utilizados como regras para os prompts e para a interpretação dos insights gerados por IA.

## Rodapé

**Autora:** Nágyla Silva  
**Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.**