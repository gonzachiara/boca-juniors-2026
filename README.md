# 🏟️ Análisis de Rendimiento Deportivo — Boca Juniors 2026

**Proyecto de análisis end-to-end sobre la temporada 2026 de Boca Juniors.**  
Recolección de datos desde múltiples fuentes públicas, modelado predictivo, scoring compuesto de jugadores y dashboard interactivo en Power BI.

---

## 📌 Objetivo

Construir un sistema de análisis completo de la temporada 2026 de Boca Juniors que permita:
- Evaluar el rendimiento ofensivo y defensivo del equipo
- Modelar la probabilidad de goles con datos reales de xG
- Rankear jugadores por posición mediante un scoring compuesto
- Visualizar todos los indicadores en un dashboard de 10 páginas

---


---

## 🔍 Fuentes de datos

Datos recolectados y consolidados manualmente desde más de 10 fuentes públicas:

| Fuente | Datos obtenidos |
|---|---|
| FBref / StatsPerform | xG, estadísticas de jugadores, Goal Log |
| Sofascore | Minutos jugados, ratings |
| Transfermarkt | Valor de mercado, transferencias |
| FootyStats / FotMob | Resultados, odds |
| Wikipedia | Información de plantilla |

> ⚠️ Limitaciones documentadas: estadísticas de porteros estimadas desde promedios de liga; dataset de transferencias incluye solo llegadas; datos del cuerpo técnico divididos entre ciclo Úbeda (base principal) y Arruabarrena (preliminar).

---

## ⚙️ Metodología

### 1. Recolección y limpieza
- Consolidación de 22 tablas estructuradas con claves únicas (`match_id`, `player_id`)
- Resolución de inconsistencias entre fuentes (fuente autoritativa: FBref Goal Log)
- Validación cruzada de resultados y estadísticas

### 2. Modelo predictivo de goles
- Distribución de Poisson calibrada con datos reales de xG por partido
- Predicción de resultados con probabilidades para victoria local, empate y victoria visitante

### 3. Scoring compuesto de jugadores
- Normalización MinMax (0–1) de métricas clave por posición
- Ponderación de variables según relevancia táctica
- Output: ranking, tabla comparativa y visualizaciones

### 4. Dashboard Power BI
Modelo de datos en **esquema estrella** con claves subrogadas reales.  
10 páginas: Visión Ejecutiva · Rendimiento · Análisis Ofensivo · Jugadores · Porteros · Disciplina · Lesiones · Mercado · Cuerpo Técnico · Comparación Internacional

---

## 📊 Hallazgos principales

- Boca rinde **mejor de visitante que de local** — resultado contra-intuitivo documentado con datos
- **~1/3 de los goles** se convirtieron después del minuto 75
- **Merentiel y Bareiro** lideran en xG/90 entre los delanteros
- **Leandro Paredes** lidera en pases clave y grandes chances creadas
- Partido vs Cruzeiro (visitante): **cero remates al arco**

---

## 🛠️ Herramientas

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)

- **Python:** pandas, numpy, matplotlib, scipy
- **Modelado:** distribución de Poisson, normalización MinMax
- **BI:** Power BI Desktop, DAX básico, Power Query, esquema estrella
- **Datos:** recolección manual, limpieza y consolidación desde múltiples fuentes

---

## 📁 Dataset completo

Los 22 archivos CSV están disponibles en Google Drive:  
🔗 [Acceder al dataset](https://drive.google.com/drive/folders/1u_6mNywMOZo-2gFCx_hF-fW6WptoycYR)

---

## 👤 Autor

**Gonzalo Chiaravalle**  
[LinkedIn](https://www.linkedin.com/in/gonzalochiaravalle) · [GitHub](https://github.com/gonzachiara)  
gonzachiaravalle@gmail.com
