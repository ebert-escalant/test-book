---
icon: cart-shopping
---

# Órdenes de Compra

Gestión de órdenes de compra vinculadas con SAP para el control de productos y generación de códigos.

{% hint style="info" %}
**Ruta:** Menú → Órdenes de compra
{% endhint %}

<!-- -->

## Listado de Órdenes

Al acceder verá la tabla con todas las órdenes de compra registradas.

![Listado de órdenes de compra](../.gitbook/assets/ordenes-lista.png)

### Columnas de la Tabla

| Columna | Descripción |
|---------|-------------|
| Pedido | Número de pedido/orden de SAP |
| Proveedor | Nombre del proveedor |
| Nro de Embarque | Identificador de embarque generado automáticamente |
| Paquete | Tipo de paquete |
| Temporada | Temporada del producto |
| Año | Año del pedido |
| Mes | Mes del pedido |
| Estado | Activo (abierto) / Inactivo (cerrado) |
| Acciones | Editar, Ver detalle |

## Buscar Órdenes

1. Localice el campo de búsqueda en la parte superior
2. Escriba el número de pedido, embarque o proveedor
3. Haga clic en **"Buscar"**
4. La tabla mostrará los resultados filtrados

## Crear Nueva Orden

### Paso 1: Abrir Formulario
1. Haga clic en el botón **"+ Nuevo"**
2. Se abrirá el modal "Vincular Orden de compra de SAP"

![Formulario de orden de compra](../.gitbook/assets/orden-form.png)

### Paso 2: Completar Campos

**Número de Pedido (Order Number)**
- Autocomplete con búsqueda dinámica
- Escriba el número de orden (mínimo 3 caracteres)
- El sistema buscará órdenes en SAP en tiempo real
- Seleccione la orden deseada de la lista
- Campo obligatorio

{% hint style="info" %}
Al seleccionar una orden, el sistema verificará automáticamente el proveedor y lo cargará en el campo correspondiente.
{% endhint %}

<!-- -->

**Proveedor**
- Se autocompleta al seleccionar el número de pedido
- Campo de solo lectura
- Muestra: Abreviatura - Descripción del proveedor
- Si el proveedor no tiene abreviatura, se abrirá un modal para ingresarla

{% hint style="warning" %}
Si aparece un mensaje de error "No se encontró el proveedor", use el botón de recarga (🔄) junto al campo para reintentar la búsqueda del proveedor.
{% endhint %}

<!-- -->

**Número de Embarque**
- Se genera automáticamente
- Formato: `[Proveedor][Paquete][Temporada][Año][Mes]`
- Campo de solo lectura
- Ejemplo: `PRO01V2501` (Proveedor: PRO, Paquete: 01, Temporada: V, Año: 25, Mes: 01)

**Paquete**
- Selector desplegable
- Muestra: Abreviatura - Descripción
- Campo obligatorio
- Afecta el número de embarque

**Temporada**
- Selector desplegable
- Muestra: Código - Descripción (ej: V - Verano)
- Campo obligatorio
- Afecta el número de embarque

**Año**
- Selector desplegable
- Muestra los últimos 20 años
- Por defecto: Año actual
- Campo obligatorio
- No editable después de crear la orden
- Afecta el número de embarque (se usan los últimos 2 dígitos)

**Mes**
- Selector desplegable
- Opciones: Enero (01) a Diciembre (12)
- Por defecto: Mes actual
- Campo obligatorio
- No editable después de crear la orden
- Afecta el número de embarque

### Paso 3: Guardar
1. Verifique que todos los campos estén completos
2. El número de embarque debe estar generado correctamente
3. Haga clic en **"Guardar"**
4. El sistema creará la orden y mostrará un mensaje de confirmación

{% hint style="warning" %}
Si no se encuentra ninguna orden con el número ingresado, aparecerá un mensaje "No se encontraron órdenes".
{% endhint %}

<!-- -->

## Editar Orden

1. Localice la orden en la tabla
2. Haga clic en el ícono **Editar** (✏️)
3. Se abrirá el formulario con los datos actuales

### Campos Editables

**En modo edición:**
- ✅ **Paquete**: Puede modificarse
- ✅ **Temporada**: Puede modificarse
- ❌ **Número de pedido**: No editable
- ❌ **Proveedor**: No editable (vinculado al pedido)
- ❌ **Año**: No editable
- ❌ **Mes**: No editable
- 🔄 **Número de embarque**: Se recalcula automáticamente si cambia paquete o temporada

4. Modifique los campos permitidos
5. Haga clic en **"Guardar"**

{% hint style="info" %}
Al cambiar paquete o temporada, el número de embarque se actualizará automáticamente manteniendo el resto de componentes.
{% endhint %}

<!-- -->

## Modal de Abreviatura de Proveedor

Si el proveedor de SAP no tiene una abreviatura registrada, aparecerá automáticamente un modal.

### Campos del Modal

| Campo | Descripción |
|-------|-------------|
| Código | Código del proveedor de SAP (solo lectura) |
| Proveedor | Nombre del proveedor (solo lectura) |
| Abreviatura | Abreviatura de 2-3 caracteres (editable, requerido) |

### Completar Abreviatura
1. Ingrese una abreviatura de 2 a 3 caracteres en mayúsculas
2. Haga clic en **"Guardar"**
3. El sistema actualizará el proveedor y cerrará el modal
4. La abreviatura se mostrará en el campo proveedor del formulario principal

{% hint style="success" %}
Una vez guardada la abreviatura, quedará registrada para futuras órdenes del mismo proveedor.
{% endhint %}

<!-- -->

## Acceder a Generar Códigos

La funcionalidad de generación de códigos está integrada dentro de cada orden de compra.

### Pasos para Acceder
1. Localice la orden de compra deseada en la tabla
2. Haga clic en el ícono de **Ver Detalle** (👁️) en la columna Acciones
3. Será redirigido automáticamente a la pantalla "Generar Códigos" de esa orden específica

{% hint style="info" %}
Cada orden de compra tiene su propio módulo de generación de códigos, permitiendo gestionar los productos específicos de ese pedido.
{% endhint %}

<!-- -->

## Características Especiales

**Búsqueda Dinámica de Órdenes SAP**
- Al escribir en el campo "Número de pedido", el sistema busca en tiempo real
- Usa debounce (retardo de 500ms) para optimizar búsquedas
- Muestra hasta 5 resultados coincidentes
- Carga automáticamente el proveedor al seleccionar

**Generación Automática de Número de Embarque**
- Se compone de partes de diferentes campos
- Se actualiza en tiempo real al cambiar cualquier componente
- Formato: Abreviatura Proveedor + Abreviatura Paquete + Código Temporada + Año (2 dígitos) + Mes (2 dígitos)

**Validación de Proveedor**
- Verifica que el proveedor exista en la base de datos local
- Si no existe, lo crea automáticamente desde SAP
- Solicita abreviatura si no está registrada
- Botón de recarga disponible para reintentar verificación

**Vista Responsive**
- En dispositivos móviles y tablets, la tabla se transforma en tarjetas
- Facilita la visualización y gestión desde cualquier dispositivo
- Mantiene todas las funcionalidades en formato optimizado
