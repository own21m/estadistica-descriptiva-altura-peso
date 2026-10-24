# Estadística descriptiva de altura y peso

Recuperación de un trabajo universitario sobre exploración de datos, estadística descriptiva y detección de valores atípicos. Reúne tres cuadernos relacionados para conservar los intentos, las diferencias y las correcciones visibles del ejercicio.

Los cuadernos del parcial identifican a Juan Pablo Gutierrez Gutierrez y Juan Pablo Yepes Valencia como integrantes. El archivo originalmente llamado `Untitled12.ipynb` no contiene una firma interna; se agrupa por sus mismos datos, ejercicios y resultados guardados.

## Contenido

- Inspección de dimensiones, columnas, tipos, valores ausentes y valores únicos.
- Media, desviación estándar, mediana, moda, rango, cuartiles y rango intercuartílico.
- Construcción de `IMC_CLASS` como variable derivada del ejercicio.
- Comparación de puntajes estandarizados y marcas binarias de valores atípicos.
- Agrupaciones, histogramas, densidades, diagramas de caja, violín y dispersión con recta ajustada.

No se ejecutaron de nuevo los cuadernos durante la recuperación. Sus resultados son salidas históricas y algunas no corresponden al código visible o contienen errores que se detallan abajo.

## Cuadernos conservados

| Archivo | Origen y alcance |
| --- | --- |
| [01-exploracion-altura-peso.ipynb](cuadernos/01-exploracion-altura-peso.ipynb) | `Untitled12.ipynb`: 28 celdas de código y 31 salidas. Usa una ruta de Drive a `SOCR-HeightWeight.csv`. |
| [02-parcial-altura-peso.ipynb](cuadernos/02-parcial-altura-peso.ipynb) | Parcial de los dos integrantes: 39 celdas, 37 de código y 41 salidas; incluye bloques repetidos y correcciones parciales. |
| [03-parcial-puntos-corregidos.ipynb](cuadernos/03-parcial-puntos-corregidos.ipynb) | `PuntosCorregidos`: 33 celdas, 28 de código y 32 salidas. Contiene correcciones explícitas de rangos, cuartiles, marcas de altura y asimetría. |

La numeración organiza la lectura y no certifica el orden cronológico ni que un archivo sea la última versión de la nube.

## Conservación y privacidad

Todo el código original se mantiene sin cambios. En la copia pública de `PuntosCorregidos` se omitió únicamente la rúbrica y las calificaciones presentes en su primera celda de Markdown. Se conservaron el encabezado de integrantes, el resto de las celdas y todas las salidas. Un aviso dentro del cuaderno señala esa omisión.

Los originales íntegros y el arreglo de celdas copiado de Colab permanecen en el respaldo local, fuera de este repositorio. [ORIGEN.md](ORIGEN.md) y [origen/verificacion.json](origen/verificacion.json) registran la procedencia, las huellas antes y después y el índice exacto de la única celda modificada. Las huellas de código coinciden en las tres copias públicas con sus fuentes locales.

## Tecnologías y datos

Python, Google Colab, pandas, NumPy, Matplotlib y seaborn. Las versiones históricas no se conocen con precisión; `requirements.txt` enumera las bibliotecas de análisis sin fijar versiones inventadas. Google Colab aporta el módulo `google.colab` que importan los cuadernos.

El ejercicio trabaja con `Index`, `Height(Inches)` y `Weight(Pounds)`. Dos cuadernos leen una copia CSV desde Google Drive; el tercero espera:

```text
/content/drive/MyDrive/parcialCienciaDeDatos/SOCR-HeightWeight.csv
```

La rúbrica original menciona Kaggle, pero no se identificó una referencia completa al dataset de origen ni una licencia verificable. El CSV no está incluido y no se verificó la disponibilidad actual del enlace de Drive. No se atribuye al equipo la creación del conjunto de datos.

## Cómo consultarlo

Los cuadernos se pueden leer directamente en GitHub. Para explorarlos de manera interactiva, abrir una copia en Google Colab y aportar el CSV con las columnas esperadas. La variante `Untitled12` monta Drive; los otros dos archivos leen un enlace CSV. La disponibilidad de los datos y los problemas de estado de sesión pueden impedir reproducirlos tal como están.

Si se prepara un entorno Python propio, las bibliotecas de análisis se declaran en:

```bash
python -m pip install -r requirements.txt
```

Esto no reproduce el entorno original ni sustituye las funciones específicas de Colab. Hacer cualquier adaptación en otra copia, manteniendo este registro del trabajo.

## Resultados guardados y diferencias

Las salidas de `PuntosCorregidos` registran 25 000 filas y tres columnas antes de eliminar `Index`, sin valores ausentes. Informan una media de altura de 67.9931 pulgadas y de peso de 127.0794 libras. El criterio de altura `abs(z) > 3` marca 51 casos; las cercas de 1.5 veces el rango intercuartílico del peso marcan 191. Estos valores no se recalcularon.

En `Untitled12`, `Outliers_Height` almacena el puntaje z continuo. Después se agrupa por ese valor y se cuentan solo registros iguales a uno, lo que produce cero casos en la salida guardada. Eso no equivale al umbral de tres desviaciones usado en `PuntosCorregidos`.

El parcial largo conserva tanto el puntaje continuo como un bloque posterior de marcas binarias. Algunas salidas muestran la columna `Index` después de una celda que la elimina, o estadísticas rotuladas con posiciones equivocadas. Sirven para entender el proceso de aprendizaje, sin certificar una ejecución limpia en orden.

## Limitaciones conocidas

- El recuento de tipos usa posiciones de `dtypes.value_counts()` y trata una de ellas como categoría. No distingue de forma general variables numéricas de categóricas.
- El parcial largo repite ejercicios y accede a posiciones de estadísticas que dejan de ser válidas al eliminar columnas. Su celda 25, con índices desde cero, comienza con una expresión `Q` sin definición visible y puede interrumpir una ejecución limpia.
- Las variantes modifican el dataframe en memoria. Repetir una eliminación o ejecutar celdas fuera de orden puede cambiar los resultados o fallar.
- Hay avisos de pandas sobre el comportamiento de `groupby` con categorías. No se validó compatibilidad con versiones actuales ni se corrigieron las API del original.
- La asimetría pequeña que imprime una variante es un resultado descriptivo; no demuestra por sí sola normalidad. No se presenta una validación inferencial de distribuciones.
- Las categorías calculadas de `IMC_CLASS` forman parte de un ejercicio de programación y no tienen validación de uso clínico en estos cuadernos. La recta de seaborn se ajusta para visualizar la relación entre las dos columnas; no es un modelo predictivo validado.

## Autoría, licencia y herramientas

Se conserva la coautoría explícita de Juan Pablo Gutierrez Gutierrez y Juan Pablo Yepes Valencia en los dos parciales. No se encontró una licencia del código y no se añadió una. La copia sin firma interna y las referencias incompletas de datos se documentan sin atribuir autoría exclusiva de cada fragmento.

La inteligencia artificial se utilizó como herramienta de aceleración de procesos para organizar la recuperación, comparar archivos, revisar contenido y preparar documentación. No se le atribuye la creación del trabajo universitario original.
