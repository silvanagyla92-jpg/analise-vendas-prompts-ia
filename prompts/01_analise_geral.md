# Prompt 01 — Análise Geral de Vendas

## 1. Objetivo

Realizar uma primeira leitura estruturada da base de vendas para compreender sua composição, verificar a qualidade dos dados e identificar padrões relevantes que possam orientar as análises posteriores.

## 2. Prompt

### 2.1 Instrução para a IA

```text
Atue como um analista de dados especializado em vendas e inteligência de negócios.

Analise exclusivamente a base de dados fornecida. Não utilize informações externas para preencher lacunas ou produzir resultados.

Antes de interpretar os resultados:

1. Identifique as colunas disponíveis e descreva brevemente a função de cada uma.
2. Informe a quantidade de registros analisados.
3. Verifique o período abrangido pela base, quando houver informação de data.
4. Verifique valores ausentes, duplicidades, inconsistências e possíveis registros inválidos.
5. Identifique as moedas existentes e mantenha os valores monetários separados por moeda.
6. Identifique os canais de venda disponíveis.
7. Identifique os países de entrega disponíveis, quando essa informação existir.
8. Diferencie fatos observados, cálculos, inferências e hipóteses.
9. Não invente valores, percentuais, rankings ou informações que não possam ser calculados diretamente a partir da base.
10. Não exponha nomes, datas de nascimento ou outros dados pessoais dos compradores.

Em seguida, apresente, somente quando calculável:

- quantidade total de registros;
- quantidade de transações distintas, utilizando um identificador adequado quando disponível;
- valor total das vendas por moeda;
- ticket médio por moeda, quando aplicável;
- principais produtos por quantidade e/ou valor, sempre respeitando a moeda;
- desempenho por canal de venda;
- desempenho por país de entrega;
- períodos de maior e menor volume de vendas, quando houver datas suficientes;
- padrões relevantes;
- possíveis anomalias ou pontos que mereçam investigação.

IMPORTANTE:
- Não some valores de moedas diferentes.
- Não trate faturamento como lucro, pois a base não fornece necessariamente custos e margens.
- Não atribua causalidade aos padrões encontrados sem evidência suficiente.
- Se uma métrica não puder ser calculada com segurança, informe explicitamente que ela não pode ser determinada.

Para cada insight relevante, informe:

- Evidência: dado ou cálculo que sustenta o insight;
- Interpretação: o que o resultado indica;
- Impacto potencial: possível relevância para o negócio;
- Confiança: alta, média ou baixa;
- Limitação: quando houver.

Finalize com até 5 perguntas de investigação que possam aprofundar a análise sem pressupor respostas que não estejam nos dados.
```

## 3. Critérios de Validação

### 3.1 Verificações

- Confirmar se todos os números apresentados podem ser reproduzidos a partir da base.
- Verificar se o modelo distinguiu observação, cálculo, interpretação e hipótese.
- Conferir cálculos de totais, médias e percentuais.
- Verificar se moedas diferentes foram mantidas separadas.
- Conferir se rankings respeitam a dimensão monetária utilizada.
- Verificar se não foram apresentadas conclusões sobre lucro sem dados de custo ou margem.
- Verificar se não foram apresentadas conclusões causais sem evidência.
- Não aceitar exposição de dados pessoais dos compradores.
- Registrar limitações decorrentes da estrutura ou qualidade da base.

## 4. Resultado Esperado

Uma visão inicial, verificável e documentada do conjunto de dados, servindo como ponto de partida para as análises específicas de produtos, vendas, clientes, países de entrega e insights estratégicos.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.