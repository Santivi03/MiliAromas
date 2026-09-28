---
version: alpha
name: Mili Aromas
description: Catálogo con carrito que confirma pedidos por WhatsApp. La estética sale de la etiqueta del producto.
colors:
  primary: "#1D1A17"
  on-primary: "#FBF9F5"
  secondary: "#5B534B"
  tertiary: "#8A5F45"
  on-tertiary: "#FFFFFF"
  neutral: "#F5F0E9"
  surface: "#FBF9F5"
  surface-alt: "#ECE5DB"
  line: "#D6CABB"
  whatsapp: "#17784A"
  on-whatsapp: "#FFFFFF"
  danger: "#A23B2A"
typography:
  display:
    fontFamily: Bodoni Moda
    fontSize: 64px
    fontWeight: 500
    lineHeight: 1.02
    letterSpacing: -0.02em
  headline:
    fontFamily: Bodoni Moda
    fontSize: 36px
    fontWeight: 500
    lineHeight: 1.1
    letterSpacing: -0.01em
  title:
    fontFamily: Bodoni Moda
    fontSize: 24px
    fontWeight: 500
    lineHeight: 1.2
  body:
    fontFamily: Hanken Grotesk
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: Hanken Grotesk
    fontSize: 13px
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: 0.08em
  price:
    fontFamily: Hanken Grotesk
    fontSize: 18px
    fontWeight: 600
    lineHeight: 1.3
    fontFeature: '"tnum" 1'
rounded:
  none: 0px
  sm: 6px
  md: 12px
  full: 999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 40px
  xxl: 72px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    rounded: "{rounded.sm}"
    padding: 14px
  button-whatsapp:
    backgroundColor: "{colors.whatsapp}"
    textColor: "{colors.on-whatsapp}"
    rounded: "{rounded.sm}"
    padding: 16px
  chip:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    rounded: "{rounded.full}"
    padding: 10px
  chip-selected:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    rounded: "{rounded.full}"
  price-tag:
    textColor: "{colors.tertiary}"
    typography: "{typography.price}"
  card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    rounded: "{rounded.md}"
    padding: 24px
  section-alt:
    backgroundColor: "{colors.surface-alt}"
    textColor: "{colors.primary}"
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.secondary}"
  input:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    rounded: "{rounded.sm}"
  divider:
    backgroundColor: "{colors.line}"
    height: 1px
  field-error:
    textColor: "{colors.danger}"
    typography: "{typography.label}"
  badge:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.on-tertiary}"
    rounded: "{rounded.full}"
---

# Mili Aromas

## Overview

La página toma prestado el lenguaje de la etiqueta de los frascos: papel crema, tinta casi negra, una serif alta y un marco de línea fina. Se siente artesanal y ordenada, sin lujo impostado. La mayoría de las visitas llegan desde Instagram en el celular, así que el diseño se piensa primero para una mano y un pulgar.

## Colors

- **Tinta (#1D1A17):** texto principal, botones de acción y marcos.
- **Tinta suave (#5B534B):** texto secundario. Pasa 4.5:1 sobre papel y superficie.
- **Arcilla (#8A5F45):** precios y el contador del carrito. Es el único acento.
- **Papel (#F5F0E9)** y **superficie (#FBF9F5):** fondo de página y de tarjetas.
- **Papel oscuro (#ECE5DB):** bandas de sección.
- **Línea (#D6CABB):** separadores decorativos, nunca como único indicador de estado.
- **Verde WhatsApp (#17784A):** solo para el botón que abre WhatsApp. Es más oscuro que el verde de la marca para que el texto blanco tenga contraste.

## Typography

Bodoni Moda para títulos, porque tiene el contraste alto de la tipografía de la etiqueta. Hanken Grotesk para texto, formularios y precios, con cifras tabulares en los montos. Los inputs nunca bajan de 16px para que iOS no haga zoom.

## Layout

Contenedor de 1180px con márgenes laterales de 20px en celular. Productos en una columna en celular y en dos columnas de tarjetas horizontales desde 760px. Las secciones se separan con 72px de aire y bandas de color, no con sombras.

## Elevation & Depth

Casi plano. Las tarjetas usan borde de 1px y nada de sombra. La única elevación real es la del panel del pedido y la barra fija inferior, que flotan sobre el contenido con una sombra suave con desplazamiento.

## Shapes

Radio de 12px en tarjetas, 6px en botones e inputs y píldora solo en los chips de aroma y el contador. Las fotos llevan un marco fino inset, como la etiqueta.

## Components

- **Chips de aroma:** radios nativos con aspecto de píldora. Seleccionado en tinta sólida. Obligatorio elegir uno.
- **Stepper de cantidad:** botones − y + de 44px con el número en el medio.
- **Barra de pedido:** fija abajo cuando hay productos. Muestra cantidad y total y abre el panel.
- **Panel del pedido:** diálogo lateral con la lista editable, los datos del cliente y el botón de WhatsApp.
- **Placeholder sin foto:** marco con el nombre de la marca en vertical, igual que la etiqueta.

## Do's and Don'ts

- Usar fotos reales de producto. Si falta una, placeholder honesto, nunca la foto de otro producto.
- No inventar datos de envío, pagos, stock ni testimonios: salen de `CONFIG` o de la dueña.
- No usar emojis ni fuentes de íconos: SVG inline.
- No sumar colores de acento: arcilla para precios, verde solo para WhatsApp.
- Respetar `prefers-reduced-motion`.
