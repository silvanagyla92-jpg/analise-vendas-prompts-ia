# Insights Consolidados

## 1. Status

**CONCLUÍDO — insights consolidados após auditoria, validação e deduplicação das bases.**

A base analítica definitiva possui **110 transações únicas e 323 unidades vendidas**. A `Updated_Anbernic_Sales_Data` não deve ser somada novamente, pois seus 30 registros correspondem por `invoice_id` a registros da base geral.

## 2. Insight 1 — Deduplicação é necessária antes da consolidação

**Evidência:** 30 registros da `Updated_Anbernic_Sales_Data` correspondem por `invoice_id` a registros da `Meganium_Sales_Data`.

**Interpretação:** a quinta planilha representa pedidos já presentes na base geral e não vendas adicionais.

**Conclusão:** a referência correta é de **110 transações únicas**, e não 140 registros físicos.

**Confiança:** alta.

## 3. Insight 2 — Etsy lidera em volume

**Evidência:** na base analítica, Etsy possui 42 transações e 115 unidades; Shopee possui 34 transações e 113 unidades; AliExpress possui 34 transações e 95 unidades.

**Interpretação:** Etsy apresenta o maior volume de transações e unidades entre os três canais operacionais.

**Limitação:** isso não demonstra maior rentabilidade, pois as moedas são múltiplas e não há custos ou margem.

**Confiança:** alta.

## 4. Insight 3 — A análise financeira deve respeitar as moedas

**Evidência:** as bases utilizam EUR, GBP e USD.

**Interpretação:** valores monetários de moedas diferentes não são diretamente comparáveis como um único total.

**Recomendação:** qualquer análise financeira consolidada futura deve definir taxa de câmbio, data de referência e regra de conversão.

**Confiança:** alta.

## 5. Insight 4 — A consistência aritmética pode ser validada

**Evidência:** a regra `total_price = quantity × unit_price` foi utilizada na validação das bases analisadas.

**Interpretação:** os campos podem apoiar análises de quantidade e valor nominal quando a relação estiver consistente.

**Limitação:** consistência aritmética não comprova margem, lucro ou correção comercial do preço.

**Confiança:** alta.

## 6. Insight 5 — Não é possível inferir lucro ou margem

**Evidência:** as bases não fornecem custos suficientes para cálculo confiável de lucro ou margem.

**Conclusão:** o projeto permite analisar volume, unidades e valores nominais por moeda, mas não rentabilidade.

**Confiança:** alta.

## 7. Insight 6 — A IA deve ser tratada como apoio à análise

**Evidência:** os prompts estabelecem validação dos números, separação entre fato, cálculo, interpretação e hipótese e proibição de conclusões sem evidência.

**Interpretação:** o valor metodológico do projeto está na combinação entre prompts estruturados, auditoria e verificação dos resultados.

**Confiança:** alta.

## 8. Limitações

1. Não foi realizada conversão cambial.
2. Não foram calculados lucro ou margem.
3. `discount_value` não deve ser tratado automaticamente como desconto efetivo sem documentação de sua semântica.
4. Novembro/2024 é período parcial nas análises que utilizam essa base.
5. Dados pessoais de compradores não devem ser expostos nos resultados.
6. Análises específicas somente devem ser consideradas executadas quando houver resultados quantitativos rastreáveis correspondentes.

## 9. Conclusão

Os principais achados consolidados são sustentados pela auditoria e pelas análises documentadas. A referência quantitativa oficial do projeto é **110 transações únicas e 323 unidades**, com moedas mantidas separadas e sem inferência de lucro ou margem.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.
