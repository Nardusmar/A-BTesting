# 🧪 Experimento A/B – Landing Page (Ecommerce)

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?logo=pandas)
![SciPy](https://img.shields.io/badge/SciPy-Estad%C3%ADstica-8CAAE6?logo=scipy)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualizaci%C3%B3n-3776AB)
![Status](https://img.shields.io/badge/Status-Completado-brightgreen)

## 📌 Descripción del proyecto

Análisis de un experimento A/B realizado sobre dos versiones de una landing page de ecommerce
(**A** y **B**), con el objetivo de determinar cuál versión genera mayor conversión y mayor
gasto promedio por usuario, y así respaldar con evidencia estadística una decisión de negocio.

## 🎯 Objetivos

- Comparar el **gasto promedio** por usuario convertido entre la página A y B
- Comparar la **tasa de conversión** entre ambas versiones
- Evaluar la relación entre **fuente de tráfico** y conversión
- Evaluar la relación entre **tipo de usuario** (nuevo/recurrente) y conversión
- Traducir los resultados en una **recomendación de negocio** clara

## 🗂️ Fuente de los datos

- **Archivo:** `landing_experiment.csv`
- **Registros:** 40,000 usuarios, 9 columnas, sin valores nulos
- **Variables:** `user_id`, `date`, `landing` (A/B), `region`, `dispositivo`, `traffic_source`,
  `user_type`, `converted`, `gasto`

## 🛠️ Herramientas utilizadas

| Herramienta | Uso |
|---|---|
| Python (Pandas, NumPy) | Carga, limpieza y validación de datos |
| SciPy (`ttest_ind`, `chi2_contingency`) | Pruebas de hipótesis estadísticas |
| Matplotlib / Seaborn | Visualización de resultados |
| Jupyter Notebook | Desarrollo del análisis completo |

## 🔍 Metodología

1. **Carga y validación de datos**: revisión de tipos, nulos, duplicados y balance del grupo A/B (50/50)
2. **Prueba T de Welch**: comparación del gasto promedio entre grupos con varianzas distintas
3. **Prueba Chi-cuadrada**: comparación de tasas de conversión, y asociación con fuente de tráfico
   y tipo de usuario
4. **Visualización**: gráficos de conteo y proporción para reforzar los hallazgos estadísticos
5. **Síntesis ejecutiva**: traducción de resultados en recomendaciones accionables

## 📈 Hallazgos clave

- 💰 **Gasto promedio**: la página B genera un gasto promedio significativamente mayor por
  usuario convertido que la página A (prueba T de Welch, p < 0.001)
- 🎯 **Tasa de conversión**: la página B convierte al **16.0%** de los usuarios frente a
  **12.6%** de la página A — una mejora de **3.4 puntos porcentuales** (Chi-cuadrada, p < 0.001)
- 🌐 **Fuente de tráfico**: Email (15.0%) y Ads (14.7%) son los canales más efectivos; Organic
  trae el mayor volumen de usuarios pero la tasa de conversión más baja (13.8%)
- 👤 **Tipo de usuario**: usuarios nuevos (14.5%) y recurrentes (14.1%) convierten de forma
  muy similar — el tipo de usuario no es un factor determinante

## 💡 Recomendaciones de negocio

- Implementar la **página B** como versión definitiva: supera a la A tanto en conversión como en gasto
- Priorizar campañas de **Email y Ads** sobre tráfico orgánico para maximizar conversiones
- No segmentar la estrategia por tipo de usuario, dado que nuevos y recurrentes se comportan de forma similar

## 📁 Estructura del repositorio

```
experimento-ab-landing-ecommerce/
├── data/
│   └── landing_experiment.csv
├── notebooks/
│   └── experimento_ab_landing_page.ipynb
├── img/
├── requirements.txt
└── README.md
```

## ▶️ Cómo reproducir este análisis

```bash
git clone https://github.com/tu-usuario/experimento-ab-landing-ecommerce.git
cd experimento-ab-landing-ecommerce
pip install -r requirements.txt
jupyter notebook notebooks/experimento_ab_landing_page.ipynb
```

## 👤 Autor

**Tu Nombre**
[LinkedIn](https://linkedin.com/in/tu-usuario) · [Portafolio](https://tu-portafolio.com)
