# Informe Final: Segmentación de Localidades de Bogotá por Mortalidad Prematura por Enfermedades Crónicas

## Contexto y fuente de datos

Dataset: Mortalidad prematura por enfermedades crónicas en Bogotá D.C., Secretaría de Salud.
164,840 registros originales, 2010–2025 (2026 excluido por incompleto). Rango de edad: 30-70 años.

## Pregunta central

¿Qué localidades de Bogotá tienen la mayor mortalidad prematura por enfermedades crónicas —
y se relaciona ese indicador con el régimen de seguridad social del fallecido?

## Hallazgos principales

### 1. Distribución por causa

- Enfermedades cerebrovasculares (45%) y neoplasias (42%) concentran la gran mayoría de las
  muertes prematuras; diabetes y respiratorias son minoritarias.
- Neoplasias afecta a población más joven (mediana ~59 años) que respiratorias (~65 años).

### 2. Tendencia temporal

- Pico marcado de enfermedades cerebrovasculares en 2021, probablemente asociado a efectos
  indirectos de la pandemia (atención tardía, colapso del sistema de salud).
- Neoplasias muestra tendencia sostenida al alza desde 2013, superando a cerebrovasculares en
  2025 — es la causa que más está creciendo proporcionalmente.

### 3. Diferencia por sexo (hallazgo clave)

- En mujeres, neoplasias es la causa dominante (51.6% de sus muertes prematuras).
- En hombres, enfermedades cerebrovasculares domina (51.8%).
- Diferencia confirmada estadísticamente: chi-cuadrado, p-valor < 0.0001.

### 4. Régimen de seguridad social

- La causa de muerte se asocia significativamente con el régimen (chi-cuadrado, p < 0.0001).
- En régimen contributivo, neoplasias domina claramente sobre cerebrovasculares.
- En régimen subsidiado, cerebrovasculares domina sobre neoplasias.
- Limitación: esta asociación no implica causalidad directa; puede reflejar diferencias de
  acceso a diagnóstico oncológico o a control preventivo cardiovascular entre regímenes.

### 5. Segmentación geográfica

- Alto riesgo (mayor volumen de muertes): Kennedy, Suba, Engativá, Ciudad Bolívar, Bosa,
  Usaquén, San Cristóbal.
- Riesgo medio: Rafael Uribe Uribe, Usme, Fontibón, Puente Aranda, Tunjuelito, Santa Fe.
- Bajo riesgo: Barrios Unidos, Teusaquillo, Chapinero, Los Mártires, Antonio Nariño,
  La Candelaria, Sumapaz.
- Limitación importante: esta segmentación usa conteos absolutos, no tasas ajustadas por
  población. Las localidades de alto riesgo son también las más pobladas de Bogotá.

## Recomendaciones de intervención

1. Estrategias de prevención diferenciadas por sexo: priorizar tamizaje oncológico
   (mamografía, citología) en mujeres, y control cardiovascular (hipertensión, colesterol)
   en hombres.
2. Reforzar detección temprana de cáncer en régimen subsidiado, donde la proporción de
   neoplasias diagnosticadas es menor — posible brecha de acceso a diagnóstico oportuno.
3. Priorizar recursos de salud pública en localidades de alto riesgo por volumen: Kennedy,
   Suba, Engativá, Ciudad Bolívar.
4. Investigar el pico de 2021 en cerebrovasculares para dimensionar el efecto indirecto de
   la pandemia en enfermedades crónicas no transmisibles.

## Limitaciones

- Segmentación por volumen absoluto, no por tasa poblacional.
- Datos con alcance Bogotá, no representativos del resto de Colombia.


