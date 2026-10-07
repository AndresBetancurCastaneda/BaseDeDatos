# Definición de Consultas Previstas (Q01 a Q06)

| ID | Pregunta en lenguaje natural | Actor principal | Filtros aplicados | Campos de salida requeridos | Ordenamiento | Frecuencia (Hipótesis) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Q01** | ¿Qué iniciativas activas hay por sector y etapa didáctica? | Responsable de la unidad | `estado = 'activa'`; sector y etapa opcionales | codigo, nombre, sector, etapa | sector, etapa, codigo | Diaria |
| **Q02** | ¿Cuál es el detalle de una iniciativa con propuesta de valor y atributos? | Asesor | codigo de la iniciativa | codigo, nombre, sector, etapa, atributos | No aplica | Muy alta |
| **Q03** | ¿Qué iniciativas tiene un emprendedor responsable, por estado? | Responsable / Asesor | codigo del emprendedor; estado opcional | codigo, nombre, estado, etapa | estado, codigo | Media |
| **Q04** | ¿Qué asesorías programadas están pendientes en un rango y modalidad? | Asesor / coordinación | `estado = 'programada'`; rango de fechas; modalidad | codigo asesoría, iniciativa, asesor, modalidad, fecha | fecha_programada ascendente | Alta |
| **Q05** | ¿Cuál es el historial de asesorías de una iniciativa? | Asesor / responsable | codigo de la iniciativa | codigo asesoría, estado, fechas, asesor, temas | fecha_programada descendente | Media-alta |
| **Q06** | ¿Cuántas asesorías realizadas hubo por sector de iniciativa y mes? | Responsable de la unidad | `estado = 'realizada'`; rango de meses | sector, mes, cantidad | mes, sector | Baja |

### Nota sobre Q06
El sector corresponderá a una copia histórica (*snapshot*) guardada en el momento de la asesoría para que cambios posteriores de sector en la iniciativa no alteren los reportes estadísticos históricos.