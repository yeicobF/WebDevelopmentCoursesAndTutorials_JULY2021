# ✅ CONSEJOS PARA ESCRIBIR MEJOR HTML Y CSS

En este documento pondré consejos para escribir mejor HTML y tener mejores
prácticas.

## 📚 FUENTES

- [(Solo lo tomé como referencia, porque solo es una guía para una empresa en específico) Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html "Google HTML/CSS Style Guide")
- [[YT: Dani Krossing] 28: How to Write Better HTML and CSS | Learn HTML and CSS | HTML Tutorial | Improve HTML and CSS](https://youtu.be/xE7VOZbHhFY "[YT: Dani Krossing] 28: How to Write Better HTML and CSS | Learn HTML and CSS | HTML Tutorial | Improve HTML and CSS")
- [HTML semantics cheat sheet](https://learn-the-web.algonquindesign.ca/topics/html-semantics-cheat-sheet/ "HTML semantics cheat sheet")
- [[YT: Fireship] 10 CSS Pro Tips - Code this, NOT that!](https://www.youtube.com/watch?v=Qhaz36TZG5Y "[YT: Fireship] 10 CSS Pro Tips - Code this, NOT that!")
- [[YT: midudev] clip-path en CSS: Muestra una porción de un elemento HTML](https://www.youtube.com/watch?v=d31rH2Eqoe0 "[YT: midudev] clip-path en CSS: Muestra una porción de un elemento HTML")
- [[YT: midudev] ☝️Scroll Snap, crea un slider sólo usando CSS 😱](https://youtu.be/uhP6OL0bwpY "[YT: midudev] ☝️Scroll Snap, crea un slider sólo usando CSS 😱")

## 🚫 **DIVITIS**

Muchas veces tendemos a trabajar totalmente con `div`s, pero esta no es la mejor
forma para trabajar, ya que esto incluso podría afectar al SEO del sitio web.

Para esto existe la semántica de HTML, la cual ayudará a que los elementos del
sitio web se identifiquen con mayor facilidad.

- Ejemplo de un código con buena estructura:

  ```html
  <section class="section-img">
    <h2>This is a title</h2>
    <p>
      This is a long paragraph that describes the image that is shown bellow
      this paragraph. Wow! Let's make some more text here!
    </p>
    <img src="imglink.jpg" alt="Image of something" />
  </section>
  ```

- Ejemplo de código con una mala estructura y "_divitis_":

  ```html
  <section>
    <div class="section-img">
      <div class="section-img-title">
        <h2>This is a title</h2>
      </div>
      <div class="section-img-p">
        <p class="p1">
          This is a long paragraph that describes the image that is shown bellow
          this paragraph.
        </p>
        <p class="p2">Wow! Let's make some more text here!</p>
      </div>
    </div>
    <div class="section-img-img">
      <img src="imglink.jpg" alt="Image of something" />
    </div>
  </section>
  ```

## ✏ TIP PARA STICKY / FIXED HEADERS

Este tip lo encontré en un comentario del video
"[10 CSS Pro Tips - Code this, NOT that!](https://www.youtube.com/watch?v=Qhaz36TZG5Y)"
y me pareció que me podría ayudar, por lo que lo agregaré a continuación:

"Greatt video as always! Here's my favourite CSS Pro Tip: There's this
obscure **CSS property** called **`scroll-padding-top`**. When you have a
**`sticky`** / **`fixed`** header, and you click an **`anchor` link**,
**_it gets hidden under the `sticky` header_**. To avoid this annoying bug,
**just give your `body` element `scroll-padding-top` equal to the `header`
height**. Along with **`scroll-behaviour: smooth`**, this will make it so that
**_when you click an anchor link, it'll scroll to it, such that it starts right
beneath the header instead of hidden under it, which is the intended
behaviour!_**"

## 🦊 FIREFOX

Es MUY RECOMENDABLE utilizar `Firefox` para hacer `debug`, ya que sus `devtools`
hasta ahora son muy superiores
(según [[YT: Fireship] 10 CSS Pro Tips - Code this, NOT that!](https://www.youtube.com/watch?v=Qhaz36TZG5Y "[YT: Fireship] 10 CSS Pro Tips - Code this, NOT that!")),
especialmente cuando se trata de CSS.

## 📦 FLEXBOX Y GRID

Flexbox y Grid son herramientas muy buenas para el desarrollo.

- Flexbox: Columnas / filas individuales.
- Grid: Múltiples filas y columnas.

### 🟨 GRID

Con `display: grid;` se pueden hacer cosas muy interesantes, tal como tener una
estructura de matriz en donde podemos distribuir elementos de la forma que
deseemos.

A continuación habrá un código de muestra, en donde:

- `display: grid;`: Forma para activar este modo de "acomodar los elementos".
- `fr`: Fractional unit. Esta es una unidad que compartirá **responsivamente**
  el espacio con otras columnas en la `grid`. Es como el
  `Expanded(flex: valor,)` en **`Flutter`**.
- `grid-template-columns: ancho-col-1 ancho-col-2 ancho-col-3;`: Tamaño de las
  columnas. Dependiendo del número de tamaños especificados, será el número de
  columnas.
- `grid-template-rows: alto-fila-1 alto-fila-2;`: Al igual que
  `grid-template-columns`, determina el tamaño, pero en este caso de las filas,
  y el número de filas dependiendo del número de medidas que se envíen.
- `place-items: center;`: Centrar los elementos.

Código:

```html
<style>
  .grid {
    display: grid;
    grid-template-columns: 1fr 500px 1fr;
    grid-template-rows: 100px 200px;
    place-items: center;
  }
</style>

<div class="grid">
  <i>😎</i>
  <i>😎</i>
  <i>😎</i>
  <i>😎</i>
  <i>😎</i>
  <i>😎</i>
</div>
```

## 🖥📱 RESPONSIVIDAD UTILIZANDO `clamp()`

Cuando queremos hacer el sitio web responsivo podemos hacer uso de las "_Media
Queries_", pero en ocasiones esto puede reducirse haciendo uso de la función
`clamp(medida-mínima, medida-preferida, medida-máxima)`, aunque puede ser un
poco confuso, por lo que pondré la comparación a continuación:

```css
/* MEDIA QUERY */

.article {
  width: 50%;
}

@media only screen and (max-width: 600px) {
  article {
    width: 200px;
  }
}

@media only screen and (min-width: 1200px) {
  article {
    width: 800;
  }
}

/* CLAMP: El código de arriba reducido a una sola línea. */

article {
  width: clamp(200px, 50%, 600px);
}
```

## 🔡 "VARIABLES" EN CSS

Se pueden definir "variables" en CSS, las cuales se pueden reutilizar en el
código. Estas variables deben ser definidas en `:root`, y deben ser
referenciadas con `var(--nombre-variable)`. Algo a tomar en cuenta, es que las
variables "**_cascade_**", es decir, que se pueden sobreescribir y los "hijos"
tomarán el valor que fue sobreescrito en la variable. A continuación se
encuentra un ejemplo de esto:

```css
:root {
  --text-color: rgb(255, 0, 0);
}

p {
  --text-color: green; /* Sobreescribimos la variable. */
  color: var(--text-color);
}

h1 {
  color: var(--text-color);
}

h2 {
  color: var(--text-color);
}
```

También se pueden combinar dichas "variables" para alcanzar valores más
complejos:

```css
:root {
  --r: 255;
  --g: 0;
  --b: 0;
  --text-color: rgb(var(--r), var(--g), var(--b)); /* COMPOSITION. */
}

p {
  --text-color: green; /* Sobreescribimos la variable. */
  color: var(--text-color);
}

h1 {
  color: var(--text-color);
}

h2 {
  color: var(--text-color);
}
```

## 🔢 CONTADORES EN HEADINGS EN CSS

Es posible agregar contadores en CSS en los headings. Esto se logra de la
siguiente forma:

```html
<style>
  :root {
    counter-reset: headings;
  }

  h1 {
    counter-increment: headings;
  }

  h1::before {
    content: counter(headings); /* Agregamos el contador antes del heading. */
  }
</style>
```

## 🟦 MATENER FOCUS EN BOTÓN E HIJOS (En un dropdown menu, por ejemplo)

Hay un problema cuando se utiliza la **pseudoclase** **_`:focus`_**, la cual es
utilizada para mostrar que el elemento está activo, como cuando estás en un
input o das click a un botón. El problema es que si se trata de un
"_dropdown menu_" y das click a uno de los elementos del menú, el botón pierde
focus y el menú se cierra.

Esto se puede solucionar con la pseudoclase **`:focus-within`**, **la cual
permanece activa mientras alguno de los hijos también tenga focus**. Esto puede
evitar hacer código de más en _`JavaScript`_, por ejemplo.

```css
.dropdown {
  opacity: 0;
  visibility: hidden;
}

button:focus-within .dropdown {
  opacity: 1;
  visibility: visible;
}
```

## 🎭 PostCSS: `Vendor prefixes` to CSS rules

Dado que hay diversas opciones en cuanto a navegadores, se tienen que agregar
"vendor prefixes", los cuales definen propiedades dependiendo de con qué
navegador se esté trabajando.

Con "_`PostCSS`_" esto se soluciona (al menos eso se mencionaba en el video), ya
que hace de un "**`AutoPrefixer`**", el cual toma el código que le des, y lo
convierte a uno con los **`vendor-prefixes`** que soporten la propiedad o un
equivalente.

## 📖 PREPROCESADORES

Existen preprocesadores para trabajar con CSS de una forma distinta a la base,
pero estos no serán utilizados en la elaboración de este proyecto.

Algunos de estos son:

- Sass
- Stylus
- Less
