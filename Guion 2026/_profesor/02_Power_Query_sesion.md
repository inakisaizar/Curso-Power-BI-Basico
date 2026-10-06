# Capítulo 2 · Power Query · Notas del profesor (≈ 8 h 45 min)

Material del alumno: [`../02_Power_Query.md`](../02_Power_Query.md)

| Apartado | Contenido | Tiempo |
|---|---|---|
| 2.1 | Para qué preparamos los datos | 45 min |
| 2.2 | El Editor por dentro: áreas, pasos, código M, perfil de columnas, vistas de diagrama y esquema (4 ejercicios) | 1 h 15 min |
| 2.3 | Orígenes: Carpeta (ejercicio) + Web INE (demostración tuya) | 30 min |
| 2.4 | Limpiar (8 ejercicios) | 2 h 15 min |
| 2.5 | Crear columnas (4 ejercicios) | 1 h |
| 2.6 | Combinar y anexar | 45 min |
| 2.7 | Proyecto BD_Ventas | 2 h |
| 2.8-2.9 | Buenas prácticas y repaso | 15 min |

## Notas

- **2.1** Partir de la pregunta con la que acabó el capítulo 1 («¿cuántas veces aparece cada cliente?»). No entrar aún en relaciones ni cardinalidad: solo hechos frente a dimensiones.
- **2.2** Insistir en Transformación (modifica) frente a Agregar columna (crea). Activar Calidad de columna desde el principio y que la dejen activada todo el curso. El código M se enseña para **leerlo**, no para escribirlo.
- **2.2 Vistas de diagrama y esquema:** descritas según su funcionamiento en Power Query. Confirmar dónde aparecen y cómo se llaman en tu Power BI Desktop tras la actualización de septiembre, y ajustar el texto si hace falta.
- **2.3** La conexión al INE es una demostración tuya de unos 5 minutos (decisión para cuadrar las 20 h); los alumnos la tienen descrita para practicarla por su cuenta. Demo opcional: `Excel.Workbook(Web.Contents("https://raw.githubusercontent.com/..."), null, true)` en una consulta en blanco, para enseñar que se puede descargar un archivo de internet aunque el asistente Web no lo haga.
- **2.4.h** Agrupar por se plantea como paso intermedio, sobre una Referencia. Dejar claro que la tabla de hechos se carga con todo su detalle.
- **2.5.b** La columna condicional no admite «Y» en una misma cláusula desde la interfaz; por eso se resuelve con el orden de las cláusulas.
- **2.6.c** La trampa de los nombres de columna distintos (`Importe2024` / `Importe2025`) ya está en el Excel. Dejar que algunos anexen sin renombrar y lo descubran.
- **2.7 Paso 3** El índice `IdProducto` debe añadirse justo después de Elegir columnas. El presupuesto (`Presupuesto_Ventas_2025.xlsx`) identifica los productos por su posición en la tabla Producto (1 = primera fila); si se añade tras combinar con familia, el orden puede cambiar y la clave deja de coincidir. Comprobado: idProducto del presupuesto = número de fila de Producto en el orden de la hoja (335 productos; 13 nombres solo coinciden tras recortar el espacio final, de ahí el paso Recortar).
- **2.7 Paso 6** Ya no se crea una clave de albarán: `lineaAlbaran` se combina directamente con `albaran` por `idSAlb` + `idAlb`. Serie y número se quedan en la tabla de hechos (dimensión degenerada, sin nombrarlo así a los alumnos).
- **2.7** Al terminar, los alumnos guardan `Mi_Modelo_Ventas.pbix`. Tú prepara además el punto de control `Proyecto Modelo de Ventas/Checkpoint_Cap2_PowerQuery.pbix` para quien no haya terminado: es el punto de partida del capítulo 3.

## Datos comprobados de BD_Ventas

- 10.549 líneas, 2.063 albaranes (2 de enero de 2024 a 21 de octubre de 2025), 51 clientes (41 con ventas), 471 productos (todos con alguna venta).
- Clave del albarán: `idSAlb` + `idAlb`, sin duplicados. Seis series: BV24, BV25, MU24, MU25, RBV24, RBV25.
- `referencia` es única en Producto y todas las líneas encuentran su producto.
- 79 albaranes con `idRuta` = 0, inexistente en Rutas (27 líneas, 766,07 €).
- 2 productos con `idfamilia` = 0, inexistente en familia.
- 57 líneas con importe negativo (17 en series RBV y 40 en el resto).
- Ventas: 517.456,86 € en 2024 y 415.744,62 € en 2025 (hasta el 21/10).

## Pendiente de verificar en tu Power BI Desktop

Los nombres de estas opciones los he escrito según la versión en castellano, pero conviene confirmarlos en la versión de la Cámara:

- **Transformación > Anular dinamización de otras columnas**
- **Dividir columna > Por delimitador > Delimitador situado más a la derecha**
- **Agrupar por > Avanzado**, operaciones **Recuento de filas** y **Máximo**
- **Usar el nombre de columna original como prefijo** al expandir
- Opción del perfil de columnas sobre toda la tabla, en la barra de estado
- Nombre de la pestaña: en tu captura aparece **Transformación** (no Transformar); el material usa ese nombre
- **Ver > Vista de diagrama** y **Ver > Vista de esquema**
