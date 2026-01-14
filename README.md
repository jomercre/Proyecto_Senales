El repositorio ha sido creado por Pol Reig Gómez, Pablo Carbonell Martínez, Joan Merlos Cremades, Héctor Torres Muñoz y Jóse Aguilar Milla con la intención de reflejar el proyecto de la asignatura Analísis 
de Señales del Máster en Ciencia de Datos de la UV.

El proyecto ha consistido en la eliminación de diferentes tipos de ruido en imágenes mediante el uso de la Transformada Wavelet Discreta o DWT, para ello se han generado diferentes archivos RMD cada uno de ellos
con la intención de realizar una función concreta.

- Preprocesado_imagenes.Rmd -> prepara las imágenes que se encuentran en la carpeta fotos_raw para poder ser analizadas. El proceso consiste en reducir las imágenes a 1024x1024 píxeles, conseguir que las diferentes
  imágenes tengan el mismo rango de valores para las bandas R, G y B y, finalmente, guardar los resultados en la carpeta fotos_clean.

- Fotos_Ruido.Rmd -> utiliza las imágenes de la carpeta fotos_clean y les introduce de forma sintética el mismo tipo de ruido en cada una de sus bandas de color. Los ruidos considerados han sido el Gaussiano, el
  Speckle, el de Poisson y el Sal y Pimienta, de forma que como resultado obtenemos una carpeta denominada fotos_ruido que contiene las imágenes de la carpeta fotos_clean, pero contaminadas con cada uno de los 4
  tipos de ruido considerados.

- Resultados.Rmd -> mediante el uso de las imágenes verdaderas localizadas en la carpeta fotos_clean y el uso de la DWT intenta eliminar el ruido de las imágenes localizadas en la carpeta fotos_ruido. Para ello
  realiza la DWT de la imagen ruidosa y procede a eliminar las componentes de detalle. El programa de forma automática nos devuelve para cada imágen ruidosa una gráfica con el RMSE en función del niveles de la DWT
  considerada y una gráfica con la imagen limpia, la imagen con ruido y la recomposición óptima utilizando DWT, es decir, aquella con menor RMSE. Cabe destacar que dichas imágenes se ven duplicadas porqué se han
  realizado dos formas de eliminación del ruido diferentes una en la que solo se eliminan los coeficientes HH (diag) y otra en la que se eliminan los coeficientes HH, HL y LH (all).

- Informe_AS.pdf -> es un archivo que contiene el procedimiento realizado para desarrollar este proyecto en conjunto con las diferentes conclusiones obtenidas.
