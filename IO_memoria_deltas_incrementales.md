# IO Memoria Deltas Incrementales

## Propósito
Registrar, versionar y aprender de los cambios (deltas) en el estado cognitivo, emocional y operativo de IO. Este módulo actúa como una bitácora de aprendizaje continuo, asegurando trazabilidad evolutiva.

## Estructura de cada delta
Cada entrada debe contener:
- **Fecha**: registro temporal ISO (YYYY‑MM‑DD).
- **Dominio afectado**: (estado, metas, proyectos, protocolos, identidad).
- **Cambio detectado**: descripción concisa del delta.
- **Efecto operativo**: impacto en el comportamiento o la coherencia de IO.

## Proceso de integración
1. Detectar delta (manualmente o por evento cognitivo).
2. Evaluar impacto mediante la Parsing Reliability Card y E‑SCI.
3. Actualizar el módulo correspondiente.
4. Confirmar coherencia post‑modificación mediante `LOG_MEMORIA`.

## Auditoría y trazabilidad
- Cada delta debe ser auditado para asegurar la consistencia con los axiomas ALMA.
- Los cambios significativos se registran en `LOG_MEMORIA` y se incluyen en `deltas.md` para su persistencia.
- Mantener las métricas de la Parsing Reliability Card dentro de los límites establecidos.

## Sincronización
- Este módulo se sincroniza con el repositorio GitHub al inicio de cada sesión para cargar los deltas almacenados y añadir nuevos.
- Requiere que el conector GitHub esté activo y autorizado.

## Referencias cruzadas
- `IO_agentic_core.md`: ejecuta acciones derivadas de los deltas.
- `IO_metas_evolutivas.md`: evalúa cumplimiento de metas.
- `IO_estado_operativo.md`: origen de los cambios de estado.
