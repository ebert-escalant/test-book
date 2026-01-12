# Colores y Tallas

## Colores

Catálogo de colores disponibles para los productos.

**Ruta:** Configuraciones → Colores

**Campos:** Código, Descripción, Valor por defecto

![Listado de colores](../.gitbook/assets/colores.png)

---

## Tallero y Tallas

Gestión de talleros (conjuntos de tallas) y sus tallas asociadas.

**Ruta:** Configuraciones → Tallero y tallas

**Campos:**
* Código SAP Tallero
* Marca asociada
* Tallas (lista)

![Talleros](../.gitbook/assets/talleros.png)

{% hint style="info" %}
Cada tallero agrupa un conjunto de tallas específico. Por ejemplo: XS, S, M, L, XL para adultos o 2, 4, 6, 8 para niños.
{% endhint %}

---

## Grupo Artículo y Tallero

Configuración de la relación entre grupos de artículos y talleros.

**Ruta:** Configuraciones → Grupo Artículo y Tallero

**Campos:**
* Grupo artículo nivel 4 (Línea)
* Grupo artículo nivel 5 (Sublínea)
* Tallero asociado

### Crear Relación

1. Haga clic en **"Nuevo"**
2. Seleccione el Grupo artículo nivel 4
3. Seleccione el Grupo artículo nivel 5
4. Seleccione el Tallero
5. Haga clic en **"Guardar"**

{% hint style="warning" %}
Esta configuración determina qué tallero se muestra automáticamente al generar códigos para un grupo de artículo específico.
{% endhint %}
