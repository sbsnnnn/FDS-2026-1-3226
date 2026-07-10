# FDS-2026-1-3226

## Objetivo del proyecto

Desarrollar un proyecto de Ciencia de Datos aplicando la metodología CRISP-DM
para analizar las tendencias de videos de YouTube en Estados Unidos, respondiendo
a los requerimientos de información de una empresa de marketing digital: qué
categorías y canales dominan las tendencias, cómo evoluciona el consumo de
contenido en el tiempo, el comportamiento geográfico por estado, y la viabilidad
de predecir el rendimiento (vistas) de un video a partir de sus métricas de
interacción iniciales.

## Integrantes

| Integrante | Código |
|---|---|
| Colonio Soto Rodrigo Aaron | u202323598 |
| Donayre Salas Julio Gabriel | u20241a112 |
| Flores Peralta Frank Alexander | u202410754 |
| Yparraguirre Aquino Sebastián Alonso | u20241e121 |

**Curso:** 1ACC0216 - Fundamentos de Data Science
**Sección:** 3226
**Profesora:** Nérida Isabel Manrique Tunque

## Descripción del conjunto de datos

El dataset utilizado es **Trending YouTube Video Statistics** (fuente original: Kaggle),
correspondiente al registro diario de videos en tendencia en Estados Unidos entre
noviembre de 2017 y junio de 2018. Para este trabajo, el dataset fue modificado
agregando las columnas `state`, `lat`, `lon` y `geometry` (asignadas de forma
aleatoria por el enunciado del curso, no representan ubicación real de usuarios).

- `USvideos_cc50_202101.csv`: 40,949 registros, 20 columnas originales.
- `US_category_id.json`: mapeo de `category_id` a nombre de categoría.
- `USvideos_limpio.csv`: dataset final tras limpieza, preprocesamiento y
  construcción de variables (40,779 filas, 36 columnas).

El informe completo del proyecto (PDF) está disponible en este repositorio / [adjuntar enlace si lo subes también aquí].

## Metodología

Se aplicó la metodología **CRISP-DM**, cubriendo: comprensión del negocio,
comprensión de los datos, preparación de los datos (limpieza, tratamiento de
outliers, feature engineering), y modelado (Regresión Lineal y Random Forest
para predecir `views`).

## Conclusiones

- Entertainment y Music dominan las tendencias en volumen (9,905 y 6,446
  apariciones), pero no necesariamente en aprobación: Music lidera en likes
  promedio (188,495) mientras Entertainment ocupa el séptimo lugar (41,798).
- Pets & Animals, Music y People & Blogs son las categorías con mejor ratio
  likes/dislikes (menor riesgo de reacción negativa); News & Politics es la
  más polarizante.
- El volumen mensual de videos en tendencia se mantuvo estable (4,800–6,200
  videos/mes) durante el período analizado, sin estacionalidad marcada.
- La presencia en tendencia está concentrada en pocos canales de medios
  establecidos (ESPN, late night shows, Netflix); el 5.7% de los canales
  aparecieron una sola vez.
- Sí es factible predecir `views` a partir de métricas de interacción
  (`likes` correlaciona 0.83 con `views`); el modelo Random Forest superó
  a la Regresión Lineal en R² y MAE.

*(Conclusiones completas de negocio, técnicas, limitaciones y trabajo futuro
disponibles en el informe PDF.)*

## Licencia

Este proyecto se distribuye bajo licencia MIT. Ver [LICENSE](./LICENSE) para más detalles.
