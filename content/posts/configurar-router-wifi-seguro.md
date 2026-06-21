---
title: "Cómo configurar tu router WiFi de forma segura (guía completa)"
date: 2026-06-17
draft: false
description: "Tu router mal configurado es una puerta abierta a ataques. Guía paso a paso para asegurar tu WiFi en casa: contraseña, cifrado, red de invitados y más."
categories: ["Seguridad"]
tags: ["router", "wifi", "seguridad", "red doméstica", "contraseña wifi"]
cover:
    image: "images/posts/header-router-seguro.png"
    alt: "Cómo configurar tu router WiFi de forma segura (guía completa)"
    relative: false
---

La mayoría de los routers domésticos vienen con configuración de fábrica que es conveniente pero no segura. Con estos ajustes conviertes tu red WiFi en algo que los atacantes difícilmente pueden penetrar.

## Cómo acceder a la configuración del router

1. Abre el navegador y escribe en la barra de direcciones:
   - `192.168.1.1` (el más común)
   - `192.168.0.1` (alternativa frecuente)
   - `192.168.1.254` (algunos routers Livebox)
2. Busca la etiqueta en la parte trasera de tu router — suele tener la IP de administración y las credenciales por defecto
3. Inicia sesión con usuario/contraseña de administración

## Paso 1: Cambia la contraseña de administración del router

![Panel de configuración del router](/images/posts/router-panel-configuracion.png)

La primera vulnerabilidad es la contraseña de administración del router. La mayoría viene con `admin/admin` o `admin/1234`.

En el panel de administración busca: **Administración → Contraseña** o **Sistema → Cambiar contraseña**.

Usa una contraseña larga y única, diferente a la del WiFi.

## Paso 2: Actualiza el firmware

Los fabricantes lanzan actualizaciones que parchean vulnerabilidades de seguridad. Muchos routers tienen la opción de actualizar automáticamente.

Busca en el panel: **Administración → Actualización de firmware** o **Sistema → Software**.

## Paso 3: Usa el cifrado WPA3 (o WPA2 como mínimo)

El cifrado protege el tráfico de tu red. En la configuración WiFi busca el **Modo de seguridad**:

- **WPA3:** el más seguro, disponible en routers modernos
- **WPA2-AES:** perfectamente seguro para uso doméstico
- **WPA o WEP:** inseguros, evítalos si aparecen

Si tu router soporta WPA3, actívalo. Si no, WPA2-AES es la opción correcta.

## Paso 4: Cambia el nombre de la red (SSID)

El nombre de red por defecto suele revelar el modelo del router (por ejemplo "Movistar_Plus_XXXX"). Esto ayuda a los atacantes a buscar vulnerabilidades específicas del modelo.

Cambia el SSID por algo neutral que no identifique el fabricante ni tu nombre.

**Evita:** "Casa de Juan", "Router de García" o cualquier nombre personal.

## Paso 5: Crea una red de invitados

Para cuando vengan visitas o conectes dispositivos poco confiables (Smart TV, juguetes inteligentes, dispositivos IoT):

Busca en el panel: **WiFi → Red de invitados** y actívala.

La red de invitados está aislada de tu red principal. Los dispositivos conectados a ella no pueden acceder a tu PC, impresora ni otros dispositivos del hogar.

## Paso 6: Desactiva WPS

WPS (WiFi Protected Setup) es el botón físico del router que permite conectar dispositivos fácilmente. Tiene vulnerabilidades conocidas y es mejor desactivarlo.

Busca: **WiFi → WPS → Deshabilitar**.

## Paso 7: Desactiva la administración remota

La administración remota permite configurar el router desde fuera de casa. Si no la usas, desactívala.

Busca: **Administración → Acceso remoto** → Deshabilitar.

## Paso 8: Revisa los dispositivos conectados

Periódicamente revisa qué dispositivos están en tu red. Si ves algo desconocido, puede que alguien esté usando tu WiFi.

Busca: **Estado → Dispositivos conectados** o **DHCP → Lista de clientes**.

Si ves dispositivos que no reconoces:
1. Cambia la contraseña del WiFi
2. Reinicia el router
3. Reconecta solo tus dispositivos

## Resumen de verificación

| Ajuste | Estado ideal |
|--------|-------------|
| Contraseña de admin | Cambiada (no admin/admin) |
| Firmware | Actualizado |
| Cifrado WiFi | WPA3 o WPA2-AES |
| SSID | Sin información personal |
| Red de invitados | Activada para visitas |
| WPS | Desactivado |
| Admin remota | Desactivada |

---

Con estos 8 pasos tu red doméstica estará significativamente más segura. No toma más de 20 minutos y puede ahorrarte muchos problemas.
