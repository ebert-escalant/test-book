---
icon: circles
---

# Grupo Artículo y Tallero

Configuración de la relación entre grupos de artículos y talleros.

**Ruta:** Configuraciones → Grupo Artículo y Tallero

## Operaciones Disponibles

### Buscar
- Use el campo de búsqueda para filtrar por código o descripción
- La tabla se actualiza automáticamente

### Sincronizar con SAP
1. Haga clic en **"Sincronizar con SAP"**
2. Confirme la acción en el mensaje emergente
3. Espere a que se complete la sincronización
4. Los datos se actualizarán automáticamente

{% hint style="info" %}
La sincronización descarga los datos actualizados desde SAP al sistema.
{% endhint %}

### Editar
1. Localice el registro en la tabla
2. Haga clic en el ícono de edición (✏️)
3. Modifique los campos necesarios
4. Haga clic en **"Guardar"**

{% hint style="warning" %}
**Restricción:** Solo se pueden editar los registros creados manualmente. Los registros sincronizados desde SAP no se pueden modificar. Esta configuración determina qué tallero se muestra automáticamente al generar códigos para un grupo de artículo específico.
{% endhint %}

| Campo | Descripción |
|-------|-------------|
| Grupo artículo nivel 4 | Línea del producto |
| Grupo artículo nivel 5 | Sublínea del producto |
| Tallero asociado | Tallero vinculado |

**Crear Relación**

1. Haga clic en **"Nuevo"**
2. Seleccione el Grupo artículo nivel 4
3. Seleccione el Grupo artículo nivel 5
4. Seleccione el Tallero correspondiente
5. Haga clic en **"Guardar"**

{% hint style="warning" %}
Esta configuración determina qué tallero se muestra automáticamente al generar códigos para un grupo de artículo específico.
{% endhint %}

![Grupo Artículo y Tallero](../.gitbook/assets/grupo-articulo-tallero.png)
