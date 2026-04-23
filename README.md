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


##  Observaciones del Dataset (EDA)

### Calidad y Estructura de los Datos
* **Nulos y Duplicados:** De las 27 variables y 10,248 observaciones, el dataset presenta integridad total (**0% de nulos** y **0% de duplicados**).
* **Tipología:** Se identifican 5 variables de tipo texto, 15 categóricas y 7 numéricas.
    * *Nota:* Las variables `Month`, `Month_Name` y `Data-Collection-date` requieren transformación a tipo **datetime** para el análisis de series de tiempo.

###  Correlaciones Significativas
* **Región vs. Inflación (1.000):** Indica que el cálculo o la fuente de inflación está directamente asociada a la segmentación regional.
* **Continente vs. Región (0.935):** Confirma una jerarquía geográfica lógica y consistente.
* **Basket_USD vs. Inflación (-0.601):** Correlación negativa que sugiere que ante un alza en la inflación local, el costo de la canasta expresado en dólares tiende a bajar (posible efecto de la devaluación cambiaria).

###  Análisis de Distribución
* **Price_USD:** Presenta **asimetría positiva**. La mayoría de los datos se concentran en precios bajos de productos básicos, con una "cola" a la derecha generada por productos de precios elevados (outliers).
* **YoY_Inflation_Estimate_Pct:** Distribución **multimodal**. Los diversos picos indican que la inflación está segmentada por regiones con realidades económicas muy distintas.
* **Breakfast_Basket_USD:** Los costos se concentran principalmente en un rango de **5 a 10 USD**, mientras que los valores entre 15 y 20 USD son menos frecuentes.

---

##  Resumen Estadístico

### Variables Numéricas relevantes
| Variable | Conteo (n) | Promedio | Mediana | Desv. Est. | Mínimo | Máximo |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Inflación YoY %** | 10,248 | 5.53% | 5.50% | 2.49% | 2.40% | 11.20% |
| **Price_USD** | 10,248 | $4.48 | $2.42 | $5.37 | $0.17 | $52.13 |
| **Basket_USD** | 10,248 | $9.56 | $9.17 | $3.98 | $2.84 | $20.61 |
| **FAO_Index_Value** | 10,248 | 125.77 | 125.90 | 0.88 | 124.20 | 127.10 |

### Variables Categóricas releventes

* **Continent:** Asia (3,612 registros).
* **Currency_local:** EUR (1,932 registros).
* **Item:** Milk (1 Liter) (732 registros).

---

##  Entregables de Análisis Externo
Debido a limitaciones de compatibilidad con widgets interactivos en GitHub, el análisis detallado generado mediante librerías de profilado se encuentra disponible en formato pdf: Profilado de datos.pdf





