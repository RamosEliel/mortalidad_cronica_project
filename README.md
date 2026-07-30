# Mortalidad Prematura por Enfermedades Crónicas en Bogotá D.C. (2010–2025)

Segmentación de localidades y análisis de factores asociados a la mortalidad prematura
(30-70 años) por enfermedades crónicas, usando datos oficiales de la Secretaría de Salud.

## Contexto

¿Qué localidades de Bogotá tienen mayor mortalidad prematura por enfermedades crónicas, y
se relaciona con el régimen de seguridad social del fallecido? Los análisis de salud pública
en Colombia suelen publicarse como PDFs institucionales; este proyecto aplica segmentación
basada en datos para identificar patrones territoriales y demográficos.

## Fuente de datos

- Mortalidad Prematura por Enfermedades Crónicas — [Datos Abiertos Bogotá](https://datosabiertos.bogota.gov.co/dataset/mortalidad-prematura-por-enfermedades-cronicas-en-bogota)
- 164,840 registros, 2010–2025

## Metodología

1. EDA y limpieza (encoding, exclusión de año incompleto, categorías agregadas)
2. Distribuciones por causa y edad de fallecimiento
3. Ranking de localidades con SQL (CTEs + LAG para variación año a año)
4. Tendencia temporal por causa con moving average
5. Cruce mortalidad × régimen de seguridad social (chi-cuadrado)
6. Cruce mortalidad × sexo (chi-cuadrado)
7. Segmentación de localidades en 3 grupos de riesgo por percentil
8. Dashboard interactivo en Plotly

## Hallazgos clave

- **Neoplasias domina en mujeres** (51.6% de sus muertes prematuras); **cerebrovasculares
  domina en hombres** (51.8%) — diferencia estadísticamente significativa (p < 0.0001).
- **Pico de enfermedades cerebrovasculares en 2021**, posible efecto indirecto de la pandemia.
- La causa de muerte se asocia significativamente con el régimen de seguridad social
  (p < 0.0001): contributivo con más neoplasias, subsidiado con más cerebrovasculares.
- **Alto riesgo por volumen:** Kennedy, Suba, Engativá, Ciudad Bolívar, Bosa, Usaquén,
  San Cristóbal.

Ver [informe completo](informe_final.md) para detalle, limitaciones y recomendaciones.

## Estructura del proyecto

```
proyecto2_mortalidad_cronica/
├── 01_eda.ipynb
├── 02_limpieza.ipynb
├── 03_distribuciones.ipynb
├── 04_ranking_localidades.ipynb
├── 05_tendencia_causas.ipynb
├── 06_regimen_seguridad_social.ipynb
├── 07_chi_cuadrado_sexo.ipynb
├── 08_segmentacion_dashboard.ipynb
├── 08_dashboard.html
└── informe_final.md
```

## Limitaciones

- Segmentación por volumen absoluto de casos, no por tasa ajustada por población.
- Régimen de seguridad social usado como proxy de acceso a salud (no hay dataset dedicado
  de acceso a servicios preventivos).

## Stack

Python · pandas · SQL (PostgreSQL/NeonDB) · matplotlib · seaborn · plotly · scipy

## Autor

Eliel Berrío — Ingeniería de Sistemas, CECAR
