#Generación fractal de terreno

##¿Qué es un fractal?
Un fractal es un fenómeno natural que puede describirse matemáticamente con un conjunto que exhibe el mismo patrón a diferentes escalas, también se conoce como simetría expansiva o simetría evolutiva. Si el patrón es exactamente el mismo independientemente de la escala se dice que existe autosimilitud.

##Paisajes fractales
Un paisaje fractal es una superficie generada por computadora basada en un algoritmo estocástico diseñado para producir comportamiento fractal que asemeja la apariencia del terreno natural. Es importante resaltar que aunque sea el resultado de una función se trata de un proceso no determinístico, es decir, aleatorio.

Muchos fenómenos naturales exhiben autosimilitud dentro de ciertos rangos y esta puede ser modelada matemáticamente mediante fractales, el ser humano utiliza las variaciones en la textura y la pendiente para ubicarse. El modelado de la superficie terrestre mediante movimiento browniano fraccionario fue propuesto por Benoît Mandelbrot, una de las personas más influyentes en el campo de fractales.

##Generación de terreno

* Matemáticas
* Ruido
* Modelos de erosión

###Desplazamiento medio

Los modelos de desplazamiento medio pueden estar relacionados con los de ruido. Se refieren a que se toma un desplazamiento medio entre la altura dada de dos puntos para general la interpolación y altura de un nuevo punto entre ellos.

###Ruido

**Ruido de valor
Este método, que comunmente se confunde con ruido de gradiente, se basa en asignar una señal de ruido aleatorio a cada uno de los valores de una matriz de alturas. Después se recorre la matriz y el valor final de cada punto se obtiene intepolando con los valores de los pundos colindantes.

**Ruido de gradiente
Similar al método de ruido de valor, lo que hace que se preste a confusión. En este caso a cada valor de la matriz de alturas se le asigna un gradiente, que se refiere a una variación y no a un valor, el valor final también se obtiene interpolando los valores de puntos colindantes. Ejemplos de este tipo son Ruido Perlin, Ruido Simplex y Ruido OpenSimplex.

**Ruido de Celda o Ruido Worley
Es un algoritmo con resultados interesantes en el que se ponen puntos aleatorios alrededor del mapa de elevaciones de interés y para cada punto el valor será la distancia al eneavo (donde n se asigna) punto más cercano. Generalmente encontrar la distancia entre todos los puntos es muy caro, computacionalmente hablando, y se divide el área en celdas, por lo que para cada punto sólo se utilizan los puntos dentro de la celda y de ahí obtiene su nombre.

**Ruido por movimiento Browniano fraccionario
El movimiento Browniano es el ruido aleatorio de las partículas suspendidas en un fluido que resulta de las colisiones con las moléculas más rápidas del fluido, en el caso del movimiento Browniano fraccionario los incrementos de ruido no tienen que ser independientes. Para obtener los valores de elevación se suman octavas de ruido sucesivas.

**Algoritmo del diamante y el cuadro



###Modelos de erosión
Los modelos de erosión se toman de las ciencias naturales. Se inicia con una imagen base en la que los valores representan elevaciones, a veces llamada continuo de elevaciones o mapa digital de elevaciones, y se le aplican métodos que simulan el desgaste que producirían ciertos elementos naturales en ese terreno. En este caso existen una variedad muy amplia de métodos y que pueden no tener relación alguna, matemáticamente hablando. Los modelos de erosión más usados son erosión hidráulica y erosión térmica.
