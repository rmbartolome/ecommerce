# REPO PROFILE
> Generado automáticamente por el instalador. Sección "Tech stack" completada manualmente.
> Actualizado en cada reinstalación o update del framework.

---

## Identificación

- **Repo:** ecommerce
- **Perfil instalado:** general
- **Framework version:** 3.0.0
- **Fecha de instalación:** 2026-06-07
- **Instalado por:** Roberto Bartolome <bartolome.roberto1@gmail.com>

---

## Señales detectadas al instalar

> El instalador detectó estas señales para sugerir el perfil seleccionado.

Instalación manual con perfil general

---

## Tech stack declarado

- **Plataforma ecommerce:** Shopify (núcleo — ADR-001)
- **Expansión multicanal:** Amazon.es y Miravia (Fase 2 vía OMS)
- **Dropshipping:** BigBuy España + Spocket (proveedores EU)
- **Print-on-Demand:** Printful + Gelato
- **IA / Automatización:** Claude (Project / Code / Cowork / Design) + Gemini Pro + ChatGPT + NotebookLM
- **Control de versiones:** Git + GitHub (repo privado)
- **Formatos de documento:** Markdown (trabajo vivo) + DOCX (entregables ejecutivos)
- **Analytics:** Shopify Analytics + Google Analytics 4
- **Deploy target:** No aplica — repositorio de gestión operativa, no software deployable
- **CI/CD:** No aplica en Fase 1. GitHub Actions para recordatorio de revisión semanal (futuro)

---

## Notas del equipo

- Este repo NO contiene código de aplicación. Es el sistema operativo operativo del portafolio: research, catálogos, estrategia, activos de marketing y configuraciones.
- Los secretos y credenciales NUNCA van en el repositorio (Shopify API keys, credenciales de proveedor, etc.).
- La carpeta `/memory/` del diseño original (ecommerce_repo_setup.md) fue reemplazada por `.ai-project/context/` al instalar el framework (ver ADR-006).
- Los documentos de estrategia en `docs/` son la versión Markdown de los .docx generados con Claude. Son la fuente de verdad operativa.

---

## Perfil aplicado

# PERFIL: general

**Cuándo usar:** Repos sin señales claras de tipo específico. Buena opción por defecto cuando el repo está en estado inicial o no encaja en los demás perfiles.

---

## Reglas activas para este perfil

- Aplicar todas las reglas core de `ai_rules.md` sin restricciones adicionales.
- No asumir stack tecnológico — está declarado arriba.
- Priorizar exploración y documentación del estado actual antes de proponer cambios.

## Restricciones específicas

- Ninguna restricción adicional más allá del core del framework.

## Riesgos comunes

- AG puede asumir un stack tecnológico sin confirmación. Siempre verificar en BRIEFING.md y este archivo.
- Sin perfil específico, las fases del PLAN.md pueden quedar demasiado genéricas. Pedir mayor detalle al usuario.

## Criterios de éxito mínimos esperados

- [x] BRIEFING.md completado por el humano antes de que AG genere GOALS.md
- [x] Tech stack declarado explícitamente en REPO_PROFILE.md
- [x] Al menos un criterio de éxito verificable en los OEs (ver GOALS.md)
