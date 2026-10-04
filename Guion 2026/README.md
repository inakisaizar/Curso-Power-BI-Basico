# Curso Power BI Básico · Cámara de Gipuzkoa · Guion 2026

Revisión del guion del curso (20 horas). Cada parte se revisa y aprueba antes de guardarse aquí.

## Enfoque del curso

1. **Power Query**: conectar los orígenes habituales en la empresa y dominar las transformaciones estándar desde la interfaz, sin código M. Power Query es la herramienta con la que construimos las tablas de hechos y dimensiones.
2. **Modelado**: crear un modelo semántico en estrella y entender la capacidad de análisis que da cruzar atributos al medir los hechos.
3. **Visualización**: lo esencial. A futuro, la IA consumirá el modelo semántico y generará informes al vuelo; el activo es el modelo.

## Estado de las partes

| Archivo | Contenido | Estado |
|---|---|---|
| `00_Auditoria.md` | Auditoría del guion anterior y propuestas | Aprobado |
| `01_Arranque.md` | Destino, interfaces de Power BI, viaje completo exprés | Pendiente |
| `02_Power_Query.md` | Fuentes y transformaciones con la interfaz | Pendiente |
| `03_Modelado.md` | Modelo en estrella, relaciones, calendario | Pendiente |
| `04_DAX.md` | Medidas básicas, inteligencia de tiempo, presupuesto | Pendiente |
| `05_Visualizacion.md` | Página Home y Obtener detalles | Pendiente |
| `06_Publicar_e_IA.md` | Power BI Service, actualización y cierre con IA | Pendiente |
| `infografias/` | Infografías de apoyo (SVG) | Pendiente |

## Preparación del equipo del alumno (primer minuto del curso)

Todos los ejercicios se conectan a archivos locales con la **misma ruta en todos los equipos**.

1. En esta página del repositorio, botón verde **Code > Download ZIP**.
2. Clic derecho sobre `Curso-Power-BI-Basico-main.zip` > **Extraer todo**.
3. Borrar la ruta que propone Windows y escribir solo **`C:\`** > **Extraer**.
4. Comprobar que existe `C:\Curso-Power-BI-Basico-main\` y que dentro están las carpetas de ejercicios (sin una segunda carpeta repetida dentro).

Plan B si el equipo no permite escribir en `C:\`: extraer en `C:\Users\Public\`.

## Decisiones tomadas

- **Conexión a los Excel**: local, desde el ZIP descomprimido. El asistente **Obtener datos > Web** no descarga archivos desde GitHub ni Dropbox (lo trata como página web y falla). La conexión web se enseña como demostración con la página del INE.
- **Ruta fija** `C:\Curso-Power-BI-Basico-main\`: permite que los .pbix de punto de control funcionen en cualquier equipo sin cambiar el origen de datos.
- **Formato**: guion en Markdown e infografías en SVG.

## Pendiente antes del curso

- [ ] Confirmar con la Cámara que los equipos permiten escribir en `C:\`.
- [ ] Cambiar el origen de datos de los .pbix del repo a `C:\Curso-Power-BI-Basico-main\...`.
- [ ] Preparar los .pbix de punto de control (tras Power Query, tras modelado, tras medidas).
