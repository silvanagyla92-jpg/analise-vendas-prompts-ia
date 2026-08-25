# Análise de Vendas com Prompts e Inteligência Artificial

Projeto desenvolvido por **Nágyla Silva** para demonstrar a aplicação prática de **prompts e ferramentas de Inteligência Artificial na análise de relatórios de vendas**, com foco na identificação de padrões, geração de insights, validação de resultados e apoio à tomada de decisão.

> **Desafio:** DIO — análise de relatórios de vendas com ferramentas de Inteligência Artificial.

## 1. Objetivo

Explorar dados de vendas utilizando prompts estruturados para:

- identificar padrões e tendências;
- analisar o desempenho das vendas;
- comparar produtos, clientes, períodos e países de entrega, quando essas dimensões estiverem disponíveis;
- extrair insights relevantes para o negócio;
- transformar resultados em recomendações estratégicas;
- documentar todo o processo de forma clara e reproduzível;
- validar os resultados gerados por IA antes de considerá-los conclusões.

## 2. Competências Demonstradas

### 2.1 Competências técnicas

- Engenharia de Prompt;
- Inteligência Artificial generativa;
- Análise exploratória de dados;
- Interpretação de informações de negócio;
- Geração e validação de insights;
- Auditoria e validação de dados;
- Deduplicação e rastreabilidade de registros;
- Documentação técnica;
- Organização de projetos no GitHub;
- Pensamento crítico sobre respostas geradas por IA.

## 3. Metodologia

O projeto segue o fluxo:

**Dados → Auditoria → Pergunta de negócio → Prompt → IA → Validação → Insight → Recomendação**

A IA é utilizada como ferramenta de apoio. As respostas geradas não são tratadas automaticamente como fatos: os resultados relevantes devem ser confrontados com os dados utilizados.

A consolidação deve ocorrer somente depois da verificação de sobreposição entre as bases. O campo `invoice_id` é utilizado como identificador prioritário para rastreabilidade e deduplicação quando disponível.

Valores monetários em **EUR, GBP e USD** permanecem separados quando não existe uma regra de conversão cambial documentada. Também não são inferidos lucro ou margem sem dados de custo.

## 4. Estrutura do Projeto

```text
analise-vendas-prompts-ia/
├── README.md
├── dados/
│   ├── README.md
│   ├── relatorio_auditoria_dados.md
│   └── planilhas/
│       ├── README.md
│       ├── Meganium_Sales_Data.csv
│       ├── Meganium_Sales_Data_-_AliExpress.csv
│       ├── Meganium_Sales_Data_-_Etsy.csv
│       ├── Meganium_Sales_Data_-_Shopee.csv
│       └── Updated_Anbernic_Sales_Data.csv
├── prompts/
│   ├── README.md
│   ├── 01_analise_geral.md
│   ├── 02_produtos.md
│   ├── 03_vendas.md
│   ├── 04_clientes.md
│   ├── 05_regioes.md
│   └── 06_insights_estrategicos.md
├── analises/
│   ├── README.md
│   ├── analise_vendas.md
│   ├── analise_produtos.md
│   ├── analise_clientes.md
│   ├── analise_regioes.md
│   ├── analise_geral_planilha_1.md
│   ├── analise_planilha_2_aliexpress.md
│   ├── analise_consolidada.md
│   ├── auditoria_cruzada_dos_dados.md
│   └── insights_estrategicos.md
├── resultados/
│   ├── README.md
│   ├── insights.md
│   ├── insights_obtidos.md
│   └── conclusao.md
├── evidencias/
│   ├── README.md
│   └── imagens/
│       └── README.md
└── docs/
    ├── README.md
    └── metodologia.md
```

### 4.1 Organização das auditorias

A auditoria de dados está dividida em duas camadas complementares:

- `dados/relatorio_auditoria_dados.md` — auditoria estrutural e de qualidade dos registros, incluindo campos, consistência e regras básicas de validação;
- `analises/auditoria_cruzada_dos_dados.md` — auditoria entre bases, com foco em correspondência de registros, rastreabilidade, sobreposição e prevenção de dupla contagem.

A separação evita confundir a validação individual das bases com a comparação entre fontes.

## 5. Fonte dos Dados

Os dados utilizados neste projeto foram disponibilizados pela **Digital Innovation One (DIO)** no laboratório **[Como Utilizar Prompts para Gerar Insights de Relatórios de Vendas](https://web.dio.me/lab/como-utilizar-prompts-para-gerar-insights-de-relatorios-de-vendas/learning/efadaa82-8f08-4186-9a42-a8255ba2fb31?back=/track/criando-prompts-inteligentes)**, integrante da trilha **Criando Prompts Inteligentes**.

A base de dados reúne registros estruturados de vendas e informações relacionadas aos produtos, permitindo explorar o desempenho comercial e identificar padrões nos dados.

Neste projeto, os dados são utilizados para aplicar prompts, realizar análises, validar as respostas geradas por Inteligência Artificial e documentar os insights obtidos.

## 6. Status Atual

A estrutura documental, a metodologia, os prompts, as bases de dados, as análises e os resultados preliminares já estão organizados no repositório.

A auditoria inicial e a análise das bases avaliadas já foram documentadas. A etapa de fechamento consiste em validar quantitativamente a sobreposição entre todas as bases, confirmar a base analítica final sem dupla contagem e revisar os resultados derivados dessa consolidação.

Até essa validação final, números, rankings e insights consolidados devem ser interpretados dentro do escopo da base explicitamente indicada em cada análise.

## 7. Resultados

Os resultados já documentados incluem análises específicas, auditoria cruzada, análise consolidada e insights metodológicos.

O arquivo `resultados/insights_obtidos.md` registra os principais achados derivados das bases avaliadas, enquanto `resultados/insights.md` e `resultados/conclusao.md` integram os resultados finais destinados à apresentação do projeto.

Resultados quantitativos devem permanecer rastreáveis aos dados utilizados e às regras de validação aplicadas.

## 8. Validação

Sempre que possível, cada insight será acompanhado de:

**Evidência → Interpretação → Impacto potencial → Recomendação**

Também serão registradas limitações, dados ausentes e situações em que a IA possa apresentar uma interpretação que não seja sustentada pela base.

As seguintes regras são obrigatórias para a consolidação:

1. verificar duplicidades e sobreposições antes de somar bases;
2. priorizar `invoice_id` para rastreabilidade quando disponível;
3. não somar diretamente EUR, GBP e USD;
4. não inferir lucro ou margem sem custos;
5. não tratar `discount_value` como desconto efetivo sem documentação da sua semântica;
6. diferenciar fatos observados de interpretações e hipóteses;
7. evitar exposição desnecessária de dados pessoais nos resultados e evidências.

## 9. Documentação

### 9.1 Áreas do projeto

- [Dados](dados/README.md)
- [Prompts](prompts/README.md)
- [Análises](analises/README.md)
- [Resultados](resultados/README.md)
- [Evidências](evidencias/README.md)
- [Documentação técnica](docs/README.md)

## 10. Autoria

**Nágyla Silva**

Projeto desenvolvido para fins educacionais e de portfólio, demonstrando competências em Inteligência Artificial, engenharia de prompts, análise de dados, auditoria, validação de respostas e documentação técnica.

## 11. Contato

**Autora:** Nágyla Silva

**Projeto:** Análise de Vendas com Prompts de IA

**Desafio:** DIO — análise de relatórios de vendas com ferramentas de Inteligência Artificial

**GitHub:** [silvanagyla92-jpg](https://github.com/silvanagyla92-jpg)

**LinkedIn:** [Nágyla Silva](https://www.linkedin.com/in/n%C3%A1gyla-silva-215aba35/)

---

**Projeto:** Análise de Vendas com Prompts de IA

**Autora:** Nágyla Silva

Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.
