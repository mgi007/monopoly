Primero creamos el repositorio git; después creamos el proyecto de eclipse en la misma ruta
que habiamos creado el repositorio git

Descargamos el archivo .zip y los descomprimimos en la carpeta src del proyecto.

En el primer commit y push subi todos los ficheros del proyecto con la libreria JUnit3 ya importada.
 
He probado la aplicación con el JUnit Test y no ha dado ningún error.
También he probado la aplicación ejecutando el método Main.

He realizado la primera refactorización cambiandole a la clase cell el nombre del atributo owner
por proprietary.

A continuación realizo el segundo push (con su commit correspondiente).

He realizado un Push Down en la clase Cell al atributo available haciendo que lo hereden todas sus
subclases; esto ha generado un par de errores en métodos que estaban fuera de esta clase.

Para solventar estos errores en vez de realizar un Undo, he realizado un Pull Up del atributo 
available de una de las subclases (en mi caso lo he hecho de la subclase GoCell).

