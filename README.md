# Taller 2 · Fundamentos de React

| Información | Detalle |
|:--|:--|
| **Estudiante** | Natalia Orozco Ropero |
| **Docente** | Luis Giovanny Carreño Ortiz |
| **Curso** | Desarrollo de Front-end |
| **Fecha de entrega** | Viernes 16 de octubre de 2026 |

## Contenido

1. [Punto 1 · ¿Qué es React?](#punto-1--qué-es-react)
2. [Punto 2 · ¿Qué problema resuelve React?](#punto-2--qué-problema-resuelve-react)
3. [Punto 3 · Principales componentes de React](#punto-3--principales-componentes-de-react)
4. [Punto 4 · Importancia de React en la industria](#punto-4--importancia-de-react-en-la-industria)
5. [Punto 5 · Grandes empresas que utilizan React](#punto-5--grandes-empresas-que-utilizan-react)
6. [Referencias](#referencias)


## Solución del taller


## Punto 1 · ¿Qué es React?

> **Actividad:** Investiga y define con tus palabras.

### ¿Qué es React y para qué sirve dentro del desarrollo web?

<div align="justify">

React es una librería de JavaScript que permite crear interfaces de usuario mediante componentes reutilizables y con un enfoque declarativo. Esto significa que, en lugar de indicar manualmente las modificaciones que se deben realizar en el DOM mediante JavaScript, se describe cómo debe verse la interfaz según el estado actual de los datos. React se encarga de actualizar la interfaz cuando estos datos cambian.

</div>

### ¿Quién lo creó y en qué año apareció?

<div align="justify">

React fue creada por un equipo de desarrolladores de Facebook liderado por Jordan Walke. El principal objetivo de Walke era crear una herramienta que simplifique el desarrollo de interfaces de usuario complejas, reduciendo la complejidad y mejorando el rendimiento. Su trabajo se hizo público en 2013.

</div>

### ¿Es una librería o un framework? Explica la diferencia y justifica tu respuesta.

<div align="justify">

React es una librería de JavaScript que proporciona herramientas para crear interfaces de usuario mediante componentes reutilizables. No se considera un framework completo porque se centra principalmente en la construcción de interfaces y no establece por sí solo una estructura integral para toda la aplicación.

</div>

<div align="justify">

La diferencia es que una librería ofrece funcionalidades específicas que el desarrollador puede utilizar según sus necesidades, mientras que un framework proporciona una estructura más amplia, convenciones y herramientas que orientan la organización y el desarrollo de una aplicación

</div>

### ¿Qué significa que React sea declarativo?

<div align="justify">

React es declarativo porque permite describir cómo debe verse la interfaz de usuario según el estado actual de los datos, sin tener que indicar manualmente cada modificación del DOM con javascript. Cuando los datos cambian, React se encarga de actualizar la interfaz para reflejar esos cambios.

</div>

## Punto 2 · ¿Qué problema resuelve React?

> **Actividad:** Explica las dificultades de manipular el DOM manualmente y cómo React ayuda a mantener la interfaz sincronizada con los datos.

### ¿Cuál era la dificultad principal de construir interfaces con JavaScript "a mano" (manipulando el DOM)?

<div align="justify">

La dificultad principal de construir interfaces a mano es que JavaScript permite manipular el DOM, por ejemplo, agregando nuevas etiquetas, modificando su contenido o eliminando elementos. Sin embargo, cuando se necesita desarrollar una interfaz extensa con muchas interacciones, la manipulación imperativa del DOM puede volverse complicada, ya que el desarrollador debe controlar manualmente los cambios y mantener actualizada la interfaz. Esto aumenta la complejidad del código y la posibilidad de cometer errores, especialmente cuando existen muchos elementos que dependen unos de otros.

</div>

### Explica la diferencia entre el enfoque imperativo y el enfoque declarativo.

<div align="justify">

El enfoque imperativo consiste en indicar paso a paso las instrucciones que se deben ejecutar para obtener un resultado. En la manipulación del DOM, el desarrollador debe especificar manualmente las operaciones necesarias para agregar, modificar o eliminar elementos mediante JavaScript.

</div>

<div align="justify">

Por otro lado, el enfoque declarativo consiste en describir el resultado que se desea obtener, es decir, cómo debe verse la interfaz en función de los datos o del estado actual, sin tener que especificar manualmente cada modificación del DOM.

</div>

### ¿Cómo ayuda React a mantener la interfaz sincronizada con los datos (el estado)?

<div align="justify">

React mantiene la interfaz sincronizada con los datos mediante el estado y el proceso de renderizado. Cuando el estado de un componente cambia mediante su mecanismo de actualización, React vuelve a renderizar el componente para reflejar los nuevos datos en la interfaz y actualiza el DOM donde sea necesario, sin que el desarrollador tenga que modificar manualmente cada elemento.

</div>

### ¿Qué rol juegan los componentes reutilizables en la solución de ese problema?

<div align="justify">

Los componentes reutilizables permiten dividir la interfaz de una aplicación en partes pequeñas e independientes que pueden utilizarse en diferentes secciones. Cada componente puede gestionar su propio estado o recibir datos de otros componentes. Esto facilita mantener la interfaz organizada y sincronizada con los datos, ya que React puede actualizar los componentes afectados cuando cambia la información, sin necesidad de modificar manualmente toda la interfaz. Además, favorecen la reutilización del código, reducen la duplicación y facilitan el mantenimiento de la aplicación.

</div>

## Punto 3 · Principales componentes de React

> **Actividad:** Para cada elemento, escribe su definición, características principales y un ejemplo de código cuando aplique, con una breve explicación.

### Componentes (qué son y cómo se crean)

<div align="justify">

Un componente es una parte independiente y reutilizable de la interfaz de usuario. Permite dividir una aplicación en secciones pequeñas, organizadas y fáciles de mantener. En React, los componentes se crean normalmente mediante funciones de JavaScript que devuelven JSX.

</div>

<div align="justify">

Algunas características de estos son:

</div>

- Se pueden utilizar en diferentes partes de una aplicación.
- Cada componente puede tener una responsabilidad específica.
- Se pueden combinar y anidar para crear interfaces más complejas.
- Se definen mediante funciones de JavaScript.
- Pueden mostrar información diferente según sus props y su estado.

<div align="justify">

Un ejemplo es:

</div>

```jsx
function Saludo() {
  return <h1>Hola, mundo</h1>;
}
```

En este caso, Saludo es un componente que devuelve un título. Se puede utilizar dentro de otro componente escribiendo \<Saludo />.

### JSX (qué es y sus reglas básicas)

<div align="justify">

JSX es una extensión de la sintaxis de JavaScript que permite escribir estructuras similares a HTML dentro del código JavaScript. React utiliza JSX para describir cómo debe verse la interfaz.

- El contenido devuelto debe estar agrupado en un elemento raíz o en un fragmento (<>...\</>).
- Cerrar todas las etiquetas: por ejemplo, \<img /> y \<input />.
- Usar className para las clases CSS en lugar de class.
- Utilizar llaves para expresiones JavaScript, por ejemplo, {nombre}.
- Escribir los nombres de los componentes con mayúscula inicial,  \<Saludo />.

Características principales: 

- Permite escribir etiquetas y elementos dentro de JavaScript.
- Utiliza llaves para incluir expresiones, como variables y cálculos.
- Permite agrupar elementos mediante un elemento raíz o un fragmento.
- Se transforma en código JavaScript para que las herramientas de React puedan 
interpretarlo.

</div>

### Props (qué son y para qué se usan)

<div align="justify">

Las props (propiedades) son datos que un componente recibe de su componente padre. Sirven para personalizar su contenido y comportamiento, lo que permite reutilizar el mismo componente con información diferente.

Características: 

- Permiten pasar datos de un componente padre a uno hijo.
- Son de solo lectura, el componente receptor no debe modificarse directamente.
- Un mismo componente puede mostrar diferentes contenidos.
- Pueden contener distintos tipos de valores como cadenas de texto, números, booleanos, arreglos, objetos y funciones.
- Permiten la comunicación entre componentes, por ejemplo, un padre puede pasar una función para que el hijo solicite una acción

Las props son los datos que se pasan a un elemento JSX. Por ejemplo, className, src, alt, width y height son algunas de las props que se pueden pasar a un elemento \<img> como se puede observar en el siguiente fragmento de codigo:

</div>

```jsx
function Avatar() {
  return (
    <img
      className="avatar"
      src="https://i.imgur.com/1bX5QH6.jpg"
      alt="Lin Lanying"
      width={100}
      height={100}
    />
  );
}

export default function Profile() {
  return <Avatar />;
}
```

### Estado(useState: qué es y cómo cambia la interfaz cuando el estado cambia)

<div align="justify">

El estado es información que un componente conserva entre sus renderizados y que puede cambiar durante la ejecución de la aplicación. Cuando el estado se actualiza mediante su función de actualización, React programa un nuevo renderizado para reflejar los cambios necesarios en la interfaz.

Características:

- Mantiene su valor entre renderizados del mismo componente mientras este conserve su identidad.
- Cuando el valor de un estado cambia, React vuelve a renderizar el componente de forma automática para actualizar la interfaz en la pantalla.
- El estado no se debe modificar directamente.
- El estado pertenece de manera local a cada instancia de un componente.

</div>

Ejemplo: 

```jsx
import { useState } from "react";

function Contador() {
  const [numero, setNumero] = useState(0);

  return (
    <div>
      <p>Contador: {numero}</p>
      <button onClick={() => setNumero(numero + 1)}>
        Aumentar
      </button>
  );
}
```
<div align="justify">
En este código useState(0) establece el valor inicial del estado en 0, número contiene el valor actual del estado y setNumero permite solicitar su actualización. Al pulsar el botón, el estado aumenta y React vuelve a renderizar el componente para mostrar el nuevo valor.

La ventaja principal es que no se necesita modificar manualmente el DOM cada vez que cambia el número ya que React se encarga de actualizar la interfaz según el estado.

</div>

### Eventos (onClick, onChange: cómo el usuario interactúa con la interfaz)

<div align="justify">

Los eventos permiten que la aplicación responda a las acciones del usuario, como hacer click en un botón, escribir en un campo de texto o seleccionar una opción.

Características:

- Permiten que la interfaz responda a las acciones del usuario, como hacer clic en un botón, escribir en un campo de texto o seleccionar una opción.
- Permiten modificar el estado de un componente a partir de las acciones del usuario, haciendo posible que la interfaz refleje los cambios.
- Proporcionan información sobre la interacción ocurrida, como el elemento que la originó o el valor introducido en un campo de texto.

### Evento onClick
Se utiliza para ejecutar una función cuando el usuario hace clic en un elemento.

</div>

```jsx
function Boton() {
  function saludar() {
    alert("¡Hola!");
  }

  return <button onClick={saludar}>Saludar</button>;
}
```
<div align="justify">
Cuando el usuario pulsa el botón, se ejecuta la función Saludar y onClick={saludar}, sin paréntesis, para pasar la función y permitir que React la ejecute cuando ocurra el evento.

### Evento onChange
Se utiliza habitualmente para responder a los cambios en campos de formulario, como los campos de texto.

</div>

```jsx
import { useState } from "react";

function CampoTexto() {
  const [nombre, setNombre] = useState("");

  return (
    <input
      value={nombre}
      onChange={(evento) => setNombre(evento.target.value)}
      placeholder="Escribe tu nombre"
    />
  );
}
```
<div align="justify">
En el anterior fragmento de código, value={nombre} hace que el campo muestre el valor guardado en el estado, onChange detecta los cambios que realiza el usuario. evento.target.value obtiene el texto que está escrito en el campo y setNombre actualiza el estado y permite que React mantenga sincronizado el campo con ese valor.
</div>

## Punto 4 · Importancia de React en la industria
<div align="justify">

> **Actividad:** Investiga y explica.

### ¿Por qué tantas empresas eligen React para sus productos web?
Las empresas eligen React porque permite construir interfaces interactivas mediante componentes reutilizables, lo que facilita organizar el código y mantener aplicaciones complejas. Además, permite actualizar la interfaz cuando cambian los datos, sin tener que modificar manualmente cada elemento del DOM. Su flexibilidad permite utilizarlo tanto en partes de una página como en aplicaciones web completas. Estas características facilitan el desarrollo y la colaboración entre equipos. (React, s. f.).

### ¿Qué aporta React al ecosistema de desarrollo (herramientas que lo rodean: empaquetadores, frameworks basados en React, etc.)?
React cuenta con un ecosistema de herramientas que amplían sus capacidades y facilitan el desarrollo de aplicaciones web. Por ejemplo, Vite permite preparar y ejecutar proyectos durante el desarrollo, mientras que Next.js incorpora funcionalidades como enrutamiento y renderizado en el servidor. También existen herramientas para depurar componentes, realizar pruebas y gestionar estilos. Estas tecnologías complementan a React y permiten adaptar el proceso de desarrollo a las necesidades de cada proyecto. (Vercel, s. f.).

### ¿Qué papel juegan su comunidad y su mantenimiento (quién lo mantiene hoy)?
La comunidad de React contribuye a su evolución mediante el desarrollo de herramientas, la documentación, la corrección de errores y el intercambio de conocimientos. Desde febrero de 2026, React pertenece a la React Foundation, una fundación independiente alojada en la Linux Foundation, con participación de empresas como Meta, Microsoft y Amazon. Sin embargo, la dirección técnica continúa en manos de las personas que contribuyen y mantienen el proyecto. Esta estructura busca favorecer la sostenibilidad y el desarrollo a largo plazo de su ecosistema. (Carroll, 2026).

### ¿Por qué es una habilidad relevante para un desarrollador front-end hoy en día?
Aprender React es relevante porque permite crear interfaces modernas, reutilizables e interactivas. Sus conceptos fundamentales, como componentes, props, estado y eventos, ayudan a organizar aplicaciones y gestionar los cambios en la interfaz. Además, conocer React facilita aprender herramientas complementarias como Next.js y trabajar en proyectos que utilizan esta tecnología. Por ello, dominarlo puede ampliar las oportunidades profesionales, especialmente cuando se combina con conocimientos sólidos de HTML, CSS y JavaScript. (React, s. f.).

## Punto 5 · Grandes empresas que utilizan React

### Meta (Facebook e Instagram)

Meta utiliza React en aplicaciones web como Facebook, Instagram y Threads. Un caso relevante es Instagram, donde React permite desarrollar interfaces interactivas que presentan publicaciones y contenido que cambia constantemente. La escala de estos productos demuestra la capacidad de React para trabajar con interfaces complejas y millones de usuarios. Según el equipo de React, también se ha implementado React Compiler en Instagram, Facebook y Threads para mejorar el rendimiento de sus aplicaciones (React, 2024).

### Shopify

Shopify utiliza React en su ecosistema de herramientas para comercio electrónico, entre ellas interfaces de administración para comerciantes. Este es un caso relevante porque sus aplicaciones deben presentar información de productos, pedidos y ventas, además de permitir que los usuarios interactúen con distintos controles. React facilita organizar estas interfaces en componentes reutilizables, lo que ayuda a desarrollar y mantener aplicaciones con funcionalidades complejas. La documentación oficial de React Native también incluye a Shopify entre las empresas que utilizan esta tecnología para aplicaciones móviles (React Native, s. f.).

### Airbnb

Airbnb utiliza React en las interfaces web de su plataforma, como las páginas que permiten buscar alojamientos y consultar anuncios. La empresa debe gestionar interfaces complejas, con filtros, resultados de búsqueda y contenido dinámico. En su blog oficial de ingeniería, Airbnb explica que actualizó sus interfaces web de React 16 a React 18, mostrando cómo mantiene y moderniza una aplicación de gran escala (Wiggins, 2024).
</div>

## Referencias
- Carroll, M. (2026, 24 de febrero). The React Foundation: A new home for React hosted by the Linux Foundation. React. [Leer referencia](https://react.dev/blog/2026/02/24/the-react-foundation)
- React. (s. f.). Describir la UI. [Leer referencia](https://es.react.dev/learn/describing-the-ui)
- React. (s. f.). Quick start. [Leer referencia](https://react.dev/learn)
- Vercel. (s. f.). Next.js documentation. [Leer referencia](https://nextjs.org/docs)
- Wiggins, A. (2024, 23 de julio). How Airbnb smoothly upgrades React. Airbnb Engineering. [Leer referencia](https://medium.com/airbnb-engineering/how-airbnb-smoothly-upgrades-react-b1d772a565fd)
- React. (2024, 21 de octubre). React Compiler Beta Release.[ https://react.dev/blog/2024/10/21/react-compiler-beta-release](https://react.dev/blog/2024/10/21/react-compiler-beta-release?utm_source=chatgpt.com)
- React Native. (s. f.). Showcase. [Leer referencia](https://reactnative.dev/showcase.html)
