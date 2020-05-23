# ¿Alguna vez te has preguntado como se vería un autoretrato tuyo si fuese pintado por picasso?
#### Esta misma pregunta surgio de mi mente como si fuese la solución para el proyecto final del curso de Redes Neuronales la Universidad de Sonora actualmente impartido por el Dr. Julio Waissman, antes siquiera de idear una respuesta feasible a dicha pregunta mejor me dispuse a la tarea de buscar código por la internet de algún programa que hiciera algo parecido a pintar como picasso pues había oido ya algo sobre las redes neuronales convolucionales y de su gran desempeño para extraer características de imágenes. Todo esto con el fin de responder a la pregunta, reproducir algunos resultados con el código encontrado, hacer varios experimentos y por supuesto crear un proyecto con el cuál aprovar el curso. El resultado de mi búsqueda, [este repositorio Github con el código original en el que esta basado este proyecto.](https://github.com/gsurma/style_transfer) 

# Voilà
![](/images/1944x3_2592_ww_self2.jpg)

## Y así sin más, pasando de la teoría o de dar incluso una explicación coherente de por que esto funciona ([Más Info Aquí](https://towardsdatascience.com/style-transfer-styling-images-with-convolutional-neural-networks-7d215b58f461)), podemos ver algunos resultados.


sentado
**Dimensiones de Input (WxH)** | **Número iteraciones en L-BFGS** | **Content Weight** | **Style Weight**
------------ | ------------- | -------------- | ----------------
(300,350) | 50 |   .0005       |    8     |

![](/images/sentado.jpg)


Persistencia
**Dimensiones de Input (WxH)** | **Número iteraciones en L-BFGS** | **Content Weight** | **Style Weight**
------------ | ------------- | -------------- | ----------------
(300,350) | 50 |   .0005       |    8     |

![](/images/persistencia.jpg)

rectoria 1
**Dimensiones de Input (WxH)** | **Número iteraciones en L-BFGS** | **Content Weight** | **Style Weight**
------------ | ------------- | -------------- | ----------------
(350,300) | 50 |   .0005       |    8     |
![](/images/rectoria1.jpg)
![](/images/rectoria2.jpg)
Cerro Campana
**Dimensiones de Input (WxH)** | **Número iteraciones en L-BFGS** | **Content Weight** | **Style Weight**
------------ | ------------- | -------------- | ----------------
(350,300) | 20 |   .0005       |    8     |
![](/images/noche.jpg)
![](/images/noche2.jpg)

Grito
**Dimensiones de Input (WxH)** | **Número iteraciones en L-BFGS** | **Content Weight** | **Style Weight**
------------ | ------------- | -------------- | ----------------
(300,350) | 50 |   .0005       |    8     |
![](/images/grito.jpg)











## Conclusiones


