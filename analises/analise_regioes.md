# Análise por País de Entrega

## 1. Status

**ESTRUTURA METODOLÓGICA — análise específica por país de entrega não registrada como resultado independente.**

A dimensão geográfica utilizada no projeto é `delivery_country`. O termo **país de entrega** é adotado como nomenclatura oficial para evitar a alternância entre "região" e "país".

## 2. Objetivo

Analisar a distribuição das vendas por país de entrega, comparando volume, unidades e valores comerciais quando os dados permitirem.

## 3. Estrutura Metodológica

Quando executada, a análise deverá registrar:

- base e período utilizados;
- prompt aplicado;
- ranking dos países de entrega;
- volume de transações e unidades;
- valores por moeda;
- participação percentual com denominador explícito;
- validação dos cálculos;
- limitações e hipóteses;
- insights e recomendações.

## 4. Regras de Validação

- Utilizar `delivery_country` como dimensão geográfica.
- Verificar valores ausentes e grafias inconsistentes.
- Não somar EUR, GBP e USD.
- Não converter moedas sem taxa e data de referência documentadas.
- Não atribuir causas às diferenças entre países sem evidência.
- Não generalizar características de consumidores a partir de dados agregados de vendas.
- Diferenciar fato, cálculo, interpretação e hipótese.

## 5. Relação com os Resultados Consolidados

A consolidação oficial do projeto possui **110 transações únicas e 323 unidades**. Esses números vêm da auditoria cruzada e não representam uma análise específica por país de entrega.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.
