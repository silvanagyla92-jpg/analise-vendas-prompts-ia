# Metodologia

Este documento registra o método utilizado para desenvolver o projeto de análise de vendas com apoio de prompts e ferramentas de Inteligência Artificial.

## 1. Preparação e Auditoria dos Dados

Foram verificadas a estrutura das planilhas, as colunas disponíveis, os tipos de dados, duplicidades, período analisado, moedas e consistência dos registros. A sobreposição entre as bases foi analisada para evitar dupla contagem.

## 2. Definição das Perguntas

As perguntas foram estruturadas a partir de objetivos de negócio, evitando análises genéricas. Foram consideradas dimensões como desempenho de vendas, produtos, evolução temporal, comportamento de clientes, canais e países de entrega.

## 3. Engenharia de Prompts

Os prompts foram estruturados com contexto, objetivo, dados a considerar, métricas, dimensões de análise, formato esperado e critérios para evitar inferências indevidas.

## 4. Aplicação da IA

As ferramentas de Inteligência Artificial foram utilizadas como apoio à interpretação dos dados e à identificação de padrões e possíveis insights. A resposta da IA não foi considerada evidência por si só.

## 5. Validação

As respostas e conclusões quantitativas foram confrontadas com os dados disponíveis. A base analítica definitiva foi estabelecida em **110 transações únicas e 323 unidades**, sem dupla contagem da `Updated_Anbernic_Sales_Data.csv`.

Os valores monetários permaneceram separados por moeda: EUR, GBP e USD. Não foi aplicada conversão cambial.

## 6. Síntese dos Insights

Os resultados validados foram transformados em insights de negócio, distinguindo evidências, cálculos, interpretações, hipóteses e limitações.

## 7. Recomendações

Quando houve evidência suficiente, os insights originaram recomendações. As recomendações foram diferenciadas dos fatos observados e das interpretações.

## 8. Documentação

O processo relevante foi registrado no GitHub, incluindo dados utilizados, prompts, análises, auditoria, evidências, resultados e limitações.

## 9. Fluxo Executado

**Dados → Auditoria → Pergunta → Prompt → Resposta da IA → Validação → Insight → Recomendação → Documentação**

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.