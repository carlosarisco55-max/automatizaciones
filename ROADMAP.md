# Roadmap — Automatizaciones

Próximos pasos, en orden de valor/esfuerzo. Última actualización: 2026-09-04.

## En progreso ahora
- [ ] Subir la estructura `automatizaciones/` a GitHub (decisión de estrategia pendiente: repo único vs. un repo por proyecto)

## Siguiente (fase 2 del Lead Generation Multicanal)
- [ ] **Dashboard de atribución** — conectar Power BI (ya tienes la skill `powerbi-report-mcp`) o un workflow de n8n programado que agregue los datos de las Data Tables (canal, score, etapa, resultado) y responda "¿qué canal trae los mejores leads de verdad?", no solo los más baratos
- [ ] **GA4 MCP oficial** (`googleanalytics/google-analytics-mcp`, ya instalado en `.claude.json` como `analytics-mcp`) — falta: crear proyecto en Google Cloud Console, activar Admin API + Data API, `gcloud auth application-default login`, pegar la ruta de credenciales y el project ID en la config, reiniciar sesión de Claude Code. Sin esto no hace falta tocar nada — el enriquecimiento de leads con GA4 ya funciona sin él (captura en cliente, no por API)

## Cuando se acepte el coste
- [ ] **SMS real** — sustituir el nodo placeholder de nurture SMS por Twilio (Twilio da algo de crédito gratis al crear cuenta, luego cobra por SMS)

## Ideas más grandes, sin fecha
- [ ] Reconstruir el **Lead Triage Agent** original (n8n Cloud + Claude API de pago) sobre este mismo stack gratuito — era el objetivo que arrancó todo esto
- [ ] Primer proyecto real en `proyectos-empresa/` (candidato: algo para Lotuscale, o un cliente)
- [ ] Explorar Ollama para inferencia 100% local — aparcado por la RAM limitada de esta máquina (7.75GB), revisar si compensa en otro equipo

## Ya cerrado (para no repetir trabajo)
- ✅ n8n local + ngrok + Groq como IA gratis ([n8n-local-lab](https://github.com/carlosarisco55-max/n8n-local-lab))
- ✅ Lead Generation Multicanal completo: captación 4 canales + GA4 + scoring configurable + CRM + pipeline de ventas + emails reales + seguridad + manejo de errores + URL estable (documentado en Notion → Automatizaciones → Proyectos personales)
