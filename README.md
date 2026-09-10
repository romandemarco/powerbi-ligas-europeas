Análisis de rendimiento — 5 grandes ligas europeas (2014-2021)

Dashboard interactivo en Power BI sobre 25.360 partidos de Premier League, LaLiga, Serie A, Bundesliga y Ligue 1.

📄 Ver el informe completo con capturas del dashboard

Pregunta

¿La producción ofensiva medida en goles esperados (xG) predice el éxito deportivo mejor que la efectividad de conversión?

La hipótesis era que generar situaciones de gol de alta probabilidad es un indicador más estable que convertir: un equipo puede tener una racha de definición, pero sostener xG alto durante temporadas implica una estructura de juego.

Qué contiene

Modelo de datos. Esquema estrella con una tabla de hechos (estadísticas por equipo y partido) y dimensiones de equipos, ligas y calendario. La tabla de calendario se generó por DAX para habilitar inteligencia de tiempo.

Transformaciones en Power Query. Normalización de tipos, conversión del resultado cualitativo (W/D/L) a puntos, y resolución de un problema de integridad referencial entre calendario y hechos mediante una clave sintética numérica (DateKey).

Medidas DAX. Alojadas en una tabla independiente para mantener consistencia: volumen (partidos, goles, xG, puntos) y rendimiento (promedios por partido de puntos, xG, goles y tiros al arco).

Cuatro vistas. Panorama general por liga, ranking de equipos con dispersión xG vs goles, tabla de posiciones acumulada del período, y evolución temporal por equipo.

Resultado

Los equipos que dominaron el período (Bayern, Barcelona, PSG, Real Madrid, Manchester City) sostuvieron los promedios más altos de xG y tiros al arco, no solo de goles. En el gráfico de dispersión se ubican consistentemente en el cuadrante de alta producción y alta conversión.

Alcance de la conclusión: el análisis es descriptivo. Muestra que los equipos con más puntos también tuvieron más xG en el mismo período, lo cual es consistente con la hipótesis pero no la prueba: para validar capacidad predictiva habría que estimar xG en un período y evaluar puntos en otro. Esa distinción entre asociación y predicción es la que trabajo en este otro proyecto.

Archivos
Archivo	Descripción
informe.pdf	Documentación completa con capturas del dashboard
dashboard.pbix	Archivo de Power BI (requiere Power BI Desktop)
Herramientas

Power BI Desktop · Power Query (M) · DAX

Proyecto final del curso de Analista de Datos — Coderhouse, diciembre 2025.
