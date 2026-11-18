[← Índice](README.md)

# NonDesigner – Preguntas frecuentes (FAQ) y solución de problemas

Respuestas a las preguntas más habituales sobre el módulo **NonDesigner** para PrestaShop (diseñador gráfico 2D para productos personalizados con archivos SVG listos para imprimir).

## Compatibilidad y requisitos

### ¿Con qué versiones de PrestaShop funciona NonDesigner?
Desde PrestaShop **1.7.6.1** hasta las versiones **8.x** y **9.x**.

### ¿Qué versión de PHP necesita NonDesigner?
Se admiten las versiones de **PHP 7.2 a 8.5**. Se necesitan las extensiones **GD Library, cURL, Zip y SimpleXML**.

### ¿NonDesigner requiere activar una licencia?
No. Una vez instalado y configurado, está inmediatamente operativo. [Detalles](instalacion.md).

### ¿NonDesigner es compatible con Multitienda de PrestaShop?
Sí. Los ajustes, las formas, las fuentes y la limpieza de diseños son compatibles con Multitienda nativo; con varias tiendas puede tener configuraciones y catálogos de fuentes distintos para cada una. En Multitienda, un control impide visualizar o exportar diseños de otra tienda («Acceso denegado»).

### ¿Cómo gestiona NonDesigner las fuentes en relación con el RGPD?
El módulo no carga las fuentes desde servicios externos en tiempo real: descarga los archivos `.ttf` en su servidor y los sirve localmente. [Detalles](configuracion-modulo.md#pestaña-gestión-de-fuentes).

## Archivos de impresión

### ¿Qué archivos genera NonDesigner para la impresión?
Para cada pedido recibido genera un archivo **SVG vectorial** y un **PNG a escala 1:1**, gestionados desde el back office. [Cómo descargarlos](pedidos-y-exportacion-svg.md).

### ¿Con qué programa abro los archivos SVG de NonDesigner?
Con **Inkscape** (gratuito), que permite también exportarlos a otros formatos compatibles con programas de diseño gráfico.

### ¿Cómo evito los márgenes blancos tras el corte del producto impreso?
Establezca el **margen de sangrado** (normalmente 2-3 mm por lado; pregunte el valor a su proveedor de impresión). [Detalles](dimensiones-producto.md#1-margen-de-sangrado-por-lado-mm).

### ¿Los diseños aparecen en los correos de confirmación del pedido?
No. El correo incluye un texto que indica la presencia de un diseño personalizado, consultable en el historial de pedidos de la cuenta del cliente.

## Problemas frecuentes

### Subo una imagen grande, pero el sistema devuelve un error. ¿Cómo lo resuelvo?
**Causa:** el tamaño del archivo supera el límite permitido por el módulo o por el servidor.

**Solución:** compruebe el valor establecido en *Configuración General → Tamaño máximo de imagen de usuario (MB)*. Si es correcto, verifique con su proveedor de hosting los límites `upload_max_filesize` y `post_max_size` en el archivo `php.ini` del servidor. [Detalles](configuracion-modulo.md#2-tamaño-máximo-de-imagen-de-usuario-mb).

### Las dimensiones del producto se leen como 0 / 0 en el frontend. ¿Cómo lo resuelvo?
**Causa:** está utilizando el método «Atributos separados» o «Valores combinados», pero el nombre/valor del atributo contiene caracteres no válidos o varios números no separados correctamente.

**Solución:** consulte de nuevo [Cómo establecer las dimensiones de impresión](dimensiones-producto.md). Para los valores combinados, utilice la letra `x` (por ejemplo, `50x70`) y **no** guiones (`-`) ni barras (`/`). Para los atributos separados, cada valor debe contener un único número.

### La limpieza automática de carritos abandonados no se inicia. ¿Cómo lo resuelvo?
**Causa:** la URL de la tarea Cron no se ha configurado correctamente en el panel del servidor (cPanel/Plesk).

**Solución:** copie la URL completa que se muestra en la pestaña *Configuración de herramientas* y asegúrese de que el servidor realice una llamada **HTTP GET** (por ejemplo, mediante `wget` o `curl`). [Detalles](configuracion-modulo.md#4-limpieza-de-diseños-de-carritos-abandonados).

### ¿Cómo gestiono las diferencias de precio (frente/reverso, esquinas redondeadas, sin impresión)?
NonDesigner no modifica el precio: utilice las combinaciones/variantes de PrestaShop. [Guía con ejemplo práctico](precios-y-variantes.md).

### ¿Puedo permitir la compra del producto sin personalización?
Sí: deje visible la opción «Activar el botón Añadir al carrito» y cree una variante «Sin impresión». [Cómo hacerlo](precios-y-variantes.md#a-cómo-vendo-también-el-producto-neutro-sin-impresión).

## Asistencia

### ¿Cómo contacto con el soporte técnico de NonDesigner?
Inicie sesión en su cuenta de **PrestaShop Addons**, vaya a **Mis compras** y envíe un mensaje a través del ticket de soporte del módulo. Las solicitudes se responden en un plazo de **24-48 horas laborables**.

---

*Antes de instalar el módulo, realice siempre una copia de seguridad de sus archivos y de su base de datos, y pruébelo primero en un servidor de pruebas.*
