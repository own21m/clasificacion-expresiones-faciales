# Exportación del laboratorio de normalización

El archivo `notebooks/00-normalizacion-filtros-imagenes.ipynb` procede de [normalizacion_filtros_prueba.ipynb](https://colab.research.google.com/drive/1SXsX6ZNFboIKXqcyHwz3VJhJZIC2wIiX), identificador `1SXsX6ZNFboIKXqcyHwz3VJhJZIC2wIiX`.

## Qué se recuperó

Se utilizó la opción **Copy All Cells** de la interfaz de Colab. La exportación proporcionó un array JSON con seis celdas de código y seis salidas guardadas.

Se verificó la igualdad estructural exacta entre ese array y el campo `cells` del cuaderno incorporado: se conservan las fuentes de código, comentarios, salidas y metadatos de cada celda. El archivo reconstruido se copió sin volver a modificarlo. No se ejecutaron sus celdas.

No se obtuvo mediante este procedimiento la descarga completa del archivo de Drive. El envoltorio `.ipynb` se reconstruyó como `nbformat=4`, `nbformat_minor=0` y `metadata={}`. Por ello no se afirma que sus bytes completos o sus metadatos de raíz coincidan con los del archivo original de Drive.

## Integridad registrada

| Comprobación | Resultado |
| --- | --- |
| Celdas conservadas | 6, iguales al array exportado |
| Salidas guardadas | 6 |
| Sintaxis Python | Las seis celdas son válidas; una solo referencia el conjunto y dos conservan código comentado para uso futuro |
| SHA256 del `.ipynb` reconstruido | `ad95e7b33259b5d12ee64155ef71e5bdfc5b13490046f53de8d63c4c95af0588` |
| SHA256 canónico del contenido de celdas | `cc9a903b2e0840673bbc2782e6cee7291d443b8f0366462382e87466e7acb6c2` |

El inventario [originales.json](originales.json) distingue `original_bytes_preserved=false`, `cells_preserved=true` y `export_file_bytes_preserved=true`. Incluye también el hash del array JSON exportado desde la interfaz. El hash canónico ordena las claves JSON para comparar la estructura; no implica modificar el código del cuaderno.

## Relación con el proyecto

Este laboratorio explora la normalización min-max, los detectores Sobel y Canny y los filtros gaussiano, de mediana y bilateral sobre una imagen. Extrae dos medias como ensayo inicial de características. No entrena un clasificador y no es una copia completa de los otros cuadernos.

Su primera celda enlaza FER2013 en Kaggle como referencia. La ruta `/content/Training_89091722.jpg` requiere una imagen local que no se incluye por separado. Las salidas históricas con la muestra se mantienen dentro del cuaderno; no se añadieron como imágenes al README.

Los otros tres cuadernos del repositorio conservan sus descargas completas y sus hashes originales, sin modificaciones por esta incorporación.
