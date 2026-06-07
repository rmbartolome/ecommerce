# PROMPT AG — Semana 3: Cierre S2 + Research Restante

> **Herramienta:** Gemini Pro (Google AI Studio o Gemini Advanced)
> **Cuándo usar:** Inmediatamente — Semana 2 está completa en entregables, falta el commit y 3 tareas de research
> **Output:** 1 corrección en archivo existente + 3 nuevos documentos + commit de Semana 2
> **Tiempo estimado:** 2 sesiones de trabajo
> **Auditor:** Claude Code revisa cada entregable antes del commit

---

## INSTRUCCIÓN DE APERTURA PARA AG

```
Eres Antigravity (AG). Estás en Semana 3 del portafolio ecommerce.

Semana 2 completada: 7 documentos de research aprobados por Claude Code.
Pendiente: 1 corrección en Tarea 4.1, commit de cierre de Semana 2,
y 3 nuevas tareas de research.

Protocolo activo:
- Leer STATUS.md antes de empezar
- Por cada entregable: indicar ruta exacta y esperar auditoría Claude Code
- No hacer commit hasta que Claude Code dé el verde

¿Listo? Confirma y comienza con el Paso 0.
```

---

## PASO 0 — Corrección pendiente en Tarea 4.1 + Commit Semana 2

**Antes de ejecutar nuevas tareas**, aplicar esta corrección al archivo existente:

**Archivo:** `shared/analytics/2026-06_comparativa_canales_venta.md`

**Corrección:** Añadir al final del Bloque 1 una sección que cubra los canales secundarios pendientes del prompt original:

```
### Canales secundarios evaluados y descartados (Fase inicial)

| Canal | Razón de descarte en Fase 1-2 |
|---|---|
| Pinterest Shopping | Gratuito pero tráfico de descubrimiento lento. Activar en Fase 3 para cosmética y moda sostenible como canal de SEO visual |
| Carrefour Marketplace | Acceso restrictivo para nuevos vendedores, proceso de alta lento. Fase 4 |
| El Corte Inglés Online | Solo acepta marcas establecidas con volumen. Fuera de alcance actual |
| Druni / Primor | No tienen marketplace abierto a terceros vendedores. Descartado |

### Top 3 canales por línea (resumen ejecutivo)

| Línea | Canal 1 (Hub) | Canal 2 (Captación) | Canal 3 (Escalado Fase 3) |
|---|---|---|---|
| Ecommerce Disruptivo | Shopify | Instagram Ads → WhatsApp (VE) | Amazon.es |
| Cosmética | Shopify | Miravia | Instagram + Telegram VE |
| Moda | Shopify | TikTok Shop | Etsy |
```

**Una vez aplicada la corrección y auditada por Claude Code:**
- Commit con mensaje: `[research] Semana 2 — research completo 7 documentos`
- Actualizar STATUS.md con Semana 2 cerrada y Semana 3 iniciada

---

## TAREA 1.3 — Evaluación de Herramientas de Detección de Tendencias

**Ruta:** `projects/01_ecommerce_disruptivo/strategy/2026-06_herramientas_deteccion_tendencias.md`

**Contexto:** Herramientas para detectar qué productos son ganadores antes de comprarlos. Solo se activará Minea en Fase 1 (según TOOLS.md v2), pero el CEO necesita saber exactamente por qué Minea y no las alternativas, con datos actualizados.

```
TAREA 1.3 — Evaluación de herramientas de detección de productos ganadores 2026

Necesito una comparativa para decidir cuál herramienta de detección de tendencias
activar en Fase 1 (presupuesto máximo ~50€/mes, uso en España y Venezuela).

HERRAMIENTAS A COMPARAR: Minea, SellTheTrend, Eprolo/Dropispy, AutoDS, Zik Analytics.

PARA CADA HERRAMIENTA:
- Precio mensual actualizado 2026 (plan básico y plan mínimo funcional)
- Plataformas que monitoriza: Amazon, TikTok Shop, Facebook Ads, Instagram Ads, Miravia
- Cobertura específica de mercado español/europeo vs USA (¿tiene datos de ES?)
- Funcionalidades únicas que la diferencian de las demás
- Limitaciones conocidas o reportadas por usuarios en 2025-2026
- Valoración actual en G2, Trustpilot o similar (con fecha aproximada)
- Integración directa con Shopify: sí/no/parcial
- Curva de aprendizaje para un operador solo sin equipo técnico: baja/media/alta

CRITERIO DE EVALUACIÓN:
Operador en Fase 1 con presupuesto <50€/mes que necesita detectar productos
ganadores para el mercado español y venezolano. Sin equipo técnico.

FORMATO DE SALIDA:
# Evaluación Herramientas Detección de Tendencias — 2026
## Fecha: 2026-06
## Tabla comparativa completa
## Análisis por herramienta (sección individual)
## Ranking final con puntuación (criteria ponderados)
## Recomendación del CTO: herramienta a activar en Fase 1 + cómo usarla
## Plan de uso: cómo usar la herramienta ganadora en el flujo de research del portafolio
## Prompt usado
```

---

## TAREA 1.4 — Shortlist de Proveedores Dropshipping para España

**Ruta:** `projects/01_ecommerce_disruptivo/operations/2026-06_proveedores_dropshipping.md`

**Contexto:** Cuando el CEO apruebe el SKU inicial del laboratorio (Tarea 1.5, próxima semana), necesitará un proveedor activo. Este documento prepara esa decisión con datos reales de 2026.

```
TAREA 1.4 — Evaluación de proveedores de dropshipping para España 2026

Necesito elegir el proveedor de dropshipping principal para la línea Ecommerce Disruptivo.
Prioridad absoluta: proveedores europeos o con almacenes en España (entrega 3-7 días).

PLATAFORMAS A EVALUAR: DSers, Spocket, Eprolo, Syncee, Modalyst, BigBuy España.

PARA CADA PLATAFORMA:
- Precio mensual actualizado 2026 (plan mínimo funcional)
- Número aproximado de proveedores españoles o europeos disponibles
- Categorías más fuertes en su catálogo (¿tienen Pet Tech? ¿Hogar inteligente? ¿Salud?)
- Tiempo de entrega promedio a España real (no el anunciado)
- Nivel de integración con Shopify: nativa/app/API + automatización de pedidos (sí/no)
- Política de devoluciones del proveedor al vendedor
- Punto débil más reportado por usuarios 2025-2026

PARA BIGBUY ESPECÍFICAMENTE:
- Condiciones de acceso para pequeños operadores en España (¿se necesita empresa constituida?)
- Catálogo en categorías Pet Tech y Hogar Inteligente
- Mínimos de compra reales (no los anunciados)
- Ventajas concretas frente a Spocket para España

PARA DSers ESPECÍFICAMENTE:
- ¿Es viable usar DSers con AliExpress para Pet Tech en España en 2026?
- ¿Hay proveedores AliExpress con almacén en España o Europa certificados?

FORMATO DE SALIDA:
# Proveedores Dropshipping — España 2026
## Fecha: 2026-06
## Tabla comparativa completa
## Análisis detallado por plataforma
## Tabla de categorías disponibles por proveedor (foco en las 6 del laboratorio)
## Ranking para el laboratorio Ecommerce Disruptivo
## Recomendación del CTO: proveedor principal + backup
## Próximos pasos: cómo activar la cuenta y conectar a Shopify
## Prompt usado
```

---

## TAREA 2.2 — Research Perfumería de Autor y Nicho España → Venezuela

**Ruta:** `projects/02_cosmetica/market_research/2026-06_perfumeria_autor_espana_venezuela.md`

**Contexto:** El research de K-Beauty (Tarea 2.1) cubrió la cosmética. La perfumería nicho requiere research separado porque tiene dinámicas distintas: distribuidores diferentes, logística más compleja (alcohol en avión), regulación SACS diferente, y audiencia objetivo distinta en Venezuela.

```
TAREA 2.2 — Research perfumería de autor y nicho para ruta España → Venezuela

Analiza el mercado de perfumería de autor y fragancias nicho para un operador
que importa desde España y vende en Venezuela.

BLOQUE 1 — MERCADO Y DEMANDA
- Tendencias de perfumería nicho y masculina en España 2025-2026 (marcas, estilos, olfativos)
- Qué tipo de fragancia tiene mayor crecimiento en búsquedas España: oriental, amaderado, gourmand, fresco
- Rango de precios que acepta el consumidor venezolano para fragancias importadas de España (USD)
- Perfumería de autor vs equivalencias: ¿qué mercado tiene más demanda en Venezuela?

BLOQUE 2 — PROVEEDORES Y MARCAS
- Marcas de perfumería nicho/autor europeas con distribución limitada o inexistente en Venezuela
- Distribuidores mayoristas de perfumería en España que vendan a revendedores con MOQ accesible
- Marcas que permiten explícitamente la reventa internacional (o al menos no la prohíben)
- Diferencia entre vender equivalencias (clones) vs marca original: riesgos legales y de reputación

BLOQUE 3 — VIABILIDAD OPERATIVA
- Restricciones para transportar perfumes por vía aérea (alcohol > 70% — ¿cómo lo gestionan los couriers puerta a puerta?)
- Comparativa de margen bruto: perfumería nicho vs K-Beauty vs body care (datos de la Tarea 2.1)
- Productos de perfumería con mejor ratio precio/peso para envío aéreo a Venezuela
- Cómo gestionar el SACS para perfumes vs skincare (¿es más sencillo o más complejo?)

BLOQUE 4 — ESTRATEGIA DE ENTRADA
- ¿Empezar con marca nicho original o con equivalencias como validación de demanda?
- Cómo posicionar la perfumería de origen español ante el consumidor venezolano
- Canales de venta en Venezuela específicos para perfumería (¿mismo que cosmética o diferente?)

FORMATO DE SALIDA:
# Research Perfumería Autor y Nicho — España → Venezuela 2026
## Fecha: 2026-06
## Resumen ejecutivo (5 líneas para el CEO)
## Análisis por bloque
## Tabla de marcas candidatas (nicho europeo, disponibilidad distribución ES)
## Tabla comparativa de márgenes: perfumería vs K-Beauty
## Tabla de riesgos logísticos (alcohol en avión, SACS perfumes)
## Recomendación del CTO: estrategia de entrada perfumería Venezuela
## Prompt usado
```

---

## INSTRUCCIÓN DE CIERRE PARA AG (Semana 3)

```
Una vez completadas las 3 tareas nuevas + corrección de 4.1:

1. Notifica a Claude Code para auditoría de Tarea 4.1 (corrección)
2. Si la corrección está aprobada: commit [research] Semana 2
3. Notifica a Claude Code para auditoría de Tareas 1.3, 1.4, 2.2
4. Si están aprobadas: commit [research] Semana 3 — herramientas, proveedores y perfumería
5. Actualizar STATUS.md con Semana 3 completada

Mensaje de commit Semana 3:
[research] Semana 3 — herramientas de detección, proveedores dropshipping y perfumería nicho

Una vez cerrada la Semana 3, el CEO tendrá suficiente información para ejecutar
las matrices de decisión (Semana 4): elegir categoría del laboratorio, SKU cosmética
y estrategia de diseño Moda.
```

---

## CHECKLIST DE REVISIÓN — Claude Code (auditor)

### Paso 0 — Tarea 4.1 corregida
- [ ] Sección de canales secundarios descartados con razón por canal
- [ ] Tabla "Top 3 canales por línea" presente y coherente con el análisis
- [ ] STATUS.md actualizado antes del commit de Semana 2

### Tarea 1.3 — Herramientas de detección
- [ ] Las 5 herramientas evaluadas con datos 2026
- [ ] Cobertura mercado ES/EU documentada por herramienta (no solo USA)
- [ ] Precio actualizado de cada plan (no datos de 2024)
- [ ] Recomendación CTO incluye cómo usar la herramienta en el flujo del portafolio
- [ ] Sin TODOs ni placeholders

### Tarea 1.4 — Proveedores dropshipping
- [ ] BigBuy evaluado con condiciones específicas de acceso para autónomos/pequeñas empresas en ES
- [ ] Tabla de categorías disponibles por proveedor cubre las 6 del laboratorio
- [ ] Recomendación CTO dice proveedor principal + backup con razón
- [ ] Próximos pasos incluyen cómo activar y conectar a Shopify

### Tarea 2.2 — Perfumería autor
- [ ] Restricciones de transporte aéreo de alcohol documentadas
- [ ] Comparativa de márgenes con K-Beauty (referencia cruzada a Tarea 2.1)
- [ ] Marcas/origen europeos vs equivalencias: posición clara sobre riesgo legal
- [ ] SACS para perfumes vs skincare: diferencia documentada
- [ ] Datos no verificados marcados [NO VERIFICADO]
