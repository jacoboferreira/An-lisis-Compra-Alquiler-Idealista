# **Análisis de la rentabilidad en la compra y venta de pisos**

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

_(Aquí puedes incluir los hallazgos principales del análisis)_

## **7. Próximos pasos**

- Ampliar el análisis a más ciudades.
- Concretar la evolución del precio por ayuntamientos y ciudades.
- Elaborar el informe en Power BI.
- Explorar nuevas metodologías para automatizar el proceso.

## **8. Contribuciones**

Si deseas contribuir a este proyecto, puedes enviar sugerencias o mejoras a través de [incluir método de contacto o repositorio].
