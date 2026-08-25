# Análises

Esta pasta documenta as análises realizadas sobre os dados de vendas e registra como os prompts foram utilizados para explorar padrões e relações relevantes.

## 1. Objetivos das Análises

- Identificar padrões de vendas;
- Comparar desempenho entre produtos, períodos, clientes e países de entrega, quando disponíveis;
- Encontrar tendências, concentrações e possíveis anomalias;
- Transformar resultados quantitativos em interpretações de negócio;
- Registrar limitações e pontos que exigem validação;
- Verificar a consistência dos dados antes da consolidação.

## 2. Fluxo de Análise

**Dados → Auditoria → Pergunta de negócio → Prompt → Resposta da IA → Verificação → Insight → Recomendação**

A resposta da ferramenta de IA é tratada como apoio à análise, e não como fonte independente de verdade.

## 3. Estrutura dos Registros

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

### Análises específicas

- `analise_vendas.md` — comportamento geral das vendas;
- `analise_produtos.md` — desempenho dos produtos;
- `analise_clientes.md` — comportamento dos clientes;
- `analise_regioes.md` — distribuição por país de entrega;
- `insights_estrategicos.md` — síntese das descobertas;
- `analise_geral_planilha_1.md` — análise da base geral;
- `analise_planilha_2_aliexpress.md` — análise do AliExpress;
- `analise_consolidada.md` — consolidação da base analítica definitiva;
- `auditoria_cruzada_dos_dados.md` — matriz quantitativa de sobreposição e deduplicação.

## 5. Distinção entre as Auditorias

### 5.1 Auditoria estrutural

`dados/relatorio_auditoria_dados.md`

Verifica estrutura, consistência aritmética, campos, valores ausentes, duplicidades internas e regras gerais de qualidade.

### 5.2 Auditoria cruzada

`analises/auditoria_cruzada_dos_dados.md`

Compara as cinco bases entre si, identifica sobreposição por `invoice_id` e define a base analítica sem dupla contagem.

## 6. Regra de Consolidação Definitiva

A auditoria quantitativa estabeleceu:

- `Meganium_Sales_Data`: 50 registros;
- AliExpress: 20 registros;
- Etsy: 20 registros;
- Shopee: 20 registros;
- `Updated_Anbernic_Sales_Data`: 30 registros correspondentes à base geral.

Portanto, a base analítica definitiva possui **110 transações únicas e 323 unidades**. A `Updated_Anbernic_Sales_Data` não deve ser somada novamente.

As moedas EUR, GBP e USD permanecem separadas. Não são permitidos cálculos de lucro ou margem sem custos suficientes.

## 7. Status

**Auditoria quantitativa de sobreposição e deduplicação: CONCLUÍDA.**

A principal pendência de integridade identificada no projeto foi encerrada: a referência quantitativa oficial para os resultados consolidados é de **110 transações únicas e 323 unidades**.

As análises específicas continuam válidas dentro do escopo indicado em cada arquivo.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.
