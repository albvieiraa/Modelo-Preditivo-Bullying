# 📊 Modelo Preditivo de Bullying

Este projeto tem como objetivo desenvolver um modelo preditivo para identificar possíveis casos de bullying com base em um dataset disponibilizado pelo  Global School-Based Student Health Survey (GSHS).  

---

## 📝 Descrição

O projeto envolve desde a análise exploratória dos dados até a construção e avaliação de um modelo preditivo utilizando **Regressão Logística**. Foram aplicadas diversas técnicas estatísticas e de visualização para entender melhor as variáveis e sua relação com o bullying.  


## 🔍 Etapas do Projeto

### 1️⃣ Análise Exploratória
- Limpeza e tratamento dos dados  
- Identificação de valores ausentes e outliers  

### 2️⃣ Análise de Correlação
- Construção da **Matriz de Correlação** para variáveis numéricas  

### 3️⃣ Análise Categórica
- Cálculo da moda para variáveis categóricas  
- Teste **Qui-Quadrado** para verificar associações  
- Visualizações gráficas para melhor interpretação  

### 4️⃣ Visualizações Gráficas
- **Histogramas** para distribuição de dados  
- **Boxplots** segmentados por gênero e idade  

### 5️⃣ Construção do Modelo Preditivo
- **Regressão Logística** para prever a ocorrência de bullying  

### 6️⃣ Avaliação do Modelo
- Cálculo de métricas de desempenho (Acurácia, Precisão, Recall, F1-Score)  
- Matriz de Confusão para análise dos acertos e erros  

---

## 📈 Interpretação do Modelo  

Com base na matriz de confusão apresentada, no relatório de classificação e no contexto fornecido, podemos tirar as seguintes conclusões sobre o modelo de previsão de bullying na escola:

1. Desempenho do Modelo:
* Acurácia Geral:
O modelo obteve 74,3% de acurácia, o que significa que ele está correto em aproximadamente 74% das previsões. Embora seja um bom valor, ele precisa ser analisado considerando o desequilíbrio entre as classes.

2. Desempenho por Classe:

* Classe 0 (Não sofreu bullying):

Precision (89%): 89% das previsões de "não sofreu bullying" estão corretas.
Recall (77%): O modelo conseguiu identificar corretamente 77% dos alunos que não sofreram bullying.
Esse desempenho é robusto, com boas métricas de precisão e recall.

* Classe 1 (Sofreu bullying):

Precision (43%): Apenas 43% das previsões de "sofreu bullying" estão corretas, indicando que o modelo tem dificuldade em ser preciso ao prever essa classe.
Recall (64%): O modelo identificou 64% dos alunos que realmente sofreram bullying. Embora não seja ideal, ele está capturando uma parte razoável dos casos positivos.
O modelo ainda apresenta dificuldades nessa classe, pois ela é menos representada (3604 casos contra 13491 da classe 0).

3. Desequilíbrio de Classes:
A base de dados apresenta um desequilíbrio significativo entre as classes:

* Classe 0 (Não sofreu bullying): 13.491 ocorrências
* Classe 1 (Sofreu bullying): 3.604 ocorrências
Esse desequilíbrio impacta diretamente o desempenho do modelo, que tende a favorecer a classe majoritária (classe 0).


### Interpretação da Matriz de Confusão:
* O modelo prevê 10.387 casos verdadeiros negativos (TN), ou seja, não sofreu bullying e foi previsto corretamente.
* Existem 2.324 verdadeiros positivos (TP), ou seja, alunos que sofreram bullying e o modelo previu corretamente.
* 3.104 falsos positivos (FP): Alunos que não sofreram bullying, mas foram incorretamente classificados como vítimas.
* 1.280 falsos negativos (FN): Alunos que sofreram bullying, mas o modelo não identificou.

### Pontos de Melhoria:
1. Balanceamento das Classes:
Para lidar com o desequilíbrio das classes, é possível:

2. Utilizar técnicas de oversampling (como SMOTE) ou undersampling.
Ajustar a métrica do modelo (como aumentar o peso da classe 1, o que já foi feito parcialmente usando class_weight='balanced').
Engenharia de Recursos:
Explorar novas variáveis e combinações, como:

3. Criar indicadores compostos relacionados a sentimentos de solidão e interações sociais.
Utilizar variáveis relacionadas a peso (abaixo, acima e obeso), que podem ter correlação com o bullying.
Avaliação de Modelos Alternativos:
Experimentar outros algoritmos, como Random Forest, Gradient Boosting ou redes neurais, que podem capturar padrões não lineares nos dados.

4. Ajuste de Hiperparâmetros:
Refinar os parâmetros do modelo para melhorar a capacidade de previsão na classe minoritária.

### Conclusão final
O modelo apresenta um bom desempenho geral para a classe majoritária (não sofreu bullying), mas ainda precisa de melhorias significativas para a classe minoritária (sofreu bullying). Considerando o objetivo da pesquisa, que é prever e prevenir o bullying, é fundamental melhorar a sensibilidade (recall) na classe 1 para identificar mais casos verdadeiros de bullying e possibilitar intervenções eficazes.

---

## 🛠️ Tecnologias Utilizadas

- **Python**  
- **Pandas** e **NumPy** (Manipulação e tratamento de dados)  
- **Matplotlib e Seaborn** (Visualização de dados)  
- **Scikit-learn** (Construção e avaliação do modelo preditivo)  

---

## 🚀 Como Executar o Projeto  

1. Clone o repositório:  
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git


2. Instale as dependências necessárias:
   ```bash
   pip install -r requirements.txt

3. Execute o Jupyter Notebook:
   ```bash
   jupyter notebook

4. Abra e execute as células do notebook para reproduzir as análises e o modelo.

## 💡 Como Contribuir
- Faça um fork do repositório
- Crie uma branch com suas alterações
- Envie um pull request

## 🤝 Desenvolvimento em Squad  

Este projeto foi desenvolvido de forma colaborativa por nossa squad **Hedy Lamar**, aplicando metodologias ágeis e compartilhando conhecimentos ao longo do processo. Trabalhamos juntos em todas as etapas, desde a análise exploratória até a construção e avaliação do modelo preditivo.  

A colaboração foi essencial para obter insights mais ricos e garantir a qualidade do modelo. Agradecemos a todas as envolvidas pelo empenho e aprendizado compartilhado! 🚀💡  

## Participantes:

