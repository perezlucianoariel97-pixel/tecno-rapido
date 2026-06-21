---
title: "Excel para principiantes: las fórmulas esenciales que todos deberían saber"
date: 2026-06-19T00:00:00+00:00
description: "Las fórmulas de Excel más usadas explicadas con ejemplos prácticos: SUMA, SI, BUSCARV, CONTAR.SI y más. Domina lo básico en una sola guía."
tags: ["Excel", "Microsoft Office", "Productividad", "Fórmulas", "Oficina"]
categories: ["posts"]
author: "Tecno Rápido"
cover:
    image: "images/posts/header-excel-formulas.png"
    alt: "Excel para principiantes: las fórmulas esenciales que todos deberían saber"
    relative: false
---

Excel sigue siendo, más de 35 años después de su lanzamiento, la herramienta más usada del mundo para trabajar con números. El problema es que la mayoría de la gente solo usa una fracción mínima de lo que puede hacer — generalmente sumas básicas y poco más.

Con un puñado de fórmulas (no necesitas memorizar cientos) puedes automatizar cálculos, organizar datos y ahorrar horas de trabajo manual. Esta guía cubre las que realmente vas a usar el 90% del tiempo.

## Antes de empezar: cómo funciona una fórmula en Excel

![Barra de fórmulas en Excel](/images/posts/excel-barra-formulas.png)


Toda fórmula en Excel empieza con el signo `=`. Por ejemplo, si escribes `=A1+A2` en una celda, Excel suma el contenido de las celdas A1 y A2 y muestra el resultado.

Las fórmulas pueden referirse a celdas individuales (`A1`), rangos (`A1:A10`) u otras hojas del mismo archivo. Esto es lo que las hace tan potentes: si cambias un número en A1, todo lo que dependa de esa celda se actualiza automáticamente.

## 1. SUMA: la más básica y la más usada

Suma todos los valores de un rango de celdas.

```
=SUMA(A1:A10)
```

Esto suma todos los números desde A1 hasta A10. Mucho más rápido que escribir `=A1+A2+A3+A4...` manualmente.

**Truco rápido:** selecciona el rango de celdas que quieres sumar y mira la barra de estado en la esquina inferior derecha de Excel — ahí aparece la suma automáticamente, sin necesidad de escribir ninguna fórmula.

## 2. PROMEDIO: la media de un grupo de números

```
=PROMEDIO(B1:B20)
```

Calcula el promedio (media aritmética) de todos los valores en el rango. Útil para calificaciones, precios promedio, tiempos promedio, lo que sea que necesites promediar.

## 3. SI: la fórmula que toma decisiones

`SI` es probablemente la fórmula más poderosa para principiantes porque introduce lógica condicional — Excel "decide" qué mostrar según una condición.

```
=SI(A1>100, "Aprobado", "Rechazado")
```

Esto dice: si el valor en A1 es mayor a 100, muestra "Aprobado"; si no, muestra "Rechazado".

**Ejemplo práctico:** calcular si un alumno aprobó según su nota.

```
=SI(B2>=6, "Aprobado", "Reprobado")
```

Puedes anidar varios SI para más de dos resultados posibles:

```
=SI(B2>=9, "Excelente", SI(B2>=6, "Aprobado", "Reprobado"))
```

## 4. CONTAR.SI: cuenta celdas que cumplen una condición

```
=CONTAR.SI(A1:A50, ">100")
```

Cuenta cuántas celdas en el rango A1:A50 tienen un valor mayor a 100. También funciona con texto:

```
=CONTAR.SI(C1:C50, "Completado")
```

Esto cuenta cuántas veces aparece la palabra "Completado" en el rango — perfecto para hacer seguimiento de tareas, pedidos o estados.

## 5. SUMAR.SI: suma solo lo que cumple una condición

Combina lo mejor de SUMA y CONTAR.SI:

```
=SUMAR.SI(A1:A50, "Ventas", B1:B50)
```

Esto suma los valores de la columna B, pero solo en las filas donde la columna A dice exactamente "Ventas". Extremadamente útil para totales por categoría sin tener que filtrar manualmente.

## 6. BUSCARV: encuentra datos en otra tabla

`BUSCARV` (Buscar Vertical) es la fórmula que separa a quien sabe Excel de quien no. Busca un valor en la primera columna de un rango y devuelve un dato de la misma fila en otra columna.

```
=BUSCARV(A1, B1:D100, 3, FALSO)
```

Esto busca el valor de A1 dentro del rango B1:D100, y devuelve el valor de la tercera columna de ese rango, en la misma fila donde lo encontró. El `FALSO` al final le dice a Excel que busque una coincidencia exacta.

**Ejemplo real:** tienes una lista de productos con sus precios en otra hoja. Con BUSCARV, escribes el nombre del producto y el precio aparece automáticamente, sin que tengas que buscarlo manualmente.

<div class="callout">
<strong>Nota para 2026:</strong> Microsoft recomienda usar <code>BUSCARX</code> en versiones recientes de Excel y Microsoft 365, ya que es más flexible que BUSCARV (puede buscar hacia la izquierda y es menos propenso a errores). Si tienes una suscripción activa de Microsoft 365, <code>BUSCARX</code> es la opción más moderna a aprender.
</div>

## 7. CONCATENAR / unir texto con &

Combina el contenido de varias celdas en una sola.

```
=A1&" "&B1
```

Si A1 tiene "Juan" y B1 tiene "Pérez", el resultado es "Juan Pérez". Muy usado para unir nombres y apellidos, o armar direcciones de correo a partir de datos separados.

## 8. HOY y AHORA: fechas automáticas

```
=HOY()
```

Muestra la fecha actual y se actualiza automáticamente cada vez que abres el archivo. Útil para calcular plazos, antigüedad o vencimientos sin tener que actualizar la fecha manualmente.

```
=AHORA()
```

Igual que HOY pero incluye también la hora exacta.

## 9. REDONDEAR: controla los decimales

```
=REDONDEAR(A1, 2)
```

Redondea el valor de A1 a 2 decimales. Imprescindible cuando trabajas con precios o porcentajes y necesitas que todo se vea prolijo y consistente.

## 10. SI.ERROR: evita que se rompa todo por un error

Cuando una fórmula da error (por ejemplo, una división por cero), Excel muestra mensajes como `#DIV/0!` que pueden romper el resto de tus cálculos. `SI.ERROR` los reemplaza por algo que tú decidas:

```
=SI.ERROR(A1/B1, "N/A")
```

Si la división da error, en vez de mostrar `#DIV/0!` muestra "N/A". Esto mantiene tus planillas limpias y profesionales incluso cuando faltan datos.

## Tabla resumen de referencia rápida

| Fórmula | Para qué sirve |
|---|---|
| `=SUMA()` | Sumar un rango de celdas |
| `=PROMEDIO()` | Calcular la media de un rango |
| `=SI()` | Tomar decisiones según una condición |
| `=CONTAR.SI()` | Contar celdas que cumplen una condición |
| `=SUMAR.SI()` | Sumar solo lo que cumple una condición |
| `=BUSCARV()` / `=BUSCARX()` | Buscar un dato en otra tabla |
| `=HOY()` | Fecha actual automática |
| `=REDONDEAR()` | Controlar decimales |
| `=SI.ERROR()` | Evitar mensajes de error visibles |

## Cómo seguir aprendiendo

No necesitas memorizar todas estas fórmulas de una sola vez. La forma más efectiva de aprender Excel es tener un problema real que resolver — una planilla de gastos, un seguimiento de ventas, una lista de tareas — e ir incorporando fórmulas a medida que las necesitas.

Con estas diez, ya vas a poder resolver la gran mayoría de los casos cotidianos que aparecen tanto en trabajos de oficina como en proyectos personales.
