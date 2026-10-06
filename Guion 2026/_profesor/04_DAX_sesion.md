# Capítulo 4 · Medidas con DAX · Notas del profesor (≈ 2 h 40 min)

Material del alumno: [`../04_DAX.md`](../04_DAX.md)

| Apartado | Contenido | Tiempo |
|---|---|---|
| 4.1 | Medida o columna calculada; contexto de filtro (4.1.a) | 20 min |
| 4.2 | Coste, Margen, % Margen, Cantidad, Nº clientes; formatos | 30 min |
| 4.3 | CALCULATE: sustituir un filtro (4.3.a) y quitarlo con ALL (4.3.b) | 30 min |
| 4.4 | GAP, % GAP, periodos comparables, formato condicional | 25 min |
| 4.5 | Ventas AA, variación, YTD, la trampa del año incompleto | 35 min |
| 4.6 | Carpetas para mostrar y descripciones | 10 min |
| 4.7 | Errores comunes y repaso | 10 min |

## Notas

- **Punto de partida:** `Mi_Modelo_Ventas.pbix` o `Checkpoint_Cap3_Modelo.pbix`. Al final, punto de control `Checkpoint_Cap4_DAX.pbix` para los capítulos 5 y 6.
- **4.1** La columna calculada se crea solo para verla y se borra. Mensaje: lo que va por fila, en Power Query; lo que depende del filtro, medida.
- **4.3.a** Que descubran que `Ventas Cervebel` repite la cifra antes de explicarlo. Enlaza con 3.4.b (misma cifra en todas las filas, causa distinta).
- **4.3.b** Con Provincia en filas, `% sobre total` da 100,00 % en todas: buena pregunta para la clase antes de explicarlo.
- **4.4** Ojo con el presupuesto: es **el mismo todos los meses** (89.342 € al mes, 1.072.098 € al año) y casi el doble de las ventas reales. Enero a septiembre de 2025: ventas 388.616,81 €, presupuesto 804.073,55 €, GAP −415.456,74 €, % GAP −51,67 %. El texto del alumno lo plantea como pregunta («¿qué le preguntarías a quien lo preparó?»). Si se quiere un presupuesto más realista, habría que regenerar el Excel con la misma estructura.
- **4.5.c** Datos comprobados: 2024 517.456,86 €; 2025 415.744,62 € (hasta el 21/10): −19,66 % en año completo. Enero a septiembre: 379.948,26 € frente a 388.616,81 €: +2,28 %. Es el mejor momento del capítulo para hablar de lectura crítica de datos.
- **4.2.c** Margen: 21,79 % en 2024 y 26,17 % en 2025. Nº clientes: 39 en 2024 y 32 en 2025.
- **4.3.b** Ventas 2025 por familia: FAMILIA MARTINEZ ZABALA 59.988,26 € (14,43 %), CERVEBEL 57.294,41 € (13,78 %), CONSERVAS MAR 32.477,50 € (7,81 %).
- **4.6** Las descripciones enlazan con el capítulo 6 (Copilot y la IA leen el modelo). No alargarlo.
- Sin columnas Offset en DimFecha (decisión tomada): los periodos se eligen con segmentaciones.
- Sin ticket medio: necesitaría contar albaranes por serie y número (COUNTROWS + SUMMARIZE), demasiado para un curso básico.

## Pendiente de verificar en tu Power BI Desktop

- **Herramientas de tabla > Nueva columna** y **Herramientas de medidas** (formato, decimales).
- **Formato condicional > Color de fuente**, estilo **Reglas**.
- Propiedades de la medida en la Vista de modelo: **Carpeta para mostrar** y **Descripción** (el nombre exacto de «Carpeta para mostrar» puede variar).
