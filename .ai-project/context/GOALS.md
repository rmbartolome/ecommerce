# GOALS — Portafolio Familiar de Emprendimientos (Ecommerce)

> Derivado del BRIEFING.md y documentos de estrategia (docs/).
> **Quién lo escribe:** Claude Code (auditor) — pendiente de validación por AG y CEO.
> **Quién lo lee:** Todos los agentes al inicio de cada sesión.
> **Cuándo se actualiza:** Solo cuando el alcance del proyecto cambia formalmente.

---

## OBJETIVO GENERAL

> Al finalizar este proyecto, el ecosistema ecommerce del Portafolio Familiar opera con las 3 líneas de negocio (Ecommerce Disruptivo, Cosmética, Moda) con tiendas Shopify activas, catálogos estructurados a 3 niveles, al menos 1 SKU por línea con unit economics positivos validados, y los primeros ingresos reales documentados en el laboratorio madre.

---

## MAPA DE OBJETIVOS

```
OBJETIVO GENERAL — Ecosistema ecommerce operativo con primeros ingresos reales
│
├── OE-1: Arquitectura de catálogo completa y validada (3 líneas)
│   ├── OE-1.1: Árbol de categorías 3 niveles — Ecommerce Disruptivo
│   ├── OE-1.2: Árbol de categorías cosmético (tipo piel, ingrediente, origen, certificación)
│   └── OE-1.3: Árbol de categorías textil con variantes talla/color y política de bundles
│
├── OE-2: Research de mercado y proveedores completado
│   ├── OE-2.1: Research mercado España — demanda, saturación, márgenes por categoría
│   ├── OE-2.2: Research mercado Venezuela — arbitraje, canales, métodos de pago, regulación
│   ├── OE-2.3: Research K-Beauty proveedores europeos + guía regulatoria SACS Venezuela
│   ├── OE-2.4: Research perfumería de autor para Venezuela
│   ├── OE-2.5: Research plataformas POD para España (Printful, Gelato, Printify)
│   └── OE-2.6: Research nichos moda España + comparativa marketplaces
│
├── OE-3: Selección de SKUs iniciales con unit economics validados
│   ├── OE-3.1: Calculadora unit economics universal funcional (3 líneas)
│   ├── OE-3.2: Categoría inicial Ecommerce Disruptivo elegida + 3 SKUs candidatos aprobados
│   ├── OE-3.3: SKU inicial Cosmética elegido con unit economics positivos y proveedor confirmado
│   └── OE-3.4: Estrategia diseños POD Moda definida (3-5 conceptos para testar)
│
├── OE-4: Shopify configurado y primera venta realizada (Ecommerce Disruptivo primero)
│   ├── OE-4.1: Tienda Shopify base configurada con árbol de categorías
│   ├── OE-4.2: 3-5 SKUs publicados con fichas de producto SEO completas
│   └── OE-4.3: Primera venta documentada — proof of concept del laboratorio
│
└── OE-5: Stack IA y procesos operativos documentados y funcionando
    ├── OE-5.1: Flujos de trabajo validados (Claude Code / Claude Project / Gemini / Claude Cowork)
    └── OE-5.2: NotebookLM alimentado con todos los documentos ejecutivos
```

---

## OBJETIVOS ESPECÍFICOS

### OE-1 — Arquitectura de Catálogo

**Descripción:** Los 3 árboles de categorías existen como archivos Markdown aprobados por el CEO, con nomenclatura de SKU definida, atributos estándar por categoría y visión para escalar a 200+ SKUs sin refactorizar la estructura.

**Criterio de éxito:**
- [ ] `projects/01_ecommerce_disruptivo/catalog/arbol_categorias_v1.md` existe, tiene 3 niveles y nomenclatura SKU
- [ ] `projects/02_cosmetica/catalog/arbol_categorias_v1.md` existe con atributos cosméticos (tipo piel, ingrediente, origen, certificación)
- [ ] `projects/03_moda/catalog/arbol_categorias_v1.md` existe con política de variantes talla/color documentada
- [ ] CEO ha revisado y aprobado los 3 árboles con "✅ Catálogo aprobado"

**Depende de:** Ninguno (prerequisito de todo lo demás)

**Notas:**
- El árbol de categorías es la decisión más difícil de corregir después — hacerlo bien en OE-1 evita refactorizar Shopify más adelante.
- Prioridad absoluta antes de configurar cualquier tienda.

---

### OE-2 — Research de Mercado y Proveedores

**Descripción:** Cada subdirectorio `market_research/`, `suppliers/` y `regulatory/` de las 3 líneas contiene documentos de research completados, con datos verificables (no inferidos) de 2025-2026, síntesis estratégica de Claude Project y el prompt de Gemini usado documentado para reproducibilidad.

**Criterio de éxito:**
- [ ] `projects/01_ecommerce_disruptivo/market_research/` tiene al menos 2 documentos de research (España + Venezuela)
- [ ] `projects/02_cosmetica/suppliers/` tiene evaluación de distribuidores K-Beauty europeos
- [ ] `projects/02_cosmetica/regulatory/` tiene guía SACS Venezuela con tiempos y costes estimados
- [ ] `projects/03_moda/suppliers/` tiene comparativa de plataformas POD para España
- [ ] Todos los documentos incluyen sección "Prompt usado" para reproducibilidad

**Depende de:** OE-1 (el árbol de categorías define qué productos researchar)

---

### OE-3 — Selección de SKUs y Unit Economics

**Descripción:** Las matrices de decisión permiten al CEO elegir con datos el SKU inicial de cada línea. La calculadora universal funciona para cualquier producto del portafolio y clasifica automáticamente viabilidad.

**Criterio de éxito:**
- [ ] `tools/margin_calculator/unit_economics_universal.md` existe con fórmulas, variables y 5 ejemplos pre-rellenados
- [ ] `projects/01_ecommerce_disruptivo/product_selection/` tiene matriz de decisión de categoría inicial aprobada
- [ ] `projects/02_cosmetica/product_selection/` tiene selección de SKU inicial con unit economics calculados
- [ ] `projects/03_moda/product_selection/` tiene estrategia de diseños POD definida
- [ ] CEO ha firmado "✅ Decisión tomada" en cada matriz

**Depende de:** OE-1 (catálogo), OE-2 (research)

---

### OE-4 — Shopify Operativo y Primera Venta

**Descripción:** La tienda del laboratorio (Ecommerce Disruptivo) está activa en Shopify, con el árbol de categorías configurado, al menos 3 SKUs publicados con fichas SEO, y la primera venta documentada como evidencia de proof-of-concept.

**Criterio de éxito:**
- [ ] URL de tienda Shopify activa y accesible (dominio configurado)
- [ ] 3-5 SKUs publicados con descripción SEO, imágenes y precio
- [ ] Al menos 1 venta real documentada en `projects/01_ecommerce_disruptivo/metrics/`
- [ ] Google Analytics 4 conectado y registrando tráfico

**Depende de:** OE-1, OE-2, OE-3

---

### OE-5 — Stack IA y Procesos Operativos

**Descripción:** Los flujos de trabajo entre agentes están validados en la práctica, no solo en papel. NotebookLM tiene todos los documentos ejecutivos cargados.

**Criterio de éxito:**
- [ ] Al menos 1 ciclo completo documentado: Gemini (research) → Claude Project (síntesis) → repo
- [ ] `shared/analytics/dashboards/` tiene definición de KPIs y umbrales de la línea madre
- [ ] NotebookLM tiene cargados los 3 documentos de estrategia v2

**Depende de:** OE-2, OE-3

---

## ROADMAP DE ENTREGA

| Fase | Semana | Objetivo(s) | Entregable verificable | Responsable |
|---|---|---|---|---|
| **Fase 0 — Arquitectura** | 1 | OE-1 + OE-3.1 | 3 árboles de categorías + calculadora unit economics | AG + CEO aprueba |
| **Fase 1 — Research** | 2-3 | OE-2 completo | 6 documentos de research en repo | AG (Gemini) → Claude Project |
| **Fase 2 — Decisión** | 4 | OE-3.2, 3.3, 3.4 | 3 matrices de decisión aprobadas por CEO | Claude Project → CEO |
| **Fase 3 — Lanzamiento** | 5-8 | OE-4 | Shopify activo + primera venta | Claude Cowork + CEO |
| **Fase continua** | Mes 3+ | OE-5 | Dashboards + NotebookLM alimentado | Todos los agentes |

---

## FUERA DE ALCANCE

- [ ] Desarrollo de software propio (ERP, plataforma propia) — Shopify es la plataforma, no se construye tecnología propia en Fase 1
- [ ] Activación de la línea Moda antes de que Ecommerce Disruptivo tenga ingresos estables
- [ ] Integración OMS multicanal (Amazon/Miravia) — Fase 2 tras validar en Shopify
- [ ] Inventario físico propio — solo dropshipping y POD en Fase 1
- [ ] Línea Cosmética Venezuela antes de tener el SACS resuelto — no comprometer capital regulatorio sin claridad

---

## RELACIÓN CON OTROS DOCUMENTOS

| Documento | Función | Cuándo leerlo |
|---|---|---|
| `BRIEFING.md` | Visión del CEO — el qué y las restricciones | Antes de escribir o cambiar GOALS.md |
| `GOALS.md` | Este archivo — mapa estratégico | Al inicio de cada sesión |
| `DECISIONS.md` | ADRs — por qué se tomaron las decisiones clave | Cuando hay una decisión arquitectónica |
| `STATUS.md` | Estado vivo del proyecto | En cada iteración activa |
| `docs/plan_research_repo.md` | Plan detallado de research con prompts | Al ejecutar tareas de Fase 1 |
| `docs/ecommerce_repo_setup.md` | Setup original del ecosistema | Referencia histórica — superado por el framework |

---

## HISTORIAL DE CAMBIOS DE ALCANCE

| Fecha | Cambio | Razón | Aprobado por |
|---|---|---|---|
| 2026-06-07 | Alcance inicial definido | Setup del framework | Claude Code (auditor) |
