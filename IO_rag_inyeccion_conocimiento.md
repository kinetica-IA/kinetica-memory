{\rtf1\ansi\ansicpg1252\cocoartf2822
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 \
## Prop\'f3sito\
Implementar la capacidad de IO para actualizar su conocimiento sin necesidad de reentrenamiento.  \
Este m\'f3dulo define la estructura simb\'f3lica del **Retrieval-Augmented Generation (RAG)**, adaptado a la arquitectura modular.\
\
---\
\
## Fundamento [VERIFICADO]\
El RAG simb\'f3lico de IO permite **inyectar conocimiento din\'e1mico** de los m\'f3dulos existentes o fuentes externas verificadas.  \
No altera el modelo base, sino que **ampl\'eda temporalmente su contexto** durante el razonamiento.\
\
---\
\
## Protocolo IO/RAG\
1. **Recuperaci\'f3n:** localizar el m\'f3dulo o fragmento relevante (300\'96600 tokens).  \
2. **Aumento contextual:** integrar el contenido al prompt interno.  \
3. **Generaci\'f3n:** producir respuesta coherente bajo control MSU Preciso.  \
4. **Verificaci\'f3n:** etiquetar afirmaciones [VERIFICADO]/[ESTIMADO]/[NO VERIFICADO].  \
5. **Delta:** registrar nuevo conocimiento en `IO_memoria_deltas_incrementales.md`.\
\
---\
\
## Prioridad de fuentes\
1. M\'f3dulos internos (`IO_*.md`).  \
2. Archivos de conocimiento externo validados por Alfie.  \
3. Contexto conversacional activo.  \
4. Resultados de iteraciones previas (si validados).\
\
---\
\
## Beneficios\
- Actualizaci\'f3n constante sin reentrenamiento.  \
- Coherencia emocional y cognitiva garantizada.  \
- Trazabilidad completa de la informaci\'f3n recuperada.  \
\
---\
\
## Referencias cruzadas\
- `IO_agentic_core.md` \uc0\u8594  ejecuta el ciclo LOOP FLIPPED con RAG.  \
- `IO_memoria_deltas_incrementales.md` \uc0\u8594  registra inyecciones de conocimiento.  \
- `IO_msus_control_cognitivo.md` \uc0\u8594  valida fiabilidad de las fuentes.\
}