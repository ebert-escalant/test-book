---
icon: print
---

# Impresora Bluetooth

Configuración para impresión de códigos de barras mediante Bluetooth.

<!-- -->

## Habilitar Bluetooth en Chrome

{% hint style="warning" %}
Este paso es **obligatorio** para usar la impresión Bluetooth.
{% endhint %}

1. Abra Google Chrome
2. En la barra de direcciones escriba:
   ```
   chrome://flags/#enable-web-bluetooth-new-permissions-backend
   ```
3. Presione **Enter**
4. Busque la opción y cámbiela a **"Enabled"**
5. Haga clic en **"Relaunch"** para reiniciar el navegador

![Configuración de chrome](../.gitbook/assets/chrome-bluetooth.png)

## Conectar Impresora

1. Encienda su impresora de códigos de barras Bluetooth
2. Asegúrese de que esté en modo de emparejamiento
3. En el sistema, acceda a la función de impresión
4. Haga clic en **"Seleccionar impresora"**
5. El navegador mostrará los dispositivos Bluetooth disponibles
6. Seleccione su impresora de la lista
7. Confirme la conexión

{% hint style="success" %}
La impresora quedará guardada para futuras impresiones.
{% endhint %}
<!-- -->

## Solución de Problemas

**No aparece el dispositivo**

| Problema | Solución |
|----------|----------|
| Impresora apagada | Verifique que esté encendida |
| Modo incorrecto | Active modo de emparejamiento |
| Bluetooth bloqueado | Reinicie el Bluetooth de la impresora |
| Lista desactualizada | Actualice la lista de dispositivos |

**Error de conexión**

| Problema | Solución |
|----------|----------|
| Web Bluetooth deshabilitado | Habilite la opción en chrome://flags |
| Cache del navegador | Reinicie el navegador completamente |
| Emparejamiento corrupto | Desempareje y vuelva a emparejar |

**No imprime**

| Problema | Solución |
|----------|----------|
| Sin papel | Verifique que tenga papel/etiquetas |
| Batería baja | Revise el nivel de batería |
| Desconectado | Verifique la conexión Bluetooth |

{% hint style="danger" %}
Si los problemas persisten, contacte al equipo de soporte técnico.
{% endhint %}
