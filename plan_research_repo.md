# PLAN DE ALIMENTACIÓN DEL REPOSITORIO

## Market Research + Selección de Productos — Las 3 Líneas

### ecommerce-portfolio · Mayo 2026

---

## CÓMO USAR ESTE PLAN

**Gemini Pro** → Investiga. Produce datos crudos.

**Claude Project** → Analiza, sintetiza, decide y genera el documento

final para el repositorio.

Cada tarea tiene formato: **[HERRAMIENTA] → qué hacer → dónde

guardar en el repo**.

Las tareas están ordenadas por secuencia lógica, no por línea. Se puede

trabajar las 3 líneas en paralelo.

---

## BLOQUE 0 — ARQUITECTURA DEL CATÁLOGO

### Prerequisito antes de cualquier research de producto

*Herramienta: Claude Project (tú solo — no necesita Gemini)*

---

### TAREA 0.1 — Diseñar el árbol de categorías del Ecommerce

Disruptivo

**Herramienta:** Claude Project

**Destino en repo:**

`projects/01_ecommerce_disruptivo/catalog/arbol_categorias_v1.md`

**Qué hacer:**

Generar el árbol de categorías del laboratorio con 3 niveles, pensado

para escalar a 200 SKUs, no solo para los primeros 5. Incluir:

- Nivel 1: categorías principales (Hogar · Tecnología · Salud/Bienestar ·

Mascotas · Sostenibilidad · Kits)

- Nivel 2: subcategorías por familia de producto

- Nivel 3: atributos estándar por categoría (material, funcionalidad, rango

de precio)

- Nomenclatura de SKU propuesta para cada categoría

**Prompt para Claude:**

```

Actúa como CTO. Genera el árbol de categorías para el catálogo del

laboratorio Ecommerce Disruptivo.

Contexto: tienda Shopify orientada a productos funcionales y estéticos

para España, con potencial LATAM.

Categorías base identificadas: Hogar inteligente, Tecnología wearable,

Salud y bienestar, Pet Tech,

Sostenibilidad, Kits y bundles.

Formato: árbol con 3 niveles + tabla de atributos estándar por categoría

+ nomenclatura SKU propuesta.

Output: Markdown listo para subir a /catalog/arbol_categorias_v1.md

```

---

### TAREA 0.2 — Diseñar el árbol de categorías de Cosmética

**Herramienta:** Claude Project

**Destino en repo:**

`projects/02_cosmetica/catalog/arbol_categorias_v1.md`

**Qué hacer:**

Árbol de categorías cosmético con atributos específicos del sector: tipo

de piel, ingrediente activo, origen geográfico, certificación (vegano, K-

Beauty, UE).

**Prompt para Claude:**

```

Actúa como CTO. Genera el árbol de categorías para el catálogo de

Cosmética, Perfumes y Marca Personal.

Mercados: Venezuela (primario) y España (validación).

Líneas identificadas: K-Beauty/Skincare · Perfumería de autor · Body

care · Kits curados · Cosmética masculina.

Formato: árbol con 3 niveles + atributos específicos de cosmética (tipo

de piel, ingrediente activo,

origen, certificación) + nomenclatura SKU propuesta (ejemplo:

SKIN1004_CENTELLA_AMPOULE_100ML).

Output: Markdown listo para /catalog/arbol_categorias_v1.md

```

---

### TAREA 0.3 — Diseñar el árbol de categorías de Moda

**Herramienta:** Claude Project

**Destino en repo:** `projects/03_moda/catalog/arbol_categorias_v1.md`

**Qué hacer:**

Árbol textil con gestión correcta de variantes talla/color desde el inicio.

Incluir política de variantes (agrupadas o independientes) y atributos

estándar europeos.

**Prompt para Claude:**

```

Actúa como CTO. Genera el árbol de categorías para el catálogo de

Moda, Diseño y Fabricación.

Mercado principal: España. Modelo de entrada: Print-on-Demand →

White Label.

Líneas identificadas: Ropa estética/identity-driven · Accesorios lifestyle

· Joyería private label · Ropa sostenible · Creator Merch.

Formato: árbol con 3 niveles + política de variantes (talla S/M/L/XL ·

colores) + atributos textiles estándar UE

+ nomenclatura SKU propuesta (ejemplo: CAP01_CAMISETA_NEGRO_M).

Output: Markdown listo para /catalog/arbol_categorias_v1.md

```

---

## BLOQUE 1 — ECOMMERCE DISRUPTIVO (Laboratorio Madre)

### Destino: `projects/01_ecommerce_disruptivo/`

---

### TAREA 1.1 — Research de mercado España: análisis por categoría

**Herramienta:** Gemini Pro → Claude Project

**Destino en repo:**

`projects/01_ecommerce_disruptivo/market_research/2026-

05_mercado_españa_categorias.md`

**Prompt para Gemini Pro:**

```

Actúa como analista de ecommerce especializado en el mercado

español 2026.

Para cada una de estas 6 categorías, proporciona datos actualizados

(2025-2026):

CATEGORÍAS A ANALIZAR:

1. Hogar inteligente y confort (cerraduras app, termos inteligentes,

hornos portátiles)

2. Tecnología wearable (anillos inteligentes, auriculares open-ear,

rastreadores fitness)

3. Salud, bienestar y deporte (dispositivos facial, gomitas vitamínicas,

accesorios pádel)

4. Pet Tech (comederos inteligentes, collares LED, rastreadores GPS

mascotas)

5. Sostenibilidad y economía circular (accesorios biodegradables, zero-

waste, moda reciclada)

6. Kits y bundles curados (combinaciones de producto de alto ticket

percibido)

PARA CADA CATEGORÍA PROPORCIONA:

- Volumen de mercado en España y tasa de crecimiento (datos 2025-

2026 verificables)

- Volúmenes de búsqueda mensuales en Google España (palabras clave

principales)

- Nivel de saturación en Amazon.es y Shopify: bajo/medio/alto +

evidencia

- Rango de precio medio al consumidor en España

- Margen bruto típico del dropshipping en esta categoría (%)

- 3 productos específicos con mayor volumen de ventas detectado

- Presencia en TikTok Shop España: emergente/activa/saturada

- Principales competidores españoles identificados (tiendas propias +

marketplaces)

- Tendencia de demanda: creciendo/estable/declinando + fuente

- Barrera de entrada para un operador nuevo sin marca: baja/media/alta

FORMATO DE SALIDA: tabla comparativa por categoría + sección de

datos duros con fuentes.

No inventes datos. Si no tienes datos verificables de 2025-2026, indícalo

claramente.

```

**Qué hace Claude Project después:**

Recibe el output de Gemini, añade análisis estratégico (qué categoría

encaja mejor con el laboratorio, cuál debe ser la primera, cuál es el

riesgo dominante) y genera el documento final.

---

### TAREA 1.2 — Research de mercado Venezuela: arbitraje e

importación

**Herramienta:** Gemini Pro → Claude Project

**Destino en repo:**

`projects/01_ecommerce_disruptivo/market_research/2026-

05_mercado_venezuela_arbitraje.md`

**Prompt para Gemini Pro:**

```

Actúa como analista de mercado especializado en Venezuela 2026.

Necesito entender el mercado de productos importados en Venezuela

para un operador que importa desde España.

BLOQUES DE ANÁLISIS:

1. CONTEXTO ECONÓMICO OPERATIVO

- Métodos de pago más usados para compras de productos importados

(Zelle, transferencia, PayPal, Binance)

- Rango de precio que acepta el consumidor venezolano para productos

importados de España (en USD)

- Canales de venta más efectivos para productos importados (Instagram,

WhatsApp, marketplaces locales)

- Barreras de entrada regulatorias actuales para importación de

productos no alimentarios

2. CATEGORÍAS CON MAYOR DEMANDA INSATISFECHA

- Qué categorías de producto tienen alta demanda pero baja oferta local

en Venezuela 2025-2026

- Qué tipo de productos importados tienen mayor margen percibido por

el consumidor venezolano

- Qué marcas o categorías europeas tienen mayor percepción de valor

aspiracional

3. CANALES DE DISTRIBUCIÓN

- Cómo funciona actualmente la importación desde España a Venezuela

(operadores, costes, tiempos)

- Principales operadores logísticos España-Venezuela conocidos

- Aranceles e impuestos de importación para productos de consumo no

alimentarios

4. RIESGOS OPERATIVOS

- Principales riesgos de operar ecommerce hacia Venezuela (cobro,

entrega, regulación)

- Casos documentados de operadores que lo están haciendo

exitosamente

FORMATO: análisis por bloque + tabla de riesgos + lista de

oportunidades concretas ordenadas por viabilidad.

```

---

### TAREA 1.3 — Evaluación de herramientas de detección de

tendencias

**Herramienta:** Gemini Pro → Claude Project

**Destino en repo:** `projects/01_ecommerce_disruptivo/strategy/2026-

05_herramientas_deteccion_tendencias.md`

**Prompt para Gemini Pro:**

```

Compara las herramientas de detección de productos ganadores para

ecommerce disponibles en 2026.

Herramientas a comparar: Minea, SellTheTrend, Eprolo, Zik Analytics,

Dropispy, AutoDS.

PARA CADA HERRAMIENTA:

- Precio mensual actual (plan básico y plan profesional)

- Qué plataformas monitoriza (Amazon, TikTok Shop, Facebook Ads, etc.)

- Especificidad para mercado español/europeo vs USA

- Funcionalidades únicas que la diferencian

- Limitaciones conocidas

- Valoración actual en reseñas (G2, Trustpilot o similar)

- Integración directa con Shopify: sí/no

CRITERIO DE EVALUACIÓN: el operador es un laboratorio comercial

pequeño con presupuesto limitado

que prioriza validación rápida sobre volumen.

FORMATO: tabla comparativa + recomendación razonada de 2

herramientas para este perfil.

```

---

### TAREA 1.4 — Shortlist de proveedores de dropshipping para España

**Herramienta:** Gemini Pro → Claude Project

**Destino en repo:**

`projects/01_ecommerce_disruptivo/operations/2026-

05_proveedores_dropshipping.md`

**Prompt para Gemini Pro:**

```

Necesito una evaluación de los mejores proveedores de dropshipping

para vender en España en 2026.

Prioridad: proveedores europeos o con almacenes en Europa (tiempos

de entrega 3-7 días).

PLATAFORMAS A EVALUAR: DSers, Spocket, Eprolo, Syncee, Modalyst,

BigBuy España.

PARA CADA PLATAFORMA:

- Precio actual (plan funcional mínimo)

- Número de proveedores españoles o europeos disponibles

- Categorías más fuertes en su catálogo

- Tiempo de entrega promedio a España

- Integración con Shopify: nivel de integración (nativa/app/API)

- Automatización de pedidos: sí/no

- Política de devoluciones del proveedor

- Punto débil más reportado por usuarios

PARA BIGBUY ESPECÍFICAMENTE:

- Condiciones de acceso para pequeños operadores en España

- Catálogo disponible y mínimos de compra

- Ventajas frente a DSers/Spocket para el mercado español

FORMATO: tabla comparativa + ranking para un operador que empieza

con budget < 500€/mes.

```

---

### TAREA 1.5 — Selección de la categoría inicial del laboratorio

**Herramienta:** Claude Project (análisis y decisión)

**Destino en repo:**

`projects/01_ecommerce_disruptivo/product_selection/2026-

05_decision_categoria_inicial.md`

**Qué hacer:**

Con los outputs de las tareas 1.1, 1.2 y 1.3, Claude Project genera una

matriz de decisión que permite al CEO elegir la categoría con la que

arranca el laboratorio.

**Prompt para Claude:**

```

Actúa como CTO del proyecto. Con los datos de research de mercado

España (tarea 1.1),

mercado Venezuela (tarea 1.2) y herramientas de detección (tarea 1.3),

genera una

matriz de decisión para elegir la categoría inicial del laboratorio.

CRITERIOS DE EVALUACIÓN (ponderados):

- Margen bruto esperado (peso 25%)

- Nivel de saturación en España (peso 20%)

- Velocidad de validación posible (peso 20%)

- Encaje con los casos de uso de Cosmética y Moda (peso 15%)

- Barrera de entrada para competidores (peso 10%)

- Complejidad logística (peso 10%)

FORMATO DE SALIDA:

1. Tabla de evaluación con puntuación por criterio para cada categoría

2. Ranking final con justificación de los 3 primeros puestos

3. Recomendación del CTO: categoría sugerida + hipótesis de validación

específica

4. 3 SKUs concretos para testear en la categoría ganadora

5. Próxima acción del CEO para cerrar esta decisión

Output: Markdown listo para /product_selection/2026-

05_decision_categoria_inicial.md

```

---

## BLOQUE 2 — COSMÉTICA, PERFUMES Y MARCA PERSONAL

### Destino: `projects/02_cosmetica/`

---

### TAREA 2.1 — Research K-Beauty: proveedores europeos y

disponibilidad

**Herramienta:** Gemini Pro → Claude Project

**Destino en repo:** `projects/02_cosmetica/suppliers/2026-

05_kbeauty_proveedores_europa.md`

**Prompt para Gemini Pro:**

```

Necesito información sobre el mercado K-Beauty (cosmética coreana) en

Europa en 2026,

orientada a un operador que quiere importar desde España hacia

Venezuela.

BLOQUE 1 — MARCAS Y DEMANDA

- Las 10 marcas K-Beauty con mayor demanda en Europa en 2025-2026

(con datos verificables)

- Marcas específicas con alta demanda documentada en Venezuela o

LATAM

- Ingredientes activos con mayor crecimiento de búsqueda: Centella

Asiática, Niacinamida,

  Retinol, Snail Mucin, Probióticos (datos de Google Trends o similar si

disponible)

BLOQUE 2 — DISTRIBUIDORES EUROPEOS

- Distribuidores mayoristas de K-Beauty con sede en España o Europa

que vendan a revendedores

- Para cada distribuidor: país, marcas representadas, MOQ mínimo,

precio medio al revendedor,

  documentación regulatoria que proveen (CPNP, AEMPS)

- Distribuidores que permiten reventa en mercados fuera de UE

(Venezuela)

BLOQUE 3 — PRECIOS Y MÁRGENES

- Precio de compra al distribuidor vs precio retail en Venezuela (ratio de

arbitraje estimado)

- Productos con mejor ratio margen/peso para envío aéreo (crítico para

rentabilidad logística)

BLOQUE 4 — REGULACIÓN

- Requisitos CPNP (Portal de Notificación de Cosméticos de la UE) para

venta en UE

- Qué documentación requiere Venezuela (SACS) para importar

cosméticos y quién la gestiona

- Riesgos regulatorios conocidos para esta ruta comercial

FORMATO: tabla de distribuidores + tabla de productos destacados +

sección regulatoria.

```

---

### TAREA 2.2 — Research perfumería de autor y nicho en España

**Herramienta:** Gemini Pro → Claude Project

**Destino en repo:** `projects/02_cosmetica/market_research/2026-

05_perfumeria_autor_españa_venezuela.md`

**Prompt para Gemini Pro:**

```

Analiza el mercado de perfumería de autor y fragancias nicho para un

operador que

importa desde España y vende en Venezuela.

BLOQUE 1 — MERCADO

- Tendencias de perfumería masculina nicho en España 2025-2026

(marcas, estilos, olfativos)

- Fragancias o categorías con mayor crecimiento en búsquedas (Google

Trends)

- Rango de precios que acepta el consumidor venezolano para

fragancias importadas de España

BLOQUE 2 — PROVEEDORES Y MARCAS

- Marcas de perfumería nicho/autor europeas sin distribución en

Venezuela (o con distribución muy limitada)

- Distribuidores mayoristas de perfumería en España que vendan a

revendedores con MOQ accesible

- Marcas que permiten explícitamente la reventa internacional

BLOQUE 3 — OPORTUNIDAD

- Comparativa de margen bruto: perfumería nicho vs K-Beauty vs body

care

- Productos de perfumería con mejor ratio precio/peso para envío aéreo

a Venezuela

- Riesgos específicos de importar perfumes (transporte aéreo de

productos con alcohol)

FORMATO: tabla de marcas candidatas + tabla de distribuidores +

análisis de viabilidad logística.

```

---

### TAREA 2.3 — Evaluación de SKU inicial: matriz de decisión

cosmética

**Herramienta:** Claude Project

**Destino en repo:** `projects/02_cosmetica/product_selection/2026-

05_decision_sku_inicial.md`

**Qué hacer:**

Con los outputs de las tareas 2.1 y 2.2, Claude genera la matriz de

decisión para elegir el primer SKU o familia de SKUs con la que arranca

la línea cosmética.

**Prompt para Claude:**

```

Actúa como CTO. Con los datos de research K-Beauty (tarea 2.1) y

perfumería (tarea 2.2),

genera la matriz de decisión para elegir el primer lote de Cosmética.

CRITERIOS (ponderados):

- Margen neto estimado (precio - coste - flete aéreo - SACS - merma)

(peso 30%)

- Disponibilidad de proveedor europeo con documentación regulatoria

UE (peso 20%)

- Ratio precio/peso (rentabilidad logística por kilo enviado) (peso 20%)

- Demanda documentada en Venezuela o LATAM (peso 15%)

- Riesgo regulatorio SACS (peso 15%)

FORMATO DE SALIDA:

1. Tabla de evaluación de las categorías candidatas (K-Beauty ·

Perfumería · Body care · Kits)

2. Ranking final con puntuación

3. SKU recomendado para el primer lote (máximo 3 referencias)

4. Cálculo orientativo de unit economics del SKU ganador

5. Proveedor o distribuidor recomendado como primer contacto

6. Próximos 3 pasos operativos para el CEO

Output: Markdown listo para /product_selection/2026-

05_decision_sku_inicial.md

```

---

### TAREA 2.4 — Research regulatorio SACS Venezuela

**Herramienta:** Gemini Pro → Claude Project

**Destino en repo:** `projects/02_cosmetica/regulatory/2026-

05_sacs_venezuela_guia.md`

**Prompt para Gemini Pro:**

```

Necesito una guía operativa actualizada (2025-2026) sobre el proceso

SACS en Venezuela

para importar cosméticos desde España.

INCLUIR:

- Qué es el SACS y qué productos lo requieren obligatoriamente

- Proceso paso a paso para obtener el registro SACS para un producto

cosmético importado

- Documentación que debe proveer el fabricante europeo (CPNP,

certificados, etiquetado)

- Papel del farmacéutico patrocinante en Venezuela: qué hace, cómo se

contrata, coste estimado

- Tiempo estimado del proceso (semanas/meses)

- Productos cosméticos con proceso SACS más rápido o simplificado

- Riesgos de vender sin SACS: multas, decomisos, precedentes

documentados

- Fuentes oficiales o consultoras especializadas en regulación cosmética

Venezuela

FORMATO: guía paso a paso + tabla de documentación requerida +

estimación de costes y tiempos.

```

---

### TAREA 2.5 — Calculadora unit economics cosmética Venezuela

**Herramienta:** Claude Project (crear herramienta)

**Destino en repo:**

`tools/margin_calculator/unit_economics_cosmetica.md`

**Prompt para Claude:**

```

Actúa como CTO. Crea una calculadora de unit economics en formato

Markdown para

evaluar la rentabilidad de cualquier SKU cosmético en la ruta España →

Venezuela.

VARIABLES DE ENTRADA:

- Precio de compra al distribuidor (€)

- Peso del producto (gramos)

- Precio de venta en Venezuela (USD)

- Tipo de envío: aéreo (€/kg estimado) o marítimo (€/kg estimado)

- Coste de gestión SACS (€, amortizado por unidad)

- Tasa de merma estimada (%)

- Tasa de cambio EUR/USD

VARIABLES DE SALIDA:

- Coste total por unidad (€)

- Precio de venta en EUR equivalente

- Margen bruto (€ y %)

- Margen neto estimado (€ y %)

- Punto de rentabilidad: mínimo de unidades para cubrir costes fijos

SACS

Incluir 3 ejemplos pre-rellenados con productos cosméticos reales de

referencia.

Output: Markdown con tabla de variables + fórmulas + 3 ejemplos.

```

---

## BLOQUE 3 — MODA, DISEÑO Y FABRICACIÓN

### Destino: `projects/03_moda/`

---

### TAREA 3.1 — Research plataformas POD para España 2026

**Herramienta:** Gemini Pro → Claude Project

**Destino en repo:** `projects/03_moda/suppliers/2026-

05_plataformas_pod_españa.md`

**Prompt para Gemini Pro:**

```

Necesito una comparativa actualizada (2026) de plataformas de Print-

on-Demand (POD)

para vender desde España, con integración Shopify.

PLATAFORMAS A EVALUAR: Printful, Printify, Gelato, SPOD, Printribe.

PARA CADA PLATAFORMA:

- Precios actuales de producción (camiseta estándar, sudadera, gorra,

tote bag)

- Tiempo de producción + tiempo de envío a España

- Almacenes o proveedores en Europa/España

- Calidad de impresión: DTG vs sublimación vs bordado — qué técnicas

ofrece

- Integración Shopify: nivel (nativa/app) + facilidad de uso reportada

- Catálogo de productos disponibles (número de referencias)

- Opciones de packaging personalizado (caja, tissue, pegatina de marca)

- Sostenibilidad: opciones de materiales orgánicos o certificados

GOTS/OEKO-TEX

- Punto débil más reportado por vendedores en 2025-2026

PARA GELATO ESPECÍFICAMENTE:

- Presencia de proveedores en España

- Opciones de papel/productos editoriales además de textil

- Comparativa de precio vs Printful para el mercado español

FORMATO: tabla comparativa completa + recomendación para un

operador que empieza en España.

```

---

### TAREA 3.2 — Research nichos de moda con mayor conversión en

España 2026

**Herramienta:** Gemini Pro → Claude Project

**Destino en repo:** `projects/03_moda/market_research/2026-

05_nichos_moda_españa.md`

**Prompt para Gemini Pro:**

```

Analiza los nichos de moda con mayor potencial de conversión para un

operador de

ecommerce en España usando POD y white label en 2026.

BLOQUE 1 — TENDENCIAS DE CONSUMO

- Categorías de ropa/moda con mayor crecimiento en ecommerce

español 2025-2026

- Estilos con mayor engagement en TikTok Shop España e Instagram

Shopping (datos o fuentes)

- Nichos infrasaturados identificados en marketplaces (Amazon Fashion,

Zalando, Miravia)

BLOQUE 2 — NICHOS ESPECÍFICOS

Para cada nicho: (ropa estética identity-driven · accesorios lifestyle ·

joyería private label · moda sostenible · creator merch)

- Tamaño estimado de audiencia en España

- Ticket medio del consumidor

- Saturación en Shopify y marketplaces: baja/media/alta

- Plataforma de descubrimiento principal (TikTok, Instagram, Pinterest,

Google)

- Ejemplo de marca o vendedor exitoso en este nicho en España

BLOQUE 3 — ACCESORIOS Y JOYERÍA

- MOQ mínimo real para joyería private label en España o Europa

- Proveedores de joyería private label con sede en España o Europa

accesibles para pequeños operadores

- Márgenes brutos típicos en joyería private label vs POD textil

FORMATO: tabla por nicho + ranking de oportunidad + ejemplos

concretos.

```

---

### TAREA 3.3 — Evaluación de diseños iniciales para POD

**Herramienta:** Claude Project

**Destino en repo:** `projects/03_moda/product_selection/2026-

05_estrategia_disenos_pod.md`

**Qué hacer:**

Definir la estrategia de los primeros diseños a testear en POD: qué tipos

de diseño, qué productos, qué estética, qué herramientas de IA usar

para generarlos.

**Prompt para Claude:**

```

Actúa como CTO. Diseña la estrategia de los primeros 3-5 diseños POD

para testear en la

línea de Moda del portafolio.

CONTEXTO:

- Audiencia potencial: comunidad de Daniely (cosmética, lifestyle,

aspiracional, 25-40 años, España y LATAM)

- Plataforma POD elegida: [completar con resultado de tarea 3.1]

- Productos a testear: camisetas + accesorios sin talla (gorras, tote bags)

PARA CADA DISEÑO PROPUESTO:

- Concepto visual (descripción para generar con Claude Design o

Midjourney)

- Producto en el que aplica

- Audiencia específica

- Copy sugerido para el listing en Shopify

- Argumento de que puede conectar con la comunidad de Cosmética

(sinergia Creator Merch)

ADICIONAL:

- Herramientas de diseño IA recomendadas para generar estos diseños

sin diseñador

- Prompt base para Claude Design o Midjourney para la estética de la

línea

Output: Markdown listo para /product_selection/2026-

05_estrategia_disenos_pod.md

```

---

## BLOQUE 4 — SHARED: INFRAESTRUCTURA COMÚN

### Destino: `shared/`

---

### TAREA 4.1 — Comparativa de marketplaces España 2026

**Herramienta:** Gemini Pro → Claude Project

**Destino en repo:** `shared/analytics/2026-

05_comparativa_marketplaces_españa.md`

**Prompt para Gemini Pro:**

```

Compara los principales marketplaces para vender productos en España

en 2026.

Contexto: vendedor pequeño con catálogo de nicho (cosmética, moda,

hogar, bienestar).

MARKETPLACES A COMPARAR: Amazon.es, Miravia, TikTok Shop

España, Zalando, El Corte Inglés online, Carrefour.es.

PARA CADA MARKETPLACE:

- Comisión por venta (% y mínimos)

- Requisitos para darse de alta como vendedor (documentación, tiempo,

costes)

- Categorías donde tiene mayor tráfico y conversión

- Nivel de competencia: saturado/medio/emergente para pequeños

vendedores

- Tiempo estimado de integración con Shopify mediante app o API

- Política de devoluciones que aplica al vendedor

- Visibilidad orgánica para nuevos vendedores: alta/media/baja

- Presencia de compradores venezolanos o LATAM: sí/no/limitada

ADICIONAL:

- En qué momento (Fase) tiene sentido entrar en cada marketplace

- Cuál es la secuencia óptima para un operador que empieza en Shopify

FORMATO: tabla comparativa + recomendación de secuencia de

entrada.

```

---

### TAREA 4.2 — Calculadora unit economics universal

**Herramienta:** Claude Project

**Destino en repo:**

`tools/margin_calculator/unit_economics_universal.md`

**Prompt para Claude:**

```

Actúa como CTO. Crea una calculadora de unit economics universal en

Markdown

que sirva para evaluar cualquier SKU en cualquiera de las 3 líneas del

portafolio.

VARIABLES DE ENTRADA:

- Línea de negocio: Ecommerce Disruptivo / Cosmética / Moda

- Precio de compra o coste de producción (€)

- Coste logístico total (€/unidad, incluyendo envío y devolución

esperada)

- Coste regulatorio amortizado por unidad (€) — para cosmética

- Precio de venta al público (€ o USD según mercado)

- Tasa de devolución esperada (%)

- Coste de adquisición de cliente CAC (€) — opcional

VARIABLES DE SALIDA:

- Margen bruto (€ y %)

- Margen neto (€ y %)

- Break-even de unidades para cubrir costes fijos

- Clasificación automática: VIABLE (>35%) / REVISAR (20-35%) / NO

VIABLE (<20%)

INCLUIR:

- 5 ejemplos pre-rellenados: 2 de cosmética, 2 de ecommerce

disruptivo, 1 de moda

- Explicación de cada variable con nota de dónde obtener el dato

Output: Markdown con tabla de variables + ejemplos + clasificación

automática.

```

---

## SECUENCIA DE EJECUCIÓN RECOMENDADA

| Semana | Tareas | Herramienta | Output en repo |

|--------|--------|-------------|----------------|

| **Semana 1** | 0.1, 0.2, 0.3 | Claude Project | 3 árboles de categorías

listos |

| **Semana 1** | 4.2 | Claude Project | Calculadora unit economics |

| **Semana 2** | 1.1, 1.2 | Gemini → Claude | Research mercado España y

Venezuela |

| **Semana 2** | 2.1, 2.4 | Gemini → Claude | Research K-Beauty + guía

SACS |

| **Semana 2** | 3.1, 3.2 | Gemini → Claude | Research POD + nichos

moda |

| **Semana 3** | 1.3, 1.4 | Gemini → Claude | Herramientas detección +

proveedores dropshipping |

| **Semana 3** | 2.2 | Gemini → Claude | Research perfumería autor |

| **Semana 3** | 4.1 | Gemini → Claude | Comparativa marketplaces |

| **Semana 4** | 1.5, 2.3, 3.3 | Claude Project | 3 matrices de decisión

(una por línea) |

| **Semana 4** | 2.5 | Claude Project | Calculadora unit economics

cosmética |

| **Semana 4** | CEO | Decisión | Cerrar categoría inicial + primer SKU de

cada línea |

---

## REGLAS PARA TRABAJAR ESTE PLAN

1. **Gemini primero, Claude después.** Gemini trae datos. Claude

analiza, decide y formatea el documento final.

2. **Cada output va al repo en el mismo día que se genera.** Si no está

en el repo, no existe.

3. **Las matrices de decisión (tareas x.5) las aprueba el CEO** antes de

pasar a ejecución.

4. **Los prompts de Gemini se guardan** en el mismo archivo

Markdown del research como sección "Prompt usado", para

reproducibilidad.

5. **Actualizar `memory/global_context.md`** después de completar

cada bloque.

6. **Subir a NotebookLM** cada documento completado para consultas

cruzadas futuras.

---

*Plan generado con Claude — Portafolio Familiar de Emprendimientos*

*NÚCLEO CENTRAL · No distribuir sin segmentar*

