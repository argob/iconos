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
La instalación requiere **Ruby 1.9.3+**, **WOFF2** y **FontForge** con las funciones de consola para Python.

```sh
# En Mac (requiere tener instalado [Homebrew](https://brew.sh/index_es)
brew tap bramstein/webfonttools
brew update
brew install woff2
brew install sfnt2woff
brew install fontforge
brew install eot-utils
gem install fontcustom

# En Linux
sudo apt-get install zlib1g-dev fontforge
git clone https://github.com/bramstein/sfnt2woff-zopfli.git sfnt2woff-zopfli && cd sfnt2woff-zopfli && make && mv sfnt2woff-zopfli /usr/local/bin/sfnt2woff
git clone --recursive https://github.com/google/woff2.git && cd woff2 && make clean all && sudo mv woff2_compress /usr/local/bin/ && sudo mv woff2_decompress /usr/local/bin/
gem install fontcustom
```

### Para compilar

```sh
fontcustom compile             # Compila la tipografía y templates
fontcustom watch               # Compila cuando las imágenes svg se cambian / agregan / eliminan
```
