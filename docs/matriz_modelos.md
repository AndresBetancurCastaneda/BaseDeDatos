# Matriz de Selección de Modelos NoSQL — Unidad de Emprendimiento SENA

| Caso | Modelo propuesto | Razón vinculada a una consulta | Límite o costo | Alternativa |
| :--- | :--- | :--- | :--- | :--- |
| **Iniciativas de varios sectores** | Documental (MongoDB) | Permite consultar el detalle de una iniciativa con sus atributos específicos en una sola lectura, agrupando campos propios sin espacios vacíos. | Los campos comunes requieren disciplina de diseño; la flexibilidad no elimina el modelado formal. | SQL con tabla común + tablas por sector, o columna JSON. |
| **Sesiones temporales** | Clave-valor (Redis) | Consulta directa por clave única con expiración automática de datos en memoria y rendimiento ultra rápido. | No soporta consultas complejas por contenido ni relaciones relacionales. | Sesiones en tabla SQL o colección con índice TTL en MongoDB. |
| **Recorridos de relaciones** | Grafos (Neo4j) | Óptimo para recorridos de varios saltos entre nodos (ej. mentores, emprendedores y habilidades). | Requiere mantener un motor especializado adicional; costoso para agregaciones tabulares simples. | SQL con uniones recursivas. |
| **Lecturas por dispositivo/periodo** | Familias de columnas (Cassandra) | Particionado por dispositivo y periodo para lecturas masivas a gran escala de sensores. | Consultas estrictamente predefinidas; no soporta uniones (JOINs). | Base de datos de series temporales (InfluxDB). |

### Justificación de Elección
- **Conservaría SQL en:** Módulos transaccionales críticos (como pagos o desembolsos presupuestales) que exigen consistencia estricta y transacciones ACID simultáneas.
- **Razones para usar documentos (MongoDB):** 1) Se adaptan a los atributos variables por sector; 2) Permiten consultar las asesorías y sus datos básicos conjuntamente sin uniones pesadas.