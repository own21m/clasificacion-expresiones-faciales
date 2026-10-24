# Observaciones de la revisión estática

Estos puntos describen el código conservado. No se aplicaron correcciones a los cuadernos.

## Limpieza que modifica el conjunto de imágenes

`remove_black_images` utiliza `os.remove` y comprueba `np.max(image) == np.min(image)`. Aunque los comentarios hablan de imágenes negras, esa condición identifica cualquier imagen uniforme, incluso si su valor constante es distinto de cero. La función se invoca para las carpetas de entrenamiento y prueba.

| Cuaderno                                 | Celda, índice cero |
| ---------------------------------------- | ------------------ |
| `01-estadisticas-filtros-svm-knn.ipynb`  | 2                  |
| `02-balanceo-augmentation-svm-knn.ipynb` | 11                 |
| `03-hog-hu-clasificadores.ipynb`         | 3                  |

En `02` las salidas históricas registran seis imágenes de entrenamiento y una de prueba eliminadas. La revisión no volvió a ejecutar esas funciones. Para experimentar, utiliza copias de las carpetas o revisa y omite esas celdas.

## Separación entre entrenamiento y evaluación

En `01`, celdas 6 y 8, y `02`, celdas 6 y 7, se combina `train_features` con `test_features` antes de ajustar `StandardScaler`. Los datos de prueba influyen así en el cálculo del preprocesamiento. No se deben interpretar esas métricas como evaluación completamente separada.

La versión `02` contiene además variantes que balancean entrenamiento y prueba mediante generación o repetición de imágenes. Sus resultados no se comparan directamente con una evaluación de las imágenes de prueba originales sin transformar.

En `03`, los modelos se entrenan y validan con un `train_test_split` de las 5000 imágenes de entrenamiento cargadas. Las salidas muestran una validación interna de 1500 imágenes. Las 1000 imágenes externas de prueba preparadas por el cargador no son las utilizadas en esas métricas.

## Dependencias y selección de archivos

La primera línea de `01` contiene el carácter superíndice 8 (`U+2078`) delante de `import cv2`. Python rechaza esa línea como sintaxis inválida. Se conserva el archivo byte por byte; para ejecutarlo sería necesario retirar ese carácter en una copia de trabajo. Las salidas guardadas corresponden a ejecuciones históricas y no demuestran que la versión descargada pueda ejecutarse sin ese ajuste.

El cargador de `03` usa `os.listdir` y selecciona los primeros archivos sin una lista ordenada guardada. Aunque el reparto interno fija `random_state=42`, la selección inicial puede variar si el sistema devuelve otro orden de archivos.

No se conservaron versiones fijas de paquetes, el conjunto completo de datos ni los modelos `.pkl`. Las referencias a estos modelos en las salidas indican lo que se guardó durante las ejecuciones originales, no que esos archivos binarios formen parte de esta publicación.

## Alcance de las etiquetas

El proyecto distingue dos etiquetas de un conjunto de imágenes. No estima emociones internas verificadas, no identifica personas y no ofrece garantías para decisiones sobre individuos. No se documenta una validación por identidad ni una evaluación en un entorno de uso real.
