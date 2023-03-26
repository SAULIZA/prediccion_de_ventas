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
![fat_content_hist](https://user-images.githubusercontent.com/119084098/227784278-f4a914e3-40ab-4c6f-be72-3ade80e4a4a9.png)
Del contenido de grasa podemos decir que, hay una gran oferta de productos con contenido de grasa bajo, sin embargo las ventas de los mismos no son diferentes a las ventas de los productos con contenido de grasa regular.
![fat_content_sales_box](https://user-images.githubusercontent.com/119084098/227783840-7781b644-b9a4-47be-887a-cd80eb4ee75e.png)
