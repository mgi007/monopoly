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
available de una de las subclases (en mi caso lo he hecho de la subclase GoCell) para subir este atributoç
a la superclase.

Realizo el tercer push con la segunda práctica de refactorización.

He extraído la interfaz de la clase Cell y la he llamado IOwnable y he seleccionado que cambien
los métodos getAvailable setAvailable getProprietary setProprietary debido a que son los que
afectan a la compra y venta de las parcelas de monopoly.

He realizado un push con el tercer paso de la refactorización.

Hemos seleccionado un fragmento de código y hemos creado un nuevo método llamado calcMonopoliesRent con esta pieza de código.
Al provar las dos opciones podemos deducir que el Eclipse reconoce si el cacho de código necesita
que le pasen alguna variable desde fuera del método o no. Yo he elegido extraer el método con
las variables ya inicializadas para que no haga falta pasarle ninguna variable desde fuera del módulo.
