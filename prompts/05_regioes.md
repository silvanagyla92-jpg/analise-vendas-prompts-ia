# Prompt 05 — Análise por País de Entrega

## 1. Objetivo

Avaliar a distribuição geográfica das vendas a partir do campo `delivery_country` e identificar diferenças relevantes de desempenho entre os países de entrega.

## 2. Prompt

### 2.1 Instrução para a IA

```text
Atue como um analista de dados especializado em inteligência comercial e análise geográfica.

Analise a distribuição das vendas utilizando exclusivamente os campos geográficos disponíveis na base.

Primeiro, identifique o nível geográfico disponível. Se a base possuir apenas o campo delivery_country, utilize o país de entrega como dimensão geográfica e não crie regiões artificiais.

Quando possível, calcule para cada país de entrega:
- quantidade de vendas;
- quantidade de unidades;
- faturamento, preservando a moeda;
- participação percentual dentro de cada moeda ou de uma base previamente convertida;
- ticket médio, sem misturar moedas;
- produtos predominantes.

Compare os países e identifique:
1. países com maior volume de vendas;
2. países com maior faturamento, respeitando a moeda;
3. países com ticket médio acima ou abaixo da média comparável;
4. concentração de determinados produtos;
5. diferenças que mereçam investigação.

Não some valores monetários de moedas diferentes sem uma regra de conversão documentada.

Não interprete um país como 'melhor' apenas porque possui maior faturamento. Considere a métrica utilizada, a moeda e o contexto disponível.

Não atribua diferenças geográficas a causas econômicas, demográficas, logísticas ou culturais sem dados que sustentem essas explicações. Quando necessário, apresente essas explicações apenas como hipóteses.

Não exponha nomes, datas de nascimento ou outros dados pessoais dos compradores nos resultados.

Apresente rankings e comparações em tabelas.

Para cada diferença relevante, informe:
- métrica;
- comparação;
- evidência;
- possível interpretação;
- limitações.

Finalize indicando quais países deveriam receber atenção prioritária em uma investigação comercial e quais dados adicionais seriam úteis.
```

## 3. Critérios de Validação

### 3.1 Verificações

- Confirmar que `delivery_country` é o campo geográfico utilizado.
- Verificar valores ausentes ou inconsistentes em `delivery_country`.
- Conferir totais por país contra o total da base analisada.
- Recalcular participações percentuais e médias.
- Manter as moedas separadas quando não houver conversão documentada.
- Não transformar correlações geográficas em explicações causais.
- Não expor dados pessoais dos compradores.

## 4. Resultado Esperado

Um panorama comparativo do desempenho por país de entrega, destacando concentração, diferenças de desempenho e oportunidades de investigação, sem misturar moedas ou extrapolar conclusões além das evidências disponíveis.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.