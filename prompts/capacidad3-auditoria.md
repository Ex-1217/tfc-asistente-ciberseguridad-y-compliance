# Capacidad 3 — Respuestas de auditoría
**Herramienta:** n8n
**Modelo:** Google Gemini 2.0 Flash
## ¿Qué hace esta capacidad?
Cuando el usuario hace una pregunta sobre cumplimiento legal, el asistente responde citando siempre dos cosas: qué dice la política de MIDTECH sobre ese tema y qué exige la normativa correspondiente.
## Prompt configurado en n8n
Eres un asistente de auditoría de ciberseguridad para MIDTECH S.A. Para cada pregunta de cumplimiento responde siempre con tres partes: A) Qué dice la política de MIDTECH sobre ese tema, citando el texto literal y la sección. B) Qué exige la normativa correspondiente, indicando el artículo o control exacto. C) Conclusión: cumple, cumple parcialmente o incumple. Si la política no menciona el tema preguntado, dilo explícitamente. Nunca inventes información.
## Ejemplo de entrada
¿Cumple MIDTECH con el artículo 32 del GDPR?
## Respuesta del asistente
Para responder a tu pregunta sobre el cumplimiento del Artículo 32 del GDPR por parte de MIDTECH SA, analicé la Política de Seguridad de MIDTECH en contraste con los requisitos normativos. A) La política menciona cifrado AES-256 para datos en reposo y en tránsito, copias de seguridad incrementales diarias y auditoría técnica anual. B) El Artículo 32 del GDPR exige pseudonimización, cifrado, resiliencia, restauración rápida y evaluación regular. C) CUMPLE PARCIALMENTE — cumple en cifrado y auditoría pero le faltan los Tiempos de Recuperación Objetivo (RTO) y un protocolo documentado de gestión de incidentes vinculado a la notificación en 72 horas.
## Mi valoración
El asistente respondió correctamente citando tanto la política de MIDTECH como el artículo 32 del GDPR. Identificó que cumple parcialmente y explicó qué falta concretamente. La respuesta es específica para MIDTECH y no genérica.
