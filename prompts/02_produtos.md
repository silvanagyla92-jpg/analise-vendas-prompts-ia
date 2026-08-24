# Prompt 02 — Análise de Produtos

## 1. Objetivo

Identificar quais produtos apresentam melhor e pior desempenho e compreender sua contribuição para vendas e faturamento.

## 2. Prompt

### 2.1 Instrução para a IA

```text
Atue como um analista de dados especializado em desempenho de produtos.

Analise os produtos presentes na base de vendas fornecida.

Primeiro, identifique quais campos podem ser usados para medir:
- quantidade vendida;
- número de transações;
- receita/faturamento;
- preço médio ou valor médio da venda;
- categoria, marca ou outro agrupamento disponível.

Depois, determine, quando os dados permitirem:
1. Os 10 produtos com maior quantidade vendida.
2. Os 10 produtos com maior faturamento.
3. Os 10 produtos com menor desempenho.
4. A participação percentual dos principais produtos no total.
5. Produtos que vendem muito, mas geram menor receita relativa.
6. Produtos que vendem menos, mas apresentam maior valor médio.
7. Categorias ou grupos com desempenho acima ou abaixo da média.

Não presuma que alta quantidade vendida significa maior rentabilidade, pois margem de lucro pode não estar disponível.

Apresente os resultados em tabelas e informe a métrica utilizada em cada ranking.

Para cada achado relevante, explique:
- o que os dados mostram;
- qual comparação foi realizada;
- qual interpretação é possível;
- qual interpretação NÃO pode ser feita sem informações adicionais.

Finalize indicando quais produtos ou categorias merecem investigação comercial e por quê.
```

## 3. Critérios de Validação

### 3.1 Verificações

- Confirmar os rankings diretamente na base.
- Conferir se quantidade e faturamento não foram tratados como a mesma métrica.
- Não afirmar lucratividade sem dados de custo ou margem.
- Verificar percentuais e médias.
- Identificar empates e critérios utilizados em caso de empate.

## 4. Resultado Esperado

Um ranking confiável do desempenho dos produtos, permitindo identificar concentração de vendas, produtos de destaque e oportunidades de investigação.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.