# Classificando Imagem de Urso

Neste projeto, foi aplicado técnicas de classificação para reconhecimento de imagens de Ursos, em que o dataset foi obtido no kaggle(pode ser acessado [aqui](https://www.kaggle.com/datasets/hoturam/bear-dataset))

Neste dataset, temos a seguinte quantidade de imagens:


![image](https://user-images.githubusercontent.com/39843884/177597560-1e5792ef-65e7-4326-98d3-dac2b0ad59f0.png)

Podemos ver que temos mais urso polar, no inicio não se fará nenhum tratamento na quantidade para servir de baseline e servir de comparação.

## Fazendo Extração de caracteristicas

Neste Processo Pegamos uma rede já treinada e usamos a mesma para fazer extração de carcteriticas, utilizando um classifcador, a rede que teve a melhro perfomace como base foi a *InceptionResNetV2* e o classificador que teve a melhor perfomace foi o KNN com as seguintes métricas:

![image](https://user-images.githubusercontent.com/39843884/177598262-908e5f9f-ddeb-47f9-91f2-f818b6e1d8ec.png)

O intuito agora é verificar se utilizando o fine tunnig o data argumentation poedmos melhorar os resultados, mas pra de inicio já temos resultados muito bom.

## Aplicando Fine-tunning

Aplicando o fine-tunning, obteve os seguintes resultados

![image](https://user-images.githubusercontent.com/39843884/177995381-8eb36ab0-0b20-4095-a9ec-91b4bf757105.png)

Comparando os resultados com o kNN da extração de caracteristicas acimas, podemos ver que tem uma diferença muito pequena nas métricas,logo o melhor a ser aplicado, pelo processamento e pela perfomace é a extração de caracteristicas.

## Conclusão

Apesar da classificação estar desbalanceada, o modelo teve uma acuracia em torno de 98%, mostrando uma boa perfomace na classificação de imagens, logo temos um bom modelo para classificar urso sem criar uma rede do zero e mostrando assim uma das vantagens de redes neurais em poder usar como base para extração de caracteristicas
