# Documentaciones
## Indice de contenido
* [Crear y subir documentación(hugo) con github pages.](#item1)
* [contenido 2](#item2)
* [contenido 3](#item3)

<a name="item1"></a>
# Crear y subir documentación(hugo) con github pages.

# Creación del proyecto.
Creamos el proyecto con el siguiente comando:
```bash
$   hugo new site [proyecto]
```
Ingresamos a la carpeta del proyecto creado (en este caso el proyecto se llama **documentacion**).
```bash
$   cd documentacion
```
## Inicialización del repo
Una vez dentro de la carpeta, debemos inicializar **git** con este comando.
```bash
$   git init
```
## Configuración del Tema

### Opción A (submodulo)
Ahora, lo que haremos es crear un submodule con un template([tema](https://github.com/onweru/compose.git)) llamado ***compose***.
```bash
$ git submodule add https://github.com/onweru/compose.git themes/compose
```
Agregamos ese tema al **config.toml**, y cambiaremos el directorio donde se crean nuestros estáticos para que Github pages lo reconozca sin problema.
```bash
$ echo ‘theme = “compose”’ >> config.toml; echo ‘publishDir = “docs”’ >> config.toml
```

### Opcion B (clonar el tema)
Clonar el tema en la carpeta ***/themes***

```bash
$ git clone https://github.com/onweru/compose.git
```
Editar el archivo **config.toml**
```bash
baseURL = "https://dominio-git/"
languageCode = "en-us"
title = "My pagina Hugo"
theme = "compose"       # nombre del tema
publishDir = "docs"     # directorio dónde se crean los estaticos para que github pages los reconozca
```
## Creación de un post
Crear una publicación.
```bash
hugo new posts/prueba.md
```
## Del lado de **github pages**
1. Crear un repositorio con el mismo nombre del proyecto.

2. en la carpeta principal del proyecto reinicializar el repo
```bash
$ git init
```
3. Subir los cambios al servidor git
```bash
$ git remote add origin git@github.com:designing-rivers/quickstart.
```
4. Ahora usamos el comando **hugo** para crear los estáticos en una carpeta llamada /docs
```bash
$   hugo
```
5. Lo siguiente que haremos es crear un commit y subirlo a nuestro repositorio
```bash
$   git add *; git commit -m "Creando blog con hugo"; git push origin master
```
6. Una vez hecho esto nos vamos a **Settings**, **Github Pages**, **Source** y seleccionamos la rama ***master***, ***/docs folder***
7. y la ruta que nos retorna la debemos colocar en el archivo de configuracion **config.toml** y la colocamos en el parametro **baseURL**
8. nuevamente corremos el comando **hugo** y enviamos los cambios al servidor
```bash
$     hugo

$     git add *; git commit -m "Creando blog con hugo"; git push origin master
```
`linea 82`
----------
<a name="item2"></a>
### Contendio 2
Ejecuta el código usando este enlace de JSFiddle y observa que la sentencia alert(), dentro de mostrarNombre(), muestra con éxito el valor de la variable nombre, la cual fue declarada en la función externa. Este es un ejemplo de ámbito léxico, el cual describe cómo un analizador sintáctico resuelve los nombres de las variables cuando hay funciones anidadas. La palabra léxico hace referencia al hecho de que el ámbito léxico se basa en el lugar donde una variable fue declarada para determinar dónde esta variable estará disponible. Las funciones anidadas tienen acceso a las variables declaradas en su ámbito exterior.

<a name="item3"></a>
### Contendio 3
Ejecuta el código usando este enlace de JSFiddle y observa que la sentencia alert(), dentro de mostrarNombre(), muestra con éxito el valor de la variable nombre, la cual fue declarada en la función externa. Este es un ejemplo de ámbito léxico, el cual describe cómo un analizador sintáctico resuelve los nombres de las variables cuando hay funciones anidadas. La palabra léxico hace referencia al hecho de que el ámbito léxico se basa en el lugar donde una variable fue declarada para determinar dónde esta variable estará disponible. Las funciones anidadas tienen acceso a las variables declaradas en su ámbito exterior.
