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
elementos, es por eso que tienen que estar bien divididos. Esto hará que no
tengamos elementos "eesclavizados".

Representa más trabajo porque todo tiene que ser manejado con clases, pero es
muy útil para el nombramiento de clases la identificación de los elementos.

> Nos ayuda a evitar que escribamos reglas CSS súper largas como:
>
> ```css
> .card .card__thumbnail {
> }
> ```
>
> Esto lo podríamos escribir solo de la siguiente manera:
>
> ```css
> .card__thumbnail {
> }
> ```
>
> **Y ya no tenemos que escribir tantas clases como en el primer método.**

## ELEMENTOS QUE SE MANEJAN EN BEM

Hay 3 tipos de elementos:

- **Bloques**

  - Componentes de nuestro sitio que creemos que podemos reutilizar.
  - Es como un componente.
  - **Podemos poner bloques dentro de bloques.**

    > ```css
    > .bloque {
    > }
    >
    > .card {
    > }
    > ```

- **Elementos**

  - Son elementos que forman parte de un bloque.

    > ```css
    > .bloque__elemento {
    > }
    >
    > .card__extracto {
    > }
    > ```

- **Modificadores**

  - Permiten modificar cómo se ve un elemento o un bloque sin afectar al
    general.

  > ```css
  > .bloque--modificador {
  > }
  >
  > .boton--absolute {
  > }
  > ```

  Para utilizarlos hay que agregar tanto en bloque, como el modificador o los
  modificadores, ya que si solo se agregan las clases con los modificadores, no
  se apicarán los estilos base. Es por esta razón por la que hay que agregar las
  clases base cuando se quieren agregar modificadores. Esto se puede ver en el
  siguiente ejemplo:

  ```html
  <a href="" class="boton boton--absolute"></a>
  ```

  En el ejemplo mostrado anteriormente, se declara el bloque, `boton`, para
  obtener los estilos base, y luego se declara la el modificador del bloque,
  `boton--absolute`, el cual ya agrega los estilos que se destinan para la
  modificación.

  Si solamente se declarara el modificador, los estilos base no serían
  aplicados.

  Además, se pueden poner tantos modificadores como quieras, logrando así, un
  mejor control, más modularizado, de los elementos.

  ```html
  <a href="" class="boton boton--absolute boton--verde"></a>
  ```
