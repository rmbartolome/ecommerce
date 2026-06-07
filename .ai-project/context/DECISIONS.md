# DECISIONS — Registro de Decisiones Técnicas y Estratégicas (ADRs)

> **Quién escribe:** Antigravity (AG) para decisiones técnicas. Claude Code para decisiones de framework.
> **Quién lee:** Ambos agentes, al inicio de cada sesión.
> **Cuándo actualizar:** Cada vez que se toma una decisión que afecte arquitectura, plataforma, stack o alcance.
>
> Un ADR en estado ACEPTADO es una restricción activa. Contradecirlo requiere pasar por el proceso de revisión.

---

## ADRs Activos

### ADR-001 — Shopify como plataforma central del ecosistema

**Estado:** ACEPTADO
**Fecha:** 2026-05-04
**Decidido por:** Roberto (CEO) — recomendación del consultor Onás

**Contexto:**
Se evaluó qué plataforma ecommerce usar como núcleo del portafolio. El ecosistema necesita una plataforma que soporte las 3 líneas de negocio, con integraciones nativas con apps de dropshipping, POD, y marketplaces secundarios (Amazon, Miravia), sin requerir desarrollo técnico propio.

**Decisión:**
Shopify es la plataforma central para todas las tiendas del portafolio. No se construye tecnología propia en Fase 1. WooCommerce, PrestaShop y plataformas propias quedan descartadas.

**Consecuencias:**
- Coste recurrente mensual desde el primer día (~29-79€/mes según plan).
- Todo el catálogo, configuraciones de tienda y flujos de venta viven en Shopify.
- La arquitectura de catálogo se diseña para Shopify (colecciones, metafields, variantes).
- La expansión a Amazon/Miravia se hace vía OMS integrado con Shopify, no de forma independiente.

**Alternativas descartadas:**
- WooCommerce: mayor fricción de mantenimiento técnico sin equipo.
- Plataforma propia: fuera de alcance y recursos actuales.

---

### ADR-002 — Secuencia de canales: Shopify → redes sociales → Amazon

**Estado:** ACEPTADO
**Fecha:** 2026-05-04
**Decidido por:** Roberto (CEO) — recomendación del consultor Onás

**Contexto:**
Se debatió si entrar directamente a Amazon.es como canal principal (por su tráfico existente) o construir primero en Shopify propio. La recomendación experta fue validar el producto y el mercado en Shopify antes de escalar a marketplaces.

**Decisión:**
Secuencia obligatoria: primero Shopify (validación y control de datos), luego redes sociales como canal de adquisición, luego Amazon/Miravia una vez hay prueba de product-market fit.

**Consecuencias:**
- No se vende en Amazon hasta tener al menos 10-20 ventas validadas en Shopify.
- Los datos de cliente y comportamiento de compra se acumulan en Shopify antes de diversificar.
- El catálogo debe estar bien estructurado desde Shopify para facilitar la exportación posterior a Amazon.

**Alternativas descartadas:**
- Entrar directo a Amazon: pierde los datos de cliente y depende del algoritmo de Amazon desde el inicio.
- Miravia primero: mercado más pequeño, menor validación de product-market fit.

---

### ADR-003 — Arquitectura de catálogo antes de configurar Shopify

**Estado:** ACEPTADO
**Fecha:** 2026-05-04
**Decidido por:** Roberto (CEO) — recomendación del consultor Onás

**Contexto:**
La configuración del catálogo en Shopify (colecciones, metafields, variantes, SKU naming) es costosa de refactorizar una vez hay productos publicados. Se identificó el riesgo de configurar Shopify sin un árbol de categorías definido.

**Decisión:**
Ningún producto se publica en Shopify hasta que el árbol de categorías de esa línea esté aprobado por el CEO. El árbol debe tener 3 niveles y nomenclatura de SKU definida para escalar a 200+ productos.

**Consecuencias:**
- OE-1 (arquitectura de catálogo) bloquea OE-4 (Shopify).
- Las primeras semanas son de diseño y research, no de publicación.
- AG no puede generar fichas de producto sin el árbol aprobado.

**Alternativas descartadas:**
- Publicar primero y organizar después: genera deuda técnica de catálogo muy difícil de pagar.

---

### ADR-004 — Stack IA del ecosistema

**Estado:** ACEPTADO
**Fecha:** 2026-05-04
**Decidido por:** Roberto (CEO)

**Contexto:**
Se necesita un stack de herramientas IA para las distintas funciones del portafolio: análisis estratégico, desarrollo técnico, operaciones, diseño, research externo y comunicaciones de marca.

**Decisión:**
Stack activo aprobado:
- **Claude Project** → cerebro estratégico, análisis, documentos ejecutivos
- **Claude Code** → auditor técnico, scripts, automatizaciones
- **Claude Cowork** → operaciones, gestión de tareas, publicación en Shopify
- **Claude Design** → mockups, activos visuales, contenido gráfico
- **Gemini Pro** → research externo con datos verificables, tendencias de mercado
- **ChatGPT** → copies persuasivos, tono de marca, comunicaciones
- **NotebookLM** → archivo vivo consultable, Audio Overview del portafolio

**Consecuencias:**
- Cada herramienta tiene un rol definido. No usar Gemini para análisis estratégico ni Claude para research de datos externos.
- Todos los outputs de investigación de Gemini deben pasar por Claude Project antes de entrar al repo.
- NotebookLM se alimenta con cada documento ejecutivo generado.

**Alternativas descartadas:**
- OpenClaw, NemoClaw, Auris — ver ADR-005.

---

### ADR-005 — Descontinuación de herramientas legadas

**Estado:** ACEPTADO
**Fecha:** 2026-05-04
**Decidido por:** Roberto (CEO)

**Contexto:**
El ecosistema venía usando OpenClaw, NemoClaw y Auris para algunas funciones. Se identificó que generaban fricción operativa y no aportaban valor diferencial frente al stack Claude + Gemini.

**Decisión:**
OpenClaw, NemoClaw y Auris quedan descontinuados en este ecosistema. Ningún agente debe referenciarlos ni intentar usarlos.

**Consecuencias:**
- Si aparece una referencia a estas herramientas en algún documento, ignorar.
- No reemplazarlos — sus funciones quedan cubiertas por el stack activo (ADR-004).

---

### ADR-006 — Framework AI Seed Projects como sistema de coordinación entre agentes

**Estado:** ACEPTADO
**Fecha:** 2026-06-07
**Decidido por:** Roberto (CEO) + Claude Code

**Contexto:**
El portafolio usa múltiples agentes IA (Claude Code, AG/Gemini, Claude Project) que operan de forma asíncrona. Se necesita un protocolo de coordinación claro para evitar conflictos, trabajo duplicado y decisiones no trazables.

**Decisión:**
El Framework AI Seed Projects v3.0.0 se instala en `.ai-project/` y es el sistema de coordinación oficial. Todos los agentes leen los archivos de `.ai-project/context/` al inicio de cada sesión antes de actuar.

**Consecuencias:**
- La carpeta `/memory/` descrita en el plan original (`ecommerce_repo_setup.md`) queda superada. Sus funciones (contexto global, estado, decisiones) las cumplen `.ai-project/context/BRIEFING.md`, `STATUS.md` y `DECISIONS.md`.
- El `CLAUDE.md` de la raíz define el rol de Claude Code como Auditor, no como implementer.
- AG (Antigravity/Gemini) es el único agente que hace git y genera archivos de proyecto.

**Alternativas descartadas:**
- Carpeta `/memory/` al estilo del plan original: funcionaría pero duplica la estructura del framework.
- Sin coordinación formal: inviable con 4+ agentes asíncronos.

---

### ADR-007 — Activación de herramientas pagas por fases (€0 hasta validación)

**Estado:** ACEPTADO
**Fecha:** 2026-06-07
**Decidido por:** Roberto (CEO) — propuesto por Claude Code

**Contexto:**
El plan original implícito activaba Shopify y herramientas de pago desde el día 1. Con €0 de ingresos durante la fase de research y arquitectura, pagar tienda y suscripciones es quemar capital sin retorno. El CEO planteó que el coste debe escalar con el progreso de validación, no preceder a la validación.

**Decisión:**
Ninguna herramienta con coste mensual se activa hasta que haya un SKU validado o una decisión de lanzamiento. La Fase 0 (research + arquitectura) opera con coste €0 usando exclusivamente el stack IA ya disponible y herramientas gratuitas (Google Trends, búsqueda manual). Las herramientas pagas activan según fase:
- Fase 0: €0 (solo IA stack + gratuitos)
- Fase 1 (validación): ~€50/mes (Minea solo)
- Fase 2 (lanzamiento): ~€150/mes (Shopify + proveedor dropshipping)
- Fase 3 (escalado): ~€300/mes (añade Amazon Seller, plan Shopify superior si justifica)

**Consecuencias:**
- Shopify se activa en Fase 2, no Fase 0. ADR-001 sigue vigente (Shopify es la plataforma) pero la activación se retrasa.
- AG no puede recomendar contratar ninguna herramienta paga sin que el CEO confirme que estamos en la fase correspondiente.
- El árbol de categorías y la nomenclatura de SKU se diseñan en Fase 0 SIN tener Shopify activo — Markdown puro.
- La validación de demanda usa canales gratuitos (Instagram orgánico, encuestas WhatsApp, landing simple) antes de comprar tráfico pago.

**Alternativas descartadas:**
- Activar Shopify en Fase 0 para "tener todo listo": quema 30-79€/mes sin uso real durante 2-3 meses.
- No definir activación por fases: deja la decisión abierta y produce gasto por inercia.

---

### ADR-008 — Estrategia multicanal con Shopify como hub central

**Estado:** ACEPTADO
**Fecha:** 2026-06-07
**Decidido por:** Roberto (CEO) — propuesto por Claude Code

**Contexto:**
El plan original implícitamente trataba Shopify como canal principal y los marketplaces como expansión futura única. El CEO planteó que pueden existir canales adicionales (Amazon, AliExpress, redes sociales, marketplaces verticales) que no son alternativas a Shopify sino complementos para multiplicar el alcance.

**Decisión:**
La estrategia es multicanal desde Fase 2. Shopify es el **hub central** donde vive el catálogo, los datos de cliente y la identidad de marca. Pero no es el único canal de venta. Cada línea de negocio tiene un mapa de canales priorizados:
- **Ecommerce Disruptivo (ES):** Shopify + Instagram + TikTok Shop → Amazon + Miravia (Fase 3)
- **Cosmética (VE + ES):** Instagram + WhatsApp Business (dominante en VE) + Shopify (validación ES) → MercadoLibre VE + Telegram (Fase 3)
- **Moda (ES):** TikTok Shop + Instagram + Shopify → Etsy + Pinterest + Vinted (Fase 3)

AliExpress queda excluido como canal de venta (sigue siendo proveedor vía DSers cuando sea necesario).

**Consecuencias:**
- ADR-002 sigue vigente (Shopify antes que Amazon como secuencia de lanzamiento) pero se complementa: canales sociales gratuitos (Instagram, TikTok Shop, WhatsApp) se activan en paralelo a Shopify, no después.
- AG debe investigar tarifas reales 2026 de cada canal antes de Fase 2 (tarea añadida en AG_SEMANA2_RESEARCH.md).
- El árbol de categorías y la nomenclatura SKU deben ser compatibles con los canales de mayor volumen (Amazon, TikTok Shop) — no solo Shopify.
- La estructura de unit economics debe poder calcular margen por canal (comisión variable: Shopify 2%, Amazon 15%, TikTok 5%, Miravia 10-12%, Etsy 6.5%).

**Alternativas descartadas:**
- Shopify only en Fase 2: pierde oportunidad de validar en marketplaces con tráfico ya construido.
- Saltar Shopify e ir directo a Amazon: pierde control de datos de cliente y dependencia algorítmica desde día 1.

---

## ADRs Deprecados o Rechazados

_(Vacío — ningún ADR deprecado aún.)_
