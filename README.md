# 📊 Conjunto de Datos de Crecimiento de Startups y Datos de Inversión

## 📌 Descripción
Este conjunto de datos contiene **5.000 registros** de crecimiento de startups y datos de inversión en varias industrias. Proporciona información sobre las tendencias de financiación, la valoración y la actividad de los inversores para nuevas empresas a nivel mundial. 

## 🎯 Objetivo

El objetivo principal de este estudio es **analizar el ecosistema de startups y las tendencias de inversión** a partir de un enfoque descriptivo y exploratorio basado en datos reales.

El análisis busca responder a los siguientes objetivos específicos:

✅ **Análisis de tendencias de inversión**  
Examinar el comportamiento de la financiación en startups, identificando patrones en el número de rondas, montos invertidos y participación de inversores en distintas industrias y regiones.

✅ **Investigación de mercado**  
Detectar industrias emergentes y ecosistemas geográficos con alto dinamismo en la creación y crecimiento de startups, identificando focos de innovación y tracción de capital.

✅ **Soporte a la toma de decisiones para inversores**  
Proveer información útil para **capitalistas de riesgo, fondos de inversión y business angels**, ayudándoles a tomar decisiones estratégicas basadas en datos sobre dónde invertir, en qué tipo de startup, y con qué expectativas de retorno.

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
| **ROI (%)** | Indica el rendimiento de la inversión |
| **Average investment per round** | es el promedio de inversión por ronda, indica la cantidad de dinero que recibe en promedio en cada ronda|
|**Growth Category** | Categoría creada para distinguir startup con valores extremos de crecimiento de startup con crecimiento típico.|
---
 
A los datos de origen se les añaden 4 columnas, ranking by value y Old, average investment per round y ROI (%). 

La clasificación de las startups según su valor se basa en su valuación de mercado. A continuación, comparto las categorías más utilizadas para clasificar las startups según su valoración:

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
│   ├── Tendencias_Startup_DB.xlsx  #Archivo con los dashboard finales
│   ├── Tendencias_Startup_EDA.xlsx # Archivo para el análisis descriptivo y bivariado
└── README.md # Informe  del análisis de datos

3 directories, 6 files
```

## 🔎 Avances del Proyecto por Sesiones

### 🧭 Sesión 1: Inicio del Proyecto
- Creación del repositorio y estructura base del proyecto.
- Documentación inicial en el archivo `README.md`.
- Carga de la base de datos original.
- Primer análisis exploratorio de cada columna.
- Investigación sobre clasificaciones de startups según su valoración, para vincularlas con los niveles de inversión y crecimiento.

---

### 🔧 Sesión 2: Transformación y Preparación de Datos
- Validación de columnas clave:
  - `Startup_Name` identificada como clave primaria sin duplicados.
  - Columnas de texto (`Industry` y `Country`) revisadas y aceptadas sin necesidad de transformación.
- Columnas numéricas de inversión fueron formateadas con separador de miles para mejorar legibilidad.
- Los Valores monetarios fueron transformados a **millares de dólares (K USD)** para facilitar el análisis y reducir ruido de cifras menores.
- Columnas numéricas adicionales validadas y mantenidas sin modificaciones.
- Incorporación de nuevas columnas:
  - `Ranking by Value`: clasificación de startups según nivel de valoración.
  - `Old`: cálculo de la antigüedad de la startup (años desde su fundación).

---

### 📊 Sesión 3: Análisis Exploratorio
- Creación del archivo principal de trabajo en Excel dentro de la carpeta `/Startup_Tendencias/`.
- Carga del dataset `startup_growth_investment_data.csv` previamente transformado.
- Ejecución del análisis descriptivo para variables numéricas.
- Revisión y análisis de variables categóricas.

---

### 🔗 Sesión 4: Correlaciones y Segmentación
- Se crea el archivo `Tendencias_Startup_EDA.xlsx` y se le carga `Tendencias_Startups.csv`
- Análisis de correlaciones entre variables clave (e.g., inversión, ROI, valuación).
- Clasificación de startups en dos categorías:
  - **Typical Growth**
  - **High Growth**
- Creación de dos nuevas tablas para el análisis independiente de cada segmento.

---

### 📈 Sesión 5: Visualización y Conclusiones
- Se crea el archivo `Tendencias_Startup_DB.xlsx`
- Se copian las tablas de datos  de `Tendencias_Startup_EDA.xlsx`
- Diseño y construcción de dashboards segmentados por tipo de startup.
- Análisis final de resultados a partir de visualizaciones.
- Redacción del informe README.md con conclusiones, recomendaciones y tendencias de inversión detectadas.


## 🚀 Análisis de los Datos

### 📊 Análisis Descriptivo

El análisis comenzó con un estudio descriptivo de las variables numéricas, seguido por una revisión de las variables categóricas. A continuación, se detallan los principales hallazgos:

#### 🔸 Funding Rounds
- La **moda es 1**, lo que indica que la mayoría de las startups han recibido solo una ronda de inversión.
- La **media es 5** y la **mediana es 6**, lo que sugiere que algunas startups han levantado múltiples rondas, elevando el promedio.
- La distribución es **simétrica y ligeramente achatada** (curtosis negativa), con una **desviación estándar de 3**, lo que indica una variabilidad moderada.

#### 🔸 Investment Amount (K USD)
- La inversión promedio es de **222K USD**, y la mediana es **215K USD**, con una moda significativamente más baja (**27K USD**), lo que indica una alta concentración de startups con inversiones pequeñas.
- La distribución es **simétrica y plana**, sin sesgos marcados, pero con evidencia de **outliers** que elevan el promedio.
- El análisis por rangos revela que muchas startups levantan capital de forma limitada, mientras unas pocas concentran los montos más altos.

#### 🔸 Valuation (K USD)
- Se observa una **alta asimetría positiva**, con algunas startups alcanzando valoraciones extremadamente altas (potenciales unicornios/decacornios).
- La **dispersión es muy elevada**, y la diferencia entre el mínimo y el máximo es abismal.
- Estas valuaciones extremas sesgan fuertemente la media, y se comportan como **outliers significativos** en el análisis global.

#### 🔸 Number of Investors
- La **media (26)**, **mediana (25)** y **moda (21)** están muy cercanas, lo que indica una **distribución equilibrada**.
- Aunque hay startups con tan solo 1 inversor y otras con hasta 50, la mayoría se concentra en un rango intermedio.
- La curtosis negativa sugiere **poca presencia de valores extremos**, haciendo de esta variable una de las más estables del conjunto.

#### 🔸 Year Founded
- El **año promedio de fundación es 2012**, con startups distribuidas mayoritariamente en los últimos 23 años.
- El año **2001 aparece como la moda**, posiblemente asociado a un auge post-burbuja puntocom.
- En los últimos 5 años se observa una **disminución en la cantidad de startups fundadas**, iniciando desde la pandemia.
- La distribución es simétrica y refleja una evolución estable del ecosistema emprendedor en el tiempo.

#### 🔸 Growth Rate (%)
- Aunque la **media es 9,290%**, la **desviación estándar es 6,012%**, lo que evidencia una **variabilidad muy alta**.
- La moda es **1,075%**, lo que indica que la mayoría de startups tienen crecimientos más moderados que el promedio.
- La distribución es **equilibrada** sin sesgo marcado, pero con una cola larga hacia startups de crecimiento exponencial.

#### 🔸 Old (Edad en años)
- Muestra un comportamiento similar a *Year Founded*.
- Puede ser útil para evaluar cuánto tiempo ha tardado una startup en alcanzar su nivel de valuación actual.
- Se recomienda su uso combinado con *Industry* para identificar trayectorias más exitosas por sector.

#### 🔸 ROI (%)
- El análisis del **ROI** muestra una gran cantidad de **outliers que distorsionan la media**.
- La **mediana se sitúa en 37.148%**, mientras que los valores extremos elevan significativamente la media.
- Un análisis de distribución revela que hay startups con ROI elevado tanto jóvenes como maduras.
- Por su valor estratégico, se decide **no eliminar estos outliers**, y mantenerlos para análisis relacional con otras variables categóricas.

#### 🔸 Average Investment per Round (K USD)
- Gran amplitud entre mínimo (**5K USD**) y máximo (**488K USD**) indica un rango muy heterogéneo.
- Estas diferencias podrían atribuirse a factores como la **industria**, la **etapa de desarrollo** o el **modelo de negocio**.

---

### 🧷 Variables Categóricas

#### 🏭 Industry
- Se destacan sectores como **HealthTech**, con alta representación en el dataset.
- Recomendable cruzar esta variable con *Country* para identificar ecosistemas sectoriales más maduros.

#### 🌍 Country
- Distribución equilibrada entre países, con **Australia liderando** en número de startups.
- Países emergentes como **Brasil e India** destacan, reflejando el crecimiento de nuevos polos de innovación.
- Útil para estudios geoestratégicos y análisis de mercados emergentes.

#### 🏅 Ranking for Value

- Esta variable contiene únicamente startups clasificadas en la categoría **Superunicorn**, lo que limita su capacidad analítica al no ofrecer variabilidad entre casos.
- Aunque puede ser útil como indicador de prestigio o madurez extrema, **su valor constante impide comparaciones internas** o segmentaciones por etapa de crecimiento.
- Por este motivo, se **descartó del análisis exploratorio principal**.
- Se recomienda considerar la inclusión de categorías más amplias (por ejemplo, *Cockroach*, *Pony*, *Centaur*, *Unicorn*, etc.) en futuras versiones del dataset para capturar mejor la evolución del ciclo de inversión y ofrecer una perspectiva más completa sobre las fases de crecimiento del ecosistema startup.

---

### ⏱️ Análisis Temporal

- La variable *Year Founded* fue utilizada como aproximación temporal y se abordó en el análisis numérico. Se utilizó para generar la columna Age, edad de la startup.


### 🧮 Tratamiento de Valores Extremos (Outliers)

Durante el análisis se identificaron startups con métricas de crecimiento **extraordinariamente altas**, las cuales se comportan como **valores atípicos (outliers)**. Estos casos, si no se tratan adecuadamente, pueden distorsionar los promedios, las correlaciones y las visualizaciones generales del conjunto de datos.

Con el fin de **mejorar la precisión del análisis** y obtener una visión más representativa del mercado, se implementó una estrategia de segmentación basada en el desempeño en métricas clave de crecimiento.

#### 🔀 Categorización de Startups:

| **Categoría**        | **Descripción** |
|----------------------|------------------|
| **High-Growth**      | Startups que presentan métricas de crecimiento excepcionalmente elevadas, muy por encima del comportamiento típico del conjunto. Incluyen niveles extremos en valuación, ROI o inversión, y actúan como outliers. Se analizan por separado para evitar sesgos en las tendencias generales. |
| **Typical Growth**   | Startups cuyos indicadores se mantienen dentro de rangos normales. Representan la mayoría del universo analizado y permiten identificar patrones de comportamiento promedio y más estables del mercado. |

#### 📌 Criterios de Segmentación para High-Growth Startups:

Se consideraron valores extremos (outliers) aquellos que superan los siguientes umbrales:

- **Valuation (K USD)** por startup > **2,000,000,000**
- **ROI por inversión (%)** > **500,000**
- **Average Investment per Round (K USD)** > **100,000**

Estas reglas permiten separar claramente las startups de comportamiento fuera de norma y analizarlas bajo una lógica independiente, sin comprometer la calidad estadística del análisis global.

---

✅ Esta segmentación facilita un análisis más **robusto y equilibrado**, permitiendo:
- Comprender las tendencias generales sin sesgos.
- Profundizar por separado en el impacto y comportamiento de startups con potencial disruptivo extremo.


### Análisis bivariado:
Para identificar posibles patrones de inversión, se realizó un análisis bivariado mediante una **matriz de correlación** entre variables clave los datos. Los resultados fueron: 
| Correlation | Variables Analizadas de interés |
|-------------|--------------------|
| **-0.46**   | Average Number of Investors + Investment per Round (K USD) |
| **-0.32**   | Average Number of Investors + Average Investment per Round (K USD) |
| **0.13**    | Valuation (K USD) + ROI (%) |
| **-0.11**   | Investment Amount (K USD) + ROI (%) |

- Las correlaciones negativas entre el número de inversores y el monto invertido por ronda sugieren que, en promedio, a mayor número de inversores, menor es la inversión individual.
- La correlación positiva entre valoración y ROI es leve, pero indica una posible tendencia donde startups con mayor valoración podrían tener retornos más altos. 


---

## 🚀 Resultados Conclusiones y hallazgos clave del análisis.

El análisis de patrones y tendencias de inversión compara startups clasificadas por su nivel de crecimiento en dos grupos: **Typical Growth** (crecimiento típico) y **High Growth** (alto crecimiento), con base en los datos de inversión, ROI, valuación y perfil de madurez.

---

### 1. 🟦 Análisis de Startups Típicas (Typical Growth)

Las startups con crecimiento típico representan el **70%** del total. Funcionan como la base para identificar comportamientos promedio en inversión y retorno.

#### Principales hallazgos:

- **Inversión promedio por ronda:** ~$205K USD.
- **ROI promedio:** **100%**.
- **Valuación promedio:** ~$8.4 Mill K USD.
- **Edad promedio:** **13 años**.
- **Número promedio de inversores:** **30**.
- **Industrias dominantes:** Blockchain, E-commerce, HealthTech.

📌 Estas startups muestran un crecimiento moderado y estable, con perfiles de inversión conservadores y bajo riesgo.

#### ✅ Valor para el Inversionista

Este perfil resulta atractivo para **inversionistas que buscan rentabilidad moderada con bajo riesgo**, ideal para estrategias diversificadas o fondos de crecimiento controlado. Permite una planificación financiera más predecible y facilita la evaluación de desempeño con base en promedios históricos del mercado.

#### ✅ Conclusión Estratégica

Las startups de crecimiento típico (*Typical Growth*) representan opciones de inversión más seguras, con proyecciones predecibles y entornos competitivos más maduros. Son especialmente atractivas para inversores que buscan un retorno sostenible a mediano o largo plazo, o que desean diversificar portafolios que ya incluyen activos más agresivos.

---

### 2. 🟥 Análisis de Startups de Alto Crecimiento (High Growth)

Constituyen el **30%** de la base y se caracterizan por un desempeño sobresaliente en métricas de inversión y rentabilidad.

#### Principales hallazgos:

- **Inversión promedio por ronda:** ~$261 K USD.
- **ROI promedio:** **~799%**.
- **Valuación promedio:** ~$17.3 Mill K USD.
- **Edad promedio:** **13 años**.
- **Número promedio de inversores:** **15**.
- **Industrias dominantes:** HealthTech, SaaS, E-commerce.

📌 Estas startups representan oportunidades de inversión con alto potencial de retorno y escalabilidad, aunque con mayor volatilidad.

#### ✅ Valor para el Inversionista

Este perfil resulta ideal para **inversionistas que buscan alto rendimiento** y están dispuestos a asumir mayor riesgo en busca de **crecimiento exponencial**. Las startups High Growth son especialmente atractivas para fondos de venture capital, ángeles inversionistas o portfolios que priorizan disrupción, escalabilidad y retorno acelerado.  
La alta inversión por ronda y los elevados ROI sugieren un entorno competitivo donde el timing y la selección sectorial son clave.

---

#### ✅ Conclusión Estratégica

Las High Growth startups representan **vehículos de inversión con gran potencial de rentabilidad**, especialmente en sectores emergentes como HealthTech, SaaS, E-commerce. A pesar de su mayor volatilidad, ofrecen oportunidades de gran escala en mercados globales.  
Son recomendadas para inversionistas que buscan **ganancias rápidas, penetración en sectores disruptivos** y capacidad de escalar a múltiples rondas de inversión. En el contexto actual, reflejan claramente hacia dónde se está desplazando el capital de riesgo global.

---

## 3. 📋 Cuadro Comparativo: Typical vs. High Growth Startups

| **Indicador**                  | **Typical Growth**                 | **High Growth**              |
|--------------------------------|------------------------------------|------------------------------|
| Participación total            | 70%                                | 30%                          |
| Inversión por ronda (K USD)    | 205.429                            | 261.261                      |
| ROI promedio (%)               | 100.067                            | 799.009                      |
| Valoración promedio (Mill USD) | 8.427.954                          | 17.320.835                   |
| Edad promedio (años)           | 13                                 | 13                           |
| Nº de inversores promedio      | 30                                 | 15                           |
| Principales sectores           | Blockchain, E-commerce, HealthTech | HealthTech, SaaS, E-commerce |

---

## 4. 📈 Conclusiones del Análisis

### 🔹 Startups de Crecimiento Típico
- Muestran un patrón de crecimiento **más estable y predecible**.
- A pesar de tener un **ROI promedio bajo**, mantienen una base sólida para estrategias de inversión seguras.
- Atraen una **base más amplia de inversionistas (30 en promedio)**, lo que puede reflejar mayor confianza o menor ticket por inversor.
- Se concentran en sectores que ya han alcanzado una etapa de madurez como **Blockchain, E-commerce y HealthTech**.
- Representan oportunidades para inversionistas interesados en **rendimientos constantes con menor exposición al riesgo**.

### 🔸 Startups de Alto Crecimiento
- Tienen un **ROI promedio significativamente mayor (799%)**, lo que demuestra un fuerte potencial de retorno.
- Aunque captan **más inversión por ronda**, lo hacen con **menos inversores (15 en promedio)**, lo que puede indicar operaciones más estratégicas o exclusivas.
- Su valoración promedio (**$17.3M USD**) es más del doble que la de las startups típicas (**$8.4M USD**), lo que refleja una mayor percepción de potencial, escalabilidad y atractivo de mercado por parte de los inversionistas.
- Están presentes principalmente en sectores innovadores como **HealthTech, SaaS y E-commerce**, apuntando a alto crecimiento y escalabilidad.
- Resultan más atractivas para inversionistas con un perfil más agresivo y enfoque en alto rendimiento.

---

## 5. 🧠 Patrones de Inversión y Tendencias

- Se observa una clara **correlación positiva entre el importe de inversión por ronda y el ROI**, especialmente en el grupo High Growth.
- El ecosistema de inversión muestra una **polarización entre estabilidad (Typical Growth)** y **rentabilidad acelerada (High Growth)**.
- Las **startups High Growth no necesariamente son más jóvenes**, lo que sugiere que el crecimiento exponencial no está limitado por la edad, sino por estrategia, sector e inversión.
- Sectores como **HealthTech y SaaS** emergen como motores de crecimiento, mientras que otros como **Blockchain** siguen dominando en las startups típicas.
- El **número de inversores** no determina el ROI, pero sí podría influir en la estructura de gobernanza y en la velocidad de toma de decisiones.

---


## 🧭 Sugerencias para Navegar el Dashboard

Para los usuarios del dashboard que analizan startups Typical Growth, recomendamos:

1. **Filtrar por industria** para detectar cuáles sectores muestran mejor eficiencia entre inversión y ROI dentro del grupo típico.
   - Ejemplo: ¿Fintech genera mejores retornos con menor inversión que E-commerce?

2. **Explorar por país o región** para identificar hubs estables de startups maduras.
   - Sugerencia: Comparar mercados como EE.UU. vs. Europa.

3. **Jugar con el filtro de edad de la startup** para detectar patrones entre madurez y rentabilidad.
   - Startups de 10+ años tienden a tener menor crecimiento, pero también menor riesgo.

4. **Observar la distribución de inversores**:
   - Menor número de inversores puede indicar oportunidades menos expuestas o con mayor concentración de control estratégico.

5. **Valorar el ROI en función del tamaño de inversión por ronda**:
   - Una ROI moderada con baja inversión puede ser más rentable que un ROI alto con inversión excesiva.


---
## 🛠️ Herramientas

**Tecnologías y software utilizados en el proyecto**

El análisis fue desarrollado en **Microsoft Excel**, utilizando funcionalidades estándar sin empleo de macros ni scripts automatizados. Se aplicaron herramientas clásicas de análisis descriptivo, filtrado y segmentación, así como tablas dinámicas para sintetizar la información.

- Se realizaron análisis descriptivo por columnas para explorar tendencias generales de métricas clave como inversión, ROI, valuación y edad de las startups.
- Para el análisis bivariado, se utilizó una **matriz de correlación** que permitió identificar relaciones entre variables como *Investment per Round*, *ROI*, *Startup Age* y *Valuation*.

### Limitaciones técnicas

- Las gráficas de correlación como **"Investment per Round vs ROI"** y **"Startup Age vs Valuation"** no pudieron ser representadas adecuadamente debido a limitaciones visuales y técnicas del entorno Excel.
- Aunque los **gráficos de dispersión** son la herramienta más apropiada para este tipo de relaciones, Excel presentó dificultades al construir representaciones limpias y funcionales en ese formato.
- Este mismo análisis, implementado en herramientas más robustas como **Power BI, Tableau o Python**, permitiría una visualización más clara, interactiva y detallada, facilitando la exploración de insights visuales.

🔍 A pesar de estas limitaciones, se logró extraer conclusiones relevantes y fundamentadas gracias al enfoque estructurado y la correcta interpretación estadística de los datos.


## 📑 Referencias

La base de datos utilizada para este proyecto fue obtenida de Kaggle:

- **Startup Growth and Investment Data**  
  Fuente: [https://www.kaggle.com/datasets/adilshamim8/startup-growth-and-investment-data](https://www.kaggle.com/datasets/adilshamim8/startup-growth-and-investment-data)

Esta fuente proporciona información detallada sobre crecimiento, inversión, valuación y otros indicadores clave del ecosistema de startups a nivel global.




