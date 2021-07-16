# Canal de YouTube: "FalconMasters"; Video: "Que rayos es la Metodología BEM explicado con un ejemplo | CSS"

En esta carpeta se encontrará el tutorial que seguí de un video en donde
explican lo que es la metodología BEM.

> FUENTE:
> [Canal de YouTube: "FalconMasters"; Video: "Que rayos es la Metodología BEM explicado con un ejemplo | CSS" - Duración: 35:15](https://youtu.be/bvnzyXGkNY4 'Canal de YouTube: "FalconMasters"; Video: "Que rayos es la Metodología BEM explicado con un ejemplo | CSS" - Duración: 35:15')
>
> CÓDIGO INICIAL PARA EL PROYECTO:
> [https://github.com/falconmasters/bem/tree/codigo_base](https://github.com/falconmasters/bem/tree/codigo_base "https://github.com/falconmasters/bem/tree/codigo_base")

## PARA QUÉ SIRVE

Permite crear componentes en la maquetación para HTML y CSS. Nos permitirá
reutilizar código.

> Permite crear componentes, moverlos de un proyecto a otro, reutilizarlos y
> agregar modificadores. Además de crear código más fácil de entender.

Además, lo que se recomienda es no poner etiquetas con las clases al definir los
elementos, es por eso que tienen que estar bien divididos.

Representa más trabajo porque todo tiene que ser manejado con clases, pero es
muy útil para el nombramiento de clases la identificación de los elementos.

## ELEMENTOS QUE SE MANEJAN EN BEM

Hay 3 tipos de elementos:

- **Bloques**

  - Componentes de nuestro sitio que creemos que podemos reutilizar.
  - Es como un componente.
  - **Podemos poner bloques dentro de bloques.**

    > ```css
    > .bloque
    > ```

- **Elementos**

  - Son elementos que forman parte de un bloque.

    > ```css
    > .bloque__elemento
    > ```

- **Modificadores**
