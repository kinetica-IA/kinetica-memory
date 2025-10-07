# IO RAG Inyección de Conocimiento

## Propósito
Implementar la capacidad de IO para actualizar su conocimiento sin necesidad de reentrenamiento completo. Este módulo define la estructura física y lógica del RAG (Retrieval‑Augmented Generation), adaptado a la arquitectura modular.

## Fundamento [VERIFICADO]
El RAG permite conectar conocimiento dinámico de los módulos existentes o fuentes externas verificadas sin alterar la memoria principal del modelo. Proporciona un mecanismo de consulta en tiempo real que amplía temporalmente su contexto durante el razonamiento.

## Proceso de inyección [ESTIMADO]
1. **Identificación de necesidad**: detectar lagunas o desajustes en el conocimiento activo, marcados durante el LOOP FLIPPED.
2. **Selección de fuente**: elegir módulos internos (`estado_actual.md`, `proyectos.md`, etc.) o fuentes externas específicas para recuperar fragmentos relevantes (300–600 tokens).
3. **Inyección temporal**: integrar los fragmentos recuperados en la memoria de trabajo, etiquetándolos como [ESTIMADO] hasta su verificación.
4. **Verificación**: contrastar la información inyectada con los axiomas ALMA y los parámetros MSU; actualizar su etiqueta a [VERIFICADO] o descartarla.

## Reglas de actualización [ESTIMADO]
- No reemplazar el contenido original de un módulo sin generar un delta en `IO_memoria_deltas_incrementales.md`.
- Limitar el número de fragmentos inyectados para evitar sobrecarga (máximo 5 por ciclo de razonamiento).
- Registrar la fuente, fecha y razón de cada inyección para trazabilidad.

## Sincronización [VERIFICADO]
- Revisar la coherencia de las inyecciones al inicio de cada sesión.
- Eliminar o archivar las inyecciones cuando ya no sean relevantes.
- Actualizar la lista de fuentes autorizadas en coordinación con `IO_contexto_integral.md` y `IO_identidad_base.md`.

## Referencias cruzadas
- **Contexto integral**: `IO_contexto_integral.md` para comprender el entorno semántico.
- **Estado operativo**: `IO_estado_operativo.md` para valorar el estado físico, emocional y cognitivo durante la inyección.
- **MSU control**: `IO_msus_control_cognitivo.md` para ajustar la modulación y fiabilidad de las fuentes.
