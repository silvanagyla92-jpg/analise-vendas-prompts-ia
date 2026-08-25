# Resultados

Esta pasta reúne os principais resultados obtidos a partir das análises de dados de vendas, mantendo a distinção entre fatos observados, interpretações, limitações e recomendações.

## 1. Objetivo

Consolidar as descobertas de forma objetiva e transformar os resultados analisados em insights que possam apoiar decisões de negócio, sem extrapolar o que os dados permitem concluir.

## 2. Tipos de Resultados

### 2.1 Categorias de resultados

- Principais indicadores de desempenho;
- Produtos ou categorias de maior destaque;
- Evolução das vendas;
- Padrões de comportamento;
- Oportunidades identificadas;
- Riscos ou pontos de atenção;
- Recomendações estratégicas;
- Limitações e ressalvas metodológicas.

## 3. Critério de Apresentação

### 3.1 Estrutura dos insights

Cada insight deverá ser apresentado, quando aplicável, com:

**Evidência → Interpretação → Impacto potencial → Recomendação**

Quando um resultado depender de cálculo, o valor deverá ser rastreável aos dados utilizados. Quando for uma interpretação, isso será explicitamente indicado.

Também devem ser informados o escopo da base analisada e as limitações que possam afetar a interpretação.

## 4. Arquivos

### 4.1 Resultados consolidados

- `insights.md` — principais insights destinados à apresentação consolidada;
- `insights_obtidos.md` — registro dos insights efetivamente obtidos durante as análises, incluindo evidências, interpretações e limitações;
- `conclusao.md` — conclusão geral do projeto.

O arquivo `insights_obtidos.md` não deve ser interpretado como uma segunda base de resultados independente. Ele funciona como registro complementar e rastreável dos achados.

## 5. Regras de Validação

Antes de considerar um resultado como consolidado:

1. a base utilizada deve estar identificada;
2. duplicidades e sobreposições entre bases devem ter sido verificadas;
3. `invoice_id` deve ser priorizado para rastreabilidade quando disponível;
4. EUR, GBP e USD não devem ser somados diretamente sem conversão cambial documentada;
5. lucro ou margem não devem ser inferidos sem dados de custo;
6. `discount_value` não deve ser interpretado como desconto efetivo sem documentação da sua semântica;
7. fatos observados devem ser diferenciados de interpretações e hipóteses;
8. dados pessoais não devem ser reproduzidos desnecessariamente nos resultados.

## 6. Status

Os resultados específicos e a auditoria metodológica já foram documentados. O fechamento quantitativo do projeto depende da validação final da sobreposição entre todas as bases e da confirmação da base analítica definitiva sem dupla contagem.

Enquanto essa etapa não for concluída, resultados consolidados devem ser apresentados com o escopo da base claramente identificado.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.
