# 📊 Projeto: Tratamentos e Testes Estatísticos

Este projeto foi desenvolvido como parte da formação de Analista de Dados na [Data Science Academy](https://www.datascienceacademy.com.br/), com foco em técnicas de limpeza, tratamento e análise estatística de dados.

## 🧰 Tecnologias Utilizadas
- 🐍 Python 3
- 📊 Pandas
- 📈 Seaborn
- 📉 Matplotlib
- 🔬 SciPy
- 🧮 NumPy
- 🧪 Watermark

## 📁 Objetivo
Aplicar técnicas de pré-processamento e testes estatísticos para avaliar a distribuição dos dados, identificar outliers e realizar análises comparativas entre faixas etárias e variáveis numéricas.

## 🔍 Principais Etapas

### 🧹 Tratamento de Dados
- Criação da variável `Faixa_Etaria` com base na idade
- Detecção e tratamento de valores ausentes
- Ajuste de tipos de dados
- Identificação e tratamento de outliers com o método do Intervalo Interquartil (IQR)

### 📊 Análise Estatística
- Verificação de assimetria com `.skew()`
- Criação de boxplots para análise de distribuição salarial por faixa etária
- Interpretação visual de padrões e desvios

### 📈 Visualização
```python
sns.set_style('ticks')
sns.boxplot(data=df, x='Faixa_Etaria', y='Salario', palette='tab10')

