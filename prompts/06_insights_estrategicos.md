# Prompt 06 — Insights Estratégicos

## 1. Objetivo

Consolidar os resultados das análises anteriores e transformar evidências verificadas em insights úteis para tomada de decisão, mantendo separação entre fatos, interpretações, hipóteses e recomendações.

## 2. Prompt

### 2.1 Instrução para a IA

```text
Atue como um analista de negócios responsável por transformar resultados de uma análise de vendas em insights estratégicos.

Utilize somente os resultados e evidências fornecidos nas análises anteriores. Não invente dados, métricas, causas ou informações externas para preencher lacunas.

Antes de gerar recomendações:

1. Verifique se os resultados utilizados são consistentes entre si.
2. Identifique possíveis contradições entre as análises.
3. Verifique a origem de cada número apresentado.
4. Identifique limitações relevantes da base e da metodologia.
5. Não combine valores monetários de moedas diferentes.
6. Não trate faturamento, preço ou volume de vendas como medida de lucro sem dados de custo ou margem.

Para cada insight, siga esta estrutura:

1. Evidência — o que os dados demonstram objetivamente.
2. Interpretação — o que essa evidência permite inferir.
3. Impacto potencial — por que o achado pode ser relevante para o negócio.
4. Recomendação — ação que poderia ser considerada com base na evidência.
5. Dados adicionais — informações necessárias para confirmar ou aprofundar a hipótese.
6. Confiança — alta, média ou baixa, com justificativa.

Priorize os insights segundo:

- relevância para o negócio;
- magnitude do efeito observado;
- consistência entre diferentes análises;
- possibilidade de ação;
- qualidade e rastreabilidade das evidências;
- risco de interpretação equivocada.

Organize os principais achados em uma matriz:

| Prioridade | Insight | Evidência | Impacto potencial | Recomendação | Confiança |
|---|---|---|---|---|---|

Depois, responda:

- Quais são os 5 principais insights sustentados pelos dados?
- Quais produtos merecem atenção e por quê?
- Quais períodos apresentam maior oportunidade ou necessidade de investigação?
- Quais padrões de clientes merecem investigação?
- Quais países de entrega apresentam maior concentração, oportunidade ou necessidade de atenção?
- Quais canais apresentam diferenças relevantes?
- Quais informações ainda estão faltando para uma decisão mais segura?

Diferencie explicitamente:

- Fato observado;
- Cálculo;
- Inferência;
- Hipótese;
- Recomendação.

REGRAS DE SEGURANÇA DA ANÁLISE:

- Não transforme correlação em causalidade.
- Não apresente hipótese como fato.
- Não apresente recomendação como conclusão comprovada.
- Não invente valores para preencher lacunas.
- Não utilize informações pessoais de compradores.
- Não faça generalizações sobre consumidores, países ou produtos sem evidência.
- Não apresente rankings financeiros que misturem moedas.
- Se duas análises apresentarem resultados incompatíveis, sinalize a inconsistência antes de concluir.

Para cada recomendação, indique:

- evidência que a motivou;
- ação sugerida;
- objetivo da ação;
- risco ou limitação;
- indicador que poderia ser acompanhado para avaliar o resultado.

Finalize com um resumo executivo de até 10 linhas, adequado para apresentação a um gestor.
```

## 3. Critérios de Validação

### 3.1 Verificações

- Cada insight deve possuir evidência rastreável.
- Cada número deve possuir origem identificável.
- Recomendações devem estar relacionadas aos achados apresentados.
- Hipóteses devem ser identificadas como hipóteses.
- Fatos, cálculos, inferências e recomendações devem permanecer diferenciados.
- Nenhum número pode ser introduzido sem origem nos dados ou nas análises anteriores.
- Valores monetários devem respeitar a moeda correspondente.
- Deve existir coerência entre os resultados específicos e a síntese final.
- Contradições entre análises devem ser identificadas e explicadas.
- Recomendações devem possuir indicador ou critério que permita avaliação posterior.

## 4. Resultado Esperado

Uma síntese executiva dos principais achados da análise, acompanhada de recomendações rastreáveis, limitações e níveis de confiança, demonstrando como prompts podem apoiar a interpretação crítica de dados e a tomada de decisão sem ultrapassar as evidências disponíveis.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.