# PROYECTO SOBRE ANÁLISIS DE SENTIMIENTOS DE RESEÑAS DE LIBROS
- Karen Huamani Ccorpuna ( [karenh88](https://github.com/karenh88) )
- Valeria Landa Cordova  ( [valeriiia11](https://github.com/Valeriiia11) )<br>

# BookFealsverse

<b>Contenido</b>:
- [Objetivos del proyecto](#objetivos)
- [Fuentes de información](#fuentes)
- [Diseño y planeamiento](#diseño)
  - [Extracción de Datos](#extraccion)
  - [Análisis de sentimientos](#analisis)
  - [Integración de Datos](#integracion)
- [Resultados y Concluisones](#resultados)
- [Desafíos](#retos)

## <font color=blue>Objetivos del proyecto</font>

>El objetivo de este proyecto es obtener información relevante sobre libros desde el sitio web Goodreads, realizar un análisis de sentimientos en las reseñas y >estructurar los datos en un formato tabular utilizando Python y diversas bibliotecas como BeautifulSoup, requests, Pandas y ParallelDots.

## <font color=blue>Fuentes de información</font>

- ### Goodreads
Se obtuvieron datos de sobre las reseñas de libros desde Goodreads utilizando sus identificadores únicos. Se utilizaron solicitudes HTTP para acceder a las páginas de libros y BeautifulSoup para analizar el contenido HTML y extraer información como títulos, puntuaciones y reseñas.

Enlace a la página: [Goodreads](https://www.goodreads.com/)

- ### Crisol
Se realizó un raspado web en el sitio web de la librería Crisol para obtener información sobre los libros más vendidos. Se utilizaron solicitudes HTTP y BeautifulSoup para extraer títulos, precios, ofertas y autores.

Enlace a la página: [Crisol](https://www.crisol.com.pe/)

- ### Komprehend
Se utilizo la api de esta pagina para hacer un analisis de sentimientos de las reseñas de los libros extraidos y tambien el analisis de emociones de las sinopsis de dichos libros.

Enlace a la página: [komprehend](https://komprehend.io)

Enlace a la documentación de la API: [APIdocs](https://apis.paralleldots.com/text_docs/index.html)


## <font color=blue>Diseños y planeamiento </font>


1. ### <font color=green>Extracción de datos </font>
    - Selección de Páginas de Interés:<br>
  Se identificaron 15 libros de interés, seleccionando las URLs correspondientes.<br><br>
    - Extracción de Información:<br>
  Se utilizó BeautifulSoup y requests para realizar solicitudes HTTP y extraer información como títulos, autores, precios, ofertas y reseñas de cada libro.<br><br>
    - Limpieza de Datos:<br>
  Se implementaron funciones para limpiar y estructurar adecuadamente los datos, eliminando caracteres especiales y palabras irrelevantes.

2. ### <font color=green>Análisis de sentimientos </font>
    - Configuración de ParallelDots:<br>
  Se configuró la API key de ParallelDots para realizar análisis de sentimientos en las reseñas.<br><br>
    - Función de Análisis de Sentimientos:<br>
  Se creó una función para obtener el análisis de sentimientos utilizando ParallelDots, aplicándola a las reseñas de cada libro.

3. ### <font color=green>Integración de datos </font>
    - Creación de DataFrames:<br>
  Generación de DataFrames para almacenar la información de los libros y los resultados del análisis de sentimientos.<br><br>
    - Integración de Datos:<br>
  Combinación de los datos obtenidos de las reseñas y los análisis de sentimientos en un único DataFrame para un análisis más completo.


## <font color=blue>Resultados y conclusiones </font>
>Este proyecto proporciona una base sólida para futuros análisis y puede ser ampliado para incluir más características y fuentes de datos. El código está >documentado y se han implementado mecanismos de manejo de errores para garantizar la robustez del programa.


## <font color=blue>Desafíos </font>

>Dentro de los desafíos que enfrentamos podemos mencionar la busqueda de una API que se adaptara a nuestras necesidades y, al mismo tiempo, afrontamos las >limitaciones de la API seleccionada. Esta presentaba un límite diario de uso, lo que dificultaba probar los códigos con la frecuencia necesaria para su >optimización y corrección de errores. Para aumentar este límite, era necesario suscribirse a un plan de pago.
>
>Otro desafio encontrado fueron los errores en las solicitudes HTTP y análisis de sentimientos los cuales solucionamos implemetando bloques ***try*** y ***except*** para manejar errores y proporcionar mensajes informativos en caso de fallos.
