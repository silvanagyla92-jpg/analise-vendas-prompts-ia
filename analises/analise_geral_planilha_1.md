# Análise Geral — Planilha 1

## 1. Escopo

Esta análise utiliza exclusivamente a **Planilha 1 — `Meganium_Sales_Data`** fornecida nesta etapa do projeto.

Os resultados abaixo **não representam ainda a análise consolidada das cinco planilhas do repositório**. As demais bases deverão ser analisadas separadamente antes de qualquer consolidação.

## 2. Qualidade e Estrutura dos Dados

- Registros analisados: **50**.
- Produtos distintos: **5**.
- Canais de venda distintos: **3**.
- Moedas: **EUR, GBP e USD**.
- Países de entrega distintos: **7**.
- Período: **20/05/2024 a 10/11/2024**.
- Duplicidades exatas nas linhas fornecidas: **0**.
- Consistência entre `quantity × unit_price` e `total_price`: **100% dos 50 registros fornecidos são consistentes**.

## 3. Volume de Vendas

Foram registradas **50 transações**, totalizando **146 unidades**.

O campo `total_price` soma **5.050 EUR, 4.620 GBP e 4.010 USD**. Esses valores devem permanecer separados, pois não existe taxa de câmbio definida no projeto.

### 3.1 Ticket médio por moeda

| Moeda | Transações | Unidades | Total informado | Ticket médio por transação |
|---|---:|---:|---:|---:|
| EUR | 19 | 54 | 5.050 | 265,79 EUR |
| GBP | 17 | 52 | 4.620 | 271,76 GBP |
| USD | 14 | 40 | 4.010 | 286,43 USD |

**Importante:** os tickets médios acima não devem ser comparados como se fossem valores equivalentes, porque estão expressos em moedas diferentes.

## 4. Descontos

O campo `discount_value` totaliza **2.314,08** nas moedas originais dos respectivos registros. Como a moeda do desconto acompanha a moeda da transação e não foi fornecida uma regra de conversão, não é correto apresentar esse valor como um único montante monetário.

A razão entre `discount_value` e `total_price`, calculada dentro da própria unidade monetária de cada registro e agregada sobre esta amostra, é de aproximadamente **16,92%**. Esse indicador deve ser interpretado como uma relação entre os campos fornecidos, e não como margem ou percentual de desconto efetivamente aplicado ao preço final, pois a documentação da base não estabelece formalmente a semântica de `total_price` em relação ao desconto.

## 5. Desempenho por Produto

| Produto | Transações | Unidades | Total informado |
|---|---:|---:|---:|
| NEW MEGANIUM RG 40XXV | 15 | 43 | 4.300 |
| NEW MEGANIUM RG35XX | 11 | 36 | 3.240 |
| MEGANIUM RG353M | 12 | 34 | 3.740 |
| NEW MEGANIUM RG28XX | 8 | 24 | 1.680 |
| NEW MEGANIUM RG CubeXX | 4 | 9 | 720 |

O **NEW MEGANIUM RG 40XXV** lidera em quantidade de unidades, com **43 unidades**, equivalente a **29,45%** das unidades da amostra.

O **NEW MEGANIUM RG35XX** ocupa a segunda posição em unidades, com **36 unidades**, enquanto o **MEGANIUM RG353M** registra **34 unidades**.

Não é metodologicamente correto comparar os valores totais dos produtos entre si como um ranking financeiro único, pois os registros utilizam EUR, GBP e USD.

## 6. Desempenho por Canal

| Canal | Transações | Unidades | Total informado |
|---|---:|---:|---:|
| Etsy | 22 | 60 | 5.460 |
| Shopee | 14 | 49 | 4.630 |
| AliExpress | 14 | 37 | 3.590 |

O **Etsy** concentra **44% das transações** e **60 das 146 unidades**, sendo o canal com maior volume de transações e unidades nesta planilha.

Os valores monetários por canal não devem ser somados ou comparados diretamente sem separar as moedas ou estabelecer uma conversão cambial documentada.

## 7. País de Entrega

| País de entrega | Transações | Unidades | Total informado |
|---|---:|---:|---:|
| UK | 13 | 40 | 3.850 |
| Canada | 8 | 25 | 2.290 |
| Australia | 7 | 21 | 2.000 |
| USA | 7 | 14 | 1.250 |
| Japan | 6 | 21 | 2.060 |
| France | 5 | 12 | 1.010 |
| Germany | 4 | 13 | 1.220 |

O **UK** apresenta o maior número de transações, com **13**, e também o maior volume de unidades, com **40**.

A concentração por país deve ser analisada principalmente por transações e unidades. O ranking de valores monetários precisa permanecer separado por moeda.

## 8. Evolução Mensal

| Mês | Transações | Unidades | Total informado |
|---|---:|---:|---:|
| Maio/2024 | 4 | 15 | 1.190 |
| Junho/2024 | 7 | 18 | 1.710 |
| Julho/2024 | 12 | 34 | 3.140 |
| Agosto/2024 | 12 | 34 | 3.260 |
| Setembro/2024 | 5 | 15 | 1.480 |
| Outubro/2024 | 7 | 23 | 2.190 |
| Novembro/2024* | 3 | 7 | 710 |

`*` Novembro contém dados somente até **10/11/2024**, portanto é um período parcial e não deve ser comparado diretamente com meses completos sem ressalva.

Julho e agosto apresentam os maiores volumes de unidades, com **34 unidades cada**. Agosto apresenta o maior `total_price` nominal agregado da tabela, **3.260**, mas esse valor mistura EUR, GBP e USD e, portanto, não representa um faturamento monetário comparável.

## 9. Principais Insights

### Insight 1 — Produto líder em volume

O NEW MEGANIUM RG 40XXV apresenta o maior volume de unidades da planilha, com **43 unidades (29,45%)**.

**Interpretação:** é o produto com maior participação no volume físico de vendas da amostra.

**Limitação:** isso não demonstra maior lucro ou margem.

**Confiança:** alta.

### Insight 2 — Etsy lidera em volume transacional

O Etsy registra **22 das 50 transações (44%)** e **60 das 146 unidades**.

**Interpretação:** o canal apresenta a maior participação em volume de transações e unidades na Planilha 1.

**Limitação:** não permite concluir que seja o canal mais rentável.

**Confiança:** alta.

### Insight 3 — UK lidera em volume de entregas

O UK concentra **13 transações e 40 unidades**, os maiores volumes entre os países da amostra.

**Interpretação:** o mercado de entrega do UK merece atenção prioritária nas análises seguintes.

**Limitação:** não há evidência suficiente para explicar por que o volume é maior.

**Confiança:** alta.

### Insight 4 — Julho e agosto concentram o maior volume físico

Cada um desses meses registra **34 unidades**, o maior volume mensal observado na planilha.

**Interpretação:** existe concentração de volume nesses dois meses.

**Limitação:** isso não comprova sazonalidade; seriam necessários mais períodos comparáveis.

**Confiança:** alta para o fato observado; baixa para qualquer explicação causal.

## 10. Limitações

1. Esta análise considera somente a Planilha 1 fornecida nesta etapa.
2. As moedas EUR, GBP e USD não foram convertidas.
3. Não há dados de custo ou margem para análise de lucro.
4. Novembro/2024 é um período parcial.
5. A relação exata entre `discount_value` e o preço efetivamente pago não está documentada na informação fornecida.
6. A análise de comportamento individual dos compradores não será publicada com nomes ou outras informações pessoais.
7. Ainda é necessário comparar esta planilha com as demais bases antes de definir uma base consolidada sem dupla contagem.

## 11. Conclusão

A Planilha 1 apresenta dados estruturados e consistentes nos 50 registros fornecidos. O maior volume físico está concentrado no **NEW MEGANIUM RG 40XXV**, no canal **Etsy** e no **UK** como país de entrega. Julho e agosto apresentam os maiores volumes mensais de unidades.

Esses resultados são válidos **para a Planilha 1** e não devem ser generalizados para todo o conjunto de arquivos do projeto até que as demais planilhas sejam auditadas e comparadas.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.