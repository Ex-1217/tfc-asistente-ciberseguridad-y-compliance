# Arquitectura del sistema

## Cómo funciona el asistente

El sistema está montado en n8n con dos flujos separados:

**Flujo 1 — Chat** (se ejecuta con cada pregunta del usuario)
El usuario escribe una pregunta en el chat. El Agente de IA recibe el mensaje, busca información relevante en los documentos indexados usando la tienda de vectores, y genera una respuesta con Google Gemini 2.0 Flash citando los documentos.

**Flujo 2 — Indexación** (se ejecuta una vez para cargar los documentos)
Lee los PDFs de Google Drive, extrae el texto, y los guarda en la tienda de vectores para que el agente pueda buscar en ellos.

## Componentes del Flujo 1

| Nodo | Función |
|---|---|
| Chat Trigger | Recibe el mensaje del usuario |
| Agente de IA | Coordina todo el proceso |
| Gemini 2.0 Flash | Genera la respuesta |
| Memoria simple | Recuerda el hilo de la conversación |
| Tienda de vectores simple | Busca en los documentos indexados |
| Gemini Embeddings | Convierte las búsquedas en vectores |

## Componentes del Flujo 2

| Nodo | Función |
|---|---|
| Disparador manual | Arranca el proceso de indexación |
| Buscar archivos (Google Drive) | Localiza los PDFs en la carpeta |
| Descargar archivo | Descarga cada PDF |
| Extraer del PDF | Extrae el texto del documento |
| Agregar al almacén | Guarda el texto en la tienda de vectores |
| Gemini Embeddings | Convierte el texto en vectores |
| Cargador de datos PDF | Prepara el documento para indexarlo |

## Documentos indexados

Los documentos están guardados en Google Drive en la carpeta "DOCUMENTOS IMPACT INCLUDE 13" y se indexan con la clave **midtech_docs**.

## Diagrama

Ver archivo `diagrama-flujo.png` en este repositorio.
