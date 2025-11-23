# Implementando uma CNN com `torchvision`

## Proposta

Uma Rede Neural Convolucional utiliza filtros bidimensionais para extrair _features_ a partir de imagens, que alimentarão pesos de uma rede neural. O objetivo da atividade é utilizar um dos datasets presentes na biblioteca `torchvision` para treinar uma CNN que irá classificar elementos do dataset FashionMNIST.

## Treinamento

Utilizando a classe `Architecture` proposta em aula, um modelo similar ao LeNet foi implementado, dispondo de camadas convolucionais, seguidas de camadas ReLU e camadas de max pooling.

## Análise dos Resultados

Inicialmente, o modelo LeNet-like não possuía camadas de dropout. Isto levou a um problema de overfitting, onde a função de perda do treinamento diminuía, mas a função de perda para o conjunto de validação não estava decrescendo. Com isso, A função de perda mostrou um comportamento mais satisfatório:
![função de perda](img/training_losses.png)
