# Projeto-Avaliativo-Final---M-dulo-1
# Desenvolvimento de IA para Análise Preditiva [T1] Situação de Aprendizagem (Projeto Avaliativo) - Módulo 1 - Semana 14

# Objetivo:
Estruturar um pipeline preditivo completo aplicado à Indústria 4.0.
# O Problema: 
Um parque fabril monitorado por sensores necessita prever quebras mecânicas nos equipamentos para evitar paradas na linha de produção. A variável alvo do projeto é binária: Falha = 1 (quando há uma avaria detectada) e Falha = 0 (funcionamento normal).

# Base de Dados (.csv): 
manutencao_preditiva.csv

# Linguagem:
VSCode

# Etapas:
# Fase 1: Análise Exploratória (EDA)
1. Apresenta as dimensões do dataset (número de linhas e colunas), os tipos de dados das variáveis e o resumo estatístico descritivo das colunas numéricas via método “.describe()”.
2. Apresenta gráficos utilizando bibliotecas Matplotlib e/ou Seaborn (Ex: histograma de distribuição das variáveis preditoras, gráfico de barras comprovando a taxa de desbalanceamento da variável alvo e um mapa de calor com a correlação de Pearson entre as variáveis). 

# Fase 2: Limpeza e Tratamento de Dados (Data Prep)
1. Identificar e remover linhas duplicadas.
2. Identificar dados ausentes e aplicar Média ou Mediana, justificando textualmente a escolha.
3. Gerar gráficos do tipo para identificar a presença de outliers nas variáveis explicativas.

# Fase 3: Feature Engineering
1. Criar nova coluna numérica por meio de operação matemática entre colunas existentes.
    Sugestão (Manutenção): potencia = velocidade_rotacao_rpm * torque_nm

# Fase 4: Divisão e Balanceamento dos Dados
1. Separar as variáveis preditoras (X) da variável alvo (y).
2. Dividir os dados em treino (80%) e teste (20%) utilizando o parâmetro stratify=y.
3. Aplicar uma técnica de reamostragem (SMOTE ou Random Under Sampling) exclusivamente nos dados de treino para evitar o vazamento de dados (Data Leakage).

   ## SMOTE escolhida uma vez que a base de dados é relativamente pequena e a criação de amostras nao causa lentidao no processo. As literaturas também indicam para controle de overfitting.
   
# Fase 5: Escalonamento de Variáveis (StandardScaler)
1. Aplicar o StandardScaler apenas nas variáveis contínuas destinadas ao modelo KNN (utilizando fit_transform no treino e transform no teste).
2. Aplicar Árvore de Decisão sem escalonamento, justificando no código o motivo de o algoritmo ser imune à escala dos atributos.

# Fase 6: Ajuste de Parâmetros e Combate ao Overfitting
1. KNN ==> Treinar o modelo variando o parâmetro n_neighbors (K) por no mínimo 3 valores ímpares (ex: K = 3, 5, 7) e registre a acurácia no treino e no teste.
2. Na Árvore ==> Treinar o modelo variando o parâmetro max_depth por no mínimo 3 limites (ex: 3, 5 e None) e registre a acurácia no treino e no teste.
3. Incluir um texto identificando em quais pontos ocorreu o overfitting e qual configuração garantiu a estabilidade no teste.

# Fase 7: Avaliação da Acurácia e Veredito Final
1. Calcular e exibir a acurácia final do melhor KNN e da melhor árvore de decisão utilizando os dados de teste.
2. Comparar as taxas de acerto e escrever uma conclusão justificando qual modelo apresentou o desempenho superior no teste e deve ser adotadopela empresa .

   ## LINK VIDEO:
   https://drive.google.com/file/d/1XJm3FIkVHZs5G3WDZ5ELLbl4IugdwYiY/view?usp=sharing
   
