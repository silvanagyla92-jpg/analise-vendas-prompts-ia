# Prompt 01 — Análise Geral de Vendas

## 1. Objetivo

Realizar uma primeira leitura estruturada da base de vendas para compreender sua composição, identificar padrões relevantes e levantar hipóteses que possam orientar análises posteriores.

## 2. Prompt

### 2.1 Instrução para a IA

```text
Atue como um analista de dados especializado em vendas e inteligência de negócios.

Analise a base de dados de vendas fornecida, considerando exclusivamente as informações presentes nos dados.

Antes de interpretar os resultados:
1. Identifique as colunas disponíveis e descreva brevemente a função de cada uma.
2. Verifique o período abrangido pela base, quando houver informação de data.
3. Identifique possíveis valores ausentes, duplicidades, inconsistências ou registros que possam afetar a análise.
4. Verifique a existência de múltiplas moedas antes de calcular ou comparar valores monetários.
5. Diferencie claramente fatos observados, cálculos, inferências e hipóteses.
6. Não invente valores que não estejam presentes na base.
7. Não exponha nomes, datas de nascimento ou outros dados pessoais dos compradores nos resultados.

Em seguida, apresente:
- quantidade total de registros;
- quantidade de vendas/transações, se essa métrica puder ser determinada;
- faturamento ou valor total, preservando a moeda ou utilizando uma conversão explicitamente documentada;
- ticket médio, quando calculável e comparável;
- principais produtos ou categorias;
- períodos de maior e menor desempenho, quando houver datas;
- principais padrões identificados;
- possíveis anomalias ou pontos que mereçam investigação.

Não some valores monetários de moedas diferentes sem uma regra de conversão documentada.

Organize a resposta em uma tabela sempre que isso facilitar a comparação.

Para cada insight, informe:
- evidência encontrada nos dados;
- interpretação;
- possível impacto para o negócio;
- nível de confiança (alto, médio ou baixo).

Finalize com até 5 perguntas de investigação que poderiam aprofundar a análise.
```

## 3. Critérios de Validação

### 3.1 Verificações

- Confirmar se todos os números apresentados podem ser reproduzidos a partir da base.
- Verificar se o modelo distinguiu observação de interpretação.
- Conferir cálculos de totais e médias.
- Verificar se moedas diferentes foram mantidas separadas ou convertidas por regra documentada.
- Não aceitar conclusões causais que não sejam sustentadas pelos dados.
- Não expor dados pessoais dos compradores.
- Registrar limitações decorrentes da estrutura ou qualidade da base.

## 4. Resultado Esperado

Uma visão inicial e verificável do conjunto de dados, servindo como ponto de partida para as análises específicas de produtos, vendas, clientes, países de entrega e insights estratégicos.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.