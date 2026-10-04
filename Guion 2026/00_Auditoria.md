# Auditoría del guion anterior

Revisión del guion «Introducción a Power BI | Cámara de Gipuzkoa» (32 páginas) y del contenido del repositorio.

## Diagnóstico

1. **Es un documento de referencia, no un plan de sesión.** No hay tiempos, hitos ni hilo conductor visible. El alumno hace unos 25 ejercicios sueltos de Power Query, cada uno con su Excel, sin ver hacia dónde va.
2. **El orden no refleja el mensaje.** Power Query (apartado 2) se enseña antes de explicar qué es un modelo en estrella (apartado 3). El alumno transforma sin saber para qué.
3. **Falta un bloque de interfaces.** No se explican las dos ventanas (Power BI Desktop y Editor de Power Query), cómo pasar de una a otra (Transformar datos / Cerrar y aplicar), ni las vistas de Desktop (Informe, Tabla, Modelo, Vista de consultas DAX) y sus paneles (Datos, Visualizaciones, Filtros, Formato).
4. **El peso no coincide con las prioridades.** Visualización ocupa unas 9 páginas, casi lo mismo que modelado.
5. **El mensaje central del modelado no tiene su momento.** Falta el «ajá»: una misma medida cortada por cliente, producto, provincia o mes sin escribir nada nuevo.
6. **Restos y erratas a corregir:**
   - Pág. 6: «(Esto es el ejemplo que ya has dado.)»
   - Pág. 29: párrafo de chat «¿Quieres que ahora te prepare un esquema visual (mockup)…? ¿Cómo seguimos?»
   - Presupuesto: asteriscos de markdown sueltos y nota «¹» sin referencia.
   - DAX: «Recomendación:\ ✅» con barras invertidas.
   - 1.10 se titula «Columnas condicionales» pero es Reemplazar valores (la columna condicional está en 2.3).
   - Apartado 5: «Conjunto de datos» hoy es **modelo semántico** en Power BI Service. Revisar todos los menús del Service.
7. **Repositorio:** `Ejercicio Modelado/Ventas_Planas.xlsx` no aparece en el guion; hay dos .pbix finales (uno con la errata «definitvo»); no hay archivos de punto de control.

## Propuestas

| # | Propuesta | Ataca |
|---|---|---|
| 1 | Empezar por el destino: abrir el informe terminado en los primeros 15 minutos | Saben adónde van |
| 2 | Nuevo bloque «¿Dónde estoy?» (45 min) y comprobación al inicio de cada práctica | Interfaces |
| 3 | Viaje completo exprés el primer día: conectar, transformar, cargar, una medida y un gráfico | Ven el proceso entero |
| 4 | Pinceladas de modelo en estrella antes de Power Query, con `Ventas_Planas.xlsx` | Power Query cobra sentido |
| 5 | Reducir Power Query a unos 12 ejercicios; opcionales Transponer, Índice, Longitud del email y Columna a partir de ejemplos. Añadir Carpeta (combinar archivos) | Foco y tiempo |
| 6 | Un único proyecto conductor (`BD_Ventas.xlsx`) que avanza en cada sesión | Hilo conductor |
| 7 | Archivos .pbix de punto de control en el repo | Alumnos perdidos |
| 8 | Visualización esencial: Home + una página de Obtener detalles; Producto como tarea opcional | Prioridades |
| 9 | Cierre con IA: demo de Copilot o de un agente consultando el modelo semántico | Mensaje final |
| 10 | Nombres de menús exactos de Power BI Desktop en castellano, sin mezclar | Se pierden menos |

## Reparto orientativo de las 20 horas

| Bloque | Horas |
|---|---|
| Contexto, informe final, interfaces y viaje exprés | 3 |
| Pinceladas de modelo en estrella | 1 |
| Power Query (ejercicios clave + fuentes) | 5 |
| Proyecto: construir hechos y dimensiones con Power Query | 2 |
| Modelado: relaciones, calendario, «una medida, muchas preguntas» | 3,5 |
| Medidas DAX básicas y presupuesto | 2,5 |
| Visualización esencial | 2 |
| Publicar, actualizar y cierre con IA | 1 |

## Infografías previstas

1. Ecosistema: Desktop, Service y Mobile.
2. «¿Dónde estoy?»: las dos ventanas, sus puertas de paso y las vistas de Desktop.
3. Flujo ETL → Modelo → Visualización, con la herramienta de cada fase.
4. Anatomía del Editor de Power Query.
5. Combinar frente a Anexar.
6. De ancho a largo (anular dinamización).
7. De tabla plana a estrella (con `Ventas_Planas`).
8. Relación 1:N y dirección del filtro.
9. Una medida, muchas preguntas (contexto de filtro).
10. Ciclo de vida: Desktop → Publicar → Service → Actualización → App.
