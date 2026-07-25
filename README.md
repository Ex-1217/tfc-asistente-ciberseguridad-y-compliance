# Asistente de Ciberseguridad y Compliance con IA

**Trabajo de Fin de Curso — Programa #IMPACT #include13 · Fundación GoodJob · Mayo – junio 2026**

---

## ¿Qué es este proyecto?

Este proyecto es mi Trabajo de Fin de Curso del programa #IMPACT #include13 de la Fundación GoodJob. He construido un asistente conversacional de ciberseguridad y compliance para MIDTECH SA, una empresa ficticia del sector farmacéutico, integrando herramientas de inteligencia artificial sin necesidad de programar.

El asistente permite al responsable de seguridad o al DPD de MIDTECH hacer preguntas en lenguaje natural y recibir respuestas concretas citando tanto la política interna de la empresa como los artículos o controles normativos correspondientes (GDPR, ISO 27001 y ENS).

---

## ¿Qué puede hacer?

- Analizar la política de seguridad de MIDTECH e identificar qué áreas cubre y qué falta
- Detectar incumplimientos comparándola con GDPR, ISO 27001 y ENS
- Responder preguntas de auditoría citando la política interna y la normativa exacta
- Proponer mejoras concretas ordenadas por prioridad y esfuerzo

---

## Herramientas utilizadas

| Para qué | Herramienta |
|---|---|
| Crear el flujo | n8n Cloud |
| Inteligencia artificial | Google Gemini Pro (gemini-pro-latest) |
| Buscar en los documentos | Tienda de vectores simple de n8n |
| Embeddings (indexación) | Google Gemini Embeddings (gemini-embedding-001) |
| Memoria del chat | Memoria simple de n8n |
| Guardar los documentos | Google Drive |

---

## Documentos que tiene el asistente

- **GDPR** — Reglamento General de Protección de Datos (UE 2016/679)
- **ISO 27001** — Estándar internacional de seguridad de la información (versión 2022)
- **ENS** — Esquema Nacional de Seguridad (Real Decreto 311/2022)
- **Política de Seguridad de MIDTECH SA** — facilitada por el profesor

---

## Cómo funciona

El sistema tiene dos flujos en n8n:

**Flujo 1 — Chat:** el usuario envía una pregunta, el agente busca en los documentos indexados, recupera los fragmentos relevantes y Gemini genera la respuesta citando fuentes concretas.

**Flujo 2 — Indexación:** se ejecuta una vez por documento. Descarga el PDF de Google Drive, extrae el texto y lo almacena en la tienda de vectores para que el Flujo 1 pueda consultarlo.

---

## Qué hay en este repositorio

- `/prompts` — los 4 prompts que controlan el comportamiento del asistente
- `ARQUITECTURA.md` — descripción técnica de cómo está montado el sistema
- `DIAGRAMA DE FLUJO.png` — diagrama visual de los dos flujos en n8n

---

**Autor:** Carlos  2026
