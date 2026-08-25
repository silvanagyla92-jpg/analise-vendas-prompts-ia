# Conclusão Final

## 1. Status

**CONCLUÍDO — síntese final após auditoria, deduplicação e validação da base analítica.**

## 2. Síntese dos Resultados

A auditoria cruzada das cinco planilhas estabeleceu uma base analítica definitiva de **110 transações únicas e 323 unidades vendidas**. A `Updated_Anbernic_Sales_Data` possui 30 registros correspondentes por `invoice_id` à base geral e, portanto, não deve ser somada novamente.

A análise demonstrou que:

- duplicidades entre bases devem ser verificadas antes de qualquer consolidação;
- `invoice_id` é o identificador prioritário para rastreabilidade e deduplicação quando disponível;
- EUR, GBP e USD devem permanecer separados na análise monetária;
- consistência entre `quantity × unit_price` e `total_price` pode ser validada aritmeticamente, mas não comprova lucro ou margem;
- não é possível inferir rentabilidade sem dados de custos e margem;
- dados pessoais de compradores não são necessários para os insights agregados e não devem ser expostos;
- respostas de IA precisam ser confrontadas com os dados e submetidas a validação crítica.

## 3. Principais Insights

O **Etsy** apresenta o maior volume entre os canais operacionais, com 42 transações e 115 unidades na base analítica. Isso representa liderança em volume, não em rentabilidade.

A deduplicação da `Updated_Anbernic_Sales_Data` evita que os mesmos pedidos sejam contabilizados duas vezes.

A utilização de múltiplas moedas impede a criação de um ranking financeiro único sem uma regra de conversão cambial documentada.

## 4. Aprendizados Metodológicos

O projeto demonstra um fluxo de trabalho em que a IA atua como ferramenta de apoio:

**Dados → Auditoria → Pergunta de negócio → Prompt → IA → Validação → Insight → Recomendação**

O principal aprendizado é que uma resposta gerada por IA não deve ser considerada automaticamente verdadeira. Totais, percentuais, rankings e conclusões precisam ser rastreáveis aos dados utilizados.

## 5. Limitações

1. Não foi realizada conversão entre EUR, GBP e USD.
2. Não foram calculados lucro ou margem por ausência de custos suficientes.
3. `discount_value` não foi interpretado automaticamente como desconto efetivo sem documentação da sua semântica.
4. Novembro/2024 é um período parcial nas análises temporais que o utilizam.
5. Não devem ser publicadas informações pessoais dos compradores.
6. As análises específicas de produtos, vendas, clientes e países de entrega somente devem ser consideradas resultados executados quando houver evidência quantitativa correspondente.

## 6. Recomendações Finais

- manter `invoice_id` como chave prioritária para auditorias e cruzamentos;
- preservar a separação das moedas;
- validar qualquer nova consolidação antes de gerar indicadores;
- utilizar prompts com critérios explícitos de validação;
- separar fatos, cálculos, interpretações, hipóteses e recomendações;
- adicionar dados de custo e margem caso o objetivo futuro seja analisar rentabilidade.

## 7. Conclusão

O projeto apresenta uma aplicação documentada de prompts de IA para análise de vendas, combinada com auditoria, deduplicação, rastreabilidade e avaliação crítica das respostas. A base quantitativa oficial é de **110 transações únicas e 323 unidades vendidas**.

Os resultados consolidados respeitam as limitações dos dados disponíveis e evitam dupla contagem, mistura indevida de moedas e inferências de lucratividade sem evidência.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.
