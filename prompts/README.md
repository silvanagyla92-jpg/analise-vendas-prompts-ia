# Prompts

Esta pasta reúne os prompts utilizados no projeto para orientar ferramentas de Inteligência Artificial na análise de dados de vendas.

## 1. Objetivo

Os prompts foram estruturados para transformar perguntas de negócio em análises claras, reproduzíveis e úteis para tomada de decisão.

## 2. Estratégia de Elaboração

### 2.1 Elementos dos prompts

Cada prompt deve, sempre que possível:

1. Definir o papel da IA;
2. Informar o objetivo da análise;
3. Indicar quais dados devem ser considerados;
4. Especificar critérios, métricas ou comparações;
5. Solicitar uma resposta estruturada;
6. Diferenciar fatos observados de interpretações;
7. Evitar conclusões sem evidência nos dados.

## 3. Organização

### 3.1 Arquivos de prompts

- `01_analise_geral.md` — visão geral do desempenho de vendas;
- `02_produtos.md` — desempenho e participação dos produtos;
- `03_vendas.md` — evolução e comportamento das vendas;
- `04_clientes.md` — análise de clientes e padrões de compra;
- `05_regioes.md` — análise por **país de entrega**, utilizando `delivery_country`;
- `06_insights_estrategicos.md` — consolidação de oportunidades, riscos e recomendações.

## 4. Validação

As respostas geradas por IA não serão consideradas automaticamente como fatos. Os resultados deverão ser confrontados com os dados da planilha e, quando necessário, recalculados ou revisados.

> **Princípio:** a IA apoia a interpretação dos dados; a evidência deve vir da base analisada.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.