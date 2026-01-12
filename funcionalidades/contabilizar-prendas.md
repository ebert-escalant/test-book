---
icon: box
---

# Contabilizar Prendas

Control de inventario de prendas organizadas por cajas vinculadas a órdenes de compra.

{% hint style="info" %}
**Ruta:** Menú → Contabilizar prendas
{% endhint %}

<!-- -->

## Listado de Órdenes de Compra

Muestra las órdenes de compra disponibles para contabilización.

![Listado de órdenes de compra](../.gitbook/assets/contabilizar-lista.png)

### Buscar Orden
1. Use el campo de búsqueda en la parte superior
2. Escriba número de pedido, embarque o proveedor
3. Haga clic en **"Buscar"**
4. La tabla mostrará los resultados

### Columnas de la Tabla

| Columna | Descripción |
|---------|-------------|
| Pedido | Número de pedido |
| Nro de Embarque | Número de embarque |
| Proveedor | Nombre del proveedor |
| Estado | Estado de la orden |
| Acciones | Botón para desplegar la lista de contabilización de prendas |

## Gestión de Cajas Contabilizadas

Una vez dentro de una orden de compra, podrá ver y gestionar las cajas contabilizadas.

### Filtros de Búsqueda

| Campo | Descripción |
|-------|-------------|
| Buscar | Filtrar por código de caja, código interno o descripción de producto (incluye escáner QR) |
| Usuario | Filtrar por usuario que registró |
| Fecha inicio | Fecha de inicio del rango |
| Fecha fin | Fecha de fin del rango |

### Operaciones Disponibles

**Crear Nuevo**
1. Haga clic en **"+ Nuevo"**
2. Complete el formulario de contabilización
3. Agregue las variantes con sus cantidades
4. Haga clic en **"Guardar"**

**Editar**
1. Localice la caja en la tabla
2. Haga clic en el ícono de edición (✏️)
3. Modifique las variantes o cantidades
4. Haga clic en **"Guardar"**

**Ver Detalle**
1. Localice la caja en la tabla
2. Haga clic en el ícono de visualización (👁️)
3. Podrá ver el detalle sin poder modificar

**Eliminar**
1. Localice la caja en la tabla
2. Haga clic en el ícono de eliminar (🗑️)
3. Confirme la acción

### Tabla de Cajas Contabilizadas

| Columna | Descripción |
|---------|-------------|
| Código de caja | Identificador único de la caja física |
| Fecha de registro | Fecha y hora de creación |
| Usuario | Usuario que registró la caja |
| Cantidad | Total de prendas en la caja |
| Acciones | Editar, Eliminar, Ver detalle |

## Formulario de Contabilización

![Formulario de contabilización](../.gitbook/assets/contabilizar-form.png)

### Campos del Formulario

**1. Código de Caja**
- Identificador único de la caja física
- Se puede escanear con QR usando el ícono de cámara
- Campo obligatorio
- Solo se puede definir una vez, no se puede modificar si ya existen registros

**2. Código Interno**
- Código del producto a contabilizar
- Se puede escanear con QR usando el ícono de cámara
- Campo obligatorio
- Al ingresarlo y presionar Enter o perder el foco, carga automáticamente las variantes del producto

**3. Variantes del Producto**
- Se muestran automáticamente al ingresar el código interno
- Agrupadas por color del producto
- Muestra: Descripción del producto y Color
- Para cada talla se muestra un campo de cantidad

**Campos de Variante:**
- **Talla**: Tamaño de la prenda
- **Cantidad**: Número de prendas de esa variante (opcional, puede dejarse vacío si no hay unidades)

{% hint style="info" %}
Al perder el foco en un campo de cantidad, el sistema verifica si esa variante ya existe en otras cajas y muestra un mensaje informativo con las cantidades por caja.
{% endhint %}

<!-- -->

**4. Agregar Variantes a la Caja**
1. Ingrese las cantidades en las tallas deseadas
2. Haga clic en **"Agregar"**
3. Las variantes se agregarán a la tabla inferior
4. Si ingresa otra variante del mismo código interno, puede seguir agregando
5. Si una variante ya existe en la tabla, se sumará la cantidad

{% hint style="warning" %}
Debe ingresar cantidad en al menos una variante para poder agregar.
{% endhint %}

<!-- -->

### Tabla de Detalle de la Caja

Muestra todas las variantes agregadas a la caja:

| Columna | Descripción |
|---------|-------------|
| Código de caja | Identificador de la caja |
| Código interno | Código del producto |
| Descripción | Nombre del producto |
| Color y talla | Color y talla de la prenda |
| Cantidad total | Número de prendas |
| Acciones | Eliminar (🗑️) - solo en modo edición |

{% hint style="success" %}
Las filas resaltadas en amarillo (cuando está en modo edición de caja existente) indican variantes nuevas que aún no estaban en el registro original.
{% endhint %}

<!-- -->

### Guardar la Contabilización

1. Verifique que todos los datos en la tabla sean correctos
2. Haga clic en **"Guardar"**
3. El sistema actualizará automáticamente el inventario
4. Se cerrará el formulario y volverá a la lista de cajas

{% hint style="warning" %}
No se puede guardar si no hay al menos una variante agregada a la tabla.
{% endhint %}

<!-- -->

## Características Especiales

**Escaneo con Cámara**
- Tanto el código de caja como el código interno tienen un ícono de cámara (QR)
- Al hacer clic, se abre el escáner de códigos QR/códigos de barras
- Facilita la captura rápida de información

**Validaciones**
- El sistema valida que el código de caja sea único
- Verifica que el código interno exista en la orden de compra
- Muestra alertas si una variante ya está en otras cajas
- Calcula automáticamente el total de prendas por caja

**Vista Responsive**
- En dispositivos móviles y tablets, la tabla se transforma en tarjetas
- Facilita la visualización y gestión desde cualquier dispositivo
