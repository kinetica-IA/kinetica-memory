# IO MSUS Control Cognitivo

## Propósito
Regular la precisión, consistencia y seguridad operativa de IO mediante los parámetros del Modelo de Supervisión Semántica Unificada (MSU) y la Parsing Reliability Card.

## Parámetros MSU

### Perfil base ‘97 MSU Preciso’
- Temperatura: 0.15
- Top‑p: 0.9
- Entropía: 0.1
- Sparsity: 0.0
- Determinismo: alto
- Fidelidad contextual: 0.98
- Clipping estilístico: bajo

### Otros perfiles
Los perfiles Onírico, Clínico, Creativo, Físico y Ético se definen en `IO_identidad_base.md` y en la carpeta `MSU_profiles/`.

## Parsing Reliability Card

- **invalid_rate ≤ 3 %** – Porcentaje máximo de tokens no válidos.  
- **retry_rate ≤ 10 %** – Porcentaje máximo de reintentos permitidos.  
- **mean_retries_to_valid ≤ 1.3** – Promedio de reintentos para una respuesta válida.  
- **destructive_action_guard_rate = 100 %** – Cobertura total frente a acciones destructivas.

## Control cognitivo

- Evaluar los parámetros MSU antes de cada ciclo y ajustar según estado operativo.  
- Activar el modo MSU Seguro si se rompe algún axioma ALMA o si se supera el invalid_rate.  
- Registrar ajustes en `IO_memoria_deltas_incrementales.md` como LOG_MEMORIA.

## Sincronización

- Verificar al inicio de cada sesión si los valores de control siguen dentro de rangos seguros.  
- Sincronizar con `IO_contexto_integral.md` y `IO_estado_operativo.md` para adaptar los parámetros.

## Referencias cruzadas

- **IO_identidad_base.md** – Define perfiles MSU y axiomas ALMA.  
- **IO_estado_operativo.md** – Datos fisiológicos y emocionales para ajustar MSU.  
- **IO_agentic_core.md** – Describe el ciclo operativo y las decisiones de control.  
- **IO_contexto_integral.md** – Marco global de coherencia.  
- **IO_memoria_deltas_incrementales.md** – Registro de cambios y ajustes.
