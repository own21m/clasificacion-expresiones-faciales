# Procedencia del laboratorio de exploración

[04-exploracion-preprocesamiento-dataset.ipynb](../notebooks/04-exploracion-preprocesamiento-dataset.ipynb) es una copia íntegra del archivo `copia.ipynb` recuperado desde una carpeta local sincronizada de Google Drive. Sus celdas, comentarios, salidas y metadatos disponibles no se modificaron.

El título coincide de forma única con una entrada del inventario, cuyo enlace es [copia.ipynb en Colab](https://colab.research.google.com/drive/1MlVQedgbzwBtGYfZfyjBAWUo40hBQSXs). Esa coincidencia permite asociar la copia como candidata; no prueba la identidad del archivo sincronizado en la nube ni que sea la versión remota actual. No se sustituyeron las descargas o exportaciones anteriores.

- SHA256 de la copia local completa: `615b73529fbfbda6cac8e396b9c784389acc46efdbcaef83ff71dd95a15eb3c7`.
- Tamaño: 931974 bytes.
- Contenido: 16 celdas, 15 de código y 11 salidas históricas.
- Las 15 celdas de código son sintácticamente válidas. No se ejecutaron durante la recuperación.

## Aportación y relación con las otras variantes

El laboratorio carga carpetas `angry` y `happy`, cuenta imágenes y dimensiones, calcula estadísticas de las imágenes crudas y obtiene ocho características combinando filtro bilateral y magnitud Sobel. Después guarda y carga arrays NPY y representa la correlación entre características y etiqueta. No contiene un clasificador.

Las funciones `normalize_image`, `calculate_statistics` y `preprocess_image` tienen la misma estructura AST que las de `01` y `02`. Ninguno de los cuatro cuadernos anteriores tiene todas las mismas fuentes, ni una celda no vacía completa idéntica a las de esta copia. Se conserva por su exploración y persistencia de características, como otra etapa del mismo proyecto.

Las salidas guardadas indican 10700 imágenes de entrenamiento y 2732 de prueba en la exploración completa. La extracción posterior limita a 50 imágenes por clase, produciendo 100 vectores por carpeta de entrenamiento o prueba. Son resultados históricos de esa copia, no medidas recalculadas.

## Límites de interpretación

La celda 10 utiliza `calculate_statistics` antes de que se defina en la celda 12, por lo que requiere estado previo para reproducir sus salidas en ese orden. No se ordenan los archivos ni se valida que cada imagen se haya leído correctamente.

Los archivos `train_images.npy` y `test_images.npy` almacenan vectores de características, aunque sus nombres y algunos comentarios digan imágenes. No se incluyen esos archivos generados ni el dataset. El código puede reemplazar archivos con esos mismos nombres cuando se ejecuta.

La fuente no declara autores, coautores, licencia ni una procedencia verificable del dataset completo. Un comentario que comienza con `prompt` no identifica por sí solo a una persona o herramienta autora. La relación con las otras variantes no prueba originalidad exclusiva de los fragmentos compartidos.

Las salidas conservadas incluyen texto de estadísticas y dos gráficos; no se extrajeron fotografías de rostros para la documentación. No se generaron nuevas métricas, no se montó Drive y no se cargaron modelos.
