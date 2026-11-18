# NonDesigner – Guía del usuario y manual de configuración (español)

**NonDesigner** es un **módulo de PrestaShop** que añade a la ficha de producto un **diseñador gráfico 2D** (editor / personalizador de productos). Los clientes añaden textos, imágenes, formas, fuentes y códigos QR para personalizar los productos en línea y, para cada pedido, el módulo genera automáticamente **archivos listos para imprimir: SVG vectorial y PNG a escala 1:1**, que se pueden gestionar directamente desde el back office de PrestaShop.

- Sitio web oficial: [nondesigner.com/es/](https://www.nondesigner.com/es/)
- Demo en línea: [nondesigner.com/demonondesigner/es/](https://www.nondesigner.com/demonondesigner/es/)
- Compra en PrestaShop Addons: [NonDesigner - Diseñador gráfico 2D para productos personalizados](https://addons.prestashop.com/es/variantes-de-productos/99215-nondesigner-disenador-grafico-2d-para-productos-personalizados.html)
- Desarrollador: [Media Web](https://www.mediaweb-x.com/)

🌐 **Idiomas:** Español (esta guía) · [todos los idiomas](../../README.md)

## Funciones principales

- Diseñador gráfico 2D en la ficha de producto, con paneles activables uno a uno: texto, imágenes, formas, capas, código QR, filtros de fotos, efectos de imagen.
- Generación automática de archivos **SVG vectoriales listos para imprimir** y **PNG 1:1** para cada pedido recibido.
- Impresión **frontal/trasera** (solo frente, frente/reverso idéntico, frente/reverso diferente).
- **Tres métodos de cálculo del tamaño** del área de impresión: dimensiones fijas, atributos separados (ancho/alto) o valores combinados (An x Al).
- **Margen de sangrado** configurable para evitar márgenes blancos tras el corte.
- Formas de producto rectangulares o redondas, con esquinas cuadradas o redondeadas.
- Fuentes instaladas **localmente en su propio servidor** (sin carga externa en tiempo real).
- Compatibilidad nativa con **Multitienda** de PrestaShop.
- Limpieza automática (Cron) o manual de los diseños de carritos abandonados.
- No requiere activación de licencia.

## Requisitos del sistema de un vistazo

| Requisito | Valor |
|---|---|
| Versiones de PrestaShop compatibles | de 1.7.6.1 a 8.x y 9.x |
| Versiones de PHP compatibles | de PHP 7.2 a PHP 8.5 |
| Extensiones PHP necesarias | GD Library, cURL, Zip, SimpleXML |
| Directivas PHP recomendadas | `upload_max_filesize` ≥ 10M, `post_max_size` ≥ 10M |

Detalles: [Requisitos e instalación](instalacion.md).

## Índice

1. [Cómo instalar el módulo NonDesigner en PrestaShop](instalacion.md) – requisitos del sistema, compatibilidad, instalación.
2. [Cómo configurar el módulo NonDesigner (ajustes globales)](configuracion-modulo.md) – pestañas General, Gestión de formas, Gestión de fuentes, Configuración de herramientas, limpieza de carritos abandonados.
3. [Cómo configurar el diseñador en un producto](configuracion-producto.md) – activación, impresión frontal/trasera, forma del producto, plantilla PDF, aplicación masiva a una categoría.
4. [Cómo establecer las dimensiones de impresión del producto](dimensiones-producto.md) – margen de sangrado y los tres métodos de cálculo del tamaño, formatos aceptados y errores frecuentes.
5. [Cómo gestionar los pedidos y descargar archivos SVG listos para imprimir](pedidos-y-exportacion-svg.md) – diseño en el back office, exportación SVG y JSON, seguridad.
6. [Cómo gestionar precios y variantes de los productos personalizados](precios-y-variantes.md) – recargos por impresión frontal/trasera, esquinas redondeadas, producto sin impresión.
7. [Preguntas frecuentes (FAQ) y solución de problemas](faq.md).

## Soporte

Inicie sesión en su cuenta de **PrestaShop Addons**, vaya a **Mis compras** y envíe un mensaje a través del ticket de soporte del módulo. Las solicitudes se responden en un plazo de 24-48 horas laborables.

## Aviso

Antes de instalar el módulo, realice una copia de seguridad de los archivos de su servidor y de su base de datos y, si es posible, pruebe primero la instalación en un servidor de pruebas.

---

*NonDesigner está desarrollado y distribuido por Media Web.*
