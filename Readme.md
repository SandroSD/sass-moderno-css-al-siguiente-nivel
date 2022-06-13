# SASS
## ¿Qué es Sass?
SASS es un preprocesador, que nos permite escribir código CSS de una manera más dinámica, agregando sintaxis de un lenguaje de programación, incluyendo variables, funciones, módulos y distintos tipos de valores.

## ¿Por qué Sass?
- Es totalmente compatible con CSS, toda la sintaxis de CSS se puede utilizar con Sass.
- Podemos escribir código más rápidamente.
- Muchos framworks se construyen con Sass.
- Hay mucha documentación.

## .sass vs .scss
El procesador Sass, pero tiene 2 sintaxis que podemos ocupar.
La primera es la sintaxis con la extensión .sass, esta sintaxis la cuál se define por no usar llaves y usar tabuladores, como python.
La segunda es bastante similar a CSS es la extensión .scss, solo agrega funcionalidades extra, si hay llaves y todo lo que conocemos.

## ¿Sass reemplaza a CSS?
No, Sass es una herramienta para escribir código CSS más rápido, limpio y modular, al final compilaremos nuestros archivos Sass, para que se conviertan en archivos CSS.

## Ejemplo:
```
.hero {
    display: flex;
    justify-content: space-between;

    &__child {
        flex: 1;
    }
}

.main {
    @extend .hero;
}
```
### Comandos para compilar:
- sass --watch (ruta al archivo)
- sass --watch (carpeta origen):(carpeta destino)

### Variables:
$nombre-variable: valor;

### Anotaciones:
- Sass no distingue - de _.

### Partials (Módulos):
Al nombre del archivo le ponemos _ adelante, no será compilado porque será llamado por otro elemento y ese lo va a compilar.
- Para exportarlo, usamos @use 'nombre del archivo' (no hace falta poner extensión del archivo).
- Si a las variables las declaramos con por ejemplo un color y el !default, para que tomen un valor por defecto, podemos cambiarles dicho color al importarlas en otro archivo.

```
_variables.scss:

$primary: royalblue;
$secondary: crimson;

index.scss:
@use 'variables' with (
    $primary: red;
    $secondary: green;
)
```

Esto lo que hará es que las variables tomen el valor del with a la hora de importarlas.

