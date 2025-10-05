# 🧠 Engenharia de Atributos e Preparação de Dados

Este projeto realiza o tratamento e preparação de uma base de dados clínica para análises preditivas. Abaixo estão os principais passos realizados no notebook `Engenharia_De_Atributos.ipynb`.

---

## 🔍 1. Tratamento de Dados

### ✅ Remoção de valores ausentes
Todos os valores nulos foram tratados ou removidos:

🧹 Remoção de colunas constantes

Colunas com apenas um valor único foram eliminadas, pois não agregam variabilidade ao modelo.

🛠️ 2. Engenharia de Atributos

Após a limpeza, foi realizada uma análise exploratória para entender a distribuição das variáveis e identificar oportunidades de transformação:

Verificação de tipos de dados (int64, object)

Identificação de variáveis categóricas com alta cardinalidade (diag_1, diag_2, diag_3)

Criação de métricas agregadas e derivadas (ex: tempo de internação, número de diagnósticos)

🧬 3. Recategorização de Variáveis Categóricas

As variáveis categóricas foram recodificadas para facilitar a modelagem:

Agrupamento de faixas etárias (age)

Padronização de valores como No, Steady, Up, Down para medicamentos

Redução de cardinalidade em variáveis como race, gender, readmitted

📊 Resultado Final

Após o tratamento, o DataFrame final possui:

98.052 registros

42 colunas limpas e relevantes

Nenhum valor nulo

Variáveis categóricas recodificadas e prontas para modelagem.
