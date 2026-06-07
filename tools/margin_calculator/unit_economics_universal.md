# Calculadora Unit Economics Universal — Portafolio Ecommerce

## Cómo usar esta calculadora
1. Identifica la línea de negocio de tu SKU (Ecommerce Disruptivo, Cosmética o Moda).
2. Localiza en la **Tabla de variables** los datos de entrada requeridos.
3. Sustituye tus datos reales en la **Fórmula** correspondiente a la línea.
4. Calcula los resultados de margen bruto y neto.
5. Compara el margen neto contra la tabla de **Criterios de clasificación** para tomar una decisión informada (Viable, Revisar o No Viable).

## Tabla de variables de entrada

| Variable | Definición | Unidad | Dónde obtener el dato |
|---|---|---|---|
| Línea de negocio | El proyecto al que pertenece el SKU | Categórico | Estrategia (Ej: Moda) |
| Coste base (COGS) | Precio de compra al proveedor o de producción | € o USD | Proveedor (BigBuy, Printful, etc.) |
| Coste logístico | Flete, aduanas, envío final y tasa de devolución | €/unidad | Cotización transitario o app dropshipping |
| Coste regulatorio | Tasa SACS o CPNP amortizada por unidad | €/unidad | Solo aplicable en Cosmética VE/UE |
| Precio Venta (PVP) | Precio final pagado por el cliente | € (ES) / USD (VE) | Estimado de mercado |
| Tipo de cambio | Conversión EUR a USD | Tasa | Mercado oficial / Paralelo (según VE) |
| Tasa de devolución | Porcentaje estimado de productos retornados | % | Referencia del sector (Textil 15%, Hogar 5%) |
| Comisión canal | Porcentaje retenido por Shopify, Amazon, Miravia... | % | Términos de la plataforma |
| Coste Adquisición (CAC) | Gasto promedio en ads para lograr 1 venta | € | Datos de campañas Meta/TikTok (Opcional) |

## Fórmulas

### Línea Ecommerce Disruptivo (Dropshipping España)
- **Coste Unitario Total (€) =** `COGS + Coste logístico + (PVP * Comisión canal) + (COGS * Tasa de devolución)`
- **Margen Bruto (€) =** `PVP - Coste Unitario Total`
- **Margen Neto (€) =** `Margen Bruto - CAC` (si aplica)
- **Margen Neto (%) =** `(Margen Neto / PVP) * 100`

### Línea Cosmética (Importación España → Venezuela)
- *Nota: Todo se convierte a USD para el cálculo final si el PVP está en USD.*
- **Coste Regulador Unitario =** `Total Tasas SACS / Lote de Unidades a Importar`
- **Coste Logístico Aéreo =** `Peso (kg) * Tarifa Courier ($/kg)`
- **Coste Unitario Total (USD) =** `(COGS en € * Tipo Cambio) + Coste Regulador Unitario + Coste Logístico Aéreo + (PVP * Comisión de pagos)`
- **Margen Bruto (USD) =** `PVP (USD) - Coste Unitario Total`
- **Margen Neto (%) =** `(Margen Bruto / PVP) * 100` *(sin CAC si la venta es orgánica en WA/IG)*
- **Ratio Precio/Peso ($/kg) =** `PVP / Peso SKU` (Mínimo recomendado $80/kg para envío aéreo)

### Línea Moda (Print-on-Demand)
- **Coste Unitario Total (€) =** `Coste base POD (Prenda + Print) + Envío al cliente + (PVP * Comisión canal) + (Coste base POD * Tasa devolución)`
- **Margen Bruto (€) =** `PVP - Coste Unitario Total`
- **Margen Neto (%) =** `((Margen Bruto - CAC) / PVP) * 100`

### Punto de Equilibrio (Break-even)
- **Break-even (unidades) =** `Costes fijos del período / Margen Neto por unidad (€)`
  *Ejemplo:* Si tienes 150€/mes de costes fijos (Shopify + Minea) y tu Margen Neto es de 10.88€ por gadget → necesitas vender **14 unidades/mes** para cubrir los costes y empezar a ganar dinero real.

## Criterios de clasificación

| Clasificación | Margen neto | Acción recomendada |
|---|---|---|
| ✅ VIABLE | > 35% | Proceder con evaluación de proveedor |
| ⚠️ REVISAR | 20-35% | Negociar precio de compra, subir PVP o abaratar envíos |
| ❌ NO VIABLE | < 20% | Descartar producto o replantear el modelo |

## Ejemplos pre-rellenados

### Ejemplo 1 — Cosmética: Sérum K-Beauty Venezuela
- **Variables:** COGS = 4.50€, Cambio = 1.10 ($4.95), Logística (Aéreo, 150g a $30/kg) = $4.50, SACS Amortizado = $0.50, Comisión = $0 (Zelle/Efectivo), PVP = $25.
- **Coste Unitario Total:** $4.95 + $4.50 + $0.50 + $0 = $9.95
- **Margen Bruto / Neto (Orgánico):** $25 - $9.95 = **$15.05 (60.2%)**
- **Resultado:** ✅ VIABLE.

### Ejemplo 2 — Cosmética: Perfume de autor Venezuela
- **Variables:** COGS = 22€, Cambio = 1.10 ($24.20), Logística (Aéreo, 400g a $30/kg) = $12.00, SACS = $0.80, Comisión = $0, PVP = $60.
- **Coste Unitario Total:** $24.20 + $12.00 + $0.80 = $37.00
- **Margen Neto:** $60 - $37 = **$23.00 (38.3%)**
- **Resultado:** ✅ VIABLE.

### Ejemplo 3 — Ecommerce Disruptivo: Gadget de hogar España
- **Variables:** COGS = 8.50€, Logística Dropshipping = 3.50€, Comisión Shopify = 2%, Tasa Devolución = 5%, CAC = 6.00€, PVP = 29.90€.
- **Coste Unitario Total:** 8.50 + 3.50 + (29.90 * 0.02) + (8.50 * 0.05) = 13.02€
- **Margen Bruto:** 29.90 - 13.02 = 16.88€
- **Margen Neto:** 16.88 - 6.00 = **10.88€ (36.4%)**
- **Resultado:** ✅ VIABLE.

### Ejemplo 4 — Ecommerce Disruptivo: Accesorio Pet Tech España
- **Variables:** COGS = 18.00€, Logística = 5.50€, Comisión Shopify = 2%, Tasa Devolución = 8%, CAC = 8.00€, PVP = 39.90€.
- **Coste Unitario Total:** 18.00 + 5.50 + (39.90 * 0.02) + (18.00 * 0.08) = 25.74€
- **Margen Bruto:** 39.90 - 25.74 = 14.16€
- **Margen Neto:** 14.16 - 8.00 = **6.16€ (15.4%)**
- **Resultado:** ❌ NO VIABLE.

### Ejemplo 5 — Moda: Camiseta POD España
- **Variables:** COGS (Printful) = 12.50€, Envío cliente = 4.20€, Comisión = 2%, Tasa Devolución = 15% (alto por talla), CAC = 7.00€, PVP = 34.90€.
- **Coste Unitario Total:** 12.50 + 4.20 + (34.90 * 0.02) + (12.50 * 0.15) = 19.27€
- **Margen Bruto:** 34.90 - 19.27 = 15.63€
- **Margen Neto:** 15.63 - 7.00 = **8.63€ (24.7%)**
- **Resultado:** ⚠️ REVISAR (Necesario subir PVP a 39.90€ o bajar CAC).

## Notas sobre márgenes mínimos por línea

> **ACLARACIÓN IMPORTANTE:** Estos son umbrales de margen **BRUTO** (antes de restar CAC y costes fijos). El criterio de clasificación de la sección anterior (VIABLE / REVISAR / NO VIABLE) aplica al margen **NETO**. Para que un producto escale, debe cumplir ambas condiciones.

| Línea | Umbral de Margen Bruto Mínimo | Justificación |
|---|---|---|
| Ecommerce Disruptivo | 60% antes de CAC | El modelo es altamente intensivo en publicidad (Meta/TikTok). Un producto sin margen bruto gigante no sobrevive el CAC. |
| Cosmética (Venezuela) | 50% | Se debe compensar el alto coste de envío aéreo, el riesgo de retención aduanera, y la caducidad. Menos CAC por ser orgánico, pero mayor riesgo operativo. |
| Moda (POD) | 45% (o > 15€ absolutos) | El CPA en moda suele ser alto y constante. Es imperativo que el beneficio bruto mínimo absoluto sea de al menos 12-15€ para ser rentable. |
