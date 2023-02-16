# Detecção de Fraudes em Cartões de Crédito usando Classificação com Árvores de Decisão

![RandomForest](https://user-images.githubusercontent.com/97552106/219500082-1f6382ad-3d68-4e48-bed5-2a53ea209e7e.png)


## :dart: Objetivo
Desenvolver e aplicar conhecimentos de Machine Learning obtido no curso de :  Árvores de Decisão - Aprofundando em Modelos de Machine Learning com a utilização de um dataset ccom transações de cartões de crédito genuínas extraídos do Kaggle.

## :bookmark: Contexto
Pesquisa da Kaspersky apurou que a fraude com cartão de crédito é ainda grande no país. A pesquisa aponta que ***20% das pessoas  tiveram seu cartão de crédito utilizado sem autorização por terceiros***, número importante quando é levado em conta a quantidade de pessoas que utilizam este meio de pagamento.

É importante que as empresas de cartão de crédito sejam capazes de reconhecer transações fraudulentas com cartão de crédito para que os clientes não sejam cobrados por itens que não compraram e não causarem prejuízos.

## :pushpin: Considerações do Dataset
- Possui transações genuínas feitas por cartões de crédito em set/2013 por titulares de cartões europeus.

- Apresenta transações ocorridas em 2 dias, onde tivemos 492 fraudes em 284.807 transações;

- O conjunto de dados está totalmente desbalanceado, onde a classe positiva (Fraudes) representa 0,172% de todas as transações;

- Os atributos identificados nas colunas por: ***`V1`, `V2`...`V28` *** tiveram seus nomes mascarados por motivos de confidencialidade sobre os dados.

- `Time` - atributo que contém os segundos decorridos entre cada transação e a primeira transação no dataset.

- `Class` - é a variável resposta e assume valor 1 para Fraudes e 0 para Não Fraude

[Fonte dos Dados](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

## :computer: Conteúdo
O Projeto foi organizados nos seguintes tópicos para uma melhor organização e compressão:
1. Sobre o Dataset do projeto e Análise Exploratória dos dados;
2. Declaração de Funções para os modelos;
3. Preparação dos dados de treino e teste;
4. Gerando o Modelo;
5. Visualizando e Salvando o Modelo
6. Avaliando as Métricas ( Score, Precision e Recall Scores)
7. Ajustando o Modelo com algoritmos (Decision Tree, Random Forest, Ada Boost)
8. Conclusão

## :closed_book: Conclusão
No primeiro teste já foi identificado um Overfiting do modelo devido o modelo estar desbalanceado, com isso, afim de termos um modelo com resultados eficazes, foi considerado as Métricas de Precisão e Recall, afim de, avaliarmos com mais detalhes o modelo e reduzir os erros (Falsos Positivos e Falsos Negativos) já que estes são cruciais para este caso. 

Foram utilizados 3 modelos, como: Decision Tree, Random Forest, Ada Booster com regularização de hiperparâmetros, onde após alguns testes o melhor resultado foi obtido com o ***Modelo Random Forest***:

***Accurancy Score:  0.9995 | Precision Score:  0.9737 | Recall Score:  0.7551***

De acordo com o Recall e a Matriz de Confusão, teremos 12 operações com cartão de crédito bloqueados como Fraudes (Falso Positivo), onde a operadora,em seguida poderá enviar um SMS ou popup no Aplicativo solicitando o reconhecimento da compra, liberando após a confirmação.
