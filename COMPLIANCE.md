# Compliance Check: Mili Aromas

Revisión: 2026-10-01 · Marco: legislación argentina. No reemplaza el asesoramiento de un abogado matriculado.

## Resumen

**Se puede publicar con condiciones.** Es un catálogo con carrito que cierra la venta por WhatsApp, así que cuenta como venta a distancia y le aplica Defensa del Consumidor. Pide nombre y notas al cliente y los guarda en el navegador.

## Qué datos trata

| Dato | Dónde |
|---|---|
| Nombre y notas (zona, horario) del cliente | `localStorage` (`miliaromas:pedido:v1`) y mensaje de WhatsApp |
| Pedido (productos, aromas, cantidades) | `localStorage` y WhatsApp (Meta) |

## Normas aplicables

| Norma | Por qué aplica | Qué exige |
|---|---|---|
| Ley 24.240 arts. 4 y 7 + Res. SCI 7/2002 | Oferta con precios al público | Precio final en pesos, con impuestos incluidos, y condiciones claras |
| Ley 24.240 art. 34 + Res. SCI 424/2020 | Venta a distancia por internet/WhatsApp | Derecho a revocar en 10 días corridos y "Botón de arrepentimiento" visible en la home |
| Res. SCI 270/2020 (Res. GMC 37/19) | Comercio electrónico | Identificar al proveedor (nombre o razón social, CUIT, domicilio, contacto) |
| Ley 25.326 art. 6 + Disp. 10/2008 | Formulario con nombre | Aviso de para qué se usa el dato y leyenda AAIP |
| ARCA (ex AFIP) | Venta online | Verificar con contador si corresponde Data Fiscal (F.960/D) y facturación |

## Requisitos

| # | Requisito | Estado | Acción |
|---|---|---|---|
| 1 | Precio final visible | Desconocido | Confirmar que los precios son finales con IVA incluido; si no, aclararlo |
| 2 | Datos del vendedor | No cumple | Agregar en el footer nombre del titular, CUIT y contacto (pedir al cliente, no inventar) |
| 3 | Botón de arrepentimiento | Parcial (01/10) | Link en el footer que abre WhatsApp con el pedido de revocación. La Res. 424/2020 lo pide en la primera pantalla: moverlo arriba cambia el diseño, queda a decisión. Mili tiene que responder con un número de trámite en 24 h |
| 4 | Condiciones de venta | No cumple | Entrega, medios de pago y cambios (ya figuran como pendientes en `PRODUCT.md`) |
| 5 | Aviso junto al formulario | Cumple (01/10) | Link "Cómo usamos tus datos" en el pie del carrito |
| 6 | Borrado local | Parcial | La política explica que el nombre queda en el navegador. Pendiente (cambia la función): que "Vaciar pedido" borre también el nombre |
| 7 | Política de privacidad | Parcial | `privacidad.html` enlazada en el footer, con derecho de revocación. Se quitó la sección de información legal (leyenda AAIP y link a Defensa del Consumidor) a pedido, porque el emprendimiento no está registrado |

## Riesgos

| Riesgo | Severidad | Mitigación |
|---|---|---|
| Falta de botón de arrepentimiento e identificación del vendedor | Media | Requisitos 2 y 3 (multas de Defensa del Consumidor) |
| Precios sin aclarar si son finales | Media | Requisito 1 |
| Nombre persistido sin aviso | Baja | Requisitos 5 y 6 |

## Acciones recomendadas

1. Pedirle a Mili titular, CUIT y condiciones de venta.
2. Agregar botón de arrepentimiento y datos del vendedor en el footer.
3. Aviso de privacidad bajo el formulario y política en el footer.

## Aprobaciones

| Quién | Por qué | Estado |
|---|---|---|
| Mili (titular) | Datos fiscales y condiciones de venta | Pendiente |
| Contador/a | Data Fiscal y facturación | Pendiente |
