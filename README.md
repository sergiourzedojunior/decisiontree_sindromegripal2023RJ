# Decision Tree Estudo de Caso de Sindrome Gripal 2023 RJ

## o projeto tem como hipótese identificar uma correlação positiva entre casos confirmados de covid e notificações de primeira dose vacinal após o registro de consulta no SUS com sintomas gripais

**Dados**

**base_url = 'https://s3.sa-east-1.amazonaws.com/ckan.saude.gov.br/SGL/2023/uf={uf}/lote=1/part-00000-be9c7ea7-4ed2-4556-be25-da48754e24bf.c000.csv'**

### Método

* 1 - captura dos dados em saude.gov.br
* 2 - tratamento dos dados
* 3 - criação de indicadores
* 4 - aplicação de one-hot encoding para customização do dataframe
* 5 - DecisionTreeClassifier para criação de coluna de scores (probabilidades)
* 6 - Teste: Accuracy
* 8 - A/B test (Hipotesys)

**Conclusão**

Um limite comum de significância é 0,05. Se o valor p for inferior a 0,05, rejeitaria a hipótese nula e concluiria que há uma diferença significativa entre os grupos. Porém, neste caso, o valor p é maior que 0,05, portanto não se rejeitaria a hipótese nula. Isso significa que, com base neste teste, não há diferença significativa nas pontuações entre os dois grupos definidos pelo Primdose_depois (primeira dose depois de testar positivamente para covid).

A hipótese do estudo era que a probalidade de testar positivamente para covid seria maior, caso a data da primeira dose registrada seria posterior a notificação de consulta e testes, porém não houve diferença significativa para os dados de 2023 no Estado do RJ.

É importante considerar que como confirmado pelos cientistas as variações no vírus faziam com que doses anteriores não evitavam a contaminação, porém diminuiam os casos do óbito. Como pode ser relatado abaixo:

The proportion of Óbito in evolucaoCaso is: 0.26%