# Procedencia y diferencias de las copias públicas

## Fuentes recuperadas

| Archivo público | Fuente local de recuperación | ID asociado en el inventario |
| --- | --- | --- |
| `01-exploracion-altura-peso.ipynb` | Archivo sincronizado `Untitled12.ipynb` | `16iKZiNrJJPLnMqTu5-t3wwK3TbOiZkP3` |
| `02-parcial-altura-peso.ipynb` | Archivo sincronizado `JuanPabloGutierrezGutierrezJuanPabloYepesValenciaPARCIAL.ipynb` | `1pE-jceDe0MmekaBlZq06oHjcM5rsk3Uk` |
| `03-parcial-puntos-corregidos.ipynb` | Copia de celdas de `PuntosCorregidos` desde la interfaz de Colab | `1zXeKS5w5ZQ3361N3--CTfQMaSD6qCNg5` |

Fecha de recuperación y revisión: 24 de octubre de 2026.

Los dos archivos sincronizados se copiaron desde `G:/My Drive/Antiguo/Colab Notebooks`. Sus identificadores se asociaron por coincidencia unívoca del título con el inventario capturado de Colab. No se afirma una comprobación independiente de metadatos en la nube ni que sean las versiones remotas más recientes. Sus copias públicas coinciden byte a byte con los archivos locales de respaldo.

`PuntosCorregidos` se recuperó desde su documento observado en Colab mediante selección y copia de todas las celdas. El portapapeles entregó un arreglo, conservado íntegro solo en el respaldo local. Se reconstruyó un objeto raíz mínimo de nbformat 4.0 con metadatos vacíos. Antes del ajuste de privacidad, las 33 celdas de ese archivo reconstruido coincidían con el arreglo copiado; no se afirma identidad byte a byte con el archivo completo de Drive.

## Único cambio de contenido para publicación

En `03-parcial-puntos-corregidos.ipynb` se modificó exclusivamente la fuente de la celda de Markdown de índice **0**. Se conservaron su encabezado y los nombres de integrantes, se omitió el bloque de rúbrica/calificaciones y se insertó:

> Rúbrica y calificaciones omitidas en la copia pública; código original conservado.

Las otras 32 celdas son iguales a las de la exportación. Las 28 celdas de código y las 32 salidas no cambiaron. Tampoco se reordenaron celdas, alteraron metadatos ni corrigieron algoritmos o resultados históricos.

En las otras dos copias no se modificó ninguna celda. No se encontró una rúbrica o calificación académica en sus fuentes o salidas revisadas. Los originales íntegros y arreglos originales de celdas no se adjuntan como respaldos en el repositorio para evitar reintroducir el contenido omitido.

## Verificación reproducible

[origen/verificacion.json](origen/verificacion.json) registra por cuaderno:

- SHA-256 del archivo local fuente y del archivo público.
- Firma de todas las fuentes antes y después de la copia pública.
- Firma del código antes y después, que coincide en cada caso.
- Conteos de celdas y salidas y los índices de celdas que cambiaron.
- Huellas de la fuente original y pública del Markdown modificado, sin publicar el contenido omitido.
- Igualdad de las demás celdas y conservación de todas las salidas.

Las huellas de archivos se calculan sobre bytes exactos. La firma de fuentes serializa en UTF-8 pares `(cell_type, source)` con `json.dumps(..., ensure_ascii=False)`, usando separadores predeterminados y el orden original. Las fuentes almacenadas en listas se unen sin separador y solo se normaliza CRLF a LF. La firma de código usa pares `(índice_de_celda_desde_cero, source)` para las celdas de código y el mismo procedimiento. No se recortan espacios ni se reformatea el código.

## Autoría y alcance

Los dos parciales identifican a Juan Pablo Gutierrez Gutierrez y Juan Pablo Yepes Valencia. `Untitled12.ipynb` no contiene firma interna; su relación se apoya en las columnas, datos de ejemplo, ejercicios y resultados coincidentes. La agrupación no certifica autoría individual de cada fragmento ni una cronología de versiones.

Los cuadernos mencionan datos de altura y peso y una copia llamada `SOCR-HeightWeight.csv`; no se recuperó el CSV ni se verificó una licencia del dataset. No hay una licencia de código declarada y esta recuperación no la asigna.

Se leyeron las fuentes y salidas como datos inertes. Los gráficos revisados son numéricos y no contienen fotografías de personas. No se ejecutaron celdas ni se verificaron de nuevo los resultados. Los errores conocidos se explican en el [README](README.md).
