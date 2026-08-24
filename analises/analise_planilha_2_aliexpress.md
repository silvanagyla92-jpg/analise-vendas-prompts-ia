# Análise da Planilha 2 — Meganium Sales Data — AliExpress

## 1. Escopo

Esta análise considera exclusivamente os 20 registros fornecidos da planilha `Meganium_Sales_Data_-_AliExpress`.

## 2. Validação inicial

- Registros analisados: **20**
- Unidades vendidas: **58**
- Produtos distintos: **5**
- Moedas: **EUR, GBP e USD**
- Países de entrega identificados: **6**
- Canal: **AliExpress** em todos os registros
- Período: **18/05/2024 a 16/10/2024**
- SKU presente em todos os registros.
- A relação `quantity × unit_price = total_price` é consistente nos 20 registros fornecidos.
- Os `invoice_id` apresentados são distintos entre os 20 registros.

## 3. Produtos

| Produto | Transações | Unidades |
|---|---:|---:|
| NEW MEGANIUM RG35XX | 5 | 14 |
| NEW MEGANIUM RG CubeXX | 5 | 12 |
| NEW MEGANIUM RG28XX | 4 | 13 |
| NEW MEGANIUM RG 40XXV | 3 | 10 |
| MEGANIUM RG353M | 3 | 9 |

O `NEW MEGANIUM RG35XX` lidera em unidades, com **14 de 58 unidades (24,14%)**. O `NEW MEGANIUM RG28XX` aparece em segundo, com **13 unidades (22,41%)**.

## 4. Moedas

- USD: 8 transações
- GBP: 7 transações
- EUR: 5 transações

Os valores monetários não foram somados entre moedas. Sem taxa de câmbio e data de referência, não é metodologicamente adequado produzir um ranking financeiro único entre EUR, GBP e USD.

## 5. Países de entrega

| País | Transações | Unidades |
|---|---:|---:|
| Germany | 5 | 14 |
| France | 5 | 12 |
| Australia | 4 | 8 |
| UK | 2 | 7 |
| Canada | 2 | 8 |
| USA | 2 | 9 |

A Alemanha possui o maior volume de unidades, com **14 de 58 (24,14%)**. A França possui 12 unidades (20,69%).

## 6. Descontos

A coluna `discount_value` está disponível e deve ser tratada separadamente do `total_price`. A existência de um valor de desconto não permite concluir, por si só, sobre lucro ou margem.

## 7. Clientes e privacidade

Os dados contêm `buyer_name` e `buyer_birth_date`. Essas informações não são reproduzidas nesta análise e não são necessárias para os insights agregados.

Como cada `invoice_id` fornecido é distinto, não há evidência nesta tabela de repetição do mesmo identificador de transação. Isso não prova que todos os compradores sejam únicos, pois não foi feita identificação nominal para fins de exposição.

## 8. Principais insights

1. O `NEW MEGANIUM RG35XX` apresenta o maior volume de unidades entre os cinco produtos analisados.
2. A Alemanha concentra o maior número de unidades por país de entrega.
3. O conjunto possui três moedas, exigindo análises monetárias separadas.
4. O canal analisado é exclusivamente AliExpress; portanto, esta planilha isoladamente não permite comparar desempenho entre canais.
5. A análise temporal cobre maio a outubro de 2024, mas há apenas 20 registros; conclusões de sazonalidade devem ser evitadas sem uma série mais completa.

## 9. Limitações

- A análise considera somente os 20 registros fornecidos.
- Não há custos, margem ou lucro.
- Não foi fornecida taxa de câmbio para conversão entre moedas.
- Não há dados suficientes nesta tabela para inferir causas das diferenças entre países ou produtos.
- O desconto não foi interpretado como lucro ou perda.

## 10. Classificação dos achados

- **Fato:** quantidade e distribuição dos registros, unidades, produtos, moedas e países.
- **Cálculo:** percentuais e agregações apresentados nesta análise.
- **Interpretação:** concentração relativa observada nas dimensões analisadas.
- **Hipótese:** qualquer explicação causal exigiria dados adicionais.
- **Recomendação:** comparar esta base com as demais planilhas antes de consolidar o desempenho geral.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.