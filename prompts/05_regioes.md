# Prompt 05 — Análise por País de Entrega

## 1. Objetivo

Analisar a distribuição das vendas por país de entrega, identificando diferenças de volume, quantidade de unidades e valor comercial entre os mercados presentes na base.

## 2. Prompt

### 2.1 Instrução para a IA

```text
Atue como um analista de dados especializado em vendas e desempenho por mercado.

Analise exclusivamente os dados fornecidos e utilize o campo de país de entrega disponível na base. Não invente regiões ou categorias geográficas que não estejam presentes nos dados.

Antes da análise:

1. Identifique o campo utilizado para representar o país de entrega.
2. Verifique valores ausentes, inconsistentes ou inválidos nesse campo.
3. Identifique as moedas existentes.
4. Verifique se existem duplicidades que possam alterar os resultados.
5. Identifique o período analisado.

Quando os dados permitirem, calcule por país de entrega:

- quantidade de transações;
- quantidade de unidades vendidas;
- valor das vendas, mantendo cada moeda separada;
- ticket médio por moeda;
- participação percentual no volume de transações;
- participação percentual nas unidades vendidas;
- participação percentual no valor das vendas, separada por moeda;
- produtos mais vendidos;
- canais de venda com maior participação.

Apresente rankings somente quando a comparação for metodologicamente válida.

Para valores monetários:

- não some moedas diferentes;
- não faça conversão cambial sem uma taxa e uma data de referência explicitamente fornecidas;
- deixe claro qual moeda está sendo analisada.

Investigue:

1. países com maior volume de vendas;
2. países com maior quantidade de unidades;
3. países com maior valor de vendas dentro de cada moeda;
4. concentração das vendas por país;
5. diferenças relevantes entre países;
6. possíveis mercados que mereçam investigação adicional.

IMPORTANTE:

- País com maior faturamento não significa necessariamente país mais lucrativo.
- Não atribua causas às diferenças entre países sem evidência.
- Não utilize informações externas para explicar desempenho, demanda, cultura, economia ou comportamento dos consumidores.
- Não faça generalizações sobre consumidores de um país com base apenas nos dados de vendas.
- Não trate correlação entre país e vendas como causalidade.

Para cada insight relevante, apresente:

- Evidência: dado ou cálculo que sustenta o insight;
- Métrica: indicador utilizado;
- Comparação: países ou grupos comparados;
- Interpretação: conclusão permitida pelos dados;
- Limitação: informação que não pode ser determinada;
- Confiança: alta, média ou baixa.

Finalize indicando até 5 oportunidades de investigação comercial baseadas nos dados e quais informações adicionais seriam necessárias para confirmar hipóteses.
```

## 3. Critérios de Validação

### 3.1 Verificações

- Confirmar que `delivery_country` foi utilizado como dimensão geográfica.
- Verificar valores ausentes e grafias inconsistentes de países.
- Recalcular quantidades, totais e percentuais.
- Confirmar que moedas diferentes permaneceram separadas.
- Verificar se os rankings são comparáveis.
- Conferir o período analisado.
- Verificar se participações percentuais utilizam o denominador correto.
- Não aceitar explicações causais sem evidência.
- Não aceitar generalizações sobre consumidores de um país sem dados que as sustentem.
- Registrar limitações relevantes.

## 4. Resultado Esperado

Uma análise verificável da distribuição das vendas por país de entrega, destacando concentração, volume, unidades e valor das vendas sem criar categorias geográficas inexistentes ou misturar moedas.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.