---
icon: chart-bar
---

# Grupo de Artículos

Gestiona la jerarquía de productos organizada en 5 niveles.

**Ruta:** Configuraciones → Grupo de Artículos

## Operaciones Disponibles

### Buscar
- Use el campo de búsqueda para filtrar por código o descripción
- La tabla se actualiza automáticamente

### Sincronizar con SAP
- Haga clic en **"Sincronizar con SAP"**
- Confirme la acción
- Se descargarán los datos actualizados desde SAP

{% hint style="info" %}
La sincronización descarga los datos actualizados desde SAP al sistema.
{% endhint %}

### Crear Nuevo
1. Haga clic en **"Nuevo"**
2. Complete el formulario con la información del grupo de artículos

<figure><img src="../.gitbook/assets/grupo-articulos-form.png" alt=""><figcaption></figcaption></figure>

| Campo | Descripción |
|-------|-------------|
| Nivel 1 | Categoría principal del producto |
| Nivel 2 | Subcategoría del producto |
| Nivel 3 | División específica |
| Nivel 4 | Línea del producto |
| Nivel 5 | Sublínea o detalle final |
| Código cubo | Identificador único del artículo |
| Largo | Dimensión de largo |
| Ancho | Dimensión de ancho |
| Alto | Dimensión de alto |
| UM Dimensiones | Unidad de medida para dimensiones |
| Volumen | Volumen del artículo |
| UM Volumen | Unidad de medida para volumen |
| Peso | Peso del artículo |
| UM Peso | Unidad de medida para peso |

3. Haga clic en **"Guardar"**

{% hint style="success" %}
El nuevo grupo de artículos quedará disponible para usar en la generación de códigos.
{% endhint %}

### Editar
1. Localice el registro en la tabla
2. Haga clic en el ícono de edición (✏️)
3. Modifique los campos necesarios
4. Haga clic en **"Guardar"**

{% hint style="warning" %}
**Restricción:** Solo se pueden editar los registros creados manualmente. Los registros sincronizados desde SAP no se pueden modificar.
{% endhint %}

### Eliminar
1. Localice el registro en la tabla
2. Haga clic en el ícono de eliminar (🗑️)
3. Confirme la acción

{% hint style="danger" %}
**Restricción:** Solo se pueden eliminar los registros creados manualmente. Los registros sincronizados desde SAP no se pueden eliminar.
{% endhint %}

## Campos

| Campo | Descripción |
|-------|-------------|
| Código cubo | Identificador único |
| Largo | Dimensión largo |
| Ancho | Dimensión ancho |
| Alto | Dimensión alto |
| UM Dimensiones | Unidad de medida |
| Volumen | Volumen calculado |
| UM Volumen | Unidad de volumen |
| Peso | Peso del artículo |
| UM Peso | Unidad de peso |
| Nivel 1 | Categoría principal |
| Nivel 2 | Subcategoría |
| Nivel 3 | División |
| Nivel 4 | Línea |
| Nivel 5 | Sublínea |

![Grupo de artículos](../.gitbook/assets/grupo-articulos.png)

## Jerarquía de Niveles

```
Nivel 1 (Categoría)
└── Nivel 2 (Subcategoría)
    └── Nivel 3 (División)
        └── Nivel 4 (Línea)
            └── Nivel 5 (Sublínea)
```

{% hint style="info" %}
Los niveles se usan en la generación de códigos para clasificar los productos.
{% endhint %}
