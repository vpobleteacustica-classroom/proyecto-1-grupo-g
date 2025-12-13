# Informe de Evaluación – Hitos 2 y 3  
**Curso:** ACUS220
**Proyecto:** Sonificación de partidas de ajedrez (PGN → MIDI)  
**Integrantes:** Lorenzo Vera, Cristian Vera, Angelo Ortiz  

---

## 1. Descripción general del proyecto

El proyecto propone la **sonificación de una partida de ajedrez** en formato PGN mediante la generación automática de un archivo **MIDI**, utilizando reglas de mapeo entre eventos del juego (pieza, captura, jaque, enroque, promoción) y parámetros musicales (nota, octava, paneo, velocity, duración).  

El cuadernillo incluye un desarrollo técnico funcional, con:
- Lectura y parsing de partidas PGN (python-chess).
- Generación de eventos MIDI (mido).
- Parametrización musical (tempo e instrumentos) y separación por color (blancas/negras).
- Interfaz gráfica simple (Tkinter) y reproducción (pygame).

La idea es creativa, original y plenamente pertinente para el curso, integrando programación, representación simbólica y diseño sonoro.

---

## 2. Evaluación por criterios (Hitos 2 y 3)

| Criterio | Peso | Nota | Comentario |
|--------|------|------|------------|
| Claridad del planteamiento del problema | 0.15 | 6.8 | Objetivo claro y motivación convincente; el enfoque de “ajedrez sonoro” es novedoso y bien delimitado. |
| Justificación y contexto del experimento | 0.10 | 6.6 | Se aprecia coherencia con antecedentes y un enfoque reproducible; podría reforzarse la conexión con criterios de diseño sonoro y evaluación. |
| Metodología y organización del notebook | 0.20 | 6.6 | Flujo de trabajo bien implementado; faltó una sección final más ordenada que resuma decisiones de diseño y resultados obtenidos. |
| Calidad del código y buenas prácticas | 0.15 | 6.7 | Código funcional y relativamente ordenado; se recomienda documentar más (comentarios/docstrings), separar módulos y agregar pruebas mínimas. |
| Análisis de resultados y visualizaciones | 0.15 | 6.3 | Se describe correctamente la lógica de transformación, pero faltaron evidencias “finales”: ejemplos sonoros, formas de onda, capturas de la GUI y comparación de casos (captura vs no captura, jaque, etc.). |
| Conclusiones y coherencia con objetivos | 0.15 | 6.2 | El prototipo cumple, pero no se consolidó un cierre académico: limitaciones, dificultades, aprendizajes y propuestas concretas de mejora. |
| Redacción, ortografía y estilo general | 0.10 | 6.5 | Presentación clara; podría pulirse el formato final (secciones de cierre, resumen ejecutivo y conclusiones). |

**Nota Hitos 2 y 3 (ponderada): 6.5**

---

## 3. Nota final del curso

- **Nota Hito 1:** 6.7  
- **Nota Hitos 2 y 3:** 6.5  

**Nota final del curso:** **6.6**

---

## 4. Comentario global de cierre

El trabajo es **muy interesante y creativo**, y cumple con una implementación técnica que permite generar un resultado real (MIDI) a partir de una partida PGN, incorporando además una interfaz simple para controlar parámetros y reproducir. En ese sentido, el proyecto **cumple con el hito 3** y demuestra un buen nivel de programación aplicada.

La principal debilidad observada no está en la idea ni en la implementación base, sino en el **cierre y la organización final**: faltó redactar de forma explícita cuáles fueron las **principales limitaciones**, dificultades encontradas, decisiones de diseño (por qué esos mapeos, rangos y parámetros) y una conclusión que sintetice logros y proyecciones.

Recomendaciones concretas (si continuaran el trabajo):
- Incluir una sección “**Limitations & Lessons learned**” (dependencias, reproducción en distintos SO, latencias GUI, etc.).
- Agregar **ejemplos sonoros** y visualizaciones (formas de onda, espectrogramas) para comparar eventos clave.
- Incorporar una evaluación mínima: por ejemplo, **métricas de densidad de eventos**, distribución de notas/velocities, o una evaluación perceptual sencilla (encuesta corta).

**Buen trabajo: proyecto original, funcional y con gran potencial si se fortalece el cierre académico.**
