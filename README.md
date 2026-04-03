# Pandas_Kaggle

Repositorio de ejercicios del curso gratuito **"Pandas"** de Kaggle Learn.

Aquí voy guardando los notebooks (ejercicios) que completé para practicar lo más importante de Pandas: crear y leer datos, seleccionar/filtrar, resumir información, agrupar, ordenar, limpiar datos (tipos y nulos) y combinar datasets.

## Contenido del repositorio

- `exercise-creating-reading-and-writing.ipynb`
- `exercise-indexing-selecting-assigning.ipynb`
- `exercise-summary-functions-and-maps.ipynb`
- `exercise-grouping-and-sorting.ipynb`
- `exercise-data-types-and-missing-values.ipynb`
- `exercise-renaming-and-combining.ipynb`

> Nota: los notebooks están hechos para correr en Kaggle (usan datasets desde `../input/...` y las utilidades `learntools`).

---

## Resumen de cada notebook (qué hace y qué se aprende)

### 1) Creating, Reading and Writing
**Archivo:** `exercise-creating-reading-and-writing.ipynb`

**Qué se hace:**
- Se crean `DataFrame` y `Series` manualmente (por ejemplo con diccionarios y listas).
- Se practica definir índices (`index=`) y nombres (`name=` en una `Series`).
- Se refuerza la idea de que el primer paso de muchos proyectos es *leer datos* y convertirlos a estructuras de Pandas.

**Qué se aprende:**
- Diferencia entre `Series` (1D) y `DataFrame` (2D).
- Cómo construir objetos básicos de Pandas desde cero.
- Conceptos de columnas, filas e índice.

---

### 2) Indexing, Selecting & Assigning
**Archivo:** `exercise-indexing-selecting-assigning.ipynb`

**Dataset:** Wine Reviews (CSV cargado con `pd.read_csv(..., index_col=0)` dentro del notebook).

**Qué se hace:**
- Se seleccionan columnas (por ejemplo `reviews['description']`).
- Se exploran tipos de objetos (`type(desc)` para verificar que una columna es un `Series`).
- Se practican técnicas de selección y filtrado típicas en análisis exploratorio.

**Qué se aprende:**
- Selección por columna y el modelo mental *DataFrame → Series*.
- Cómo inspeccionar rápidamente un dataset (`head()`) y su estructura.
- Bases de indexación y asignación para crear nuevas variables/columnas.

---

### 3) Summary Functions and Maps
**Archivo:** `exercise-summary-functions-and-maps.ipynb`

**Dataset:** Wine Reviews.

**Qué se hace:**
- Se calculan estadísticas resumen (ej. `median()` sobre `points`).
- Se obtienen categorías únicas con `unique()`.  
- Se generan conteos por categoría (ej. cuántas reviews por país) y se crean `Series` derivadas.
- Se practica aplicar funciones a datos ("maps"), para transformar columnas.

**Qué se aprende:**
- Funciones resumen (`median`, `mean`, `min`, `max`, etc.).
- Cómo crear nuevas representaciones a partir de columnas (`Series` nuevas).
- Transformaciones rápidas de datos usando `map`/`apply` (según el ejercicio).

---

### 4) Grouping and Sorting
**Archivo:** `exercise-grouping-and-sorting.ipynb`

**Dataset:** Wine Reviews.

**Qué se hace:**
- Se agrupa información con `groupby()` para responder preguntas del tipo:
  - ¿Quiénes son los reviewers más comunes? (conteo por `taster_twitter_handle`).
  - ¿Cuál es la mejor puntuación máxima por cada precio? (`groupby('price').points.max()`).
- Se ordenan resultados para encontrar máximos/mínimos y comparar categorías.

**Qué se aprende:**
- `groupby()` como herramienta clave para análisis por grupos.
- Agregaciones (conteo, máximos, mínimos) y cómo interpretarlas.
- Ordenamiento (`sort_values`) para ranking y comparación.

---

### 5) Data Types and Missing Values
**Archivo:** `exercise-data-types-and-missing-values.ipynb`

**Dataset:** Wine Reviews.

**Qué se hace:**
- Se inspeccionan tipos de datos (`dtype`).
- Se convierten tipos con `astype()` (ej. números a texto).
- Se trabaja con valores nulos/faltantes (missing values) y se practican estrategias básicas para tratarlos.

**Qué se aprende:**
- Por qué importan los tipos (numérico vs texto) al analizar.
- Cómo convertir tipos correctamente.
- Cómo detectar y manejar valores faltantes para evitar errores y sesgos.

---

### 6) Renaming and Combining
**Archivo:** `exercise-renaming-and-combining.ipynb`

**Dataset:** Wine Reviews.

**Qué se hace:**
- Se renombran columnas para que sean más descriptivas (ej. `region_1 → region`, `region_2 → locale`) con `rename()`.
- Se renombra el eje/índice con `rename_axis()`.  
- Se practican conceptos para *combinar* datasets (según el tutorial: joins/concat), además de dejar el dataset más limpio y consistente.

**Qué se aprende:**
- Buenas prácticas de limpieza: nombres claros y consistentes.
- Renombrado de columnas y ejes.
- Conceptos base para combinar dataframes (`concat`/`merge`) cuando los datos están en varias tablas.

---

## Qué me llevo del curso

Después de completar estos ejercicios, los puntos más importantes que me quedan son:

- Pandas gira alrededor de **Series** y **DataFrames**.
- Saber **seleccionar, filtrar y asignar** es lo que más se usa en el día a día.
- Las funciones de resumen y el **groupby** permiten contestar preguntas de negocio rápido.
- Antes de analizar de verdad, casi siempre hay que **limpiar**: tipos correctos, valores nulos, nombres coherentes.
- Para proyectos reales, combinar tablas (merge/concat) es esencial.

## Referencia

- Curso: Kaggle Learn — Pandas (gratuito)