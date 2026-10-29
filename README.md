# Detección de olas de calor y tendencias térmicas en Chile

Análisis de temperaturas diarias (2012) de estaciones meteorológicas chilenas, automatizado con funciones reutilizables en Python.

## Qué incluye
- **Limpieza y preparación**: índice temporal a partir de año/mes/día, tipado, deduplicación y reporte de datos faltantes.
- **Funciones utilitarias**: rango térmico diario, clasificación de días (frío / templado / caluroso) y cuantiles mensuales por estación.
- **Detección de olas de calor**: eventos de ≥ 3 días consecutivos sobre el percentil 90 mensual de cada estación, con inicio, fin y duración, más un ranking Top-10 por severidad y duración.
- **Matriz calendario** día × mes de olas de calor (Temuco).
- **Correlación de Pearson** entre olas de calor, latitud y altitud.
- **Tendencia anual** por estación con `numpy.polyfit` (estaciones con mayor calentamiento y enfriamiento).
- **Visualizaciones**: series TMín/TMáx, medias mensuales con barras de error y días extremos (P99).

## Estructura
```
heatwave_temperature_analysis.ipynb
temperaturasDiariasPorEstaciones2012.csv
```

**Stack:** Python · pandas · NumPy · Matplotlib · Seaborn
