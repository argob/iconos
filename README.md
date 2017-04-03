![Poncho](img/poncho.gif)

### [Ver listado de íconos](//argob.github.io/iconos)

# Uso

Para utilizar los iconos son necesarios los archivos de la carpeta **dist**.
En el html hay que llamar al archivo *icono-arg.css*.

```html
<link href="path/to/css/icono-arg.css" rel="stylesheet">
```

Algo importante, es que la relación de las carpetas css y fonts deben quedar como están para que funcionen las rutas relativas.

# Desarrollo

El archivo editable con todos los íconos es [src/Iconos.ai](src/Iconos.ai).
Los iconos exportados en svg van en **src/_icons/**

### Instalación de ambiente de desarrollo

Para compilar la tipografía se utiliza [Font Custom](https://github.com/FontCustom/fontcustom). 
La instalación requiere **Ruby 1.9.2+** y **FontForge** con las funciones de consola para Python.

```sh
# En Mac
brew install fontforge --with-python
brew install eot-utils
gem install fontcustom

# En Linux
sudo apt-get install fontforge
wget http://people.mozilla.com/~jkew/woff/woff-code-latest.zip
unzip woff-code-latest.zip -d sfnt2woff && cd sfnt2woff && make && sudo mv sfnt2woff /usr/local/bin/
gem install fontcustom
```

### Para compilar

```sh
fontcustom compile             # Compila la tipografía y templates
fontcustom watch               # Compila cuando las imágenes svg se cambian / agregan / eliminan
```
