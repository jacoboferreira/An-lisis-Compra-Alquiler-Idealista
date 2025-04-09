# **Análisis de la rentabilidad en la compra y alquiler de pisos**

Un análisis de la compra y alquiler de viviendas en las ciudades de Madrid, Sevilla y Algeciras.

## **1. Resumen o descripción**

En este proyecto se ha recopilado información sobre la compra y alquiler de viviendas en las ciudades de Madrid, Sevilla y Algeciras, con el objetivo de analizar qué tipo de vivienda y sus características tienen una mayor capacidad de retorno. Además, se incluye un análisis evolutivo del coste de compra y alquiler de viviendas en estas tres ciudades.

## **2. Estructura del repositorio**

- 📂 **Alquiler:** Contiene los archivos Excel descargados y el acumulado en bruto de alquiler, organizados en carpetas por ciudad.
- 📂 **Compras:** Contiene los archivos Excel descargados y el acumulado en bruto de compras, organizados en carpetas por ciudad.
- 📂 **Evolutivo:** Contiene los archivos Excel descargados y el acumulado en bruto de la evolución del coste de compra y alquiler por ciudad.
- 📄 **Acumulado compra:** Recopila los datos en bruto por ciudad antes de la consulta.
- 📄 **Acumulado nuevo - alquiler:** Documentos con las tablas de datos limpios para su análisis.
- 📊 **Análisis comparativo:** Documento de Excel que contiene todos los datos listos para analizar y los dashboards.
- 📄 **Datos limpios compra:** Documento con datos ampliados de compras para incluir en el análisis.

## **3. Instalaciones y requisitos**

Para ejecutar este proyecto, es necesario contar con las siguientes herramientas:

- Microsoft Excel
- Query
- Python
- Idealista
- Listly.io

## **4. Explicación de los datos**

Para comprender y llevar a cabo el análisis, es importante tener conocimiento del sector inmobiliario (*real estate*). Los documentos de datos se dividen en tres categorías: **compra, alquiler y evolutivo**.

En los documentos de **compra y alquiler**, las columnas son las mismas. A continuación, se describen las principales:

- **Título:** Nombre del anuncio.
- **Ciudad:** Ciudad en la que se encuentra la vivienda.
- **Coste:** Precio en euros.
- **Habitaciones:** Número de habitaciones.
- **Metros cuadrados:** Superficie total del inmueble.
- **Vivienda:** Tipo de inmueble (piso o casa).

Además, existen otras columnas como: **Ascensor, Garaje (exterior/interior), columnas calculadas, negocio y área de la ciudad**.

En el caso del **evolutivo**, se utilizarán las siguientes cuatro columnas en el análisis:

- **Fecha (año y mes)**
- **Año**
- **Precio por metro cuadrado**
- **Ciudad**

## **5. Proceso llevado a cabo**

El proceso del análisis se realizó en bloques. Primero, se verificó si era posible representar los datos en un dashboard para los análisis. Posteriormente, se repitió el proceso de obtención de datos para obtener una muestra más representativa.

### **Descarga de datos**
Se investigó una plataforma gratuita que permitiera descargar datos de Idealista en formato Excel. Se pudo realizar este proceso con las limitaciones de la versión gratuita. 

Al descargar los datos de los pisos en alquiler, se observó que tenían una estructura adecuada. Sin embargo, en el caso de los pisos en compra, la información estaba distribuida de forma estructurada pero con mucha separación.

### **Limpieza de los datos**
Primero, se analizó qué datos se descargaban, su formato y su relevancia. Luego, se estructuraron y dividieron para el análisis.

Inicialmente, la información no seguía un patrón uniforme, por lo que se tuvo que ordenar manualmente eliminando, añadiendo o cambiando el orden de las columnas.

Una vez organizado, los datos se procesaron con Power Query en Excel para realizar la limpieza: 
- Extracción de información según delimitadores.
- División de columnas.
- Inserción de nuevas columnas.
- Reemplazo de valores.

Para los documentos de compras, se utilizó un código en Python para estructurar la información en columnas, quedando con la misma estructura que los documentos de alquiler.

### **Unión de la información**
Los datos obtenidos estaban divididos por ciudades y en cada documento había 32 filas.

Primero, se unificó la información estructurada. Luego, se aplicó el proceso mencionado anteriormente y se crearon dos documentos acumulados: uno para alquiler y otro para compra.

El último documento creado para este análisis fue el **"Análisis comparativo"**, que consta de 7 hojas:

1. **Tabla de alquiler:** Información consolidada de los pisos en alquiler de las 3 ciudades.
2. **Tabla de compra:** Información consolidada de los pisos en venta de las 3 ciudades.
3. **Gráficos:** Tablas dinámicas y gráficos para el dashboard.
4. **Dashboard 1:** Visualización de las características de los pisos más rentables para compra y alquiler, así como su evolución.
5. **Dashboard 2:** Visualización de la cantidad de unidades disponibles.
6. **Evolutivo alquiler:** Tabla con los precios medios por metro cuadrado según fechas.
7. **Evolutivo compra:** Tabla con los precios medios por metro cuadrado según fechas.

## **6. Resultados y conclusiones**

Se ha llevado un análisis de los precios de compra y alquiler de viviendas en las ciudades de Madrid, Sevilla y Algeciras. Los datos han sido obtenidos de Idealista. Se ha obtenido una muestra de 2826 viviendas en venta y 1217 viviendas en alquiler. De esas corresponde a las siguientes ciudades:

- **Algeciras**: Venta 58 (846 (6.8%)) / Alquiler 60 (102 (60.7%))
- **Sevilla**: Venta 645 (10.557 (6.1%)) / Alquiler 270 (1.730 (15.6%))
- **Madrid**: Venta 2123 (22.999 (9.2%)) / Alquiler 887 (11.686 (7.5%))

Las cifras mostradas entre paréntesis son el número de viviendas publicitadas en Idealista a fecha de 08/04/2025. La intención a futuro es ampliar las zonas y profundizar por distritos de interés.

## Tabla 1 – Tiempo de recuperación (años) Piso-Habitaciones

| Piso Habitaciones | Madrid | Sevilla | Algeciras |
|-------------------|--------|---------|-----------|
| 1                 | 26     | 20      | 11        |
| 2                 | 38     | 21      | 13        |
| 3                 | 36     | 19      | 15        |
| 4                 | 37     | 22      | 15        |
| 5                 | 23     | NA      | 22        |
| 6                 | 46     | NA      | NA        |

## Tabla 2 – Tiempo de recuperación (años) Piso-Exterior-Interior

| Piso     | Madrid | Sevilla | Algeciras |
|----------|--------|---------|-----------|
| Exterior | 46     | 22      | 17        |
| Interior | 37     | 21      | 11        |

## Tabla 3 – Tiempo de recuperación (años) Piso-Garaje

| Piso       | Madrid | Sevilla | Algeciras |
|------------|--------|---------|-----------|
| Garaje     | 42     | 22      | 16        |
| Sin Garaje| 50     | 23      | 18        |
| Pago       | 40     | 20      | 19        |

## Tabla 4 – Tiempo de recuperación (años) Piso-Ascensor

| Piso         | Madrid | Sevilla | Algeciras |
|--------------|--------|---------|-----------|
| Ascensor     | 47     | 22      | 17        |
| Sin ascensor | 27     | 20      | 7         |

## Tabla 5 – Evolución del coste en alquiler desde 2020

| Año  | Madrid | Sevilla | Cádiz |
|------|--------|---------|-------|
| 2020 | 0%     | 0%      | 0%    |
| 2021 | -7%    | -1%     | 1%    |
| 2022 | -2%    | 0%      | 8%    |
| 2023 | 7%     | 6%      | 14%   |
| 2024 | 19%    | 11%     | 20%   |
| 2025 | 25%    | 16%     | 23%   |

## Tabla 6 – Evolución del coste en compra desde 2020

| Año  | Madrid | Sevilla | Cádiz |
|------|--------|---------|-------|
| 2020 | 0%     | 0%      | 0%    |
| 2021 | 5%     | -1%     | 2%    |
| 2022 | 10%    | 1%      | 5%    |
| 2023 | 13%    | 7%      | 13%   |
| 2024 | 22%    | 11%     | 19%   |
| 2025 | 31%    | 12%     | 23%   |

## Tabla 7 – Evolución del coste en alquiler desde 2015

| Año  | Madrid | Sevilla | Cádiz |
|------|--------|---------|-------|
| 2015 | 0%     | 0%      | 0%    |
| 2016 | 6%     | 6%      | 3%    |
| 2017 | 15%    | 11%     | 7%    |
| 2018 | 23%    | 17%     | 13%   |
| 2019 | 27%    | 24%     | 17%   |
| 2020 | 28%    | 28%     | 21%   |
| 2021 | 23%    | 24%     | 22%   |
| 2022 | 26%    | 28%     | 28%   |
| 2023 | 33%    | 32%     | 33%   |
| 2024 | 42%    | 36%     | 37%   |
| 2025 | 46%    | 40%     | 40%   |

## Tabla 8 – Evolución del coste en compra desde 2015

| Año  | Madrid | Sevilla | Cádiz |
|------|--------|---------|-------|
| 2015 | 0%     | 0%      | 0%    |
| 2016 | -1%    | 0%      | -1%   |
| 2017 | 1%     | -1%     | 0%    |
| 2018 | 13%    | 0%      | 4%    |
| 2019 | 21%    | 2%      | 7%    |
| 2020 | 21%    | 2%      | 9%    |
| 2021 | 24%    | 1%      | 10%   |
| 2022 | 28%    | 3%      | 13%   |
| 2023 | 31%    | 9%      | 21%   |
| 2024 | 38%    | 13%     | 26%   |
| 2025 | 45%    | 14%     | 30%   |



Viendo los datos y analizando los tiempos de recuperación de inversión, teniendo en cuenta los incrementos de precios tanto en alquiler como en compra, se pueden destacar los siguientes puntos:

- **Madrid**: Los precios están completamente inflados. Comprar ahora puede suponer una pérdida de capital, ya que los precios podrían verse afectados por una posible crisis económica o cambios de políticas. Esto se evidencia en las tablas 5, 6, 7 y 8, con un incremento superior al 40% tanto en compra como en alquiler. Además, el precio de compra tiene una diferencia del 5% por encima del alquiler, lo que puede prolongar aún más el tiempo de recuperación de la inversión.

  También es notable que muchas personas jóvenes que se mudaron a Madrid para estudiar o comenzar a trabajar están considerando regresar a sus ciudades de origen, ya que los precios actuales superan ampliamente su capacidad de ahorro. Aquellos que logran comprar, a menudo deben alejarse de las zonas donde solían vivir debido a la falta de asequibilidad.

  En mi opinión, actualmente no es el mejor momento para comprar una vivienda en Madrid como inversión, especialmente si ello implica utilizar todos los ahorros, ya que representa un gran riesgo según los datos analizados.

- **Sevilla**: Puede representar una mejor oportunidad para comprar vivienda. Desde 2015, el precio de la vivienda ha aumentado un 14%, mientras que el alquiler ha subido un 40%. Esto sugiere que, en caso de una bajada de precios en la compra, no será tan drástica como en Madrid. Además, los incrementos en el alquiler podrían estar relacionados con una preferencia local por alquilar, sin haber sufrido la misma presión externa que infló los precios en Madrid.

  La población de Sevilla tampoco ha crecido significativamente en los últimos años, ya que muchos jóvenes emigran para trabajar. Sería útil profundizar en datos como el crecimiento de la población con capacidad de compra o el número de nuevas viviendas construidas.

- **Algeciras**: Es la ciudad con un coste menor y con mejor retorno para la inversión en vivienda. Según los datos por número de habitaciones, el tiempo máximo de recuperación es de 22 años. Es una ciudad pequeña, con menor desarrollo industrial y con una población que a menudo migra por trabajo. Sin embargo, el coste de vida es significativamente menor, lo que puede representar una ventaja competitiva para la inversión.

## **7. Próximos pasos**

- Ampliar el análisis a más ciudades.
- Concretar la evolución del precio por ayuntamientos y ciudades.
- Elaborar el informe en Power BI.
- Explorar nuevas metodologías para automatizar el proceso.

## **8. Contribuciones**
Si deseas contribuir a este proyecto, puedes enviar sugerencias a través de:
- **LinkedIn:** [www.linkedin.com/in/jacobo-pérez-ferreira-0937905b](www.linkedin.com/in/jacobo-pérez-ferreira-0937905b)
- **Email:** jacoboferreira91@gmail.com
