# Predição de Doenças Cardíacas utilizando Machine Learning

**Aluno:** Gabriel Citroni Uliana - NUSP: 9779367<br>

**Disciplina:** SME0878 - Mineração Estatística de Dados<br>
**Professor:** Francisco Aparecido Rodrigues<br>
Universidade de São Paulo - ICMC, São Carlos, Brasil.<br>
2º Semestre - 2021

## Descrição do Projeto
Nesse projeto farei o uso dos conceitos aprendidos ao longo do semestre com o intuito de ***Predizer Doenças Cardiacas utilizando Machine Learning***.<br>
Através do uso de diferentes técnicas e modelos, em seguida analisarei os resultados de cada um para concluir qual apresenta o melhor resultado para esse problema.

## Referências

Para esse projeto, uso como base o artigo publicado por Aman Kharwal, encontrado em: https://thecleverprogrammer.com/2020/11/10/heart-disease-prediction-using-machine-learning/

E os dados também usados nesse mesmo artigo, disponiveis em: https://raw.githubusercontent.com/amankharwal/Website-data/master/heart.csv

## Classificação

Comparamos diversos métodos de classificação, utilizando validação cruzada.<br>
Para cada Classificador nós treinamos o modelo e predizemos os valores de doenças cardíacas do grupo de teste.
<br> Fazemos isso de 2 formas:
<br>1º - Com todas os dados do dataset, utilizando todos os atributos disponiveis.
<br>2º - Com a aplicação de Principal Component Analysis com 90% de cumulative explained variance, utilizando apenas 17 componentes do dataset

## Conclusão

Apresentando os resultados das classificações de forma ordenada.



| Modelo | Resultado AUC |
| -------- | -------- |
| K-Neibhors Euclidean(PCA) | 0.8732425662572721 |
| K-Neibhors Minkowski(PCA) | 0.8732425662572721 |
|  K-Neibhors Manhattan(PCA) | 0.8571468972204267 |
| Logistic Regression | 0.8557409502262443 |
| K-Neibhors Euclidean | 0.8545067065287654 |
| K-Neibhors Minkowski | 0.8545067065287654 |
| K-Neibhors Manhattan | 0.8542441014867486 |
| K-Neibhors Chebyshev(PCA) | 0.8512908047834518 |
| Bernoulli NB | 0.8490829023917259 |
| Bernoulli NB (PCA) | 0.8425702973497092 |
| SVM | 0.8412714124111182 |
| SVM (PCA) | 0.8394452973497091 |
| Random Forest | 0.8369242889463477 |
| Random Forest (PCA) | 0.8361122333548803 |
| Logistic Regression (PCA) | 0.8275513089851325 |
| Gaussian NB (PCA) | 0.8057813510019392 |
| K-Neibhors Chebyshev | 0.7696468972204266 |
| Gaussian NB | 0.7396816418875243 |


Podemos notar que o uso de Principal Component Analysis foi decisivo para melhorar a predição para os modelos de K-Neighbors.
<br> Fazendo com que KNN - Euclidean (PCA), KNN- Minkowski (PCA) produzissem os melhor resultados para o nosso dataset.
<br>Por outro lado, se não usassemos PCA o melhor modelo seria o Logistic Regression, um modelo de aprendizado supervisionado.

<br>Concluindo, para esse dataset o melhor modelo testado foi o K-Neighbors, um modelo de aprendizado não supervisionado, com as métricas Euclidean e Minkowski e utilizando a redução de dimensionalidade dos dados (PCA).

