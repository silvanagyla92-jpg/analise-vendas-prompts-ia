# Análise Consolidada dos Dados

## 1. Objetivo

Consolidar os registros das bases operacionais após a auditoria cruzada, preservando rastreabilidade, deduplicação e separação monetária.

## 2. Base analítica definitiva

A auditoria cruzada identificou cinco planilhas no repositório, mas apenas quatro devem participar da soma das vendas:

1. `Meganium_Sales_Data` — 50 registros;
2. `Meganium_Sales_Data_-_AliExpress` — 20 registros;
3. `Meganium_Sales_Data_-_Etsy` — 20 registros;
4. `Meganium_Sales_Data_-_Shopee` — 20 registros.

A `Updated_Anbernic_Sales_Data` possui 30 registros correspondentes por `invoice_id` a registros da base geral e deve ser tratada como representação alternativa, não como fonte independente.

### Resultado da deduplicação

- Registros nas quatro bases operacionais: **110**;
- Registros adicionais da base alternativa: **30**;
- Registros físicos se todas as planilhas fossem somadas: **140**;
- **Transações únicas na base analítica: 110**;
- **Unidades vendidas: 323**.

## 3. Distribuição por canal

| Canal | Transações | Unidades |
|---|---:|---:|
| Etsy | 42 | 115 |
| Shopee | 34 | 113 |
| AliExpress | 34 | 95 |
| **Total** | **110** | **323** |

O Etsy concentra o maior volume de transações e unidades na base analítica. Isso é uma conclusão de **volume**, não de rentabilidade.

## 4. Produtos

Foram identificados cinco modelos:

1. NEW MEGANIUM RG35XX
2. NEW MEGANIUM RG 40XXV
3. NEW MEGANIUM RG28XX
4. NEW MEGANIUM RG CubeXX
5. MEGANIUM RG353M

As bases com SKU permitem padronização adicional dos produtos.

## 5. Período observado

Os registros da base analítica abrangem o período de **20/05/2024 a 10/11/2024**.

Novembro contém somente registros até 10/11/2024 e, portanto, é um período parcial.

## 6. Moedas

Foram identificadas três moedas:

- EUR;
- GBP;
- USD.

Os valores nominais de `total_price` da base analítica são:

| Moeda | Total nominal |
|---|---:|
| EUR | 10.510 |
| GBP | 8.670 |
| USD | 10.430 |

**Não existe um total financeiro único em moeda comum neste projeto.** Somar EUR, GBP e USD diretamente produziria um indicador sem significado financeiro válido. Uma consolidação monetária exige taxa de câmbio e data de referência documentadas.

## 7. Integridade dos valores

A regra de consistência adotada é:

`total_price = quantity × unit_price`

Os registros analisados apresentam consistência com essa relação.

## 8. Descontos

`discount_value` permanece como campo separado. A documentação disponível não permite afirmar se o valor representa o desconto efetivamente abatido da venda ou outra medida operacional.

Por isso, não foram calculados receita líquida, margem ou lucro a partir desse campo.

## 9. Lucro e margem

Não é possível calcular lucro ou margem de forma confiável porque as bases não apresentam custos de aquisição, custos operacionais ou outra estrutura de custo suficiente.

## 10. Rastreabilidade e privacidade

`invoice_id` é a chave prioritária para rastreabilidade e deduplicação.

Os campos `buyer_name` e `buyer_birth_date` não devem ser reproduzidos em resultados agregados, pois não são necessários para os insights de negócio documentados.

## 11. Principais conclusões

### Fatos observados

- A base analítica possui **110 transações únicas**.
- Foram registradas **323 unidades**.
- Existem três canais: Etsy, Shopee e AliExpress.
- Existem cinco produtos identificáveis.
- Existem três moedas: EUR, GBP e USD.
- A `Updated_Anbernic_Sales_Data` contém 30 registros que correspondem à base geral e não devem ser somados novamente.

### Interpretações válidas

- Etsy é o canal de maior volume físico na base consolidada.
- A análise por valor monetário deve permanecer separada por moeda.
- A deduplicação é necessária antes de qualquer indicador consolidado.

### Inferências que não devem ser feitas

Os dados não sustentam conclusões sobre:

- canal mais lucrativo;
- produto mais lucrativo;
- margem;
- lucro;
- efeito causal dos descontos;
- sazonalidade definitiva.

## 12. Conclusão

A base analítica definitiva do projeto é composta pelas quatro bases operacionais, totalizando **110 transações únicas e 323 unidades**. A quinta planilha deve ser preservada como evidência de transformação/correspondência, mas excluída dos cálculos consolidados para evitar dupla contagem.

Essa definição encerra a principal pendência quantitativa identificada na auditoria e estabelece uma referência única para os prompts, análises e resultados finais do projeto.

## Rodapé

**Autora:** Nágyla Silva  
**Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.**