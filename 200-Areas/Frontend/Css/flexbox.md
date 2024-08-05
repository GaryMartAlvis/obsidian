(Flexible Box Layout - Diseño flexible de casa)

### Contenedor Flex (Propiedades del contenedor)
- **`display: flex`** o **`display: inline-flex`**: Define un contenedor flexible.
- **`flex-direction`**: `row`, `row-reverse`, `column`, `column-reverse`. Define la dirección en la que se colocarán los elementos flexibles. 
- **`flex-wrap`**: `nowrap`, `wrap`, `wrap-reverse`. Especifica si los elementos flexibles deben forzar una sola línea o pueden envolverse.
- **`flex-flow`**: Una abreviatura para combinar `flex-direction` y `flex-wrap`.
- **`justify-content`**: `flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `space-evenly`. Alinea los elementos flexibles a lo largo del eje principal.
- **`align-items`**: `flex-start`, `flex-end`, `center`, `baseline`, `stretch`. Alinea los elementos flexibles a lo largo del eje transversal.
- **`align-content`**: `flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `stretch`. Alinea las líneas del contenedor flexible cuando hay espacio extra en el eje transversal.

### Elementos Flex (Propiedades de los elementos flexibles)
- **`order`**: Define el orden de los elementos flexibles.
- **`flex-grow`**: Define la capacidad de un elemento flexible para crecer si es necesario.
- **`flex-shrink`**: Define la capacidad de un elemento flexible para encogerse si es necesario.
- **`flex-basis`**: Define el tamaño principal inicial de un elemento flexible.
- **`flex`**: Una abreviatura para `flex-grow`, `flex-shrink` y `flex-basis`.
- **`align-self`**: Permite al elemento flexible alinearse en el eje transversal, sobrescribiendo el valor de `align-items`.
    - Valores: `auto`, `flex-start`, `flex-end`, `center`, `baseline`, `stretch`.

```css
.container {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  align-content: space-around;
}

.item {
  flex: 1 1 100px; /* flex-grow, flex-shrink, flex-basis */
  order: 2;
  align-self: flex-start;
}
```