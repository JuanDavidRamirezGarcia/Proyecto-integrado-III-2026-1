# Proyecto-integrado-III

## I Definición del problema

**Definición de problema y su impacto**

Según la **FAO** los precios mundiales de productos alimenticios subieron en marzo de 2026 por segundo mes consecutivo. Debido en gran medida al conflicto que hay en Medio Oriente, el cual ha encarecido los precios energéticos y por ende el precio de alimentos, los cuales cuestan más su producción. Como muestra el índice de precios, subió un 2,4% más que en febrero del mismo año y un 1% más que el promedio del año anterior. Se espera que los precios sigan subiendo a medida que el conflicto continúe.

Para Latinoamérica el impacto será el mismo, el alza de precios de productos de la canasta básica, ya que la región depende de fertilizantes importados para la producción, lo cual aumenta el costo de producción y cultivo. En consecuencia, estos precios se trasladan al consumidor y impactan el alza del costo de vida.

De acá la importancia de analizar los precios de algunos alimentos en Colombia y compararlos con los precios de otros países en la región.

Fuente: https://www.fao.org/newsroom/detail/fao-food-price-index-rises-in-march-as-near-east-conflict-raises-energy-costs/es


## Formulación pregunta de investigación

**Pregunta de investigación:**

¿Cómo varió el costo de la "Canasta de Desayuno" (Breakfast Basket) en las ciudades de Colombia comparado con el promedio regional de Latinoamérica entre octubre de 2025 y marzo de 2026, y qué categorías de alimentos fueron las más volátiles?


## Definición de métricas

Definición de métricas para evaluar el éxito del análisis.

1. Puntaje de encarecimiento: Esta métrica mide el índice de encarecimiento acumulado. Asignando a todos los países un puntaje base de 100 puntos y comparando los precios a través del tiempo.

$Puntaje=(\frac{Price-USD-actual}{Price-USD-octubre-2025})*100$

2. Variación del costo de la canasta familiar: Esta métrica nos mostrará el porcentaje total de encarecimiento de los productos de la canasta básica.

$variacion=(\frac{Breakfast-Basket-Marzo2026-Breakfast-Basket-Octubre2025}{Breakfast-Basket-Octubre2025})*100$

3. Diferencia del costo de la canasta en dolares= En esta variable se va a comparar el costo en dólares de la canasta básica con el promedio de los países de Latinoamérica.

$Brecha-(USD) = Breakfast-Basket-USD_{Colombia} - Promedio-Basket-USD_{Latam}$



