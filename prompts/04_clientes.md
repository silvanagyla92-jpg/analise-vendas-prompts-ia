# Prompt 04 — Análise de Clientes

## Objetivo

Investigar o comportamento de compra dos clientes e identificar padrões de recorrência, concentração e valor das compras.

## Prompt

```text
Atue como um analista de dados especializado em comportamento de clientes e vendas.

Analise os registros de clientes presentes na base, respeitando exclusivamente as informações disponíveis.

Primeiro, identifique se existe um identificador de cliente confiável e quais campos permitem medir o comportamento de compra.

Quando possível, calcule:
- número total de clientes identificáveis;
- número de clientes com uma ou mais compras;
- quantidade média de compras por cliente;
- valor total comprado por cliente;
- ticket médio por cliente;
- frequência de compra;
- clientes com maior volume de compras;
- clientes com maior valor total de compras;
- concentração do faturamento entre os principais clientes.

Se houver informação temporal suficiente, investigue também:
- clientes recorrentes;
- novos clientes por período;
- clientes sem compras recentes;
- intervalo médio entre compras.

Não classifique clientes como 'fiéis', 'inativos' ou 'perdidos' sem definir previamente o critério e verificar se os dados sustentam essa classificação.

Não exponha informações pessoais desnecessárias. Trabalhe preferencialmente com identificadores agregados ou anonimizados.

Apresente os resultados em tabelas e destaque padrões relevantes.

Para cada insight, informe:
- evidência;
- métrica utilizada;
- interpretação;
- limitação;
- nível de confiança.

Finalize com recomendações de investigação comercial baseadas nos padrões observados, sem afirmar causalidade quando ela não puder ser demonstrada.
```

## Critérios de validação

- Confirmar se o identificador de cliente é adequado.
- Verificar duplicidades e registros inconsistentes.
- Recalcular médias, totais e percentuais.
- Definir explicitamente qualquer critério de recorrência ou inatividade.
- Evitar conclusões sobre comportamento que não possa ser observado nos dados.

## Resultado esperado

Uma visão estruturada do comportamento dos clientes, com foco em frequência, valor, recorrência e concentração das vendas.