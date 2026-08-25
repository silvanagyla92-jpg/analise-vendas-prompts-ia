# Análises

Esta pasta documenta as análises realizadas sobre os dados de vendas e registra como os prompts foram utilizados para explorar padrões e relações relevantes.

## 1. Objetivos das Análises

### 1.1 Finalidades

- Identificar padrões de vendas;
- Comparar desempenho entre produtos, períodos, clientes e países de entrega, quando disponíveis;
- Encontrar tendências, concentrações e possíveis anomalias;
- Transformar resultados quantitativos em interpretações de negócio;
- Registrar limitações e pontos que exigem validação;
- Verificar a consistência dos dados antes da consolidação.

## 2. Fluxo de Análise

### 2.1 Etapas

**Dados → Auditoria → Pergunta de negócio → Prompt → Resposta da IA → Verificação → Insight**

A resposta da ferramenta de IA será tratada como apoio à análise, e não como fonte independente de verdade.

## 3. Estrutura dos Registros

### 3.1 Elementos obrigatórios

Cada análise deverá apresentar, quando aplicável:

1. **Pergunta analisada**;
2. **Dados utilizados**;
3. **Prompt aplicado**;
4. **Resultado observado**;
5. **Validação dos dados**;
6. **Interpretação**;
7. **Insight para o negócio**;
8. **Limitações ou ressalvas**.

## 4. Arquivos

### 4.1 Análises específicas

- `analise_vendas.md` — análise do comportamento geral das vendas;
- `analise_produtos.md` — desempenho dos produtos;
- `analise_clientes.md` — comportamento dos clientes;
- `analise_regioes.md` — distribuição e desempenho por país de entrega;
- `insights_estrategicos.md` — síntese das descobertas relevantes;
- `analise_geral_planilha_1.md` — análise específica da Planilha 1 (`Meganium_Sales_Data`), com escopo e métricas explicitamente delimitados;
- `analise_planilha_2_aliexpress.md` — análise específica da base do AliExpress;
- `analise_consolidada.md` — consolidação das bases consideradas após a auditoria, respeitando as regras de deduplicação e separação monetária;
- `auditoria_cruzada_dos_dados.md` — comparação entre bases, identificação de correspondências, rastreabilidade e prevenção de dupla contagem.

## 5. Distinção entre as Auditorias

A auditoria do projeto possui duas camadas complementares:

### 5.1 Auditoria estrutural

`dados/relatorio_auditoria_dados.md`

Verifica a estrutura e a qualidade básica dos registros, incluindo campos, consistência aritmética, valores ausentes, duplicidades e regras gerais de validação.

### 5.2 Auditoria cruzada

`analises/auditoria_cruzada_dos_dados.md`

Compara as bases entre si para identificar registros correspondentes, sobreposição, uso de `invoice_id` e risco de dupla contagem.

Essa distinção evita tratar uma validação individual como se fosse uma auditoria completa de integração entre fontes.

## 6. Regras para Consolidação

Antes de qualquer consolidação:

1. verificar a sobreposição entre as bases;
2. priorizar `invoice_id` para rastreabilidade quando disponível;
3. não somar EUR, GBP e USD diretamente;
4. não inferir lucro ou margem sem custos;
5. não interpretar `discount_value` como desconto efetivo sem documentação suficiente;
6. diferenciar fatos observados de interpretações e hipóteses;
7. evitar exposição desnecessária de dados pessoais nos resultados.

## 7. Status

As análises e auditorias já documentadas devem ser interpretadas de acordo com o escopo indicado em cada arquivo. O fechamento quantitativo do projeto exige a validação final da sobreposição entre todas as bases e a confirmação da base analítica definitiva sem dupla contagem.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.
