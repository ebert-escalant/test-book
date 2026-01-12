# Contabilizar Prendas

Control de inventario de prendas organizadas por cajas.

**Ruta:** Menú → Contabilizar prendas

## Listado

Muestra las órdenes de compra disponibles para contabilización:

| Columna | Descripción |
|---------|-------------|
| Pedido | Número de pedido |
| Nro de Embarque | Identificador |
| Proveedor | Nombre del proveedor |
| Estado | Estado de la orden |
| Acciones | Contabilizar |

![Listado contabilizar](../.gitbook/assets/contabilizar-lista.png)

## Buscar Orden

1. Use el campo de búsqueda
2. Escriba número de pedido, embarque o proveedor
3. La tabla se filtrará automáticamente

## Realizar Contabilización

1. Localice la orden deseada
2. Haga clic en **"Contabilizar"**
3. Complete el formulario:

| Campo | Descripción |
|-------|-------------|
| Caja | Código de la caja física |
| Código interno | Código del producto |
| Lista de variantes | Códigos escaneados |

4. Escanee o ingrese los códigos de las prendas
5. Verifique el resumen:
   * Código de caja
   * Código interno
   * Descripción
   * Color y talla
   * Cantidad
6. Haga clic en **"Guardar"**

![Formulario contabilizar](../.gitbook/assets/contabilizar-form.png)

{% hint style="success" %}
El sistema actualizará automáticamente el inventario al guardar.
{% endhint %}
