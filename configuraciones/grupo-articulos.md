# Grupo de Artículos

Gestiona la jerarquía de productos organizada en 5 niveles.

**Ruta:** Configuraciones → Grupo de Artículos

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
