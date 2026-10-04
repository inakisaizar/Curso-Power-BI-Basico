# Material del profesor

Notas de sesión, tiempos y decisiones. No forma parte del entregable del alumno.

## Estado de los capítulos

| Capítulo | Alumno | Notas de sesión | Estado |
|---|---|---|---|
| Auditoría del guion anterior | | `00_Auditoria.md` | Aprobado |
| 1. Primeros pasos | `01_Arranque.md` | `01_Arranque_sesion.md` | Aprobado |
| 2. Power Query | `02_Power_Query.md` | `02_Power_Query_sesion.md` | Aprobado (2.7 corregido: IdProducto) |
| 3. Modelado | `03_Modelado.md` | `03_Modelado_sesion.md` | Aprobado |
| 4. DAX | | | Pendiente |
| 5. Visualización | | | Pendiente |
| 6. Publicar e IA | | | Pendiente |

## Decisiones tomadas

- **Conexión a los Excel:** local, desde el ZIP descomprimido en `C:\`. El asistente **Obtener datos > Web** no descarga archivos desde GitHub ni Dropbox: los trata como página web y falla. Sí funciona `Excel.Workbook(Web.Contents("https://raw.githubusercontent.com/..."), null, true)` en una consulta en blanco; se puede enseñar como demostración. La conexión web para alumnos se enseña con la página del INE.
- **Ruta fija** `C:\Curso-Power-BI-Basico-main\`: los .pbix de punto de control funcionan en cualquier equipo sin cambiar el origen.
- **Formato:** capítulos en Markdown para el alumno, infografías SVG 16:9 intercaladas, también para proyectar.
- **Separación:** el material del alumno en `Guion 2026/`; lo del profesor en `Guion 2026/_profesor/`.
- **Excel del repo:** se mantienen sin modificar los que usa el curso. Eliminados por no usarse: Transponer (1.6), Parámetros (bloque 4) y mini proyecto (bloque 5). Nuevo: `Ejercicios Power Query/PQ Carpeta/Ventas_2024/` (12 CSV generados a partir de `Ventas_Planas.xlsx`).
- **Nombre de la pestaña:** en la versión en castellano es **Transformación**.

## Pendiente antes del curso

- [ ] Confirmar con la Cámara que los equipos permiten escribir en `C:\` (plan B: `C:\Users\Public\`).
- [ ] Cambiar el origen de datos de los .pbix del repo a `C:\Curso-Power-BI-Basico-main\...`.
- [ ] Preparar los .pbix de punto de control (tras Power Query, tras modelado, tras medidas). El primero: `Proyecto Modelo de Ventas/Checkpoint_Cap2_PowerQuery.pbix`, al terminar el proyecto 2.7. El segundo: `Checkpoint_Cap3_Modelo.pbix`, al terminar el capítulo 3.
- [ ] Confirmar en Power BI Desktop (actualización de septiembre) el nombre y la ubicación de la vista de diagrama y la vista de esquema, y ajustar el apartado 2.2 y la infografía 08 si hace falta.
- [ ] Revisar que los nombres de menús de los capítulos coinciden con la versión de Power BI Desktop instalada en la Cámara.
