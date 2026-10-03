# Propuesta asistida de familia de material para la declaración de envases

Proyecto final de la asignatura de Procesamiento del Lenguaje Natural
(Máster en Big Data, Business Analytics e Inteligencia Artificial, ESIC).

El prototipo propone la familia de material y el peso de un componente de
envase a partir de su descripción libre en el BOM, y decide si la propuesta
pasa a confirmación rápida o a revisión detallada.

## Contenido

| Fichero | Descripción |
| --- | --- |
| `componentes_envase_ficticio.csv` | 189 descripciones ficticias de componentes de envase con su familia y peso |
| `generar_dataset_ficticio.py` | Script que genera el conjunto de datos de forma reproducible |
| `proyecto_nlp_envases.ipynb` | Notebook con todos los experimentos del informe |

## Técnicas

- Extracción del peso con expresiones regulares.
- Clasificación de la familia con una regla de palabras clave y TF-IDF de caracteres + regresión logística.
- Búsqueda de componentes similares con TF-IDF de caracteres, comparada con embeddings E5.

## Cómo ejecutarlo

1. Descarga el notebook y el CSV en la misma carpeta.
2. Abre el notebook en Jupyter o Google Colab y ejecuta todas las celdas.
   En Colab, sube antes el CSV al panel de archivos.

Requisitos: `pandas`, `scikit-learn`, `spacy` (modelo `es_core_news_sm`)
y, para la comparación con E5, `sentence-transformers`.

## Aviso sobre los datos

Todos los datos son ficticios y se generaron para esta demostración.
No contienen información de ninguna empresa.
