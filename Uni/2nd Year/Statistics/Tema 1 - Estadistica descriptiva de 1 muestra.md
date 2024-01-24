

>[!info] Tablas de frequencias 
>### $n_i$ - Frecuencia absoluta 
>El número de veces que se repite el valor $x_i$ .
> ### $f_i$ - Frecuencia relativa 
> $f_i = \frac{n_i}{N}$ es la proporción (porcentaje) de $n_i$.
> 
> 
%% > ### Freciencia absoluta acumulada
> ### Frecuencia relativa acumulada %%

## Tipos de variable
- Cualitativas (categoricas)
	-  Nominal
	- Ordinal

- Cuantitativas
	- Discretas
	- Continuas
	![[DistribucionFrecAgrupadas.png]]

## Medidas caracteristicas

**Medidas de Posición:**
- **Media:** Valor promedio de un conjunto de datos. $$\overline{x} = \sum_{i=1}^{k}\frac{x_i n_i}{N}$$
- **Mediana:** Teniendo los datos ordenados de menor a mayor, es el valor que deja la misma cantidad de datos a su izquierda y a su derecha.
- **Moda:** Valor más frecuente en un conjunto de datos.
- **Cuantiles:** Divisiones del conjunto de datos en partes iguales (porcentajes).
	- $P_{25}$ - 25% de datos por debajo
	- $P_{50}$ - 50% de datos por debajo
	- $P_{75}$ - 75% de datos por debajo

**Medidas de Dispersión - Absolutas:**
- **Recorrido (Rango):** $(R = \max\{x_i\} - \min\{x_i\})$
- **Rango intercuartílico:** $(RI = IQR = Q3 - Q1)$
- **Varianza:** $(s^2 = \frac{\sum_{i=1}^{N}(x_i - \bar{x})^2}{N} = \frac{\sum_{i=1}^{N}x_i^2}{N} - \bar{x}^2)$ (siempre mayor o igual a cero)
- **Desviación típica:** $(s = \sqrt{s^2})$ (siempre raíz positiva)
- **Varianza insesgada:** $(s^*_2 = \frac{\sum_{i=1}^{N}(x_i - \bar{x})^2}{N-1} = \frac{N \cdot s^2}{N-1})$
- **Desviación típica insesgada:** $(s^* = \sqrt{s^*_2})$ (también conocida como sd; es la que calcula el R-commander)

**Medidas de Dispersión - Relativas:**
- **Rango relativo:** Coeficiente que compara el recorrido con la media.
- **Coeficiente de variación de Pearson (CV):** Proporción de la desviación típica en relación con la media.

**Medidas de Forma:**
- **Asimetría:** Desviación y dirección de la distribución de datos con respecto a la media.
- **Apuntamiento:** Mide la "altura" y forma de las colas de la distribución en comparación con una distribución normal.

- **Recorrido (Rango):** \(R = \max\{x_i\} - \min\{x_i\}\)
- **Rango intercuartílico:** \(RI = IQR = Q3 - Q1\)
- **Varianza:** \(s^2 = \frac{\sum_{i=1}^{N}(x_i - \bar{x})^2}{N} = \frac{\sum_{i=1}^{N}x_i^2}{N} - \bar{x}^2\) (siempre mayor o igual a cero)
- **Desviación típica:** \(s = \sqrt{s^2}\) (siempre raíz positiva)
- **Varianza insesgada:** \(s^*_2 = \frac{\sum_{i=1}^{N}(x_i - \bar{x})^2}{N-1} = \frac{N \cdot s^2}{N-1}\)
- **Desviación típica insesgada:** \(s^* = \sqrt{s^*_2}\) (también conocida como sd; es la que calcula el R-commander)