# PROYECTO DE PREDICCIÓN DE VENTAS
## INTRODUCCIÓN
Nuestro primer proyecto como científico de datos es la predicción de ventas. Se nos ha dotado de un conjunto de datos de ventas de productos, las variables que componen el conjunto de datos es el siguiente:
* Item identifier: Es un identificador de un producto
* Item weight: El peso del producto
* Item fat content: Contenido de grasa del producto (low, regular)
* Item visibility: Indica el porcentaje de visibilidad del producto en exhibición 
* Item type: Iindica el tipo de producto (tipo desayuno, comida congelada, frutas y vegetales, etc)
* Item MRP: El precio de venta al público
* Outlet identifier: Identificación de la tienda
* Outlet establishment year: Año de establecimiento de la tienda
* Outlet size: Tamaño de la tienda
* Outlet location type: Es el tipo de hubicación de la tienda (tier 1, 2 o 3)
* Outlet type: Tipo de tienda (supermercado tipo 1, 2 o 3, tienda de abastos)
* Item outlet sales: venta de un producto en una tienda
Dado el conjunto de datos con las características mencionadas, se tiene como objetivo predecir las ventas de los productos que se ofertan en las distintas tiendas.

## ANÁLISIS DE LOS DATOS
![Capture](https://user-images.githubusercontent.com/119084098/227784396-976baa8b-1a16-4c3a-a6bd-db7cac4da6e6.PNG)

![Capture2](https://user-images.githubusercontent.com/119084098/227784500-86c12eaf-79cc-48fd-be52-3c079a20a3df.PNG)

* Del contenido de grasa podemos decir que, hay una gran oferta de productos con contenido de grasa bajo (gráfico de barras del contenido de grasa de los productos), sin embargo las ventas de los mismos no son diferentes a las ventas de los productos con contenido de grasa regular (gráfico de caja de las ventas de productos según su contenido de grasa).
 
![Capture1](https://user-images.githubusercontent.com/119084098/227784634-aef66719-beed-4938-9aa3-6ec504a5a269.PNG)

* De los tipos de productos podemos decir que hay una gran demanda de cierto tipo de productos (según el gráfico de barras del tipo de producto)

![Capture3](https://user-images.githubusercontent.com/119084098/227784856-36e1747a-0ed8-4e7f-9e09-fbdbaebec3c5.PNG)

![Capture4](https://user-images.githubusercontent.com/119084098/227784862-5cf1d1a8-be14-4066-861d-42d22e45afa5.PNG)

* Del gráfico de barras del tipo de ubicación de la tienda se puede ver que existe una diferencia de tiendas dependiendo del tipo de lugar, además se puede ver que las ventas dependiendo del tipo de lugar de las tiendas varían con cierta dependencia también.

![Capture5](https://user-images.githubusercontent.com/119084098/227785066-1a0f9ece-f159-44bf-a4f6-e02ca5796efd.PNG)

![Capture6](https://user-images.githubusercontent.com/119084098/227785081-510507c9-09a6-48c2-80fc-f71b5721a039.PNG)

* Del gráfico de barras del tipo de tienda se puede observar que hay diferencia entre la cantidad e ciertos tipos de tienda y otros, así mismo las ventas en las distintas tiendas varían según el gráfico de caja y bigotes.

![Capture7](https://user-images.githubusercontent.com/119084098/227785228-7279bbc0-e287-46b1-bf88-e49eab7ba07e.PNG)

* Del gráfico de calor podemos ver que solamente la columna de precios de productos tiene una cierta correlación con la venta de los productos.

## PREDICCIÓN DE VENTAS

* Con base en las características de los datos encontradas podemos decir que, para nuetro modelo de predición solamente es necesario variables como: el precio de productos, el tipo de tiendas, el tipo de hubicación de la tienda y el tipo de producto.

### Regresión lineal
![Capture8](https://user-images.githubusercontent.com/119084098/227785699-23bd2a47-498c-4aa8-b031-1b6d0138e282.PNG)

* El primer modelo que se usó para la predicción en la pregresión lineal, se puede observar en el gráfico la relación que existe entre las ventas reales y las ventas predichas, lo ideal sería obtener puntos al rededor de una linea recta, esto no se ve. Lo que se ve son puntos difusos, lo que quiere decir visualmente que la predicción en mala. El cálculo de la puntuación R^2 es de 0.38 tanto para los datos de entrenamiento como para los datos de testeo, lo cual es bajísimo. Además el error de la predicción ronda los 1299 dólares para los datos de testeo y 1345 dólares para los datos de entrenamiento.

## Árbol de decisión
![Capture9](https://user-images.githubusercontent.com/119084098/227785891-043ea39d-453b-4c36-8a71-e9a17a7f66ff.PNG)

* Para el árbol de decición fue necesario el ajuste de la profundidad máxima, el cual fue de 5. De no hacer este ajuste el modelo sufría un sobreajuste con los datos de entrenamiento.

![Capture10](https://user-images.githubusercontent.com/119084098/227785939-d5a9db18-f2c9-4861-a46b-1e432d38b1a9.PNG)

* Una vez desbierto el hiperparámetro max depth, se realizó el ajuste. La puntuación obtenida de R^2 en este caso es de 0.6 para los datos de entrenamiento y 0.59 para los datos de testeo. La predición mejor en este caso, sin embargo la puntuación R^2 sigue siendo bajo. De hecho, el error ahora es de 1082 para los datos de entrenamiento y 1056 para los datos de testeo. Visualmente se puede observar el gráfico de ventas reales vs ventas predichas, ahora los puntos no son tan difusos como antes.

## CONCLUSIONES Y RECOMENDACIONES
* Los dos modelos usados para predecir las ventas tuvieron un rendimiento bajo, sin embargo el árbol de decisión obtuvo mejores resultados.
* Se recomienda usar o pedir a la empresa más variables de los productos para la predicción de ventas. Si complicamos más el modelo es mu probable que mejore el ajuste.



