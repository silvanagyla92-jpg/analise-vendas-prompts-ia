# Prompt 05 — Análise por Regiões

## Objetivo

Avaliar a distribuição geográfica das vendas e identificar diferenças relevantes de desempenho entre regiões.

## Prompt

```text
Atue como um analista de dados especializado em inteligência comercial e análise geográfica.

Analise a distribuição das vendas por região utilizando exclusivamente os campos geográficos disponíveis na base.

Primeiro, identifique quais níveis geográficos existem, por exemplo:
- país;
- estado/província;
- cidade;
- região;
- território;
- outro agrupamento disponível.

Depois, quando possível, calcule para cada região:
- quantidade de vendas;
- faturamento;
- participação percentual no total;
- ticket médio;
- quantidade de clientes;
- produtos ou categorias predominantes.

Compare as regiões e identifique:
1. regiões líderes em volume;
2. regiões líderes em faturamento;
3. regiões com ticket médio acima ou abaixo da média;
4. regiões com concentração relevante de determinados produtos;
5. diferenças que mereçam investigação.

Não interprete uma região como 'melhor' apenas porque possui maior faturamento. Considere a métrica utilizada e o contexto disponível.

Não atribua diferenças regionais a causas econômicas, demográficas, logísticas ou culturais sem dados que sustentem essas explicações. Quando necessário, apresente essas explicações apenas como hipóteses.

Apresente rankings e comparações em tabelas.

Para cada diferença relevante, informe:
- métrica;
- comparação;
- evidência;
- possível interpretação;
- limitações.

Finalize indicando quais regiões deveriam receber atenção prioritária em uma investigação comercial e quais dados adicionais seriam úteis.
```

## Critérios de validação

- Confirmar a classificação geográfica dos registros.
- Verificar valores ausentes ou inconsistentes em campos de região.
- Conferir totais regionais contra o total geral.
- Recalcular participações percentuais e médias.
- Não transformar correlações geográficas em explicações causais.

## Resultado esperado

Um panorama comparativo da performance regional, destacando concentração, diferenças de desempenho e oportunidades de investigação.