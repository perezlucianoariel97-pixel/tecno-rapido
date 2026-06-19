---
title: "Copias de seguridad automáticas en Windows: configúralo una vez y olvídate"
date: 2026-05-28
draft: false
description: "Guía para principiantes sobre el Programador de tareas de Windows. Crea copias de seguridad automáticas nocturnas sin instalar nada extra."
categories: ["Windows"]
tags: ["backup", "copia de seguridad", "automatización", "windows", "programador de tareas"]
---

Perder archivos importantes es una de las experiencias más frustrantes en informática. La buena noticia: Windows tiene todo lo necesario para hacer copias de seguridad automáticas sin instalar ningún programa extra. Configúralo una vez y nunca más te preocupes.

## La regla 3-2-1 de las copias de seguridad

Antes de empezar, entiende este principio básico:

- **3** copias de tus datos
- **2** en soportes diferentes (disco local + nube, por ejemplo)
- **1** fuera de tu ubicación física (nube o disco en otro lugar)

Para la mayoría de usuarios, con 2 copias (local + nube) es suficiente.

## Método 1: Historial de archivos de Windows (el más fácil)

Windows 10 y 11 incluyen **Historial de archivos**, que hace copias automáticas de tus archivos a un disco externo o unidad de red.

**Cómo configurarlo:**

1. Conecta un disco externo o USB
2. Ve a **Configuración → Sistema → Almacenamiento → Opciones de copia de seguridad avanzadas**
3. Haz clic en **Agregar una unidad** y selecciona tu disco externo
4. Activa **Realizar copia de seguridad de mis archivos automáticamente**
5. Ajusta la frecuencia (cada hora es el valor por defecto, puedes cambiarlo)

Ahora Windows guarda versiones de tus archivos automáticamente. Si borras algo por error, puedes recuperarlo desde el historial.

## Método 2: Script batch + Programador de tareas

Para más control, crea un script que copie exactamente lo que quieres donde quieres.

**Paso 1 — Crea el script de copia:**

Abre el Bloc de notas y pega esto:

```batch
@echo off
set ORIGEN=%USERPROFILE%\Documents
set DESTINO=D:\Backup\Documents
xcopy "%ORIGEN%" "%DESTINO%" /E /I /H /Y /D
echo Copia completada: %date% %time% >> D:\Backup\log.txt
```

Cambia `D:\Backup` por la ruta de tu disco externo. Guarda el archivo como `backup.bat`.

**Paso 2 — Prográmalo con el Programador de tareas:**

1. Abre el **Programador de tareas** (`Windows + S` → buscar "Programador de tareas")
2. Haz clic en **Crear tarea básica**
3. Nombre: "Copia de seguridad nocturna"
4. Disparador: **Diariamente** a las **23:00**
5. Acción: **Iniciar un programa** → selecciona tu archivo `backup.bat`
6. En opciones avanzadas, marca **Ejecutar si el equipo funciona con batería** y **Ejecutar aunque el usuario no haya iniciado sesión** (requiere contraseña de administrador)

A partir de ahora, cada noche a las 23:00 tu PC hace la copia solo.

## Método 3: Copia a la nube con OneDrive o Google Drive

La forma más sencilla para archivos críticos: activa la sincronización automática a la nube.

**OneDrive (ya incluido en Windows):**
1. Abre OneDrive (icono en la barra de tareas)
2. Ve a Configuración → Copia de seguridad
3. Activa las carpetas que quieres sincronizar: Escritorio, Documentos, Imágenes

**Google Drive:**
1. Descarga Google Drive para escritorio
2. Selecciona las carpetas a sincronizar
3. Listo — todo lo que cambies en esas carpetas se sube automáticamente

## ¿Con qué frecuencia hacer backup?

Depende de cuánto te puedes permitir perder:

| Frecuencia | Ideal para |
|------------|-----------|
| Tiempo real (nube) | Documentos de trabajo activos |
| Diaria | Proyectos personales, fotos nuevas |
| Semanal | Archivos que cambian poco |
| Mensual | Archivos históricos, backups completos |

## Verifica tus copias de seguridad

Una copia de seguridad que nunca has probado puede no funcionar cuando la necesites. Una vez al mes, comprueba que puedes recuperar un archivo desde tu backup. Son 5 minutos que pueden salvarte de un desastre.

---

Configurar esto hoy te tomará 30 minutos. No hacerlo puede costarte horas, días o datos irremplazables.
