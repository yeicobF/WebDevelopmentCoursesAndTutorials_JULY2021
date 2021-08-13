# APUNTES GENERALES: HTML

En este archivo se encontra rán apuntes generales respecto a HTML que no
pertenecen a un curso como tal, sino a videos o información suelta.

> Archivo iniciado: Martes, 13 de JULIO del 2021.

## **FUENTES**

Gran parte del contenido de este archivo lo obtuve de uno que ya había creado
cuando estaba haciendo el proyecto de Fundamentos de Desarrollo Web del ciclo
2020-2021/B. La fuente de dicho archivo es la siguiente:

- [proyecto-yeicobF/DOCUMENTOS/ApuntesGenerales_HTML_CSS.md](https://github.com/Fundamentos-Web/proyecto-yeicobF/blob/main/DOCUMENTOS/ApuntesGenerales_HTML_CSS.md "proyecto-yeicobF/DOCUMENTOS/ApuntesGenerales_HTML_CSS.md")

### WEB EN GENERAL

- [Learn the Web | HTML semantics](https://learn-the-web.algonquindesign.ca/topics/html-semantics/ "Learn the Web | HTML semantics")
- [Learn the Web | HTML semantics cheat sheet](https://learn-the-web.algonquindesign.ca/topics/html-semantics-cheat-sheet/ "Learn the Web | HTML semantics cheat sheet")
- [Learn the Web | Naming conventions](https://learn-the-web.algonquindesign.ca/topics/naming-conventions/ "Learn the Web | Naming conventions")

### YOUTUBE

- [[YT PLAYLIST by Thomas Bradley] HTML semantics](https://youtube.com/playlist?list=PLWjCJDeWfDdc0Sp_DinOWnodw3KnWCwc1 "[YT PLAYLIST by Thomas Bradley] HTML semantics")
- [[YT: Fazt] Curso HTML para Principiantes](https://youtu.be/rbuYtrNUxg4 "[YT: Fazt] Curso HTML para Principiantes")

## **CONTENIDOS**

- [**FUENTES**](#fuentes)
  - [WEB EN GENERAL](#web-en-general)
  - [YOUTUBE](#youtube)
- [**CONTENIDOS**](#contenidos)
- [HTML SEMANTICS](#html-semantics)
  - [Phrasing elements](#phrasing-elements)
  - [Images with captions](#images-with-captions)
  - [Document elements](#document-elements)
  - [Sections & articles](#sections--articles)
  - [Headers & footers in sections & articles](#headers--footers-in-sections--articles)
  - [Meaningless elements](#meaningless-elements)
  - [Break](#break)
  - [Horizontal rule](#horizontal-rule)
  - [More specific elements](#more-specific-elements)
  - [Entities](#entities)
- [ETIQUETAS](#etiquetas)
  - [`<meta>`](#meta)
    - [Atributos](#atributos)
  - [`<header>`](#header)
  - [`<nav>`](#nav)
  - [`<section>`](#section)
  - [`<adress>`](#adress)

## HTML SEMANTICS

Los siguientes elementos los tomé del siguiente sitio web:
[**_HTML semantics_**](https://learn-the-web.algonquindesign.ca/topics/html-semantics/ "Learn the Web | HTML semantics")

### Phrasing elements

- **`<em>`** — for emphasizing text, like is spoken word, to make some words
  more important.
- **`<strong>`** — for even more emphasis than **`<em>`**.
- **`<i>`** — for language elements: text in another language, ship names,
  sarcasm, irony, movie titles, TV show titles.
- **`<b>`** — for keywords; is the word important while searching for the
  website?

### Images with captions

If an image has a caption that describes the image you can surround the image
tag with more elements.

- **`<figure>`** — defining the image as having a caption
- **`<figcaption>`** — marking up the caption itself

```html
<figure>
  <img src="images/trex.jpg" alt="" />
  <figcaption>Photo of T-Rex skeleton in the Ottawa museum.</figcaption>
</figure>
```

When you have a **`<figcaption>`**, the alt attribute can be left empty if the
caption does a good job describing the image.

### Document elements

- **`<header>`** — for more important information, like the masthead of the
  website, where the name and logo and navigation are.
- **`<nav>`** — navigation, defining the navigation of the website.
- **`<footer>`** — for less important information, like the footer of the
  website, usually includes the copyright statement, social icons, etc.
- **`<main>`** — for defining the primary content.
- **`<aside>`** — for secondary information, stuff that's not required to
  understand the primary content, like sidebars, pull quotes, etc.

```html
<!-- The website masthead with the navigation -->
<header>
  <h1>Prehistoric creatures</h1>
  <!-- The website's primary navigation -->
  <nav>⋮</nav>
</header>

<!-- The <main> content of the website: what your user came to see -->
<main>
  <h2>Land animals</h2>
  ⋮
</main>

<!-- Secondary information that's helpful but not necessary for understanding -->
<aside>
  <h2>Prehistoric environment</h2>
  ⋮
</aside>

<!-- Website footer, copyright information, terms, etc. -->
<footer>
  <p>© 1138 Dinosaurs</p>
</footer>
```

### Sections & articles

- **`<section>`** — for grouping content together that has a heading—there's no
  point using a section if it doesn't have a unique heading.
- **`<article>`** — for independent content, stuff that can be removed from this
  website and would still be understandable, like blog posts & products.

### Headers & footers in sections & articles

You can put **`<header>`** and **`<footer>`** and **`<main>`** elements inside
**`<article>`** tags and **`<section>`** tags.

_The elements can be used to denote the importance of the information inside the
article._

```html
<article>
  <!-- Denotes more important information inside the article -->
  <header>
    <h2>Diplodocus stuffed toy</h2>
    <p>Super awesome introduction to the toy.</p>
  </header>

  <!-- Denotes the main content of the article -->
  <main>
    <p>Lots…</p>
    <p>Of…</p>
    <p>Details…</p>
  </main>

  <!-- Denotes secondary, related information -->
  <aside>
    <h3>Other sauropods</h3>
    <ul>
      <li>Brachiosaurus</li>
    </ul>
  </aside>

  <!-- Denotes less important information in the article -->
  <footer>
    <p>Written by a person.</p>
    <time datetime="1982-10-28">Published: Today</time>
  </footer>
</article>
```

### Meaningless elements

There are two elements in HTML that don't add meaning to the content, but can be
used as styling hooks, if need to group things together when creating your
layout.

- **`<div>`** — a meaningless group, has restrictions on what elements it can go
  inside.
- **`<span>`** — small runs of meaningless text.

```html
<!-- We could use the <span> tag to individually colour all the letters -->
<h1>
  <span>R</span>
  <span>a</span>
  <span>i</span>
  <span>n</span>
  <span>b</span>
  <span>o</span>
  <span>w</span>
</h1>

<main>
  <!-- Using a <div> as a styling hook: maybe a random coloured box -->
  <div>
    <h2>Prehistoric creatures</h2>
    ⋮
  </div>

  <!-- Another group of elements -->
  <div>
    <h2>Prehistoric environment</h2>
    ⋮
  </div>
</main>
```

### Break

In HTML there's an element to add a line break. It should never be used to make
space in your website, that's what CSS is for.

_Only use a **`<br>`** tag if the line break is part of the content._

A good example is an address. In an address, the formatting of each line is
important so a **`<br>`** tag is important.

```html
<address>
  24 Sussex Drive<br />
  Ottawa, ON<br />
  K1A 0A3
</address>
```

Another good example of when to use a **`<br>`** tag would be in poems: each
stanza is a paragraph, and each line as a break after it.

### Horizontal rule

HTML has a tag called the horizontal rule, the **`<hr>`** tag. It's meant to be
used as a thematic break in your content.

A great example of a thematic break is from novels: when you're reading a novel
and there is a space between paragraphs, or a little decoration: that's an
**`<hr>`**, because it's a scene break.

The default CSS style, applied by browsers, to **`<hr>`** tags is to make it
look like a line. Do not use an **`<hr>`** to make lines, that's not its
purpose. If you want to make a line, use CSS.

```html
<p>A theropod dinosaur from the Late Jurassic period.</p>

<hr />

<p>The Brontosaurus is now a dinosaur again after many years.</p>
```

### More specific elements

For defining certain types of data and document information.

- **`<time datetime="">`** — Times, dates, durations; the datetime attribute is
  for the computer readable information.
- **`<data value="">`** — Numberical data: weight, length, mass, etc.; the value
  attribute is for the computer readable information.
- **`<del>`** — Deleted content.
- **`<ins>`** — Newly inserted content.
- **`<dfn>`** — A word or term currently being defined.
- **`<abbr title="">`** — Abbreviations and acronyms; the title attribute is
  used for the full version.
- **`<mark>`** — Highlight text, like in search results.
- **`<sub>`** — Subscript.
- **`<sup>`** — Superscript.

```html
<!-- Distinct points in time-->
<time datetime="1980">Brontosaurus discovery</time>
<time datetime="1980-05-21">Empire Strikes Back released May, 1980</time>
<time datetime="1977-09-05T12:56:00">
  Voyager 1 launched Sept. 5, 1977 at 12:56
</time>

<!-- Time periods -->
<time datetime="P365D">Earth's orbit around the Sun</time>
<time datetime="PT0H22M">22 minutes to bake cookies</time>

<data value="0.9865">Distance from Earth to Sun: 0.9856 au</data>
The Brontosaurus <data value="15">weighed 15 tonnes</data> & was
<data value="22">22 metres long</data>.

<ins datetime="2015">Brontosaurus becomes a valid dinosaur again</ins>
<del datetime="1980-05-21T19:30">See Empire Strikes Back</del>

<p>A <dfn>dinosaur</dfn> was a large prehistoric land reptile.</p>
<abbr title="Hypertext Markup Language">HTML</abbr>

<!-- The current page highlighted in the navigation -->
<a href="#"><mark>Home</mark></a>

<p>Distance from Earth to Sun: 1.476×10<sup>8</sup> km</p>
<p>H<sub>2</sub>O</p>
```

### Entities

Some characters cannot be written in the text content of HTML because the
characters are reserved for the HTML syntax.

- **`&gt;`** — for making greater than symbols
- **`&lt;`** — for making less than symbols
- **`&amp;`** — for writing ampersands
- **`&nbsp;`** — to put a space between words that will never break or word wrap

```html
<p>10 &gt; 9 = yes</p>
<p>600 &lt; 601 = yes</p>
<strong>Big &amp; hairy</strong>
<!-- The unit will never break away from the numbers -->
<p>0.9856&nbsp;au</p>
```

## ETIQUETAS

Hay etiquetas que le dan mayor valor a los buscadores y a la web en general para
dar más contexto de la estructura de un sitio web y su contenido. Es aqui en
donde se encuentran los **_HTML semantics_** (así encontré el concepto), los
cuales le dan un mayor contexto a un sitio web.

> Lo que ponga entre comillas en esta sección puede provenir del sitio
> [**HTML semantics cheat sheet**](https://learn-the-web.algonquindesign.ca/topics/html-semantics-cheat-sheet/ "Learn the Web | HTML semantics cheat sheet").

### `<meta>`

Esta etiqueta no tiene una etiqueta que cierre, ya que cierra en la misma
declaración.

Tiene atributos para especificar qué información le daremos al navegador.

No se ve en la página web, pero específica atributos a la web.

#### Atributos

- **charset**: Codificación de caracteres del sitio web.
  - Por lo general se utiliza **_`UTF-8`_**.
- **name**: Nombre de qué información se le dará al navegador.
  - _"description"_: Descripción del sitio.
  - _"author"_: Autor del sitio.
  - _"keywords"_: Palabras clave que definen al sitio y su contenido.
    - Hoy en día, los buscadores ya no hacen mucho uso de las keywords, pero no
      está de más.
- **content**: Descripción del sitio web.

```html
<meta name="description" content="Esta es mi primera página web." />
<meta name="author" content="yeicobf" />
<meta
  name="keywords"
  content="Palabras clave 1, palabras clave 2, palabras clave 3"
/>
```

### `<header>`

No es una etiqueta que altere el cómo se ve el navegador, pero sí cómo la web lo
identifica.

> " When inside `<body>` it's the website masthead.
>
> When inside `<article>` it's the most important information. "

```html
<header>
  <h1>Mi Blog</h1>
</header>
```

### `<nav>`

Identificar items de navegación, los cuales al clickar se manda a otra página.

> "Defines a group a navigation links."

Por lo general dentro contiene una lista de elementos con enlaces, tal como una
lista desordenada (Unordered list: **`<ul>`**) o una ordenada (Ordered list:
**`<ol>`**).

```html
<nav>
  <ul>
    <li>Principal</li>
    <li>Ayuda</li>
    <li>Contacto</li>
  </ul>
</nav>
```

### `<section>`

Destinada a una sección.

> "A group in a series of related content pieces."

### `<adress>`

Es útil para indicar que el contenido se trata de una dirección de internet.

> "Contact information, email, tel, postal address, etc."

```html
<address>
  <a href="https://google.com">Visita Google</a>
</address>
```

```html
<address>
  Jet Propulsion Laboratory
  <br />4800 Oak Grove Drive <br />Pasadena, California <br />91109
</address>
```

### **`<button>`**

> "Represents a interactive, clickable **button**.
>
> Should be used in forms and with JavaScript.
>
> **_Do not use to link to another page—use the `<a>` tag._**"
