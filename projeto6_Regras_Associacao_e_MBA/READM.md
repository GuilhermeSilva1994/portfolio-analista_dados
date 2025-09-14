# 🛒 Análise de Cesta de Produtos com Regras de Associação

## 📌 Introdução

Este projeto tem como objetivo analisar o comportamento de compra dos clientes de um supermercado por meio da técnica de **Regras de Associação**, utilizando o algoritmo **Apriori**. A partir das transações realizadas, buscamos identificar padrões de coocorrência entre produtos e gerar insights que possam apoiar decisões estratégicas de negócio. Além disso foram respondidas 10 perguntas de negócio!

---

## 🎯 Objetivos de Negócio

- Identificar produtos frequentemente comprados juntos.
- Descobrir oportunidades de **cross-selling** e **promoções combinadas**.
- Otimizar o layout de loja e a disposição de produtos.
- Apoiar decisões de estoque com base em padrões de consumo.

---

## 📊 Descrição dos Dados

O conjunto de dados contém transações de pedidos realizados por clientes, com os seguintes campos principais:

- `id_pedido`: identificador único da transação.
- `Produtos`: lista de IDs dos produtos comprados em cada pedido.

Além disso, foi utilizada uma base complementar com informações dos produtos:

- `product_id`: identificador do produto.
- `product_name`: nome do produto.
- `aisle_id` e `department_id`: localização do produto na loja.

---

## 🧹 Pré-processamento

- Conversão das listas de produtos em tuplas para compatibilidade com o algoritmo Apriori.
- Filtragem de transações para limitar o volume de dados (amostra de 50.000 pedidos).
- Criação de estrutura para cálculo de métricas como suporte, confiança e lift.

---

## 🧠 Implementação do Algoritmo Apriori

Utilizamos a biblioteca `efficient_apriori` para aplicar o algoritmo Apriori:

```python
itemsets_ap, rules_ap = apriori(transacoes_mba_tupla[:50000], min_support=0.01, min_confidence=0.2)
```

- `min_support`: frequência mínima de ocorrência de um item ou conjunto.
- `min_confidence`: probabilidade mínima de ocorrência de um item dado outro.

---

## 📈 Interpretação das Regras

Para cada par de produtos analisados, foram calculadas as seguintes métricas:

- **Support A**: frequência do produto A.
- **Support B**: frequência do produto B.
- **Support AB**: frequência da combinação A + B.
- **Confidence AB**: probabilidade de B dado A.
- **Lift AB**: impacto da presença de A na probabilidade de B (valores >1 indicam associação positiva).

As regras foram enriquecidas com os nomes dos produtos para facilitar a interpretação.

---

## 🧾 Conclusões e Insights

- Produtos básicos como arroz, leite e carnes apresentam forte associação entre si.
- Itens orgânicos tendem a aparecer juntos, sugerindo um perfil de consumidor específico.
- As regras geradas podem ser aplicadas em campanhas de marketing, sugestões de compra e organização de prateleiras.

