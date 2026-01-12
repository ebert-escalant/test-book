---
icon: chart-pie
---

# Clase de Valorización

Catálogo de clases de valorización para los productos.

**Ruta:** Configuraciones → Clase de Valorización

## Operaciones Disponibles

### Buscar
1. Use el campo de búsqueda para filtrar por código o descripción
2. Haga clic en el botón **"Buscar"**
3. La tabla mostrará los resultados

### Sincronizar con SAP
1. Haga clic en **"Sincronizar con SAP"**
2. Confirme la acción en el mensaje emergente
3. Espere a que se complete la sincronización
4. Los datos se actualizarán automáticamente

{% hint style="info" %}
La sincronización descarga los datos actualizados desde SAP al sistema.
{% endhint %}
<!-- -->

### Editar
1. Localice el registro en la tabla
2. Haga clic en el ícono de edición (✏️)
3. Modifique el campo disponible

![Formulario Clase de Valorización](../.gitbook/assets/clase-valorizacion-form.png)

| Campo | Descripción |
|-------|-------------|
| Valor por defecto | Marca o desmarca si este material es el predeterminado |

4. Haga clic en **"Actualizar"**

{% hint style="warning" %}
Solo se puede editar el campo **"Valor por defecto"**. Los campos Código y Descripción son de solo lectura ya que provienen de SAP.
{% endhint %}
<!-- -->

### Campos

| Campo | Descripción |
|-------|-------------|
| Código | Código de la clase |
| Descripción | Nombre de la clase |
| Valor por defecto | Indica si es la clase predeterminada |

{% hint style="info" %}
La sincronización descarga los datos actualizados desde SAP al sistema.
{% endhint %}

{% hint style="success" %}
El valor por defecto se seleccionará automáticamente en los formularios de creación.
{% endhint %}

![Clase de Valorización](../.gitbook/assets/clase-valorizacion.png)
