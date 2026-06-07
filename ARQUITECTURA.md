# Arquitectura del sistema

## Componentes

| Componente | Tecnología |
|---|---|
| Orquestación | n8n Cloud |
| Modelo LLM | Google Gemini Pro (gemini-pro-latest) |
| Embeddings | Google Gemini Embeddings (gemini-embedding-001) |
| Base de conocimiento | Tienda de vectores simple (n8n) |
| Gestor documental | Google Drive |
| Memoria | Memoria simple n8n |

---

## Flujo 1 — Chat con el usuario

Chat Trigger → Agente de IA → Respuesta

El Agente de IA tiene conectados:
- **Modelo de chat:** Google Gemini Pro (gemini-pro-latest)
- **Memoria simple:** mantiene el contexto de la conversación
- **Tienda de vectores:** recupera fragmentos de los documentos indexados

---

## Flujo 2 — Indexación de documentos

Disparador manual → Buscar archivos (Google Drive) → Descargar archivo → Extraer texto del PDF → Tienda de vectores simple

Este flujo se ejecuta una vez para indexar todos los documentos.

---

## Documentos indexados

- GDPR (CELEX_32016R0679_ES_TXT.pdf)
- ISO 27001 (ISO27001_2022.pdf)
- ENS (BOE-A-2022-7191-consolidado.pdf)
- Política de Seguridad de MIDTECH SA

---

## URL del asistente

`https://proyecto-midtech.app.n8n.cloud/webhook/3426a235-152d-4bcf-a3b3-d11ab231b784/chat`
