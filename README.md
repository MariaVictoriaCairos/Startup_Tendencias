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
- Startup_Name es la clave y tiene valores únicos 
- Las columna de texto Industry y Country están correctas, no requieren transformación de datos.
- Las columnas numericas se formaten con separador de miles para facilitar la lectura y validar. Las columnas numericas son correctas.
- Se incorpora la columna "Ranking by Value" para categorizar las startup por su valoración.
- Se incorpora la columna "Old" para validar la relación de antiguedad con el nivel de inversión.

## 🚀 Resultados
Conclusiones y hallazgos clave del análisis.

## 🛠️ Herramientas
Tecnologías y software utilizados en el proyecto.

## 📑 Referencias
Fuentes de información y bibliografía utilizada.



