# Unidad de Emprendimiento SENA: NoSQL Semana 1

Repositorio colaborativo de artefactos, matrices de diseño, reglas y scripts de prueba para bases de datos NoSQL.

## Estructura
- `docs/`: Contiene `matriz_modelos.md`, `consultas_Q01_Q06.md` y `reglas.md`.
- `scripts/`: Contiene el script de prueba `01_explorar.js`.
- `evidencias/`: Contiene el registro técnico del entorno en `entorno.md`.

## Ejecución del Script de Demostración
Desde la carpeta `scripts/`, ejecuta en tu terminal con mongosh autenticado:
```bash
mongosh "mongodb://127.0.0.1:27017/emprendimiento_sena_lab" --username aprendiz_nosql --authenticationDatabase emprendimiento_sena_lab --file 01_explorar.js