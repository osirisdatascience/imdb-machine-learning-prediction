# imdb-machine-learning-prediction


O projeto está dividido por células de markdown, com explicação clara do objetivo de cada célula de código.

As perguntas foram respondidas:

Qual filme você recomendaria para uma pessoa que você não conhece?
# Minha estratégia é seguir 3 regras
# Regra 1 - Quantidade de votos desse filme tem que estar próximo a mediana, por dar indícios de uma quantidade recorrente de votos, sendo comum
# Regra 2 - Nota IMDB acima da média, dos filmes que tenham nmero de votos proximo a mediana
# Regra 3 - Faturamento acima da média, dos filmes que tenham nota acima da media e que tenham quantidade de votos prox da mediana
# Regra 4 - Meta_score acima da media, dos filmes que tenham faturamento acima da media, tenham nota acima da media e que tenham quantidade de votos prox da mediana
#  e por fim, obter o filme com maior soma de Meta_score e IMDB_Rating



Quais são os principais fatores que estão relacionados com alta expectativa de faturamento de um filme? 
Sabemos que corelação não implica em causalidade, mas existem variáveis altamente relacionadas com o faturamento, até mesmo variáveis categóricas, como o gênero, encontrará no código

Quais insights podem ser tirados com a coluna Overview? É possível inferir o gênero do filme a partir dessa coluna?
A forma com a qual é tratada os overviews, pode indicar tendências na hora de definir o gênero.

Modelo de Regressão foi implementado para prever a nota IMDB do livro em questão:
Explique como você faria a previsão da nota do imdb a partir dos dados:
1. Seleção de Variáveis
Vamos usar as variáveis numéricas que, com base na análise exploratória de dados, têm uma correlação potencial com a nota do IMDb:

Meta_score: A pontuação média de críticos, que geralmente correlaciona com a percepção geral de qualidade.
No_of_Votes: O número de votos que um filme recebeu no IMDb, um indicativo de popularidade e engajamento.
Gross: A receita bruta do filme, refletindo o sucesso financeiro e, possivelmente, a aceitação popular.
Essas variáveis foram escolhidas porque são numéricas e têm impacto direto ou indireto na nota de um filme.

2. Preparação dos Dados
Remover Variáveis Categóricas: Excluir todas as variáveis não numéricas do DataFrame.
Conversão de Tipos: Garantir que todas as variáveis numéricas estejam no formato correto (por exemplo, converter Gross de string para float).
Divisão dos Dados: Separar os dados em conjuntos de treino e teste.
3. Modelagem
Vamos utilizar a regressão linear, uma técnica simples mas poderosa para prever valores contínuos. A regressão linear é fácil de interpretar e serve como um bom ponto de partida.

4. Avaliação do Modelo
Para avaliar a performance do modelo, usaremos a Mean Squared Error (MSE), que mede a média dos quadrados dos erros. O MSE é útil porque penaliza erros grandes mais fortemente, dando uma indicação clara da precisão do modelo.

Quais variáveis e/ou suas transformações você utilizou e por quê?
Variáveis Utilizadas: Meta_score, No_of_Votes, Gross. Estas foram escolhidas com base na análise de que elas têm impacto significativo na nota do IMDb.

Qual tipo de problema estamos resolvendo (regressão, classificação)? 
Problema Resolvido: Problema de regressão, onde prevemos uma variável contínua (IMDB_Rating).

Qual modelo melhor se aproxima dos dados e quais seus prós e contras? 
Modelo: O Linear Regression foi utilizado, que é simples de interpretar e funciona bem para relações lineares.

Qual medida de performance do modelo foi escolhida e por quê?
Performance: A Mean Squared Error (MSE) foi escolhida como a métrica de performance para avaliar a precisão do modelo, pois penaliza grandes erros e é amplamente usada em problemas de regressão.


Necessidade de instalação: Arquivo requirements.txt

