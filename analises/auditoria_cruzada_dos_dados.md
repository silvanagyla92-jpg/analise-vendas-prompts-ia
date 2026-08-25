# Auditoria Cruzada dos Dados

## 1. Objetivo

Esta auditoria verifica a consistência estrutural e a relação entre as cinco bases de vendas do projeto, com foco em duplicidades, correspondências, integridade aritmética, sobreposição entre fontes e definição da base analítica final.

## 2. Bases analisadas

| Base | Registros | Papel na consolidação |
|---|---:|---|
| `Meganium_Sales_Data` | 50 | Base geral operacional |
| `Meganium_Sales_Data_-_AliExpress` | 20 | Base específica do canal |
| `Meganium_Sales_Data_-_Etsy` | 20 | Base específica do canal |
| `Meganium_Sales_Data_-_Shopee` | 20 | Base específica do canal |
| `Updated_Anbernic_Sales_Data` | 30 | Representação alternativa de registros da base geral |

As quatro primeiras bases somam **110 registros operacionais**. A quinta base possui **30 registros**, todos correspondentes a registros da `Meganium_Sales_Data` por `invoice_id` e atributos transacionais compatíveis.

## 3. Resultado quantitativo da sobreposição

A matriz abaixo registra a sobreposição identificada por `invoice_id`:

| Base A | Base B | Registros A | Registros B | `invoice_id` coincidentes | Resultado |
|---|---|---:|---:|---:|---|
| `Meganium_Sales_Data` | AliExpress | 50 | 20 | 0 | Independentes |
| `Meganium_Sales_Data` | Etsy | 50 | 20 | 0 | Independentes |
| `Meganium_Sales_Data` | Shopee | 50 | 20 | 0 | Independentes |
| `Meganium_Sales_Data` | `Updated_Anbernic_Sales_Data` | 50 | 30 | **30** | Duplicação/representação alternativa |
| AliExpress | Etsy | 20 | 20 | 0 | Independentes |
| AliExpress | Shopee | 20 | 20 | 0 | Independentes |
| Etsy | Shopee | 20 | 20 | 0 | Independentes |

Assim, a soma física das cinco planilhas seria de **140 linhas**, mas a base analítica deduplicada contém **110 transações únicas**. As 30 linhas adicionais da `Updated_Anbernic_Sales_Data` não devem ser contabilizadas novamente.

## 4. Unidades vendidas

A base geral contém **146 unidades**. As bases específicas acrescentam:

- AliExpress: **58 unidades**;
- Etsy: **55 unidades**;
- Shopee: **64 unidades**.

Portanto:

**146 + 58 + 55 + 64 = 323 unidades.**

As 30 linhas da `Updated_Anbernic_Sales_Data` são representações alternativas e não acrescentam unidades ao total analítico.

## 5. Canais na base analítica

Após a deduplicação, os 110 registros distribuem-se por canal da seguinte forma:

| Canal | Transações | Unidades |
|---|---:|---:|
| Etsy | 42 | 115 |
| Shopee | 34 | 113 |
| AliExpress | 34 | 95 |
| **Total** | **110** | **323** |

Esses valores são adequados para análises de volume. Não representam ranking de faturamento comparável entre moedas.

## 6. Moedas e valores monetários

Foram identificadas EUR, GBP e USD. Na base analítica de 110 registros, os valores nominais de `total_price` totalizam, separadamente:

| Moeda | Total nominal |
|---|---:|
| EUR | 10.510 |
| GBP | 8.670 |
| USD | 10.430 |

Esses valores **não devem ser somados entre si**. Não foi aplicada conversão cambial porque o projeto não definiu taxa nem data de referência.

## 7. Integridade aritmética

A regra de validação adotada é:

`total_price = quantity × unit_price`

Os registros das quatro bases operacionais analisadas apresentam consistência com essa regra. A `Updated_Anbernic_Sales_Data` também mantém os mesmos valores transacionais dos registros correspondentes, apesar da alteração de nomenclatura dos produtos.

## 8. Correspondência entre produtos e SKUs

As bases com SKU apresentam o seguinte relacionamento:

| SKU | Produto padronizado |
|---|---|
| `SKU-35XX01` | NEW MEGANIUM RG35XX |
| `SKU-40XXV01` | NEW MEGANIUM RG 40XXV |
| `SKU-28XX01` | NEW MEGANIUM RG28XX |
| `SKU-CUBEXX01` | NEW MEGANIUM RG CubeXX |
| `SKU-353M01` | MEGANIUM RG353M |

A `Updated_Anbernic_Sales_Data` não possui SKU e utiliza nomes ANBERNIC, mas mantém `invoice_id` e os demais atributos transacionais que permitem sua identificação como representação alternativa da base geral.

## 9. `discount_value`

O campo `discount_value` deve permanecer separado de `total_price`. A documentação disponível não permite afirmar se o desconto já está refletido no `total_price` ou se deve ser subtraído dele. Portanto, não é permitido inferir receita líquida, margem ou lucro a partir desses campos isoladamente.

## 10. Regra de consolidação definitiva

Para os resultados quantitativos do projeto, deve ser utilizada a seguinte regra:

1. considerar as quatro bases operacionais (`Meganium_Sales_Data`, AliExpress, Etsy e Shopee);
2. usar `invoice_id` como chave prioritária de rastreabilidade;
3. excluir a `Updated_Anbernic_Sales_Data` da soma de vendas, tratando-a como representação alternativa dos 30 registros correspondentes;
4. manter EUR, GBP e USD separados;
5. não calcular lucro ou margem sem custos;
6. não interpretar `discount_value` como desconto efetivamente abatido sem documentação adicional;
7. não expor `buyer_name` ou `buyer_birth_date` nos resultados agregados.

## 11. Conclusão da auditoria

A auditoria quantitativa fecha a principal questão de integridade do projeto: a base analítica correta contém **110 transações únicas e 323 unidades**, e não 140 transações, porque as 30 linhas da `Updated_Anbernic_Sales_Data` correspondem a registros já presentes na base geral.

A consolidação deve, portanto, usar as quatro bases operacionais como fontes de vendas e manter a quinta base apenas como evidência de correspondência/transformação.

**Status da auditoria:** CONCLUÍDA para a definição da base analítica e das regras de deduplicação.

## Rodapé

**Autora:** Nágyla Silva  
**Projeto integrante do portfólio prático em Inteligência Artificial, desenvolvido para demonstrar competências em treinamento e avaliação de sistemas de IA, análise crítica de respostas e anotação de dados, aplicadas às funções de AI Trainer, AI Response Evaluator e Data Annotator, com base em experiência em QA e Auditoria.**