# AdminExpress – Página de Login

Actividad en Clase – Semana 2
**Asignatura:** Ingeniería Web – Universidad de las Américas (UDLA)
**Autor:** Sebastián Almachi

## Descripción

Réplica del diseño de una página de inicio de sesión ("AdminExpress") hecha solo con **HTML y CSS**. El trabajo se enfoca en el diseño: la estructura se arma con **CSS Grid** y se adapta a distintos tamaños de pantalla con **Media Queries**.

## Estructura del proyecto

```
Actividad en Clase-Semana2/
├── index.html   → Estructura de la página
├── style.css    → Estilos, Grid y Media Queries
└── README.md
```

## Tecnologías utilizadas

- **HTML5**: etiquetas semánticas (`main`, `section`, `article`, `header`, `form`, `footer`).
- **CSS3**: Grid, Flexbox y Media Queries.
- **Font Awesome 6.4.0** (por CDN): íconos de sobre, candado y ojo en los campos.

## Estructura con HTML y Grid

El contenedor principal `.grid-container` divide la pantalla en dos columnas iguales:

```css
.grid-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    height: 100vh;
}
```

| Columna | Clase | Contenido |
|---|---|---|
| Izquierda | `.left-panel` | Fondo azul con el nombre **AdminExpress** |
| Derecha | `.right-panel` | Formulario de inicio de sesión (`.login-box`) |

Dentro de cada panel, el contenido se centra con Flexbox (`align-items` y `justify-content: center`). El formulario tiene un ancho máximo de `420px` para que no se estire en pantallas grandes.

## Uso de Media Queries

```css
@media (max-width: 768px) {
    .grid-container { grid-template-columns: 1fr; }
    .left-panel     { display: none; }
    ...
}
```

| Pantalla | Ancho | Comportamiento |
|---|---|---|
| Escritorio | más de 768px | Dos columnas: panel azul + formulario |
| Tablet / Móvil | hasta 768px | Una sola columna; se oculta el panel azul y queda solo el formulario, igual al diseño del celular |

En móvil también se reduce el tamaño del título y el padding del panel.

## Paleta de colores

| Color | Hex | Uso |
|---|---|---|
| Azul principal | `#0d6efd` | Panel izquierdo, botón y enlaces |
| Azul hover | `#0b5ed7` | Botón al pasar el mouse |
| Gris claro | `#fcfcfc` | Fondo del formulario |
| Gris texto | `#8c8c8c` | Subtítulo y texto secundario |

## Cómo ejecutarlo

1. Descargar o descomprimir la carpeta del proyecto.
2. Abrir `index.html` en cualquier navegador.
3. Para probar el diseño responsive, presionar **F12** y activar la vista de dispositivos (**Ctrl + Shift + M**), luego cambiar entre tamaños de pantalla.

> Se necesita conexión a internet para que carguen los íconos de Font Awesome.
