# Uso de jupyter notebook
En caso de que ya conozcas como utilizar jupyter no es necesario que veas este contenido, pero si precisas de un breve repaso aqui lo hare.

Al hacer click en launch jupyter se abrira una nueva pestaña en nuestro navegador predeterminado. En caso de que querramos conectarnos desde otro navegador podemos hacer click derecho sobre el logo de jupyter y copiar el link para pegarlo en el navegador que sea de nuestro agrado. 

Porque es importante lo anterior? Por motivos de seguridad si queremos acceder a la pagina de nuestro servidor debemos proporcionar una credencial que nos acredite como usuarios legitimos del servicio, esto se logra facilmente usando ese link que acabas de copiar.

## Que es jupyter notebook
Jupyter notebook es un documento interactivo que ves en tu navegador y te permite ejecutar codigo de Python o R segun hayas seleccionado, ademas de poder darle formato con parrafos, ecuaciones, figuras al texto que estes escribiendo para documentar tus analisis. Esta combinacion es la que lo vuelve una herramienta fundamental por ejemplo para analisis exploratorios, ya que te permite tener en un solo lugar el codigo, las visualizaciones y tus comentarios sobre el analisis.

## Eligiendo en donde guardar nuestros archivos

Una vez dentro de la pagina se nos presentara una ventana con carpetas, parecido al explorador de archivos de Windows. Debes navegar a donde quieras almacenar tus archivos y una vez en la carpeta elegida hacer click en New. Esto abrira una nueva pestaña y estaremos listos para nuestra primer clase del curso.

## Nombre del notebook
Hacer click en untitled y colocar el nombre deseado. En este caso elijo "uso de jupyter notebook"

Tenemos un menu en la barra superior que nos permitira realizar todas las acciones que precisemos, algunas de ellas son: guardar, editar, instertar. Ademas contamos con iconos de acceso rapido, los mismos podemos editarlos de ser necesario para nuestra comodidad.

## Donde ver la version de Python que estamos ejecutando
Arriba a la derecha podemos ver que el servidor esta ejecutando Python 3, pero si quisieramos conocer en mas detalle podemos escribir en el primer bloque de codigo: 

```python
from platform import python_version
print(python_version())
```
Y presiona Run en la barra de botones, la version que nos muestra al ejecutarse es 3.7.4. Puede ser que recibas una version distinta dependiendo de la ultima version que este utilizando anaconda.

## Primer codigo en jupyter
Escribamos en el proximo bloque de codigo:

```python
print('¡Hola, mundo!')
```

Ahora puedes presionar de nuevo el boton de Run, o para hacerlo mas dinamico presiona shift+enter e inmediatamente se ejecutara este bloque dando una devolucion y pasando al siguiente bloque para que puedas ejecutarlo con shift+enter o para que continues escribiendo las lineas de codigo que te permitiran completar tu proyecto de Data Science.

## Algunos metodos abreviados de teclado utiles
* Comentar multiples lineas: Ctrl + /  en Windows o Cmd + / en Mac
* Ejecutar un bloque de codigo: Shift + Enter

## Ejercicio
Prueba conectandote a jupyter desde un navegador que no sea el predeterminado usando localhost:8888

Que ocurre? Te pide una contraseña o token. Esto es por seguridad.
