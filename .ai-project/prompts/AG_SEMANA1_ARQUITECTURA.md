# PROMPT AG — Semana 1: Arquitectura de Catálogo

> **Herramienta:** Gemini Pro (Google AI Studio o Gemini Advanced)
> **Cuándo usar:** Una vez que el CEO haya aprobado TOOLS.md (`✅ Herramientas aprobadas`)
> **Output:** 4 archivos Markdown en el repositorio
> **Tiempo estimado:** 1 sesión de trabajo (2-3 horas)

---

## INSTRUCCIÓN DE APERTURA PARA AG

Copia y pega el siguiente bloque completo como primer mensaje en Gemini Pro:

---

```
Eres Antigravity (AG), el agente Builder/Implementer del Portafolio Familiar de Emprendimientos.

Tu CEO es Roberto. Operas bajo el framework AI Seed Projects v3.0.0.

CONTEXTO DEL PROYECTO:
Este repositorio centraliza 3 líneas de negocio ecommerce:
1. Ecommerce Disruptivo — laboratorio de validación comercial (España)
2. Cosmética, Perfumes y Marca Personal — importación España → Venezuela
3. Moda, Diseño y Fabricación — Print-on-Demand, mercado España

Plataforma central: Shopify (decisión cerrada, no debatir)
Stack IA: Claude (análisis), Gemini Pro (tú — research y generación), ChatGPT (copies)

RESTRICCIONES INAMOVIBLES:
- El árbol de categorías debe tener 3 niveles y servir para escalar a 200+ SKUs
- La nomenclatura de SKU debe ser consistente, corta y sin caracteres especiales
- No inventar datos de mercado — si no sabes algo, indicar dónde buscar
- Cada archivo generado va en la ruta exacta indicada

TU TAREA DE HOY:
Ejecutar las 4 tareas de Semana 1 en orden. Por cada tarea:
1. Genera el contenido completo en formato Markdown
2. Indica la ruta exacta donde debe guardarse en el repo
3. Espera confirmación antes de pasar a la siguiente

¿Listo? Confirma que has entendido el contexto y espera la primera tarea.
```

---

## TAREA 0.1 — Árbol de Categorías: Ecommerce Disruptivo

**Ruta de destino:** `projects/01_ecommerce_disruptivo/catalog/arbol_categorias_v1.md`

Pega este prompt tras confirmar contexto:

```
TAREA 0.1 — Árbol de categorías del Ecommerce Disruptivo

Genera el árbol de categorías para el laboratorio de validación comercial.

CONTEXTO:
- Tienda Shopify orientada a productos funcionales y estéticos para España
- Expansión potencial a LATAM (Venezuela)
- Modelo de entrada: dropshipping europeo (BigBuy España + Spocket)
- Categorías base identificadas en el plan estratégico:
  * Hogar inteligente y confort
  * Tecnología wearable
  * Salud, bienestar y deporte
  * Pet Tech
  * Sostenibilidad y economía circular
  * Kits y bundles curados

FORMATO DE SALIDA — Markdown completo listo para subir al repo:

# Árbol de Categorías — Ecommerce Disruptivo v1

## Criterios de diseño del catálogo
[Explica brevemente la lógica del árbol — qué prioridades guiaron las decisiones]

## Estructura de 3 niveles

### NIVEL 1 — Categorías principales
[Para cada categoría de nivel 1:]

#### [Nombre Categoría N1]
**Código:** [CAT-XX]
**Descripción:** [una línea]
**Razón de inclusión:** [por qué tiene potencial en España 2026]

**Subcategorías (Nivel 2):**
- [Nombre N2] — [Código N2-XX] — Atributos: [lista de atributos estándar]
  - [Producto tipo N3] — Nomenclatura SKU: [CÓDIGO-DESCRIPCION-VARIANTE]
  - [Producto tipo N3] — Nomenclatura SKU: [CÓDIGO-DESCRIPCION-VARIANTE]

## Tabla de nomenclatura SKU

| Categoría N1 | Prefijo | Ejemplo SKU | Estructura |
|---|---|---|---|
| [nombre] | [XXX] | [XXX-PRODUCTO-VAR] | [PREFIJO-NOMBRE-VARIANTE] |

## Atributos estándar por categoría

| Categoría | Atributos obligatorios | Atributos opcionales |
|---|---|---|
| [nombre] | [lista] | [lista] |

## Reglas de nomenclatura SKU
[Máximo 5 reglas claras para aplicar en cualquier producto futuro]

## Productos excluidos de este catálogo
[Lista explícita de lo que NO entra y por qué — evita ambigüedad]
```

---

## TAREA 0.2 — Árbol de Categorías: Cosmética

**Ruta de destino:** `projects/02_cosmetica/catalog/arbol_categorias_v1.md`

```
TAREA 0.2 — Árbol de categorías de Cosmética, Perfumes y Marca Personal

Genera el árbol de categorías para la línea de cosmética.

CONTEXTO:
- Mercado primario: Venezuela (importación desde España)
- Mercado secundario: España (validación digital)
- Modelo: importar productos cosméticos europeos con alta percepción de valor en Venezuela
- Líneas identificadas en el plan estratégico:
  * K-Beauty / Skincare (coreano — Centella Asiática, Niacinamida, Snail Mucin)
  * Perfumería de autor y nicho
  * Body care y cuidado personal
  * Kits curados (sets de regalo de alta percepción)
  * Cosmética masculina
- Atributos clave en cosmética: tipo de piel, ingrediente activo, origen geográfico, certificación (vegano, K-Beauty, UE, COSMOS)
- Regulación crítica: SACS Venezuela para importación, CPNP para venta en UE

FORMATO DE SALIDA — Markdown completo:

# Árbol de Categorías — Cosmética v1

## Criterios de diseño del catálogo cosmético
[Lógica específica para cosmética: atributos regulatorios, naming de origen, certificaciones]

## Estructura de 3 niveles

[Mismo formato que Tarea 0.1, adaptado a cosmética]

## Tabla de atributos cosméticos

| Atributo | Valores posibles | Obligatorio |
|---|---|---|
| Tipo de piel | Seca / Grasa / Mixta / Sensible / Normal / Todo tipo | Sí |
| Ingrediente activo | [lista de los más relevantes] | Sí (máx 3) |
| Origen | Corea / Francia / España / Japón / Alemania / Otro | Sí |
| Certificación | K-Beauty / Vegano / COSMOS / Sin certificación | No |
| Regulación SACS | Requerida / No requerida / Pendiente | Sí (para Venezuela) |

## Nomenclatura SKU cosmético

Ejemplo: SKIN1004_CENTELLA_AMPOULE_100ML
Estructura: [MARCA/ORIGEN]_[INGREDIENTE]_[TIPO]_[VOLUMEN]

## Reglas de etiquetado bilingüe
[Mínimo requerido en etiqueta para Venezuela y para España — diferencias clave]
```

---

## TAREA 0.3 — Árbol de Categorías: Moda

**Ruta de destino:** `projects/03_moda/catalog/arbol_categorias_v1.md`

```
TAREA 0.3 — Árbol de categorías de Moda, Diseño y Fabricación

Genera el árbol de categorías para la línea de moda.

CONTEXTO:
- Mercado principal: España
- Modelo de entrada: Print-on-Demand (Printful + Gelato) → White Label → Marca propia
- Audiencia: comunidad de Daniely (lifestyle, cosmética, aspiracional, 25-40 años, España y LATAM)
- Líneas identificadas:
  * Ropa estética / identity-driven (camisetas, sudaderas, diseños propios)
  * Accesorios lifestyle sin talla (gorras, tote bags, bolsos)
  * Joyería private label (accesorios)
  * Moda sostenible (materiales orgánicos, GOTS/OEKO-TEX)
  * Creator Merch (vinculado a la marca personal de Daniely)
- CRÍTICO: Shopify maneja variantes talla/color de forma compleja — el árbol debe definir
  explícitamente cómo se agrupan los productos (variantes del mismo producto vs productos
  independientes) para evitar configuraciones incorrectas

FORMATO DE SALIDA — Markdown completo:

# Árbol de Categorías — Moda v1

## Criterios de diseño del catálogo textil
[Lógica de variantes talla/color en Shopify — política explícita]

## Política de variantes (CRÍTICO)

### Productos con variantes agrupadas (mismo SKU padre)
[Qué tipos de producto se configuran como un solo producto con variantes de talla/color]

### Productos independientes (SKU diferente por color/diseño)
[Qué tipos de producto van como listings independientes]

## Estructura de 3 niveles

[Mismo formato que anteriores, adaptado a textil]

## Atributos estándar textiles UE

| Atributo | Valores posibles | Obligatorio |
|---|---|---|
| Talla | XS / S / M / L / XL / XXL / Única | Sí (excepto accesorios) |
| Material | [lista — algodón, poliéster, algodón orgánico, etc.] | Sí |
| Técnica impresión | DTG / Sublimación / Bordado / Serigrafía | Sí (para POD) |
| Certificación | GOTS / OEKO-TEX / Ninguna | No |

## Nomenclatura SKU textil

Ejemplo: CAP01-CAMISETA-NEGRO-M
Estructura: [COLECCIÓN]-[PRODUCTO]-[COLOR]-[TALLA]

## Guía de sizing europeo
[Tabla de tallas con equivalencias ES/FR/DE para evitar devoluciones]
```

---

## TAREA 4.2 — Calculadora Unit Economics Universal

**Ruta de destino:** `tools/margin_calculator/unit_economics_universal.md`

```
TAREA 4.2 — Calculadora de Unit Economics Universal

Crea una calculadora de unit economics en formato Markdown que sirva para evaluar
cualquier SKU en las 3 líneas del portafolio: Ecommerce Disruptivo, Cosmética y Moda.

VARIABLES DE ENTRADA:
- Línea de negocio: Ecommerce Disruptivo / Cosmética (Venezuela) / Moda (POD)
- Precio de compra o coste de producción (€)
- Coste logístico total (€/unidad — incluye envío al cliente y tasa de devolución esperada)
- Coste regulatorio amortizado (€/unidad) — solo para cosmética Venezuela (SACS)
- Precio de venta al público (€ para España, USD para Venezuela)
- Tasa de cambio EUR/USD (para línea Cosmética Venezuela)
- Tasa de devolución esperada (%)
- Comisión de plataforma / marketplace (%) — Shopify 2%, Amazon 15%, etc.
- Coste de adquisición de cliente CAC (€) — opcional, para calcular LTV

VARIABLES DE SALIDA:
- Coste total por unidad (€)
- Margen bruto (€ y %)
- Margen neto (€ y %)
- Clasificación automática: ✅ VIABLE (>35%) / ⚠️ REVISAR (20-35%) / ❌ NO VIABLE (<20%)
- Break-even: mínimo de unidades para cubrir costes fijos del período
- Ratio precio/peso (€/kg) — crítico para envíos aéreos a Venezuela

FORMATO DE SALIDA — Markdown completo:

# Calculadora Unit Economics Universal — Portafolio Ecommerce

## Cómo usar esta calculadora
[Instrucciones claras en 5 pasos]

## Tabla de variables de entrada

| Variable | Definición | Unidad | Dónde obtener el dato |
|---|---|---|---|
| [variable] | [qué es] | [€/%/USD] | [fuente o cómo calcularlo] |

## Fórmulas

### Línea Ecommerce Disruptivo (Dropshipping España)
[Fórmulas paso a paso con variables nombradas]

### Línea Cosmética (Importación España → Venezuela)
[Fórmulas incluyendo conversión EUR/USD, SACS amortizado, flete aéreo]

### Línea Moda (Print-on-Demand)
[Fórmulas incluyendo coste base POD, margen sobre precio de venta]

## Criterios de clasificación

| Clasificación | Margen neto | Acción recomendada |
|---|---|---|
| ✅ VIABLE | > 35% | Proceder con evaluación de proveedor |
| ⚠️ REVISAR | 20-35% | Negociar precio de compra o ajustar PVP |
| ❌ NO VIABLE | < 20% | Descartar o replantear completamente |

## Ejemplos pre-rellenados

### Ejemplo 1 — Cosmética: Sérum K-Beauty Venezuela
[Ejemplo real con todos los campos]

### Ejemplo 2 — Cosmética: Perfume de autor Venezuela
[Ejemplo real]

### Ejemplo 3 — Ecommerce Disruptivo: Gadget de hogar España
[Ejemplo real]

### Ejemplo 4 — Ecommerce Disruptivo: Accesorio Pet Tech España
[Ejemplo real]

### Ejemplo 5 — Moda: Camiseta POD España
[Ejemplo real]

## Notas sobre márgenes mínimos por línea

[Tabla de umbrales mínimos reales para cada línea, con justificación]
```

---

## INSTRUCCIÓN DE CIERRE PARA AG

Una vez generados los 4 archivos:

```
Confirma que has completado las 4 tareas. Para cada archivo generado, indica:
1. Ruta exacta donde debe guardarse
2. Fecha del archivo (hoy: 2026-06-07)
3. Si hay alguna decisión que requiere confirmación del CEO antes de usar el archivo

No hagas commit todavía. El CEO revisará los archivos y aprobará antes de que se haga el commit.
Cuando el CEO apruebe, haz commit con el mensaje:
[catalog] Semana 1 — árboles de categorías v1 y calculadora unit economics

Después de la aprobación, actualiza .ai-project/context/STATUS.md marcando las tareas completadas.
```

---

## CHECKLIST DE REVISIÓN (Claude Code — auditor)

Tras recibir los archivos de AG, Claude Code verifica:

- [ ] Los 3 árboles tienen exactamente 3 niveles (no más, no menos)
- [ ] Las nomenclaturas de SKU son consistentes dentro de cada línea
- [ ] La calculadora tiene fórmulas explícitas, no solo descripciones
- [ ] Los ejemplos de la calculadora usan números reales (no 0 ni placeholders)
- [ ] No hay TODOs ni [completar] sin resolver
- [ ] Las rutas de los archivos son exactamente las indicadas en GOALS.md
- [ ] El árbol de Moda define explícitamente la política de variantes Shopify
- [ ] El árbol de Cosmética incluye los atributos regulatorios SACS y CPNP
