### Colores Principales
```css
/* Fondo principal */
background-color: #2a2d32;

/* Borde y detalles */
border-color: rgb(255, 255, 255);

/* Hover en botones */
background-color: rgba(255, 255, 255, 0.5);

/* Sombras y efectos */
box-shadow: 0px 0px 15px rgba(0, 255, 0, 0.3);
```

### Tipografías Usadas
- **Bezaen** (Personalizada, utilizada en los títulos principales)
- **Bellerose** (Sans-serif, usada en los textos generales)

```css
@font-face {
    font-family: 'Bezaen';
    src: url('../fonts/Bezaen.otf') format('opentype');
}

* {
    font-family: 'Bellerose', sans-serif;
}
```

## Logo Personal
El logo personal se encuentra en **img/logo.png**.

## Librerías Utilizadas
- [FontAwesome 6.5.1](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css) → Para iconos
- [Bootstrap](https://getbootstrap.com/) → Para estructurar algunos elementos
- [W3Schools](https://www.w3schools.com/) → Referencias y snippets de código
- [Eniun](https://eniun.com/) → Recursos adicionales

## Enlaces a Código Usado
- [W3Schools](https://www.w3schools.com/)
- [Eniun](https://eniun.com/)

## Problemas Técnicos y Soluciones

### Oscurecer la Imagen de Fondo del Header
**Problema:** El fondo de la cabecera no tenía suficiente contraste con el texto.

**Solución:** Se agregó un **degradado semitransparente** encima del fondo.
```css
header {
    background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url('../img/header.gif') center/cover no-repeat;
}
```

### Enlace del Botón "Contáctame"
**Problema:** El botón redirigía a "#" en lugar de la página de contacto.

**Solución:** Se cambió el enlace a **contact.html**.
```html
<a href="contact.html" class="contact-btn">Contáctame</a>
```

### Ajuste de Iconos en la Sección de Habilidades
**Problema:** Los iconos no estaban alineados correctamente en diferentes dispositivos.

**Solución:** Se utilizó **grid CSS** para organizar las imágenes de las herramientas.
```css
.iconos-skills {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(70px, 1fr));
    gap: 15px;
    justify-content: center;
}
```