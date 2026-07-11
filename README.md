# Projeto-Avaliativo-Final---M-dulo-1
# Desenvolvimento de IA para Análise Preditiva [T1] Situação de Aprendizagem (Projeto Avaliativo) - Módulo 1 - Semana 14

# Objetivo:
Estruturar um pipeline preditivo completo aplicado à Indústria 4.0.
# O Problema: 
Um parque fabril monitorado por sensores necessita prever quebras mecânicas nos equipamentos para evitar paradas na linha de produção. A variável alvo do projeto é binária: Falha = 1 (quando há uma avaria detectada) e Falha = 0 (funcionamento normal).

# Base de Dados (.csv): 
manutencao_preditiva.csv

# Etapas:
# Fase 1: Análise Exploratória (EDA)
Apresente as dimensões do dataset (número de linhas e colunas), os tipos de dados das variáveis e o resumo estatístico descritivo das colunas numéricas via método “.describe()”.
Plote, no mínimo, 3 gráficos analíticos bem fundamentados utilizando bibliotecas como Matplotlib ou Seaborn (Ex: histograma de distribuição das variáveis preditoras, gráfico de barras comprovando a taxa de desbalanceamento da variável alvo e um mapa de calor com a correlação de Pearson entre as variáveis).
Insira uma célula de texto analisando os valores numéricos e os padrões identificados nos gráficos, explicitando como eles direcionam a estratégia de modelagem.

# Fase 2: Limpeza e Tratamento de Dados (Data Prep)
Identifique e remova as linhas duplicadas.
Identifique dados ausentes e aplique a imputação por Média ou Mediana, justificando textualmente a escolha com base na distribuição dos dados.
Gere gráficos do tipo boxplot para identificar a presença de outliers nas variáveis explicativas.

# Fase 3: Feature Engineering
Crie uma nova coluna numérica por meio de operação matemática entre colunas existentes, tratando os valores nulos previamente.
Sugestão (Manutenção): potencia = velocidade_rotacao_rpm * torque_nm
(É permitida a criação de outra combinação matemática, desde que explicada no vídeo e documentada no notebook).

# Fase 4: Divisão e Balanceamento dos Dados
Separe as variáveis preditoras (X) da variável alvo (y).
Divida os dados em treino (80%) e teste (20%) utilizando o parâmetro stratify=y.
Aplique uma técnica de reamostragem (SMOTE ou Random Under Sampling) exclusivamente nos dados de treino para evitar o vazamento de dados (Data Leakage).

# Fase 5: Escalonamento de Variáveis (StandardScaler)
Aplique o StandardScaler apenas nas variáveis contínuas destinadas ao modelo KNN (utilizando fit_transform no treino e transform no teste).
Mantenha os dados da Árvore de Decisão sem escalonamento, justificando no código o motivo de o algoritmo ser imune à escala dos atributos.

# Fase 6: Ajuste de Parâmetros e Combate ao Overfitting
No KNN: Treine o modelo variando o parâmetro n_neighbors (K) por no mínimo 3 valores ímpares (ex: K = 3, 5, 7) e registre a acurácia no treino e no teste.
Na Árvore: Treine o modelo variando o parâmetro max_depth por no mínimo 3 limites (ex: 3, 5 e None) e registre a acurácia no treino e no teste.
Insira um texto identificando em quais pontos ocorreu o overfitting e qual configuração garantiu a estabilidade no teste.

# Fase 7: Avaliação da Acurácia e Veredito Final
Calcule e exiba a acurácia final do melhor KNN e da melhor árvore de decisão utilizando os dados de teste.
Compare as taxas de acerto e escreva uma conclusão justificando qual modelo apresentou o desempenho superior no teste e deve ser adotado pela empresa.
