# Procedencia de los cuadernos

Se recuperaron cuatro cuadernos proporcionados por el usuario y relacionados con el procesamiento de imágenes y la clasificación `angry`/`happy`. Los cuadernos `01`, `02` y `03` conservan los archivos completos descargados, byte por byte. El laboratorio `00` conserva las seis celdas y salidas exportadas desde la interfaz de Colab, con un envoltorio de cuaderno reconstruido.

El archivo [00-normalizacion-filtros-imagenes.ipynb](../notebooks/00-normalizacion-filtros-imagenes.ipynb) procede de [normalizacion_filtros_prueba.ipynb](https://colab.research.google.com/drive/1SXsX6ZNFboIKXqcyHwz3VJhJZIC2wIiX). La documentación de [su exportación UI](EXPORTACION-NORMALIZACION.md) distingue la conservación de celdas de la conservación del archivo completo.

| Archivo del repositorio                  | Fuente de Colab                                                                                                          |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| `01-estadisticas-filtros-svm-knn.ipynb`  | [ProcesamientoDeImagenes.ipynb](https://colab.research.google.com/drive/1Lu1sgCCQ5-jbSJj_bKNuJhEL-2jGx7Ie)               |
| `02-balanceo-augmentation-svm-knn.ipynb` | [sistema-reconocimiento-emociones-ia-1.ipynb](https://colab.research.google.com/drive/1cujJ44Hh-vScQMSjpRg-lx-lCRbN-1a-) |
| `03-hog-hu-clasificadores.ipynb`         | [emotion-recognition.ipynb](https://colab.research.google.com/drive/1hP1HcbwYB3Osr08moLfrKRq7ARajBMee)                   |

El inventario [originales.json](originales.json) registra tamaños, SHA256, número de celdas y comprobaciones de sintaxis. En `01`, `02` y `03` los hashes corresponden a los archivos completos descargados y coinciden con las copias renombradas. En `00` el hash corresponde al archivo reconstruido, no al original completo de Drive; también se registran hashes del contenido de celdas exportado.

La clasificación de los cuadernos y la documentación se prepararon mediante lectura estática el 24 de octubre de 2026. Las fechas de las salidas corresponden a ejecuciones históricas, no a un entrenamiento realizado en esa fecha.

## Elementos compartidos

Las versiones `02` y `03` comparten exactamente la celda que cuenta imágenes por clase y la función de eliminación de imágenes negras. La carga, extracción de características y entrenamiento difieren, por lo que se conservan las dos variantes completas.

## Imágenes de documentación

- `images/svm-validacion-interna.png`: PNG original de la salida de la celda 6, índice cero, del cuaderno `03`.
- `images/knn-validacion-interna.png`: PNG original de la salida de la celda 7 del mismo cuaderno.

Se decodificaron las imágenes ya almacenadas dentro de los `.ipynb`; no se ejecutó ni se alteró código para producirlas. No se extrajeron galerías de rostros para la documentación.

## Autoría y licencia

No aparecen nombres de autores, coautores ni una licencia explícita en el contenido de estos tres cuadernos. Los identificadores de autoría técnicos de Colab se conservan dentro del JSON y no se interpretan como nombres o permisos de licencia.

Este repositorio conserva los archivos facilitados y añade documentación sobre su contenido. No impone una nueva licencia al código, a los datos o a sus salidas, ni declara que todas las imágenes sean de autoría propia.
