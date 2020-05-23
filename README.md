# ¿Alguna vez te has preguntado como se vería un autoretrato tuyo si fuese pintado por picasso?
#### Esta misma pregunta surgio de mi mente como si fuese la solución para el proyecto final del curso de Redes Neuronales la Universidad de Sonora actualmente impartido por el Dr. Julio Waissman, antes siquiera de idear una respuesta feasible a dicha pregunta mejor me dispuse a la tarea de buscar código por la internet de algún programa que hiciera algo parecido a pintar como picasso pues había oido ya algo sobre las redes neuronales convolucionales y de su gran desempeño para extraer características de imágenes. Todo esto con el fin de responder a la pregunta, reproducir algunos resultados con el código encontrado, hacer varios experimentos y por supuesto crear un proyecto con el cuál aprovar el curso. El resultado de mi búsqueda, [este repositorio Github con el código original en el que esta basado este proyecto.](https://github.com/gsurma/style_transfer) 

# Voilà
![](/images/1944x3_2592_ww_self2.jpg)

## Y así sin más, pasando de la teoría o de dar incluso una explicación coherente de por que esto funciona ([Más Info Aquí](https://towardsdatascience.com/style-transfer-styling-images-with-convolutional-neural-networks-7d215b58f461)), podemos ver algunos resultados.


**Dimensiones de Input (WxH)** | **Número iteraciones en L-BFGS** | **Content Weight** | **Style Weight**
------------ | ------------- | -------------- | ----------------
(300,350) | 50 |   .0005       |    8     |

![](/images/sentado.jpg)


**Dimensiones de Input (WxH)** | **Número iteraciones en L-BFGS** | **Content Weight** | **Style Weight**
------------ | ------------- | -------------- | ----------------
(300,350) | 50 |   .0005       |    8     |

![](/images/persistencia.jpg)


**Dimensiones de Input (WxH)** | **Número iteraciones en L-BFGS** | **Content Weight** | **Style Weight**
------------ | ------------- | -------------- | ----------------
(350,300) | 50 |   .0005       |    8     |


![](/images/rectoria1.jpg)


![](/images/rectoria2.jpg)


**Dimensiones de Input (WxH)** | **Número iteraciones en L-BFGS** | **Content Weight** | **Style Weight**
------------ | ------------- | -------------- | ----------------
(350,300) | 20 |   .0005       |    8     |



![](/images/noche1.jpg)


![](/images/noche2.jpg)

**Dimensiones de Input (WxH)** | **Número iteraciones en L-BFGS** | **Content Weight** | **Style Weight**
------------ | ------------- | -------------- | ----------------
(300,350) | 50 |   .0005       |    8     |



![](/images/grito.jpg)





## Conclusiones

* Aunque los resultados fueron satisfactorios aun se pueden hacer modificaciones a los hyperparámetros para conseguir mejores resultados, por ejemplo aumentado las dimensiones del input o variando los valores Content Weight y Style Weight así como dar un mayor numero de iteraciones. 
* Las dimensiones (350 x 300)px para el input del modelo fueron escogidas por ser las mayores dimensiones que era capaz de procesar el optimizador en tiempo aceptable (debido al relativamente poco poder de computo que poseo). 
* Mayores dimensiones generaban imágenes poco modificadas con el estilo deseado, esto debido a que el incremento de parámetros que actualizar aumentaba el error de la función a optimizar y hacía que la convergencia en el optimizador fuese mas lenta requiriendo mayor número de iteraciones y por consiguiente mayor tiempo de ejecucion el cuál finalmente no se invirtió.
* L-BFGS tarda alrededor de 15 min en finalizar para las dimensiones (350 x 300)px con 50 iteraciones. Más de una hora para dimensiones (500 x 550) o mayores con el mismo número de iteraciones (con el equipo de cómputo donde se desarrollo este proyecto)
* Se pueden probar otras arquitecturas de red neuronal, asi como los pesos de distintas capas para desarrollar la función a optimizar.
