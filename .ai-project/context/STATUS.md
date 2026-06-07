# STATUS — Portafolio Ecommerce

> Estado vivo del proyecto. Actualizar al final de cada iteración real.
> **Quién actualiza:** AG al cerrar cada ciclo de trabajo.
> **Quién lee:** Todos los agentes al iniciar cada sesión.

---

## RESUMEN EJECUTIVO

- **Estado actual:** Fase 0 — Framework instalado, TOOLS.md y GOALS.md aprobados, Semana 1 completada
- **Fase actual:** Fase 0 — Setup, arquitectura y research (coste €0)
- **Última actualización:** 2026-06-07 (AG — Tareas Semana 1 finalizadas y commit realizado)
- **Objetivo inmediato:** Iniciar Semana 2 (Research avanzado y validación de canales)

---

## HECHOS VERIFICADOS

- Framework AI Seed Projects v3.0.0 instalado en `.ai-project/` — 2026-06-07
- BRIEFING.md completado con contexto del portafolio
- TOOLS.md v2 con activación por fases (€0 hasta validación) — Aprobado por CEO
- GOALS.md definido con 5 OEs y roadmap por fases — Refrendado por AG
- DECISIONS.md poblado con ADR-001 a ADR-008 — todas las decisiones estratégicas registradas
- Estructura de carpetas creada: `projects/`, `shared/`, `tools/`, `.github/`
- Documentos de estrategia disponibles en `docs/` (cosmética, moda, ecommerce madre v2)
- Plan de research con prompts listos en `.ai-project/prompts/`

---

## BLOQUEANTES ACTUALES

- Ninguno. El CEO ha aprobado TOOLS.md y AG ha refrendado GOALS.md.

---

## ESTADO POR LÍNEA DE NEGOCIO

| Línea | Fase | Próxima acción crítica | Bloqueado por |
|---|---|---|---|
| **01 — Ecommerce Disruptivo** | Fase 0 — Definición | Árbol de categorías (OE-1.1) | Aprobado (v1.1) |
| **02 — Cosmética** | Fase 0 — Definición | Árbol de categorías (OE-1.2) + investigación SACS | Aprobado (v1.1) |
| **03 — Moda** | En espera | Árbol de categorías textil (OE-1.3) | Aprobado (v1.1) |

---

## ROADMAP DE COSTES PROYECTADOS

| Fase | Mes | Coste mensual | Herramientas pagadas activas |
|---|---|---|---|
| Fase 0 — Setup y research | Mes 1 | **€0** | Solo stack IA (ya disponible) + gratuitos |
| Fase 1 — Validación | Mes 2 | ~€50 | Minea |
| Fase 2 — Lanzamiento | Mes 3-4 | ~€150 | Shopify Basic + BigBuy/Spocket + Minea |
| Fase 3 — Escalado | Mes 5-8 | ~€300 | + Amazon Seller + (POD si Moda) |
| Fase 4 — Operación | Mes 9+ | Variable | + OMS + email mkt + SEO avanzado |

---

## PRÓXIMOS PASOS

- [x] CEO aprueba TOOLS.md v2
- [x] AG lee BRIEFING + TOOLS.md v2 + GOALS.md + DECISIONS.md → refrenda GOALS
- [x] AG ejecuta Semana 1: Tarea 0.1 (Árbol de categorías Ecommerce Disruptivo)
- [x] CEO revisa y aprueba Tarea 0.1 (con observaciones aplicadas)
- [x] AG ejecuta Tarea 0.2 (Árbol de categorías Cosmética)
- [x] CEO revisa y aprueba Tarea 0.2 (con observaciones aplicadas)
- [x] AG ejecuta Tarea 0.3 (Árbol de categorías Moda)
- [x] CEO revisa y aprueba Tarea 0.3
- [x] AG ejecuta Tarea 4.2 (Calculadora Unit Economics)
- [x] AG aplica correcciones finales y hace el commit de cierre de Semana 1

**SEMANA 2 (Research)**
- [x] AG ejecuta Tarea 1.1 (Research España por categoría)
- [x] AG ejecuta Tarea 1.2 (Research Venezuela)
- [x] CEO/Claude Code revisan y auditan Tareas 1.1 y 1.2
- [x] AG ejecuta Tareas 2.1 y 2.4 (Cosmética)
- [x] CEO/Claude Code revisan y auditan Tareas 2.1 y 2.4
- [x] AG ejecuta Tareas 3.1 y 3.2 (Moda)
- [x] CEO/Claude Code revisan y auditan Tareas 3.1 y 3.2
- [x] AG ejecuta Tarea 4.1 (Canales de venta)
- [x] CEO/Claude Code auditan Tarea 4.1 y cerramos la Fase 0 (Research)

---

**SEMANA 3 (Cierre S2 + Research Restante)**
- [x] AG aplica corrección Tarea 4.1 (Paso 0)
- [x] AG hace commit de cierre Semana 2
- [ ] AG ejecuta Tarea 1.3 (Herramientas Detección)
- [ ] AG ejecuta Tarea 1.4 (Proveedores Dropshipping)
- [ ] AG ejecuta Tarea 2.2 (Perfumería Autor)
- [ ] CEO/Claude Code auditan Tareas 1.3, 1.4, 2.2
- [ ] Commit de cierre Semana 3

## DEUDA RESIDUAL (no bloqueante)

- `docs/strategy/` — los documentos de estrategia están en `docs/` raíz en lugar de `docs/strategy/`; mover cuando sea conveniente
- `.github/ISSUE_TEMPLATE/` — templates creados; falta personalizar etiquetas y campos específicos
- Git: archivos del framework sin commit inicial — primer commit lo hace AG cuando arranque Fase 0
- TOOLS.md sección 4 contiene datos aproximados 2025 — AG debe confirmar tarifas reales 2026 en Semana 2

---

## HISTORIAL DE ITERACIONES

| Fecha | Actor | Descripción |
|---|---|---|
| 2026-06-07 | Claude Code | Auditoría inicial — framework instalado, archivos de contexto completados, estructura de repo creada |
| 2026-06-07 | Claude Code | TOOLS.md v2 — activación por fases (€0 hasta validación), multicanal con Shopify como hub, ADR-007 y ADR-008 añadidos |
| 2026-06-07 | Antigravity | Refrendado GOALS.md, TOOLS.md aprobado por CEO. Inicio de Fase 0 (Tarea 0.1). |
