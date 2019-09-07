# Projeto 1 - Encontrando Doadores para a CharityML
Primeiro projeto do NanoDegree de Engenheiro Machine Learning da Udacity. Consiste em aplicar técnicas de aprendizagem supervisionada sobre os dados coletados pelo censo dos Estados Unidos para ajudar a CharityML (uma instituição de caridade fictícia) a identificar as pessoas com maior probabilidade de doar à causa deles.

# Objetivo do Projeto
Avaliar e otimizar vários agentes de aprendizagem supervisionada para determinar qual algoritmo levará ao maior rendimento com doações, ao mesmo tempo em que reduz também o número total de cartas enviadas.

# Destaques do Projeto
Este projeto foi desenvolvido para se familiarizar com os muitos algoritmos de aprendizagem supervisionada disponíveis em sklearn e também para mostrar como cada modelo funciona e performa em um determinado tipo de dado. É importante em machine learning compreender exatamente quando e onde um determinado algoritmo deve ser usado e quando deve ser evitado.

Aprendizados com esse projeto:
- Como identificar se o pré-processamento é necessário e como aplicá-lo.
- Como estabelecer uma referência para uma solução do problema.
- O que cada um dos vários algoritmos de aprendizagem supervisionada realiza, considerando um conjunto de dados específico.
- Como avaliar se um candidato a modelo de solução é adequado ao problema.

# Modelos Usados no Projeto
Ensemble Methods (Gradient Boosting), Gaussian Naive Bayes (GaussianNB) e Logistic Regression.

# Resultados dos Modelos
Com relação ao tempo, podemos ver uma grande diferença entre os modelos. Porém, como o nosso objetivo não é rodar o modelo em tempo real e não precisamos de um resultado em tempo real, é melhor deixar esse parâmetro de lado e escolher pela assertividade. No quesito assertividade, o modelo que se saiu melhor e o que eu indico é o Gradient Boosting Classifier. Se verificarmos o F score para o conjunto de testes quando 100% do conjunto de treino é utilizado, essse model é o que tem o melhor desempenho. Quanto ao tempo de predição, ele não é o mais rápido, porém não é o mais lento. Isso se dá porque as árvores são constuídas sequencialmente, fazendo com que o treinamento demore um pouco mais. Só que ele é um aprendiz melhor. É um ótimo modelo para classificação e para dizer quem será um possível doador ou não.

# Explicação do Modelo Escolhido
O modelo escolhido foi o Gradient Boosting Classifier. É uma técnica de aprendizado de máquina supervisionada usada para criar modelos preditivos baseados em árvore de classificação. É supervisionada pois é fornecido um conjunto de dados de treinamento rotulado para construir o modelo de árvore de classificação ou regressão. Uma árvore de classificação é um tipo de árvore de decisão. A saída de uma árvore de classificação é uma classe. Por exemplo, dado um conjunto de dados do paciente, você pode tentar prever se o paciente terá câncer. A classe seria "terá câncer" ou "não terá câncer". Ou, no nosso caso, se será um possível "doador" ou "não doador". Ele treina uma árvore de cada vez, onde cada nova árvore ajuda a corrigir erros cometidos por árvores previamente treinadas. Com cada árvore adicionada, o modelo se torna ainda mais expressivo e assertivo. Esse modelo é ótimo para classificação, que é justamente o nosso problema, prever doadores.
