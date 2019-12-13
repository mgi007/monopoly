Primero creamos el repositorio git; después creamos el proyecto de eclipse en la misma ruta
que habíamos creado el repositorio git.

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

** NOTA: En el push de "Refactorización Cuatro" vienen los pasos de la refactorización 3 y 4 debido a que se me olvido hacer
un push al terminar la refactorización 3.

Hemos seleccionado un fragmento de código y hemos creado un nuevo método llamado calcMonopoliesRent con esta pieza de código.
Al provar las dos opciones podemos deducir que el Eclipse reconoce si el cacho de código necesita
que le pasen alguna variable desde fuera del método o no. Yo he elegido extraer el método con
las variables ya inicializadas para que no haga falta pasarle ninguna variable desde fuera del módulo.

He realizado un push con la refactorización 4.

He creado un método del get del colorGroup y le he llamado colorGroup

He realizado un push con la refactorización 5.

He cambiado el tipo del parámetro que devuelve el método getPropertyNumberForColor de String a int

He añadido un parámetro booleano que por defecto es true llamado visibility al método getPropertyNumberForColor.

He cambiado el tipo de dato que retorna el método playAction de void (no retorna ningún valor) a boolean.
Cambiar el tipo del resultado de void a boolean
Añadir un nuevo parámetro del de tipo String que se llama msg y por defecto es nulo.

Al hacer las refacorizaciones del ejercicio 6 de esta práctica se producen errores en otras partes del
código relacionadas con la parte cambiada y que tendremos que ir solventando una a una.

La respuesta a la pregunta final se debe a que hemos cambiado un método en la superclase Cell por lo que
todas las subclases de la clase Cell que invoquen el método playAction tendrán un error debido al cambio
realizado que tendremos que solventar.

Este error se debe a que hemos cambiado el método de void (que no retorna ningúna valor), a boolean que
nos retornará un valor de tipo booleano por lo que tendremos que añadir un return false o un return true
en todas las llamadas que hagan a este método las subclases de la superclase Cell.



