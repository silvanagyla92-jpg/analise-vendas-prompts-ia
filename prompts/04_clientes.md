# Prompt 04 — Análise de Clientes

## 1. Objetivo

Investigar o comportamento de compra dos clientes e identificar padrões de frequência, recorrência, concentração e valor das compras, preservando a privacidade dos dados pessoais.

## 2. Prompt

### 2.1 Instrução para a IA

```text
Atue como um analista de dados especializado em comportamento de clientes e desempenho comercial.

Analise exclusivamente os registros fornecidos. Não utilize informações externas para preencher lacunas ou inferir características dos compradores.

Antes da análise:

1. Identifique se existe um identificador de cliente confiável.
2. Identifique os campos disponíveis para medir frequência, quantidade e valor das compras.
3. Verifique duplicidades e inconsistências que possam alterar as métricas.
4. Identifique as moedas existentes e mantenha valores monetários separados por moeda.
5. Verifique a disponibilidade de datas para análises de recorrência.
6. Identifique quais informações são dados pessoais e não devem ser expostas nos resultados.

Quando os dados permitirem, calcule:

- número de clientes identificáveis;
- número de clientes com pelo menos uma compra;
- quantidade de compras por cliente;
- quantidade média de compras por cliente;
- valor total comprado por cliente, separado por moeda;
- ticket médio por cliente e por moeda, quando aplicável;
- frequência de compra;
- clientes com maior quantidade de compras;
- concentração das vendas entre os principais clientes;
- distribuição dos clientes por quantidade de compras.

Se houver informação temporal suficiente, investigue:

- clientes recorrentes;
- primeira e última compra por cliente, quando apropriado;
- novos clientes por período;
- intervalo entre compras;
- clientes sem compras no período mais recente, desde que o critério seja definido e o período permita essa análise.

IMPORTANTE SOBRE PRIVACIDADE:

- Não apresente nomes, datas de nascimento, endereços ou outros dados pessoais.
- Não reproduza registros individuais desnecessariamente.
- Utilize agregações, categorias ou identificadores anonimizados.
- Se a base não possuir um identificador de cliente adequado, informe a limitação e não tente reconstruir uma identidade por suposição.

IMPORTANTE SOBRE INTERPRETAÇÃO:

- Não classifique um cliente como fiel, inativo, perdido ou de alto valor sem definir uma regra objetiva.
- Não confunda maior valor de compra com maior lucratividade.
- Não some valores de moedas diferentes.
- Não atribua motivos ao comportamento do cliente sem evidência.
- Não infira idade, perfil, preferências ou características pessoais a partir de nome ou data de nascimento.

Para cada insight, apresente:

- Evidência: dado ou cálculo que sustenta o resultado;
- Métrica: cálculo utilizado;
- Interpretação: o que os dados permitem concluir;
- Limitação: o que não pode ser determinado;
- Confiança: alta, média ou baixa.

Finalize com recomendações de investigação comercial baseadas exclusivamente nos padrões observados e indique quais dados adicionais seriam necessários para aprofundar a análise.
```

## 3. Critérios de Validação

### 3.1 Verificações

- Confirmar se o identificador de cliente é adequado e consistente.
- Verificar duplicidades e registros inconsistentes.
- Recalcular totais, médias, frequências e percentuais.
- Confirmar que valores monetários permanecem separados por moeda.
- Verificar se os critérios de recorrência e inatividade foram definidos antes da classificação.
- Conferir o período utilizado em análises temporais.
- Garantir que nenhum dado pessoal seja exposto nos resultados.
- Não aceitar inferências sobre perfil, preferência ou comportamento sem evidência.
- Não aceitar conclusões de lucratividade sem dados de custos ou margem.
- Registrar limitações decorrentes da identificação dos clientes e da cobertura temporal.

## 4. Resultado Esperado

Uma visão estruturada e verificável do comportamento de compra dos clientes, destacando frequência, recorrência, concentração e valor das compras, sem exposição de dados pessoais ou extrapolação além das evidências disponíveis.

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.