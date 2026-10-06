# Capítulo 3 · Modelado · Notas del profesor (≈ 4 h)

Material del alumno: [`../03_Modelado.md`](../03_Modelado.md)

| Apartado | Contenido | Tiempo |
|---|---|---|
| 3.1 | Qué es un modelo semántico; estrella frente a tabla plana | 20 min |
| 3.2 | Vista de modelo; borrar relaciones automáticas; desactivar Fecha y hora automáticas | 20 min |
| 3.3 | Relaciones 1:N, claves, dirección del filtro (3.3.a) | 40 min |
| 3.4 | Una medida, muchas preguntas (3.4.a y 3.4.b) | 30 min |
| 3.5 | «(En blanco)» y la ruta «Sin ruta» (3.5.a) | 25 min |
| 3.6 | DimFecha en DAX, marcar como tabla de fechas, ordenar meses, relacionar | 40 min |
| 3.7 | FactPresupuesto, dimensiones compartidas, granularidad | 40 min |
| 3.8 | Ocultar claves, formatos, Resumir por, tabla de medidas, disposiciones | 25 min |
| 3.9 | Errores comunes y repaso | 10 min |

## Notas

- **Punto de partida:** `Mi_Modelo_Ventas.pbix` del alumno o `Checkpoint_Cap2_PowerQuery.pbix`. Al final del capítulo conviene tener otro punto de control: `Checkpoint_Cap3_Modelo.pbix`.
- **3.2** Borrar las relaciones que haya detectado Power BI antes de empezar. Si alguien no las borra y le aparecen relaciones extrañas, es un buen ejemplo para comentar.
- **3.3** La frase que tienen que llevarse: «el filtro cae de las dimensiones a los hechos». Repetirla en 3.4, 3.5 y 3.7.
- **3.4.b** Borrar la relación con DimRuta y ver el total repetido es el momento clave del capítulo. Dejar que lo descubran antes de explicarlo.
- **3.5** Con los datos actuales, la fila «(En blanco)» suma 766,07 € (27 líneas, todas de albaranes con idRuta = 0). Hay 79 albaranes con idRuta = 0, pero la mayoría no tienen líneas.
- **3.6** DimFecha va del 1/1/2024 al 31/12/2025 (731 filas). El código es el del guion anterior, apuntando a `FactVentas[Fecha]` y sin las columnas Offset (decisión: quitarlas del curso; con datos hasta octubre de 2025 y TODAY() en 2026 saldrían vacías y confunden). El DAX no se explica a fondo: es el capítulo 4. `FORMAT(..., "mmmm")` devuelve el mes en el idioma de la configuración regional del modelo; si salen en inglés, revisar **Archivo > Opciones > Configuración regional** del archivo actual.
- **3.7** Datos comprobados del presupuesto: 7.572 filas, 32 clientes (todos existen en Cliente), 335 productos distintos, fechas fin de mes de enero a diciembre de 2025. Total `ImportePpto` ≈ 1.072.098 €; ventas reales 2025 (hasta el 21/10) ≈ 415.745 €. La diferencia es grande: es un buen gancho para el capítulo 4 (GAP y %GAP), pero no anticipar conclusiones de negocio.
- **3.7** Comprobado: `idProducto` del presupuesto coincide con el número de fila de Producto (los 335 nombres coinciden, 13 de ellos solo tras recortar el espacio final; por eso el paso Recortar en DimProducto).
- **3.7** Las columnas del presupuesto se renombran a `ImportePpto` y `CostePpto` para que la medida se pueda llamar `Presupuesto` sin chocar con el nombre de una columna.
- **3.8** Ocultar las columnas de fecha de las tablas de hechos es deliberado: obliga a usar DimFecha y evita que ventas y presupuesto se filtren por fechas distintas.
- **3.9** Varios a varios, filtro bidireccional y copo de nieve solo se nombran. No hacer demostraciones.

## Pendiente de verificar en tu Power BI Desktop

- Texto exacto del cuadro de relación: **Cardinalidad** «Varios a uno (\*:1)», **Dirección del filtro cruzado** «Única», casilla **Activar esta relación**.
- **Archivo > Opciones y configuración > Opciones > Archivo actual > Carga de datos**: casilla **Detectar automáticamente nuevas relaciones después de cargar los datos** y, en **Inteligencia de tiempo**, **Fecha y hora automáticas**.
- **Herramientas de tabla > Marcar como tabla de fechas** y **Herramientas de columna > Ordenar por columna**.
- **Herramientas de medidas > Tabla principal** (para mover medidas a `_Medidas`).
- Panel **Propiedades** de la Vista de modelo: **Está oculto** y **Resumir por**.
- Disposiciones de la Vista de modelo: pestaña **Todas las tablas**, botón **+** y opción **Agregar tablas relacionadas**.
