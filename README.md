# 📊 Conjunto de Datos de Crecimiento de Startups y Datos de Inversión

## 📌 Descripción
Este conjunto de datos contiene **5.000 registros** de crecimiento de startups y datos de inversión en varias industrias. Proporciona información sobre las tendencias de financiación, la valoración y la actividad de los inversores para nuevas empresas a nivel mundial. 

## 🎯 Objetivo

El objetivo del estudio es analizar el ecosistema de las startup y predicciones sobre tendencias de inversión. 

---
## 📂 Características del Conjunto de Datos

| **Nombre de la columna** | **Descripción** |
|----------------------|------------------------------------------------|
| **Startup Name** | Nombre de la startup |
| **Industry** | Sector industrial (por ejemplo, IA, Fintech, HealthTech, etc.) |
| **Funding Rounds** | Número de rondas de financiación recibidas |
| **Investment Amount (USD)** | Inversión total recibida en USD |
| **Valuation (USD)** | Valoración estimada de la empresa en USD |
| **Number of Investors** | Total de inversores que respaldan la startup |
| **Country** | País donde se basa la startup |
| **Year Founded** | Año en que se fundó la startup |
| **Growth Rate (%)** | Porcentaje de tasa de crecimiento anual |
| **Ranking by value** | Clasificación de la startup de acuerdo a niveles de valoracion de las startup |
| **Old** | Años desde la creación de la startups |
---

A los datos de origen se le añaden dos columnas, ranking by value y Old. 
La clasificación de las startups según su valor se basa en su valuación de mercado. A continuación, te comparto las categorías más utilizadas para clasificar las startups según su valoración:

- Cockroach 🪳
Valuación: Menos de $10 millones
Son startups en etapas muy tempranas, resistentes y enfocadas en la supervivencia con poco capital.

- Pony 🐎
Valuación: Entre $10 y $100 millones
Startups en crecimiento con tracción y potencial de escalabilidad.

- Centaur 🏇
Valuación: Entre $100 y $999 millones
Empresas con crecimiento sólido, cercanas a alcanzar el estatus de unicornio.

- Unicorn  🦄
Valuación: Más de $1,000 millones ($1B)
Startups privadas con un alto crecimiento y gran potencial de disrupción en su industria.

- Decacorn 🦄✨
Valuación: Más de $10,000 millones ($10B)
Empresas privadas con crecimiento exponencial y dominantes en su sector.

- Hectocorn o Superunicorn 🦄🔥
Valuación: Más de $100,000 millones ($100B)
Startups extremadamente exitosas, con presencia global y que pueden rivalizar con empresas establecidas en el mercado.



## 📂 Estructura del Proyecto

```bash
.
├── Datos # Carpeta de los datos del proyecto
│   ├── Tendencias_Startups.csv # Archivo final para el análisis
│   ├── Tendencias_Startups.xlsx # Archivo de Transformación
│   └── startup_growth_investment_data.csv # Datos originales
├── Excel
└── README.md

3 directories, 4 files
```

## 💡 Casos de Uso

✅ **Análisis de tendencias de inversión** - Analizar las tendencias de financiación y el interés de los inversores en todas las industrias.

✅ **Predicción de la valoración de startups** - Entrenar modelos de aprendizaje automático para predecir las valoraciones basadas en las rondas de financiación.

✅ **Investigación de mercado** - Identificar industrias en auge y ecosistemas de startups exitosos.

✅ **Toma de decisiones de inversores** - Ayudar a capitalistas de riesgo y a inversores ángeles a tomar decisiones basadas en datos.

---
## 🔎 Posibles Exploraciones

- 📈 **¿Qué industrias atraen más fondos?**
- ⏳ **¿Cómo crece la valoración de las startups con el tiempo?**
- 🌍 **¿Qué países tienen las startups de más rápido crecimiento?**
- 🔗 **¿Cuál es la correlación entre las rondas de financiación y la tasa de crecimiento?**

📢 Este conjunto de datos se genera sintéticamente, pero sigue patrones de inversión realistas para apoyar la investigación y el análisis. 🚀

## 🔎 Avances del proyecto por sesiones
### Sesión 1
- Creación del repositorio
- Documentación inicial en el Readme
- Carga de datos
- Análisis Iniciál de cada columna de los datos
- Investigación sobre clasificaciónes de las startups para determinar relaciones con los niveles de inversion.

### Sesión 2
Sesión de transformación de datos. Se valida cada una de las columnas
- Startup_Name es la clave y tiene valores únicos. No hay repetición de datos. 
- Las columna de texto Industry y Country están correctas, no requieren transformación de datos.
- Las columnas numéricas de monedas se formaten con separador de miles para facilitar la lectura y validar. Estan columnas se tranforman en millares de $ por no ser representativo en el análisis los valores menores que el millar. 
- El resto de columnas numéricas están correctas y se mantinen iguales.
- Se incorpora la columna "Ranking by Value" para categorizar las startup por su valoración.
- Se incorpora la columna "Old" para validar la relación de antiguedad con el nivel de inversión.

### Sesión 3
- Se crea en la carpeta excel el archivo donde se van a analizar los datos y se cresrá el dashboard.
- Se cargan los datos .csv transformados en la sesión 2
- Se realiza el análisis descriptivo numéricos.
- Se realiza el análisis categórico.


## 🚀 Análisis de los datos
Se inicia el análisis descriptivo numérico de las columnas. A continuación se comenta cada una de ellas.
- Funding Rounds. La moda es 1, lo que nos indica que la mayoría de las startups han conseguido solo una ronda de inversión. El promedio es 5 y la mediana es 6, lo que indica que algunas han logrado levantar más rondas que la media. La variabilidad en el número de rondas de financiamiento no es extremadamente alta (desviación estándar de 3).
La distribución es simétrica y achatada, lo que significa que los valores extremos no tienen un impacto significativo.
- Investment Amount (K USD) : Para el análisis de los niveles de inversión se utilizarón rangos de inversión. La media y la mediana se encuentran en el mismo rango de datos, con inversiones entre 200 y 300 mil millones de dolares, con una variación baja entre ambos. Aunque la inversión media es 222 mil K USD, la mediana es menor (215 mil K USD) y la moda mucho menor (27 mil K USD), lo que indica que hay muchas startups que reciben importes bajos de inversión, mientras que unas pocas han conseguido cifras altas. 
La distribución es simétrica y plana, lo que significa que no hay sesgos significativos ni una concentración extrema de valores altos o bajos.
Los datos sugieren que el ecosistema de inversión tiene startups que levantan pequeñas rondas de capital con frecuencia, pero algunas pocas logran inversiones mucho más altas.
- Valuation (k USD): se observa una distribución sesgada. La mayoría de las startups tienen valoraciones relativamente bajas, pero unas pocas con valoraciones extremadamente altas están influyendo en la media.
La dispersión es alta. La diferencia entre las valuaciones más bajas y más altas es enorme, lo que sugiere una gran desigualdad en el ecosistema de startups.
Debido a la curtosis y asimetría, es probable que haya unas pocas startups tipo “unicornio” o incluso “decacornio” que estén inflando el promedio.
- Number of Investors. El número de inversores por startup está muy equilibrado.  Como la media (26), mediana (25) y moda (21) están relativamente cercanas, se puede concluir que la distribución del número de inversionistas por startup es bastante estable.
Aunque hay startups con muy pocos inversionistas y otras con el máximo de 50, la mayoría se encuentra en un rango intermedio.
Hay pocos valores extremos. La curtosis negativa indica que la distribución no tiene demasiados valores atípicos, lo que sugiere que no hay startups con cantidades extremadamente altas o bajas de inversionistas en comparación con el resto.
- Year Founded. La evolución en el tiempo ha sido estable. La mayoría de las startups han sido fundadas en los últimos 23 años, con una concentración promedio en 2012. Al graficar agrupados por cada 5 años se observa que en los últimos 5 años hay una bajada importante del número de startup. el comienzo de esta bajada fue el año de la pandemia y no ha dejado de bajar.
Es interesante que 2001 sea el año más común de fundación, lo que podría coincidir con un auge particular en la creación de startups después del colapso de la burbuja de las puntocom.
No hay sesgo evidente, lo que sugiere que el ecosistema de startups ha crecido de manera estable en el tiempo.
- GRowth rate %. Aunque la media es 9290%, la desviación estándar es 6012%, lo que indica que algunas startups han experimentado crecimientos exponenciales, mientras que otras tienen valores significativamente más bajos.
La moda de 1075% sugiere que, aunque algunas startups crecen a tasas extremadamente altas, la mayoría tiene un crecimiento mucho menor.
Los datos tienen una distribución equilibrada. No hay sesgo extremo en los datos, lo que indica que el crecimiento está distribuido de manera relativamente uniforme entre startups de bajo y alto crecimiento.
- Old. La antiguedad tiene un comportamiento igual a los años de fundación.

Los datos tienen tres columnas categóricas las cuales se analizan a continuación:

- Industry: categorizadas por tipo de industria destaca Healthtech. Es interesante cruzar este datos por país para encontrar conecentraciones de industria con ecosistemas maduros de inversión. 
- Country: No hay una diferencia extrema entre los países en términos de startups, pero Australia destaca como el país con mayor cantidad.
Se observa una distribución equilibrada, con algunos países levemente por encima o por debajo del promedio.
Es interesante que algunos mercados emergentes como Brasil e India se encuentren en posiciones destacadas, lo que sugiere un ecosistema de startups en crecimiento.
- Ranking for Value: los datos corresponden solo a la categoria de Superunicorn. Seria interesante para profundizar incorporar datos con fases más tempranas de inversión.

No se realiza análisis Temporal de los datos por no tener campos relacionados con fechas. hay un campo relacionado con fecha que se analizó en el apartado de análisis numérico.

## 🚀 Resultados
Conclusiones y hallazgos clave del análisis.

## 🛠️ Herramientas
Tecnologías y software utilizados en el proyecto.

## 📑 Referencias
Fuentes de información y bibliografía utilizada.



