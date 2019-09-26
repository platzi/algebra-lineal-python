# Guia de Instalacion de Anaconda y Python

## Porque Python para Data Science
Si ya conoces el lenguaje Python no hace falta que te cuente porque es el elegido en la industria para dar vida a los proyectos de Data Science. Pero si no estas familiarizado con Python estas son algunas de sus caracteristicas:

* Es poderoso y sencillo
* Tiene multiples paquetes estadisticos y de aprendizaje automatico listos para usar
* Una comunidad muy activa a la que siempre puedes consultar

Y cuenta con muchas mas, pero te invito a descubrirlas junto a mi mientras exploramos el mundo del Algebra Lineal con Python.

## Porque Anaconda
Anaconda nos provee de una plataforma muy completa para poder desarrollar nuestros proyectos de Data Science, simplifica la tarea de instalacion y configuracion de las distintas aplicaciones que necesitaremos usar en nuestro viaje. Podemos utilizarlo tanto por terminal como por interfaz grafica (GUI). Por el momento avancemos con la segunda opcion, es mas amigable para quien no esta acostumbrado a la linea de comandos.

Algunas ventajas de utilizar Anaconda para tus proyectos son:
* Manejar los entornos de trabajo con Conda (todas las dependencias de librerias se resuelven en el momento de instalacion)
* Posibilidad de compartir, colaborar y reproducir los proyectos
* Puedes pasar tu proyecto a produccion solo con un click (una vez configurado)

Dentro de las variadas aplicaciones que nos ofrece Anaconda vamos a utilizar Jupyter Notebooks con Python 3.7.

### Instalacion

Para realizar la instalacion debes seguir los siguientes pasos:

1. Ir a https://www.anaconda.com/distribution/
2. Selecciona tu version de Sistema Operativo: Windows - macOS - Linux
3. Haz click en Descargar/Download "Python 3.7 version" (o click en la version adecuada para tu CPU 64-bit o 32-bit)

![Captura Pantalla Descarga Anaconda](imagenes/01.anaconda.captura.pantalla.descarga.png?raw=true "Descarga Instalador Anaconda")
Imagen -> 01.anaconda.captura.pantalla.descarga.png

Despues de descargar el instalador grafico, debes abrirlo y seguir las instrucciones que se presentaran en pantalla. Estas son una serie de preguntas para realizar la instalacion, las opciones por defecto estan bien, no hay necesidad de cambiarlas.

### Iniciando Anaconda

Una vez que finalizada la instalacion debes abrir el programa Anaconda Navigator para que podamos crear el entorno en cual estaremos estudiando y actualizar los paquetes.

Haz click en Environments y despues click en +Create. Se abrira una ventana para crear un nuevo entorno. 

Imagen -> 02.anaconda.captura.environments.select.png
Imagen -> 03.anaconda.captura.create.select.png

Rellena los siguientes campos:

* Name: Platzi - FundamentosAL
* Packages: tilde en Python y del menu desplegable selecciona 3.7

Imagen -> 04.anaconda.captura.popup.creacion.entorno.png

Haz click en Create. Ahora el computador se tomara un momento para configurar el nuevo entorno y actualizarlo. Cuando termine veras una pantalla similiar a esta 

Imagen -> 05.anaconda.captura.entorno.creado.png

Los paquetes que ves son los que estan instalados por defecto, necesitas instalar varios mas. Haz click en installed y cambialo a not installed.

Imagen -> 06.anaconda.captura.packages.notinstalled.png

 En el recuadro de search packages pon:

* Jupyter Notebook
* scipy (tambien instalara numpy)
* pillow (libreria para manejo de imagenes)
* imageio (lectura / escritura de imagenes)
* matplotlib (para graficar)
* seaborn (visualizaciones estadisticas)
* scikit-learn (aprendizaje automatico - lo usaremos para un ejemplo de PCA) 

En cada uno de los casos haz click en el recuadro y marcalo para instalar. Una vez que los tengas seleccionados haz click en Apply. Anaconda procesara por ti todas las dependencias y abrira una nueva ventana para que aceptemos los paquetes a instalar, haz click en Apply.

Una vez finalizada la instalacion y actualizacion de paquetes en el entorno Platzi - FundamentosAL hacemos click en Home, y Launch Jupyter Notebook. Una nueva pestaña se abrira en nuestro navegador con jupyter, ya estamos listos para comenzar el aprendizaje de Fundamentos de Algebra Lineal con Python.

### Ejercicio

Instala el paquete seaborn. Es un paquete para visualizar datos.

A mi tambien me paso la primera vez no saber por donde comenzar, asi que si necesitas ayuda aqui te dejo un paso a paso.

1 - Desde Anaconda Navigator, haz click en Environments
2 - Selecciona el entorno donde quieres instalar el paquete (Platzi - FundamentosAL)
3 - Selecciona en el menu desplegable Not Installed
4 - Escribe en el recuadro de busqueda seaborn
5 - Haz click en el paquete seaborn
6 - Haz click en Apply
7 - Haz click en Apply, pero esta vez en el pop up que aparecio para aceptar todas las dependencias.

Listo! Felicitaciones, instalaste tu primer libreria para visualizacion de datos en Python.

Puedes copiar y pegar en una de las celdas en Jupyter el siguiente codigo para ver un grafico de la cantidad de pasajeros en avion entre 1949 y 1960 por mes.

```Python
import seaborn as sns
vuelos = sns.load_dataset("flights")
vuelos = vuelos.pivot("month", "year", "passengers")
ax = sns.heatmap(vuelos)
```
