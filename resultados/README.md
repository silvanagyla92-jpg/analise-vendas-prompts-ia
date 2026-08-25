# Resultados

Esta pasta reúne os principais resultados obtidos a partir das análises de dados de vendas, mantendo a distinção entre fatos observados, cálculos, interpretações, limitações e recomendações.

## 1. Objetivo

Consolidar as descobertas de forma objetiva e transformar os resultados analisados em insights que possam apoiar decisões de negócio, sem extrapolar o que os dados permitem concluir.

## 2. Base Analítica Definitiva

A auditoria cruzada das cinco planilhas estabeleceu a base analítica sem dupla contagem:

- `Meganium_Sales_Data`: 50 registros;
- AliExpress: 20 registros;
- Etsy: 20 registros;
- Shopee: 20 registros;
- `Updated_Anbernic_Sales_Data`: 30 registros correspondentes por `invoice_id` à base geral.

As quatro bases operacionais totalizam **110 transações únicas e 323 unidades**. A `Updated_Anbernic_Sales_Data` é uma representação alternativa de pedidos já presentes na base geral e, portanto, **não deve ser somada novamente**.

As moedas **EUR, GBP e USD** permanecem separadas. Não foi aplicada conversão cambial.

## 3. Tipos de Resultados

- Principais indicadores de desempenho;
- Produtos ou categorias de maior destaque;
- Evolução das vendas;
- Padrões de comportamento;
- Oportunidades identificadas;
- Riscos ou pontos de atenção;
- Recomendações estratégicas;
- Limitações e ressalvas metodológicas.

## 4. Arquivos

### 4.1 Resultados consolidados

- `insights.md` — síntese consolidada dos principais insights validados;
- `insights_obtidos.md` — registro rastreável dos insights efetivamente obtidos durante as análises;
- `conclusao.md` — conclusão final do projeto.

O arquivo `insights_obtidos.md` funciona como registro complementar dos achados e não representa uma segunda base de resultados independente.

## 5. Estrutura dos Insights

Cada insight deve apresentar, quando aplicável:

**Evidência → Cálculo → Interpretação → Impacto potencial → Recomendação → Dados adicionais → Confiança**

Quando um resultado depender de cálculo, o valor deverá ser rastreável aos dados utilizados. Quando for uma interpretação ou hipótese, isso será explicitamente indicado.

## 6. Regras de Validação

Antes de considerar um resultado como consolidado:

1. a base utilizada deve estar identificada;
2. duplicidades e sobreposições entre bases devem ter sido verificadas;
3. `invoice_id` deve ser priorizado para rastreabilidade quando disponível;
4. EUR, GBP e USD não devem ser somados diretamente sem conversão cambial documentada;
5. lucro ou margem não devem ser inferidos sem dados de custo;
6. `discount_value` não deve ser interpretado automaticamente como desconto efetivo sem documentação de sua semântica;
7. fatos observados devem ser diferenciados de cálculos, interpretações e hipóteses;
8. dados pessoais não devem ser reproduzidos desnecessariamente nos resultados.

## 7. Status

**CONCLUÍDO — auditoria quantitativa, deduplicação e definição da base analítica.**

A referência quantitativa oficial para os resultados consolidados é de **110 transações únicas e 323 unidades**.

As análises específicas de produtos, evolução das vendas, clientes e países de entrega somente devem ser apresentadas como resultados executados quando houver evidência quantitativa correspondente. Estruturas metodológicas não devem ser confundidas com análises realizadas.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.
