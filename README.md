Asistente de Ciberseguridad y Compliance con IA

Trabajo de Fin de Curso — Programa #IMPACT #include13
Fundación GoodJob · Mayo – junio 2026

---

¿Qué es este proyecto?

Este proyecto es mi Trabajo de Fin de Curso del programa #include13 de la Fundación GoodJob. He tardado casi dos semanas en conseguir que funcionara, con muchos intentos fallidos por el camino, y al final pude construirlo con ayuda de Claude como herramienta de apoyo.

El asistente es un chatbot de ciberseguridad para MIDTECH S.A., una empresa ficticia del sector farmacéutico. Lee los documentos de normativa y la política de seguridad de la empresa, y responde preguntas sobre cumplimiento legal en lenguaje normal.
El mayor reto ha sido construir el flujo en n8n desde cero — tuve problemas con la conexión de los nodos, con la API de Gemini que agotó la cuota gratuita durante las pruebas, y con entender cómo funciona el RAG para que el asistente busque en los documentos y no responda de memoria. Al final conseguí montarlo todo y aprender cómo funciona por dentro.

¿Qué puede hacer?

- Analizar la política de seguridad de MIDTECH y ver qué falta
- Detectar incumplimientos comparándola con GDPR, ISO 27001 y ENS
- Responder preguntas de auditoría citando los documentos reales
- Proponer mejoras ordenadas por importancia

Herramientas que he usado

| Para qué | Herramienta |
|---|---|
| Crear el flujo | n8n |
| Inteligencia artificial | Google Gemini 2.0 Flash |
| Buscar en los documentos | Tienda de vectores de n8n |
| Memoria del chat | Memoria simple de n8n |
| Guardar los documentos | Google Drive |

Documentos que tiene el asistente

- GDPR — Reglamento europeo de protección de datos
- ISO 27001 — Estándar de seguridad de la información
- ENS — Esquema Nacional de Seguridad español
- Política de Seguridad de MIDTECH S.A. (facilitada por el profesor)

Qué hay en este repositorio

- **/prompts** — los 4 prompts que controlan el comportamiento del asistente
- **ARCHITECTURE.md** — cómo está montado el sistema
- **diagrama-flujo.png** — diagrama visual del flujo en n8n

Autor
Carlos · #include13 · Fundación GoodJob · 2026
