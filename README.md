# Análise de Vendas com Prompts e Inteligência Artificial

Projeto desenvolvido por **Nágyla Silva** para demonstrar a aplicação prática de **prompts e ferramentas de Inteligência Artificial na análise de relatórios de vendas**, com foco na identificação de padrões, geração de insights, validação crítica e apoio à tomada de decisão.

> **Desafio:** DIO — análise de relatórios de vendas com ferramentas de Inteligência Artificial.

## 1. Objetivo

Explorar dados de vendas utilizando prompts estruturados para:

- identificar padrões e tendências;
- analisar desempenho das vendas;
- comparar produtos, clientes, períodos, canais e países de entrega, quando disponíveis;
- extrair insights relevantes para o negócio;
- transformar resultados em recomendações estratégicas;
- validar criticamente as respostas geradas por IA;
- documentar todo o processo de forma clara e reproduzível.

## 2. Competências Demonstradas

### 2.1 Competências técnicas

- Engenharia de Prompt;
- Inteligência Artificial generativa;
- Análise exploratória de dados;
- Auditoria e validação de dados;
- Deduplicação e rastreabilidade;
- Interpretação de informações de negócio;
- Geração e validação de insights;
- Documentação técnica;
- Organização de projetos no GitHub;
- Pensamento crítico sobre respostas geradas por IA.

## 3. Metodologia

O projeto segue o fluxo:

**Dados → Auditoria → Pergunta de negócio → Prompt → IA → Validação → Insight → Recomendação**

A IA é utilizada como ferramenta de apoio. As respostas geradas não são tratadas automaticamente como fatos: os resultados relevantes devem ser confrontados com os dados utilizados.

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

## 5. Fonte dos Dados

Os dados utilizados neste projeto foram disponibilizados pela **Digital Innovation One (DIO)** no laboratório **Como Utilizar Prompts para Gerar Insights de Relatórios de Vendas**, integrante da trilha **Criando Prompts Inteligentes**.

Neste projeto, os dados são utilizados para aplicar prompts, realizar análises, validar as respostas geradas por Inteligência Artificial e documentar os insights obtidos.

## 6. Auditoria e Base Analítica Definitiva

A auditoria cruzada considerou as cinco planilhas do repositório.

As quatro bases operacionais possuem:

- `Meganium_Sales_Data`: 50 registros;
- AliExpress: 20 registros;
- Etsy: 20 registros;
- Shopee: 20 registros.

Essas quatro bases totalizam **110 transações operacionais e 323 unidades**.

A `Updated_Anbernic_Sales_Data` possui **30 registros correspondentes por `invoice_id`** à base geral. Ela é uma representação alternativa dos mesmos pedidos e, portanto, **não deve ser somada novamente**.

A base analítica definitiva é, portanto:

> **110 transações únicas — 323 unidades vendidas.**

As moedas **EUR, GBP e USD** são mantidas separadas. Não foram aplicadas conversões cambiais.

## 7. Status Atual

**Auditoria quantitativa de sobreposição e deduplicação: CONCLUÍDA.**

A estrutura documental, os prompts, as análises específicas e a consolidação estão organizados. A definição da base analítica definitiva encerra a principal pendência de integridade identificada na auditoria.

Os resultados quantitativos consolidados devem utilizar exclusivamente a base de 110 transações únicas.

## 8. Validação

Sempre que possível, cada insight será acompanhado de:

**Evidência → Cálculo → Interpretação → Impacto potencial → Recomendação**

Também serão registradas limitações, dados ausentes e situações em que a IA possa apresentar uma interpretação que não seja sustentada pela base.

## 9. Documentação

- [Dados](dados/README.md)
- [Prompts](prompts/README.md)
- [Análises](analises/README.md)
- [Resultados](resultados/README.md)
- [Evidências](evidencias/README.md)
- [Documentação técnica](docs/README.md)

## 10. Autoria

**Nágyla Silva**

Projeto desenvolvido para fins educacionais e de portfólio, demonstrando competências em Inteligência Artificial, engenharia de prompts, análise de dados, auditoria, validação crítica e documentação técnica.

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
