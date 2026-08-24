# Prompt 01 — Análise Geral de Vendas

## Objetivo

Realizar uma primeira leitura estruturada da base de vendas para compreender sua composição, identificar padrões relevantes e levantar hipóteses que possam orientar análises posteriores.

## Prompt

```text
Atue como um analista de dados especializado em vendas e inteligência de negócios.

Analise a base de dados de vendas fornecida, considerando exclusivamente as informações presentes nos dados.

Antes de interpretar os resultados:
1. Identifique as colunas disponíveis e descreva brevemente a função de cada uma.
2. Verifique o período abrangido pela base, quando houver informação de data.
3. Identifique possíveis valores ausentes, duplicidades, inconsistências ou registros que possam afetar a análise.
4. Diferencie claramente fatos observados, cálculos, inferências e hipóteses.
5. Não invente valores que não estejam presentes na base.

Em seguida, apresente:
- quantidade total de registros;
- quantidade de vendas/transações, se essa métrica puder ser determinada;
- faturamento ou valor total, se houver campo adequado;
- ticket médio, quando calculável;
- principais produtos ou categorias;
- períodos de maior e menor desempenho, quando houver datas;
- principais padrões identificados;
- possíveis anomalias ou pontos que mereçam investigação.

Organize a resposta em uma tabela sempre que isso facilitar a comparação.

Para cada insight, informe:
- evidência encontrada nos dados;
- interpretação;
- possível impacto para o negócio;
- nível de confiança (alto, médio ou baixo).

Finalize com até 5 perguntas de investigação que poderiam aprofundar a análise.
```

## Critérios de validação

- Confirmar se todos os números apresentados podem ser reproduzidos a partir da base.
- Verificar se o modelo distinguiu observação de interpretação.
- Conferir cálculos de totais e médias.
- Não aceitar conclusões causais que não sejam sustentadas pelos dados.
- Registrar limitações decorrentes da estrutura ou qualidade da base.

## Resultado esperado

Uma visão inicial e verificável do conjunto de dados, servindo como ponto de partida para as análises específicas de produtos, vendas, clientes, regiões e insights estratégicos.