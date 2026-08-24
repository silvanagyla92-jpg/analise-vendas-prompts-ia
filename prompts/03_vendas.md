# Prompt 03 — Evolução e Desempenho das Vendas

## 1. Objetivo

Analisar a evolução das vendas ao longo do tempo, identificando tendências, variações relevantes, períodos de maior e menor desempenho e possíveis pontos de atenção.

## 2. Prompt

### 2.1 Instrução para a IA

```text
Atue como um analista de dados especializado em séries temporais e desempenho comercial.

Analise exclusivamente os dados fornecidos e não utilize informações externas para preencher lacunas.

Antes dos cálculos:

1. Identifique o campo de data utilizado.
2. Informe a data inicial e final disponíveis.
3. Verifique datas ausentes, inválidas ou períodos incompletos.
4. Defina a granularidade da análise: diária, semanal, mensal, trimestral ou anual, conforme adequado aos dados.
5. Identifique as moedas existentes.
6. Verifique se existem duplicidades ou registros que possam distorcer a evolução temporal.

Quando os dados permitirem, calcule:

- quantidade de transações por período;
- quantidade de unidades vendidas por período;
- valor das vendas por período, mantendo moedas separadas;
- ticket médio por período e por moeda, quando aplicável;
- crescimento ou queda percentual entre períodos comparáveis;
- melhor e pior período segundo cada métrica utilizada;
- variações em relação ao período anterior;
- desvios relevantes em relação à média, quando a comparação for estatisticamente adequada.

Para comparações temporais:

- utilize períodos de mesma duração sempre que possível;
- sinalize períodos incompletos;
- não compare diretamente valores de moedas diferentes;
- explique a fórmula utilizada para percentuais de crescimento ou queda.

Investigue:

1. tendências de crescimento ou queda;
2. picos e vales de vendas;
3. possíveis padrões sazonais;
4. mudanças bruscas ou anomalias;
5. alterações relevantes por produto, canal ou país de entrega, quando os dados permitirem.

IMPORTANTE:
- Correlação temporal não prova causalidade.
- Não atribua uma causa a uma variação sem evidência.
- Não confunda aumento de quantidade com aumento de faturamento.
- Não confunda faturamento com lucro.
- Não invente eventos externos para explicar mudanças observadas.

Para cada tendência relevante, apresente:

- Evidência: dado ou cálculo observado;
- Comparação: períodos ou grupos comparados;
- Interpretação: o que os dados permitem concluir;
- Hipótese: somente quando houver uma explicação plausível que ainda não possa ser comprovada;
- Dados adicionais necessários: quando a explicação não puder ser confirmada;
- Confiança: alta, média ou baixa.

Finalize com:

- 3 principais tendências observadas;
- 3 pontos que exigem investigação;
- 3 perguntas para aprofundamento.
```

## 3. Critérios de Validação

### 3.1 Verificações

- Confirmar a data inicial e final utilizadas.
- Verificar o tratamento de períodos incompletos.
- Recalcular taxas de crescimento e queda.
- Confirmar a granularidade dos períodos comparados.
- Verificar se moedas diferentes permaneceram separadas.
- Conferir médias, totais e percentuais.
- Confirmar se tendências apresentadas são sustentadas pelos dados.
- Verificar se hipóteses foram diferenciadas de fatos.
- Não aceitar explicações causais sem evidência.
- Registrar anomalias e limitações relevantes.

## 4. Resultado Esperado

Uma análise temporal verificável das vendas, capaz de demonstrar tendências, variações e pontos de atenção sem misturar moedas, ignorar períodos incompletos ou extrapolar conclusões além das evidências disponíveis.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.