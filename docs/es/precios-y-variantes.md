[← Índice](README.md) · [← Pedidos y exportación SVG](pedidos-y-exportacion-svg.md) · Página siguiente: [FAQ →](faq.md)

# Cómo gestionar precios y variantes de los productos personalizados con NonDesigner

## ¿NonDesigner modifica el precio del producto?

No. El módulo **NonDesigner** gestiona **exclusivamente la interfaz gráfica** y la experiencia de personalización visual; **no modifica directamente el precio** del producto.

Todas las diferencias de precio (recargos o descuentos por las opciones de procesamiento, como la impresión frontal/trasera, las esquinas redondeadas o la ausencia de impresión) deben gestionarse **de forma nativa a través de las combinaciones/variantes de PrestaShop**.

## ¿Cómo establezco el precio de la impresión frontal/trasera, las esquinas redondeadas o la ausencia de impresión? (ejemplo práctico)

### A. ¿Cómo vendo también el producto neutro sin impresión?

Para ofrecer tanto el producto en bruto/sin imprimir como el personalizado:

1. Cree un grupo de atributos (por ejemplo, **«Impresión»**) y añada entre sus valores la opción **«Sin impresión»** (o «Sin personalización»).
2. Asigne al valor «Sin impresión» el **precio base** del producto sin procesar.
3. Establezca la opción **Activar el botón «Añadir al carrito»** en **Sí** (consulte [Configuración del producto](configuracion-producto.md#qué-hace-la-opción-activar-el-botón-añadir-al-carrito)).

### B. ¿Cómo establezco los recargos de las opciones de impresión?

1. Cree los valores para las opciones de impresión (por ejemplo, **«Impresión solo frontal»**, **«Impresión frontal y trasera»**, **«Esquinas redondeadas»**).
2. En el panel **Combinaciones** de PrestaShop, establezca el **impacto en el precio** (recargo) de cada combinación que implique procesamiento.
3. En la pestaña **NonDesigner** del producto, **asigne los valores de atributo** a las opciones correspondientes del módulo (por ejemplo, vincule «Impresión frontal y trasera» con el modo frente/reverso del diseñador). Consulte [impresión frontal/trasera](configuracion-producto.md#cómo-configuro-la-impresión-frontaltrasera) y [esquinas redondeadas](configuracion-producto.md#cómo-configuro-las-esquinas-redondeadas).

### Resultado

Cuando el cliente selecciona la variante en la página del producto **antes de abrir el diseñador**, PrestaShop calcula y aplica automáticamente el **precio correcto en el carrito**.

---

Página siguiente: [FAQ →](faq.md)
