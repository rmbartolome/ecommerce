# REPOSITORIO: ecommerce-portfolio

## Ecosistema Ecommerce — Cosmética · Moda · Ecommerce Disruptivo

### Portafolio Familiar de Emprendimientos

**Versión:** 1.0

**Fecha:** Mayo 2026

**Clasificación:** Núcleo Central

**CEO:** Roberto

**CTO / AI Assistant:** Claude (Project + Code + Design)

---

## 1. PROPÓSITO DEL REPOSITORIO

Este repositorio centraliza **todo el trabajo del ecosistema ecommerce**

del portafolio en un solo lugar estructurado, versionado y colaborable entre

Roberto (CEO), Claude Code (CTO técnico), Claude Cowork (operaciones) y

Claude Design (activos visuales).

No es solo código. Es el sistema operativo completo de tres líneas de

negocio:

- **Ecommerce Disruptivo** — Laboratorio madre de validación comercial

- **Cosmética, Perfumes y Marca Personal** — Importación → marca

curada → white label

- **Moda, Diseño y Fabricación** — POD → white label → marca propia

Todo lo que se produce, decide, diseña, publica o mide **vive aquí**.

---

## 2. ESTRUCTURA DEL REPOSITORIO

```

ecommerce-portfolio/

│

├── .github/

│   ├── ISSUE_TEMPLATE/

│   │   ├── decision.md          → Template para decisiones estratégicas

│   │   ├── research.md          → Template para encargos de

investigación

│   │   └── task.md              → Template para tareas operativas

│   └── workflows/

│       └── weekly-review.yml    → Recordatorio semanal de revisión

(futuro)

│

├── memory/                      ← CEREBRO DEL REPO — Claude lee esto

primero

│   ├── CLAUDE.md                → Instrucciones permanentes para

Claude Code/Cowork

│   ├── global_context.md        → Estado actual del ecosistema

ecommerce

│   ├── agents.md                → Qué hace cada herramienta IA y cuándo

usarla

│   ├── decisions_log.md         → Registro de decisiones tomadas

(fecha + razón)

│   └── skills.md                → Capacidades disponibles en este proyecto

│

├── projects/

│   ├── 01_ecommerce_disruptivo/ ← Línea madre — laboratorio

comercial

│   │   ├── README.md

│   │   ├── market_research/     → Estudios de mercado y análisis de

tendencias

│   │   ├── product_selection/   → Fichas de producto candidato,

evaluaciones

│   │   ├── strategy/            → Estrategia, hipótesis de validación,

roadmap

│   │   ├── catalog/             → Arquitectura de catálogo, árbol de

categorías, SKUs

│   │   ├── operations/          → Proveedores, logística, fulfillment

│   │   └── metrics/             → KPIs, umbrales, resultados reales

│   │

│   ├── 02_cosmetica/            ← Caso de uso — importación + marca

curada

│   │   ├── README.md

│   │   ├── market_research/

│   │   ├── product_selection/   → Shortlist de SKUs, evaluación K-

Beauty, perfumería

│   │   ├── strategy/            → Tesis, secuencia de fases, pricing

│   │   ├── catalog/             → Árbol de categorías cosmético,

atributos, SKU naming

│   │   ├── regulatory/          → SACS Venezuela, CPNP UE, AEMPS,

fichas regulatorias

│   │   ├── suppliers/           → Proveedores europeos, distribuidores K-

Beauty

│   │   ├── logistics/           → Operadores Venezuela, cálculo unit

economics

│   │   ├── marketing/           → Estrategia de contenido, calendario,

copies

│   │   └── metrics/

│   │

│   └── 03_moda/                 ← Caso de uso — POD + white label +

marca propia

│       ├── README.md

│       ├── market_research/

│       ├── product_selection/   → Diseños candidatos, nichos,

proveedores POD

│       ├── strategy/            → Tesis, modelos de entrada, secuencia

│       ├── catalog/             → Árbol textil, variantes talla/color, SKU

naming

│       ├── designs/             → Activos de diseño, mockups, fichas de

colección

│       ├── suppliers/           → Printful, Printify, Gelato, fabricantes

España

│       ├── marketing/           → Estrategia de contenido, TikTok Shop,

Creator Merch

│       └── metrics/

│

├── shared/                      ← Activos transversales a las 3 líneas

│   ├── shopify/

│   │   ├── store_config/        → Configuración base de tienda, apps,

integraciones

│   │   ├── themes/              → Customizaciones de tema

│   │   └── oms_integration/     → Configuración OMS multicanal

(Amazon, Miravia)

│   ├── marketing/

│   │   ├── brand_identity/      → Paletas, tipografías, guías de marca

por línea

│   │   ├── content_calendar/    → Calendario editorial unificado

│   │   ├── ad_copy/             → Copies de anuncio reutilizables

│   │   └── social_templates/    → Templates para Instagram, TikTok,

WhatsApp

│   ├── analytics/

│   │   └── dashboards/          → Definición de dashboards y métricas

unificadas

│   └── legal/

│       └── templates/           → Términos, política de privacidad, GDPR

│

├── docs/                        ← Documentación ejecutiva del proyecto

│   ├── strategy/

│   │   ├── 11_ecommerce_madre_v2.docx

│   │   ├── 09_cosmetica_v2.docx

│   │   └── 10_moda_v2.docx

│   ├── decisions/               → PDFs/docs de decisiones estratégicas

│   └── briefings/               → Briefings semanales del estado del

ecosistema

│

├── tools/                       ← Scripts y automatizaciones del ecosistema

│   ├── catalog_builder/         → Scripts para generar fichas de

producto en batch

│   ├── sku_generator/           → Generador de nomenclatura de SKUs

│   ├── margin_calculator/       → Calculadora de unit economics (precio

+ flete + tasas)

│   └── content_generator/       → Prompts y scripts para generación de

contenido IA

│

├── .gitignore

├── README.md                    ← Este archivo

└── CHANGELOG.md                 → Registro de cambios importantes del

repositorio

```

---

## 3. /memory/ — EL CEREBRO DEL REPOSITORIO

Esta carpeta es la más importante. **Claude Code, Claude Cowork y

Claude Design leen `/memory/` al inicio de cada sesión** antes de hacer

cualquier cosa. Es el contexto permanente que permite que cualquier

instancia de Claude retome el trabajo exactamente donde se quedó.

### 3.1 `memory/CLAUDE.md` — Instrucciones permanentes para Claude

```markdown

# CLAUDE.md — Instrucciones para Claude en este repositorio

## Identidad y rol

Eres el CTO y asistente del CEO de este proyecto de ecommerce.

Roberto es el CEO y el decisor final. Tú ejecutas, propones y documentas.

Nunca tomes decisiones estratégicas sin aprobación explícita del CEO.

## Contexto del proyecto

Este repositorio gestiona 3 líneas de ecommerce del Portafolio Familiar de

Emprendimientos:

1. Ecommerce Disruptivo — laboratorio comercial madre

(projects/01_ecommerce_disruptivo/)

2. Cosmética, Perfumes y Marca Personal (projects/02_cosmetica/)

3. Moda, Diseño y Fabricación (projects/03_moda/)

Mercados: España (validación digital) y Venezuela (importación/arbitraje).

Plataforma central: Shopify → Amazon/Miravia como expansión validada.

## Lo que haces en cada sesión

1. Leer memory/global_context.md → ¿qué está activo? ¿qué cambió?

2. Leer memory/decisions_log.md → ¿qué se ha decidido ya? No repitas

debates cerrados.

3. Ejecutar la tarea del CEO con el contexto cargado.

4. Al terminar: actualizar global_context.md si hubo cambios de estado.

5. Registrar decisiones nuevas en decisions_log.md.

## Reglas de operación

- NO hacer cambios destructivos en catalog/, shopify/ o tools/ sin

aprobación explícita.

- NO crear nuevas carpetas de proyecto sin instrucción del CEO.

- NO comprometer capital (proveedores, SKUs, campañas) sin decisión

explícita.

- Los secrets y credenciales NUNCA van en el repositorio.

- Documentar TODO lo que se genera: si no está en el repo, no existe.

- Preferir Markdown para documentos de trabajo, .docx para entregables

formales.

## Herramientas del ecosistema (Mayo 2026)

- Claude Project: cerebro estratégico y análisis (eres tú en modo Project)

- Claude Code: desarrollo técnico, scripts, automatizaciones (eres tú en

modo Code)

- Claude Cowork: operaciones y gestión de tareas (eres tú en modo

Cowork)

- Claude Design: activos visuales, mockups, diseños (eres tú en modo

Design)

- Gemini Pro: research externo, validación de mercado

- ChatGPT: comunicaciones persuasivas, tono de marca

- NotebookLM: archivo consultable, Audio Overview del portafolio

## Lo que NO usamos en este proyecto

- OpenClaw / NemoClaw / Auris — descontinuados en este ecosistema

## Stack técnico del repositorio

- Control de versiones: Git + GitHub

- Documentos ejecutivos: .docx (generados con docx-js)

- Documentos de trabajo: Markdown

- Scripts: Python o Node.js según la tarea

- Tienda: Shopify (sin construir tecnología propia en Fase 1)

```

### 3.2 `memory/global_context.md` — Estado actual del ecosistema

```markdown

# global_context.md — Estado del Ecosistema Ecommerce

**Última actualización:** [FECHA]

**Actualizado por:** [Claude Code / Roberto]

## Estado por línea

### 01 — Ecommerce Disruptivo

- **Fase actual:** Definición estratégica

- **Próxima acción crítica:** Definir árbol de categorías base del catálogo

- **Decisiones pendientes:** Categoría inicial, mercado de validación,

fulfillment

- **Bloqueado por:** Reunión núcleo para cerrar decisión de categoría

- **Ingresos actuales:** €0

### 02 — Cosmética

- **Fase actual:** Definición estratégica

- **Próxima acción crítica:** Elegir SKU inicial y proveedor K-Beauty

- **Decisiones pendientes:** Árbol de categorías cosmético, método de

cobro Venezuela

- **Bloqueado por:** Selección de proveedor regulatoriamente conforme

- **Ingresos actuales:** €0

### 03 — Moda

- **Fase actual:** Definición estratégica — en espera de línea madre

- **Próxima acción crítica:** Definir árbol de categorías textil

- **Decisiones pendientes:** Plataforma POD, primer diseño a testar

- **Activación:** Solo cuando Ecommerce Disruptivo tenga ingresos

estables

- **Ingresos actuales:** €0

## Decisiones globales cerradas

- Plataforma central: Shopify (decisión Onás — Mayo 2026)

- Secuencia: Shopify → redes sociales → Amazon (decisión Onás — Mayo

2026)

- Arquitectura de catálogo: crítica antes de lanzar (decisión Onás — Mayo

2026)

- Stack IA activo: Claude (Project/Code/Cowork/Design) + Gemini +

ChatGPT + NotebookLM

- Stack IA descontinuado: OpenClaw, NemoClaw, Auris

## Próxima sesión de trabajo

- **Objetivo:** [COMPLETAR]

- **Herramienta principal:** [Claude Code / Claude Cowork / Claude

Design]

- **Output esperado:** [COMPLETAR]

```

### 3.3 `memory/agents.md` — Mapa de herramientas IA

```markdown

# agents.md — Quién hace qué en el ecosistema IA

## Arquitectura de decisión

Roberto (CEO — decisor final)

│

├── Claude Project ────────── Cerebro estratégico, análisis,

documentos ejecutivos

│   ├── Claude Code ────────── Desarrollo técnico, scripts,

automatizaciones

│   ├── Claude Cowork ──────── Operaciones, gestión de

tareas, flujos de trabajo

│   └── Claude Design ──────── Activos visuales, mockups,

contenido gráfico

│

├── Gemini Pro ─────────────── Research externo,

datos de mercado, validación

├── ChatGPT ────────────────── Comunicaciones

persuasivas, copies de marca, tono

└── NotebookLM ─────────────── Archivo vivo,

consultas cruzadas, Audio Overview

## Cuándo usar cada uno

| Tarea | Herramienta |

|-------|-------------|

| Análisis estratégico, decisiones, documentos ejecutivos | Claude Project |

| Scripts, automatizaciones, generación de fichas en batch | Claude Code |

| Gestión de tareas, flujos operativos, seguimiento | Claude Cowork |

| Mockups, diseños de producto, banners, social assets | Claude Design |

| Research de mercado, tendencias, datos verificables | Gemini Pro |

| Copies de marca, mensajes a participantes, tono persuasivo | ChatGPT |

| Consultas cruzadas entre documentos, Audio Overview | NotebookLM |

## NO usar en este proyecto

- OpenClaw / NemoClaw / Auris — fuera del stack activo

```

### 3.4 `memory/decisions_log.md` — Registro de decisiones

```markdown

# decisions_log.md — Registro de Decisiones del Ecosistema

Formato: [FECHA] | [ÁREA] | [DECISIÓN] | [RAZÓN] | [DECIDIDO POR]

---

## 2026-05

| Fecha | Área | Decisión | Razón | Decidido por |

|-------|------|----------|-------|--------------|

| 2026-05-04 | Stack IA | Descontinuar OpenClaw, NemoClaw y Auris |

Consolidar en Claude ecosystem | Roberto |

| 2026-05-04 | Plataforma | Shopify como base central del ecosistema |

Recomendación experto Onás | Roberto |

| 2026-05-04 | Secuencia | Shopify → redes → Amazon (no al revés) |

Validar en Shopify antes de escalar | Roberto |

| 2026-05-04 | Catálogo | Arquitectura de catálogo antes de lanzar |

Costoso de corregir después (Onás) | Roberto |

| 2026-05-04 | Repositorio | Crear ecommerce-portfolio en Git | Centralizar

operación de las 3 líneas | Roberto |

```

---

## 4. FLUJO DE TRABAJO CON IA

### 4.1 Inicio de sesión — Protocolo estándar

```

INICIO DE CADA SESIÓN DE TRABAJO:

│

1. Claude lee memory/CLAUDE.md         → Instrucciones permanentes

2. Claude lee memory/global_context.md  → ¿Qué está activo? ¿Qué

cambió?

3. Claude lee memory/decisions_log.md   → ¿Qué está ya decidido?

4. CEO comunica el objetivo de la sesión

5. Claude ejecuta con contexto completo

│

AL FINALIZAR LA SESIÓN:

│

6. Actualizar global_context.md si hubo cambios de estado

7. Registrar nuevas decisiones en decisions_log.md

8. Hacer commit de todo lo generado con mensaje descriptivo

9. Subir a NotebookLM si es documento ejecutivo

```

### 4.2 Tipos de sesión y herramienta principal

| Tipo de sesión | Herramienta | Output típico |

|----------------|-------------|---------------|

| Análisis de mercado | Claude Project + Gemini | Documento de research

en /market_research/ |

| Selección de producto | Claude Project | Ficha evaluación SKU en

/product_selection/ |

| Diseño de catálogo | Claude Code | Árbol de categorías + plantilla SKUs

en /catalog/ |

| Estrategia de marketing | Claude Project + ChatGPT | Plan editorial en

/marketing/ |

| Diseño de activos | Claude Design | Mockups, banners en /designs/ o

/marketing/ |

| Publicación de producto | Claude Cowork | Ficha Shopify lista en /catalog/

|

| Gestión de inventario | Claude Cowork + Claude Code | Dashboard

métricas en /metrics/ |

| Script o automatización | Claude Code | Script funcional en /tools/ |

| Revisión semanal | Claude Cowork | Briefing en /docs/briefings/ |

### 4.3 Flujo de research de mercado

```

CEO define hipótesis de producto o categoría a investigar

│

├── Gemini Pro → Research externo (tendencias, datos, competidores,

precios)

│

├── Claude Project → Síntesis y análisis estratégico

│   └── Output: documento en projects/XX/market_research/YYYY-

MM-DD_tema.md

│

└── NotebookLM → Archivo para consultas cruzadas futuras

```

### 4.4 Flujo de selección y publicación de producto

```

CEO aprueba categoría a testear

│

├── Claude Code → Generar ficha de evaluación SKU (margen,

proveedor, regulación)

│   └── Output: projects/XX/product_selection/YYYY-MM-

DD_SKU_evaluacion.md

│

├── CEO → Decisión go/no-go

│

├── Claude Code → Generar ficha de producto Shopify (descripción

SEO, atributos, variantes)

│   └── Output: projects/XX/catalog/SKU_shopify_listing.md

│

├── Claude Design → Generar mockups e imágenes de producto

│   └── Output: projects/XX/designs/ o

shared/marketing/brand_identity/

│

└── Claude Cowork → Publicar en Shopify + registrar en catalog/

```

### 4.5 Flujo de creación de contenido para marketing

```

CEO define tema o producto a comunicar

│

├── Claude Project → Estrategia del contenido (qué decir, a quién, en

qué canal)

│

├── Claude Design → Creación de activos visuales (posts, reels, stories)

│   └── Output: shared/marketing/social_templates/

│

├── ChatGPT → Copy persuasivo adaptado al tono de cada marca/línea

│   └── Output: shared/marketing/ad_copy/

│

└── Claude Cowork → Programar en calendario editorial

    └── Output: shared/marketing/content_calendar/

```

---

## 5. CONVENCIONES DEL REPOSITORIO

### 5.1 Naming de archivos

```

# Documentos de trabajo

YYYY-MM-DD_descripcion_corta.md

Ejemplo: 2026-05-10_kbeauty_proveedores_españa.md

# Fichas de SKU

SKU_[MARCA]_[LINEA]_[REFERENCIA]_[VOLUMEN].md

Ejemplo: SKU_SKIN1004_CENTELLA_AMPOULE_100ML.md

# Diseños y activos

[linea]_[tipo]_[descripcion]_[version].[ext]

Ejemplo: cosmetica_post_instagram_centella_v1.png

# Documentos ejecutivos (docx)

[numero]_[linea]_[tema]_v[version].docx

Ejemplo: 09_cosmetica_estrategia_v2.docx

```

### 5.2 Convenciones de Git

```bash

# Mensajes de commit

[área] acción descriptiva en presente

# Ejemplos:

[cosmetica] añadir evaluación SKU Skin1004 Centella Ampoule

[catalog] definir árbol de categorías cosmético nivel 1-3

[marketing] generar calendario editorial semana 2

[strategy] cerrar decisión de fulfillment Fase 1

[tools] añadir calculadora unit economics Venezuela

[memory] actualizar global_context tras reunión núcleo

# Ramas

main          → estado aprobado por el CEO

dev           → trabajo en curso

feature/tema  → desarrollo de una funcionalidad específica

```

### 5.3 Issues de GitHub — Templates

**Template: Decisión estratégica**

```markdown

## Decisión pendiente: [TÍTULO]

**Línea afectada:** 01_ecommerce / 02_cosmetica / 03_moda / shared

**Prioridad:** CRÍTICA / ALTA / MEDIA

**Fecha límite:** [FECHA]

### Contexto

[Por qué hay que tomar esta decisión ahora]

### Opciones

- Opción A: [descripción]

- Opción B: [descripción]

### Recomendación del CTO

[Análisis y recomendación de Claude]

### Decisión del CEO

[ ] Pendiente

[ ] Aprobada: [opción elegida]

[ ] Aplazada hasta: [fecha]

```

**Template: Encargo de research**

```markdown

## Research: [TÍTULO]

**Línea:** [línea de negocio]

**Herramienta:** Gemini Pro / Claude Project

**Output esperado:** [formato y ubicación]

### Pregunta a responder

[Qué necesitamos saber exactamente]

### Criterios de calidad

[Qué hace bueno este research]

### Estado

[ ] Pendiente

[ ] En progreso

[ ] Completado → [enlace al archivo]

```

---

## 6. CONFIGURACIÓN INICIAL — SETUP DEL REPOSITORIO

### 6.1 Crear el repositorio en GitHub

```bash

# 1. Crear repo en GitHub (privado)

# Nombre: ecommerce-portfolio

# Descripción: Ecosistema Ecommerce — Cosmética · Moda · Ecommerce

Disruptivo

# Visibilidad: Privado

# Inicializar con README: Sí

# 2. Clonar localmente

git clone https://github.com/[usuario]/ecommerce-portfolio.git

cd ecommerce-portfolio

# 3. Crear la estructura de carpetas

mkdir -p .github/ISSUE_TEMPLATE

mkdir -p .github/workflows

mkdir -p memory

mkdir -p

projects/01_ecommerce_disruptivo/{market_research,product_selection,strategy,catalog,operatio

mkdir -p

projects/02_cosmetica/{market_research,product_selection,strategy,catalog,regulatory,suppliers

mkdir -p

projects/03_moda/{market_research,product_selection,strategy,catalog,designs,suppliers,marke

mkdir -p

shared/{shopify/{store_config,themes,oms_integration},marketing/{brand_identity,content_calen

mkdir -p docs/{strategy,decisions,briefings}

mkdir -p

tools/{catalog_builder,sku_generator,margin_calculator,content_generator}

# 4. Crear archivos base

touch memory/CLAUDE.md

touch memory/global_context.md

touch memory/agents.md

touch memory/decisions_log.md

touch memory/skills.md

touch CHANGELOG.md

touch .gitignore

# 5. Crear .gitignore

cat > .gitignore << 'EOF'

# Secrets y credenciales — NUNCA en el repo

.env

.env.*

secrets/

credentials/

*.key

*.pem

# Sistema operativo

.DS_Store

Thumbs.db

# Node / Python

node_modules/

__pycache__/

*.pyc

.venv/

# Archivos temporales

*.tmp

*.bak

~*

# Activos pesados (usar Git LFS si es necesario)

*.mp4

*.mov

*.psd

*.ai

EOF

# 6. Primer commit

git add .

git commit -m "[repo] setup inicial — estructura completa del ecosistema

ecommerce"

git push origin main

```

### 6.2 Copiar los documentos ejecutivos existentes

```bash

# Copiar los docs v2 generados con las recomendaciones de Onás

cp 11_ecommerce_madre_v2.docx docs/strategy/

cp 09_cosmetica_v2.docx docs/strategy/

cp 10_moda_v2.docx docs/strategy/

git add docs/strategy/

git commit -m "[docs] añadir documentos estratégicos v2 con

recomendaciones Onás"

git push origin main

```

### 6.3 Poblar los archivos /memory/

```bash

# Copiar el contenido de las secciones 3.1 a 3.4 de este documento

# en sus respectivos archivos memory/*.md

git add memory/

git commit -m "[memory] inicializar cerebro del repositorio — CLAUDE.md,

global_context, agents, decisions"

git push origin main

```

### 6.4 Configurar Claude Code para este repositorio

Cuando abras Claude Code en este directorio, el archivo

`memory/CLAUDE.md` se carga automáticamente como contexto. Claude

Code leerá las instrucciones permanentes, el estado actual y el log de

decisiones antes de ejecutar cualquier tarea.

**Instrucción de apertura de sesión para Claude Code:**

```

Lee memory/CLAUDE.md, memory/global_context.md y

memory/decisions_log.md.

Confirma el estado actual del ecosistema y espera instrucciones del CEO.

```

---

## 7. ROADMAP DEL REPOSITORIO

### Fase 0 — Setup (Semana 1)

- [ ] Crear repositorio en GitHub (privado)

- [ ] Ejecutar setup inicial (sección 6.1)

- [ ] Poblar archivos /memory/ con contexto actual

- [ ] Copiar documentos estratégicos v2 a /docs/strategy/

- [ ] Primera sesión con Claude Code: verificar que lee el contexto

correctamente

### Fase 1 — Ecommerce Disruptivo activo (Semanas 2–6)

- [ ] Definir árbol de categorías con Claude Code →

/01_ecommerce_disruptivo/catalog/

- [ ] Research de categoría inicial con Gemini →

/01_ecommerce_disruptivo/market_research/

- [ ] Evaluar primeros 3 SKUs candidatos →

/01_ecommerce_disruptivo/product_selection/

- [ ] Configurar Shopify base con Claude Cowork

- [ ] Crear calculadora unit economics → /tools/margin_calculator/

- [ ] Primer diseño de ficha de producto →

/01_ecommerce_disruptivo/catalog/

### Fase 2 — Cosmética activada (Meses 2–3)

- [ ] Árbol de categorías cosmético → /02_cosmetica/catalog/

- [ ] Research regulatorio SACS Venezuela → /02_cosmetica/regulatory/

- [ ] Evaluación shortlist K-Beauty → /02_cosmetica/product_selection/

- [ ] Estrategia de contenido Daniely → /02_cosmetica/marketing/

- [ ] Activos de marca visual → /shared/marketing/brand_identity/

### Fase 3 — Moda activada (Mes 3–6, tras señal de mercado)

- [ ] Árbol de categorías textil con variantes → /03_moda/catalog/

- [ ] Integración Printful/Printify con Shopify → /shared/shopify/

- [ ] Primeros 3 diseños POD → /03_moda/designs/

- [ ] Estrategia Creator Merch → /03_moda/marketing/

### Fase continua — Operación y escalado

- [ ] OMS multicanal → /shared/shopify/oms_integration/

- [ ] Dashboard de métricas unificado → /shared/analytics/

- [ ] Automatización de generación de contenido →

/tools/content_generator/

---

## 8. SESIÓN INAUGURAL — PRIMER COMANDO A CLAUDE CODE

Una vez creado el repositorio y poblados los archivos /memory/, la primera

sesión de trabajo con Claude Code arranca con este prompt:

```

Eres el CTO de este proyecto de ecommerce. Yo soy el CEO.

Lee memory/CLAUDE.md para entender tus instrucciones permanentes.

Lee memory/global_context.md para ver el estado actual del ecosistema.

Lee memory/decisions_log.md para saber qué está ya decidido.

Confirma que has cargado el contexto correctamente con un resumen de:

1. Las 3 líneas activas y su estado

2. Las 3 decisiones más recientes registradas

3. La próxima acción crítica en cada línea

Después de confirmar, espera mi primera instrucción de trabajo.

```

---

*Documento generado con Claude — Portafolio Familiar de

Emprendimientos*

*NÚCLEO CENTRAL · No distribuir sin segmentar*

