# PROMPT AG — Semana 2: Research de Mercado

> ⚠️ **SEMANA 2 EN PASE DE LIMPIEZA** — 2026-06-07
> Todos los entregables completados y auditados. Pendiente aplicar correcciones de Tarea 4.1
> y ejecutar el commit de cierre. Ver Semana 3 para el pase de limpieza + commit.

---

> **Herramienta:** Gemini Pro (Google AI Studio o Gemini Advanced)
> **Cuándo usar:** Una vez completada y aprobada la Semana 1 (árboles de categorías)
> **Output:** 7 documentos de research en el repositorio (tareas 1.1, 1.2, 2.1, 2.4, 3.1, 3.2, 4.1)
> **Tiempo estimado:** 2-3 sesiones de trabajo
> **Nota:** Gemini Pro hace el research. Claude Project sintetiza y genera el documento final.

## ESTADO DE ENTREGABLES (para referencia)

| Tarea | Archivo | Estado Claude Code |
|---|---|---|
| 1.1 | `01_ecommerce_disruptivo/market_research/2026-06_mercado_espana_categorias.md` | ✅ Aprobado |
| 1.2 | `01_ecommerce_disruptivo/market_research/2026-06_mercado_venezuela_arbitraje.md` | ✅ Aprobado |
| 2.1 | `02_cosmetica/suppliers/2026-06_kbeauty_proveedores_europa.md` | ✅ Aprobado |
| 2.4 | `02_cosmetica/regulatory/2026-06_sacs_venezuela_guia.md` | ✅ Aprobado |
| 3.1 | `03_moda/suppliers/2026-06_plataformas_pod_espana.md` | ✅ Aprobado |
| 3.2 | `03_moda/market_research/2026-06_nichos_moda_espana.md` | ✅ Aprobado |
| 4.1 | `shared/analytics/2026-06_comparativa_canales_venta.md` | ⚠️ Aprobado con correcciones menores pendientes |

---

---

## INSTRUCCIÓN DE APERTURA PARA AG

```
Eres Antigravity (AG), el agente Builder/Implementer del portafolio ecommerce.
Semana 1 completada: los 3 árboles de categorías y la calculadora están aprobados.

Tu tarea esta semana es ejecutar el research de mercado para las 3 líneas.

PROTOCOLO DE RESEARCH:
1. Para cada tarea: primero haces el research con datos verificables
2. Luego sintetizas con análisis estratégico
3. El documento final incluye siempre una sección "Prompt usado" para reproducibilidad
4. Si un dato no está disponible o no es verificable, lo indicas explícitamente — nunca inventas cifras
5. Cada archivo se guarda en la ruta exacta indicada

¿Listo? Confirma y ejecuta las tareas en el orden indicado.
```

---

## TAREA 1.1 — Research Mercado España: Análisis por Categoría

**Ruta:** `projects/01_ecommerce_disruptivo/market_research/2026-06_mercado_espana_categorias.md`

```
TAREA 1.1 — Research de mercado España para Ecommerce Disruptivo

Actúa como analista de ecommerce especializado en el mercado español 2026.

Para cada una de estas 6 categorías del árbol de Ecommerce Disruptivo, proporciona
datos actualizados (2025-2026):

CATEGORÍAS:
1. Hogar inteligente y confort (cerraduras app, termos inteligentes, hornos portátiles)
2. Tecnología wearable (anillos inteligentes, auriculares open-ear, rastreadores fitness)
3. Salud, bienestar y deporte (dispositivos facial, gomitas vitamínicas, accesorios pádel)
4. Pet Tech (comederos inteligentes, collares LED, rastreadores GPS mascotas)
5. Sostenibilidad y economía circular (accesorios biodegradables, zero-waste, moda reciclada)
6. Kits y bundles curados (combinaciones de producto de alto ticket percibido)

PARA CADA CATEGORÍA:
- Volumen de mercado en España y tasa de crecimiento (datos 2025-2026 — indicar fuente)
- Volúmenes de búsqueda mensuales en Google España (palabras clave principales)
- Nivel de saturación en Amazon.es y Shopify: bajo/medio/alto + evidencia
- Rango de precio medio al consumidor en España (€)
- Margen bruto típico en dropshipping europeo para esta categoría (%)
- 3 productos específicos con mayor volumen de ventas detectado
- Presencia en TikTok Shop España: emergente/activa/saturada
- Principales competidores españoles (tiendas propias + marketplaces)
- Tendencia de demanda: creciendo/estable/declinando + fuente
- Barrera de entrada para operador nuevo sin marca: baja/media/alta

FORMATO DE SALIDA:
# Research Mercado España — Ecommerce Disruptivo
## Fecha: 2026-06
## Metodología y fuentes utilizadas
## Tabla comparativa por categoría
## Análisis por categoría (sección individual para cada una)
## Síntesis estratégica: ranking de categorías por oportunidad
## Recomendación del CTO: categoría sugerida para el laboratorio + hipótesis
## Prompt usado [incluir el prompt completo que se usó para este research]
```

---

## TAREA 1.2 — Research Mercado Venezuela: Arbitraje e Importación

**Ruta:** `projects/01_ecommerce_disruptivo/market_research/2026-06_mercado_venezuela_arbitraje.md`

```
TAREA 1.2 — Research mercado Venezuela para arbitraje desde España

Actúa como analista de mercado especializado en Venezuela 2026.

Necesito entender el mercado de productos importados en Venezuela para un operador
que importa desde España hacia Venezuela.

BLOQUE 1 — CONTEXTO ECONÓMICO OPERATIVO
- Métodos de pago más usados para compras de productos importados en Venezuela
  (Zelle, transferencia bancaria local, PayPal, Binance, Pago Móvil)
- Rango de precio que acepta el consumidor venezolano para productos importados de España (USD)
- Canales de venta más efectivos para productos importados (Instagram, WhatsApp, marketplaces locales)
- Plataformas locales de ecommerce con tráfico real en Venezuela 2025-2026

BLOQUE 2 — CATEGORÍAS CON MAYOR DEMANDA INSATISFECHA
- Qué categorías tienen alta demanda pero baja oferta local en Venezuela
- Qué tipo de productos importados tienen mayor margen percibido por el consumidor venezolano
- Qué marcas o categorías europeas tienen mayor percepción de valor aspiracional en Venezuela

BLOQUE 3 — CANALES DE DISTRIBUCIÓN
- Cómo funciona la importación desde España a Venezuela (operadores, costes, tiempos)
- Principales operadores logísticos España-Venezuela conocidos (nombres reales si existen)
- Aranceles e impuestos de importación para productos de consumo no alimentarios

BLOQUE 4 — RIESGOS OPERATIVOS
- Principales riesgos de operar ecommerce hacia Venezuela (cobro, entrega, regulación)
- Mitigaciones documentadas para cada riesgo
- Casos conocidos de operadores que lo hacen exitosamente

FORMATO DE SALIDA:
# Research Mercado Venezuela — Arbitraje desde España
## Fecha: 2026-06
## Análisis por bloque
## Tabla de riesgos operativos y mitigaciones
## Lista de oportunidades ordenadas por viabilidad
## Síntesis estratégica: encaje con las 3 líneas del portafolio
## Prompt usado
```

---

## TAREA 2.1 — Research K-Beauty: Proveedores Europeos

**Ruta:** `projects/02_cosmetica/suppliers/2026-06_kbeauty_proveedores_europa.md`

```
TAREA 2.1 — Research K-Beauty proveedores europeos para ruta España → Venezuela

Necesito información sobre el mercado K-Beauty en Europa en 2026, orientada
a un operador que importa desde España hacia Venezuela.

BLOQUE 1 — MARCAS Y DEMANDA
- Las 10 marcas K-Beauty con mayor demanda en Europa en 2025-2026 (con datos verificables)
- Marcas con demanda documentada en Venezuela o LATAM
- Ingredientes activos con mayor crecimiento: Centella Asiática, Niacinamida, Retinol,
  Snail Mucin, Probióticos (datos de búsqueda si disponibles)

BLOQUE 2 — DISTRIBUIDORES EUROPEOS
- Distribuidores mayoristas de K-Beauty con sede en España o Europa que vendan a revendedores
- Para cada distribuidor: país, marcas representadas, MOQ mínimo, precio al revendedor,
  documentación regulatoria que proveen (CPNP, AEMPS)
- Distribuidores que permiten reventa en mercados fuera de UE (Venezuela)

BLOQUE 3 — PRECIOS Y MÁRGENES
- Precio de compra al distribuidor vs precio retail en Venezuela (ratio de arbitraje estimado)
- Productos con mejor ratio margen/peso para envío aéreo

BLOQUE 4 — REGULACIÓN
- Requisitos CPNP para venta en UE y qué implica para revendedores
- Qué documentación requiere Venezuela (SACS) para importar cosméticos
- Riesgos regulatorios conocidos para esta ruta comercial

FORMATO DE SALIDA:
# Research K-Beauty — Proveedores Europeos
## Fecha: 2026-06
## Tabla de distribuidores europeos
## Tabla de marcas y productos destacados
## Análisis de márgenes y viabilidad logística
## Sección regulatoria (CPNP + SACS)
## Recomendación del CTO: top 3 proveedores para contactar
## Prompt usado
```

---

## TAREA 2.4 — Guía Regulatoria SACS Venezuela

**Ruta:** `projects/02_cosmetica/regulatory/2026-06_sacs_venezuela_guia.md`

```
TAREA 2.4 — Guía operativa SACS Venezuela para importación de cosméticos

Necesito una guía operativa actualizada (2025-2026) sobre el proceso SACS en Venezuela
para importar cosméticos desde España.

INCLUIR:
- Qué es el SACS y qué productos lo requieren obligatoriamente
- Proceso paso a paso para obtener el registro SACS para un cosmético importado
- Documentación que debe proveer el fabricante europeo (CPNP, certificados, etiquetado)
- Papel del farmacéutico patrocinante en Venezuela: qué hace, cómo se contrata, coste estimado
- Tiempo estimado del proceso completo (semanas/meses)
- Productos cosméticos con proceso SACS más rápido o simplificado
- Riesgos de vender sin SACS: multas, decomisos, precedentes documentados
- Fuentes oficiales o consultoras especializadas en regulación cosmética Venezuela

NOTA: Si no tienes datos verificables actualizados sobre algún punto, indícalo
explícitamente en lugar de inferir. Este documento tomará decisiones de capital.

FORMATO DE SALIDA:
# Guía Regulatoria SACS Venezuela — Cosméticos Importados
## Fecha: 2026-06
## Resumen ejecutivo (para el CEO — 5 líneas máximo)
## Qué es el SACS y qué requiere
## Proceso paso a paso
## Tabla de documentación requerida por tipo de producto
## Estimación de costes y tiempos
## Tabla de riesgos operativos
## Productos recomendados para empezar (menor fricción regulatoria)
## Contactos y recursos (consultoras, reguladores)
## Prompt usado
```

---

## TAREA 3.1 — Research Plataformas POD para España

**Ruta:** `projects/03_moda/suppliers/2026-06_plataformas_pod_espana.md`

```
TAREA 3.1 — Comparativa de plataformas Print-on-Demand para España 2026

Comparativa actualizada de plataformas POD para vender desde España con integración Shopify.

PLATAFORMAS: Printful, Printify, Gelato, SPOD, Printribe

PARA CADA PLATAFORMA:
- Precios actuales de producción: camiseta estándar, sudadera, gorra, tote bag (€)
- Tiempo de producción + tiempo de envío a España (días)
- Almacenes o proveedores en España/Europa
- Técnicas de impresión disponibles: DTG, sublimación, bordado, serigrafía
- Integración Shopify: nivel (nativa/app) + facilidad reportada
- Número de referencias en catálogo
- Opciones de packaging personalizado (caja, tissue, pegatina de marca)
- Sostenibilidad: materiales orgánicos o certificados GOTS/OEKO-TEX disponibles
- Punto débil más reportado por vendedores en 2025-2026
- Política de devoluciones en caso de error de producción

PARA GELATO ESPECÍFICAMENTE:
- Presencia de proveedores en España
- Comparativa de precio vs Printful para el mercado español

FORMATO DE SALIDA:
# Research Plataformas POD — España 2026
## Fecha: 2026-06
## Tabla comparativa completa
## Análisis detallado por plataforma
## Tabla comparativa de precios para 4 productos base
## Recomendación del CTO: plataforma principal + alternativa para este perfil
## Próximos pasos: cómo abrir cuenta y testar calidad antes de publicar
## Prompt usado
```

---

## TAREA 3.2 — Research Nichos de Moda España

**Ruta:** `projects/03_moda/market_research/2026-06_nichos_moda_espana.md`

```
TAREA 3.2 — Research nichos de moda con mayor conversión en España 2026

Analiza los nichos de moda con mayor potencial para un operador de ecommerce en España
usando POD y white label en 2026.

BLOQUE 1 — TENDENCIAS DE CONSUMO
- Categorías de ropa/moda con mayor crecimiento en ecommerce español 2025-2026
- Estilos con mayor engagement en TikTok Shop España e Instagram Shopping
- Nichos infrasaturados en marketplaces (Amazon Fashion, Zalando, Miravia)

BLOQUE 2 — ANÁLISIS POR NICHO
Para cada nicho (ropa estética identity-driven / accesorios lifestyle / joyería private label
/ moda sostenible / creator merch):
- Tamaño estimado de audiencia en España
- Ticket medio del consumidor (€)
- Saturación en Shopify y marketplaces: baja/media/alta
- Plataforma de descubrimiento principal (TikTok, Instagram, Pinterest, Google)
- Ejemplo de marca o vendedor exitoso en España en este nicho

BLOQUE 3 — JOYERÍA Y ACCESORIOS PRIVATE LABEL
- MOQ mínimo real para joyería private label en España o Europa
- Proveedores de joyería private label accesibles para pequeños operadores
- Márgenes brutos típicos: joyería private label vs POD textil

BLOQUE 4 — CREATOR MERCH
- Cómo funciona el modelo Creator Merch en España (TikTok Shop, Instagram)
- Ejemplos de creadores españoles con merch propio exitoso
- Qué tipo de diseños convierten mejor en la audiencia lifestyle/cosmética 25-40 años

FORMATO DE SALIDA:
# Research Nichos Moda — España 2026
## Fecha: 2026-06
## Tabla comparativa por nicho
## Análisis por nicho (sección individual)
## Ranking de oportunidad (1-5 nichos)
## Recomendación del CTO: nicho inicial + tipo de diseño para testear
## Prompt usado
```

---

## TAREA 4.1 — Comparativa Canales de Venta España + Venezuela 2026

**Ruta:** `shared/analytics/2026-06_comparativa_canales_venta.md`

> **Crítica para validar TOOLS.md v2 antes de Fase 2.** Los datos del TOOLS.md actual son aproximados de 2025 — aquí los confirmamos para 2026.

```
TAREA 4.1 — Confirmar tarifas y viabilidad de canales de venta multicanal 2026

Estoy preparando una estrategia multicanal donde Shopify es el hub pero se vende también
en marketplaces y redes sociales. Necesito datos verificables de 2026 (no inferidos).

BLOQUE 1 — CANALES PARA ESPAÑA
Para cada canal, datos actualizados a 2026:
- Amazon.es Seller (plan Profesional): cuota mensual, comisión por categoría (cosmética, hogar, moda, electrónica), tiempo de alta, requisitos
- Miravia: cuota mensual o gratuita, comisión por categoría, requisitos de alta, integración Shopify
- TikTok Shop España: comisión por venta, requisitos de seller, integración Shopify, categorías permitidas
- Instagram Shopping: comisión real (0% pero hay costes ocultos?), requisitos de catálogo
- Etsy: cuota listado (€0.20?), comisión por venta, viabilidad para POD textil de diseños propios
- Pinterest Shopping: comisión, requisitos
- Wallapop: viabilidad real para validar demanda B2C de productos nuevos
- Vinted: viabilidad para vender moda nueva (no segundo mano)
- Carrefour Marketplace: cuota, comisión, requisitos de acceso
- El Corte Inglés Online (marketplace): requisitos reales y comisión
- Druni / Primor marketplace cosmética: ¿existen versiones marketplace abierto?
- Zalando Connected Retail / Zalando Partner: requisitos para acceso de operador pequeño

BLOQUE 2 — CANALES PARA VENEZUELA
- MercadoLibre Venezuela 2026: ¿sigue activo? ¿qué tráfico real tiene? ¿comisiones?
- WhatsApp Business: catálogo, pagos integrados, datos de uso comercial en Venezuela
- Instagram: catálogo, pago, datos de uso comercial en Venezuela
- Telegram canales comerciales: tamaño de audiencia, modelo de pago
- Otros marketplaces locales activos en Venezuela 2026

BLOQUE 3 — COMPATIBILIDAD CON SHOPIFY
Para cada canal de Bloque 1 y 2, indicar:
- ¿Existe app oficial Shopify → canal?
- ¿La integración sincroniza stock automáticamente?
- ¿Sincroniza pedidos en ambas direcciones?
- ¿Coste de la app?

BLOQUE 4 — DESCARTADOS
- AliExpress como canal de venta para vendedor europeo: confirmar que no es viable o explicar por qué
- Cualquier otro canal que se evaluó y descartó con razón

FORMATO DE SALIDA:
# Comparativa de Canales de Venta — España y Venezuela 2026
## Fecha: 2026-06
## Resumen ejecutivo (5 líneas para el CEO)
## Tabla maestra: canal × cuota × comisión × cuándo activar
## Análisis por canal (sección individual con datos reales 2026)
## Compatibilidad Shopify (matriz)
## Top 3 canales por línea (recomendación CTO):
  - Línea 01 Ecommerce Disruptivo
  - Línea 02 Cosmética
  - Línea 03 Moda
## Alertas: canales donde la información 2026 no está clara y requiere contacto directo
## Prompt usado
```

---

## PROTOCOLO DE ENTREGA PARA AG

Al finalizar cada tarea de research:

```
Para cada documento generado, confirma:
1. El archivo incluye sección "Prompt usado" con el prompt completo
2. Los datos que no fue posible verificar están explícitamente marcados como [NO VERIFICADO]
3. Las fuentes están citadas o se indica que no hay fuentes disponibles
4. La ruta del archivo es exactamente la indicada

Cuando tengas los 6 archivos listos:
- NO hagas commit todavía
- Notifica al CEO para revisión
- El CEO y Claude Code revisan juntos
- Solo después de aprobación: commit con mensaje [research] Semana 2 — research completo 6 líneas

Actualiza STATUS.md con los hechos verificados de esta semana.
```

---

## CHECKLIST DE REVISIÓN (Claude Code — auditor)

- [ ] Todos los archivos tienen sección "Prompt usado"
- [ ] Ningún dato inventado — los no verificados están marcados [NO VERIFICADO]
- [ ] Las rutas de archivo son exactamente las del GOALS.md
- [ ] Cada documento tiene "Recomendación del CTO" con propuesta accionable
- [ ] Los nombres de archivo siguen la convención: `YYYY-MM_tema_breve.md`
- [ ] STATUS.md actualizado con los hechos verificados
- [ ] No hay archivos .tar.gz, .zip ni "te muestro lo que haría" sin evidencia
