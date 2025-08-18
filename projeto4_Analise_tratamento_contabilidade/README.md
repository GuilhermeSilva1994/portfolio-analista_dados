📊 Análise e Tratamento de Dados Contábeis

  Este projeto tem como objetivo explorar, tratar e visualizar dados contábeis a partir de lançamentos financeiros. Utilizando Python e bibliotecas como Pandas, Seaborn    e Matplotlib, foram geradas visualizações e estatísticas que ajudam a compreender melhor a estrutura dos dados e identificar padrões relevantes.


📈 Análises Realizadas

  Distribuição temporal dos lançamentos: Gráfico de linha mostrando a variação dos valores ao longo do tempo (data_lancamento).
  
  Distribuição por tipo de moeda: Gráfico de barras com contagem por categoria de moeda.
  
  Frequência de contas:
  
    Contas de débito (conta_debito)
    
    Contas de crédito (conta_credito)
    
    Centros de custo (centro_custo)

📌 Conclusões

  A distribuição dos valores por período mostra variações que podem indicar sazonalidade ou eventos contábeis específicos.
  
  A maioria dos lançamentos está concentrada em poucas moedas, o que pode facilitar a padronização e análise futura.
  
  As contas de débito, crédito e centros de custo apresentam uma dispersão elevada, com muitas categorias únicas e baixa frequência. Isso sugere que os dados podem estar   fragmentados ou que há necessidade de agrupamento por categorias mais amplas.
  
  A presença de valores como "?" em conta_credito indica dados faltantes ou mal formatados, o que pode impactar a qualidade das análises e requer tratamento adicional.
