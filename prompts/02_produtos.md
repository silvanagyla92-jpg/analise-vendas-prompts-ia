# Prompt 02 — Análise de Produtos

## 1. Objetivo

Identificar produtos com maior e menor desempenho e compreender sua contribuição para o volume de vendas e para o valor comercial das transações.

## 2. Prompt

### 2.1 Instrução para a IA

```text
Atue como um analista de dados especializado em desempenho de produtos.

Analise exclusivamente os produtos presentes na base fornecida.

Antes dos rankings:

1. Identifique o campo que representa o produto.
2. Identifique os campos disponíveis para quantidade, transações e valores monetários.
3. Verifique se existem categorias, marcas ou outros agrupamentos.
4. Identifique as moedas existentes.
5. Verifique valores ausentes, duplicidades e registros que possam distorcer os rankings.

Depois, calcule, somente quando houver dados suficientes:

1. Os 10 produtos com maior quantidade vendida.
2. Os 10 produtos com maior valor de vendas, mantendo cada moeda separada.
3. Os produtos com menor desempenho, informando claramente a métrica utilizada.
4. A participação percentual dos principais produtos no volume de unidades vendidas.
5. A participação percentual no valor das vendas, separada por moeda.
6. Produtos com alto volume de unidades e menor valor médio por unidade.
7. Produtos com menor volume de unidades e maior valor médio por unidade.
8. Desempenho por categoria, marca ou agrupamento disponível.

Para cada ranking, informe:
- métrica utilizada;
- período analisado;
- moeda, quando aplicável;
- critério de ordenação;
- tratamento de empates, quando houver.

IMPORTANTE:
- Não some valores de moedas diferentes.
- Não trate preço ou faturamento como lucro.
- Não afirme que um produto é mais rentável sem dados de custo ou margem.
- Não atribua causa ao desempenho de um produto sem evidência.
- Não invente categorias ou características que não existam na base.

Para cada achado relevante, apresente:

- Evidência: cálculo ou dado que sustenta o achado;
- Interpretação: o que o resultado permite concluir;
- Limitação: o que não pode ser concluído com os dados disponíveis;
- Confiança: alta, média ou baixa.

Finalize indicando quais produtos ou grupos merecem investigação comercial e explique a justificativa baseada nos dados.
```

## 3. Critérios de Validação

### 3.1 Verificações

- Reproduzir os rankings diretamente a partir da base.
- Conferir quantidade, transações e valores separadamente.
- Verificar se os valores monetários foram comparados somente dentro da mesma moeda.
- Conferir percentuais, médias e participações.
- Confirmar o período utilizado.
- Identificar e documentar empates.
- Não aceitar afirmações de lucratividade sem dados de custo ou margem.
- Verificar se nenhuma característica de produto foi inferida sem evidência.
- Registrar limitações relevantes.

## 4. Resultado Esperado

Um diagnóstico verificável do desempenho dos produtos, destacando volume, valor das vendas e padrões relevantes sem misturar moedas ou transformar indicadores de vendas em conclusões sobre lucratividade.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.