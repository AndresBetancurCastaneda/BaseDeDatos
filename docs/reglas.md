# Reglas de Negocio del Sistema

1. **Códigos únicos:** Formatos estándar `EMP-001` para emprendedores, `INI-001` para iniciativas y `ASE-001` para asesorías.
2. **Relación Emprendedor-Iniciativa:** Cada iniciativa cuenta con un responsable existente; una persona puede tener varias iniciativas.
3. **Vínculo de Asesoría:** Cada asesoría se vincula a una iniciativa existente e incluye el código del asesor (`ASR-001`).
4. **Sectores y Etapas:** Sectores permitidos (`tecnologia`, `alimentos`, `economia_circular`). Etapas (`idea`, `validacion`, `puesta_en_marcha`).
5. **Estados:** Iniciativa (`activa` / `archivada`). Asesoría (`programada` / `realizada` / `cancelada`).
6. **Fechas y Reprogramaciones:** Se registra `fecha_programada` y `fecha_realizacion`. La fecha original nunca se modifica para ocultar reprogramaciones.
7. **Franjas de Asesores:** Un asesor no puede tener dos asesorías cruzadas en la misma franja de 1 hora en punto (ej. 08:00 - 09:00).
8. **Historial al Archivar:** Archivar una iniciativa no borra su historial de asesorías previas.

### Preguntas para la Dirección y Riesgos
- **Pregunta 1:** ¿Las reprogramaciones de asesorías deben generar un registro nuevo o conservar rastro en el mismo documento?
- **Pregunta 2:** ¿Los reportes mensuales deben reflejar el sector histórico o el actual?
- **Riesgo:** Crecimiento excesivo de documentos si se embeben historiales masivos de asesorías de manera descontrolada dentro de un único documento de iniciativa.