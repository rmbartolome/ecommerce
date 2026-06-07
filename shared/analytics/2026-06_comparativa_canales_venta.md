# Comparativa Canales de Venta — España y Venezuela 2026
## Fecha: 2026-06

## BLOQUE 1 — Mercado España B2C (Marketplaces y Social Commerce)

| Canal / Plataforma | Cuota Mensual | Comisión por Venta (Aprox.) | Categorías Estrella | Integración Shopify |
|---|---|---|---|---|
| **Amazon.es (FBA/FBM)** | 39€ | Moda: 5-10% (<20€). General: 8-15% | Electrónica, Hogar, Belleza | Alta (App oficial / CedCommerce) |
| **Miravia** | 0€ | 6-15% (Moda/Belleza: 13-15%) | Belleza, Moda, Hogar | Media (Channable / CedCommerce) |
| **TikTok Shop ES** | 0€ | 9% (7% Belleza/Electrónica) | Moda (Merch), Belleza | Alta (Nativa / App oficial) |
| **Etsy** | 0€ | ~6.5% + 0.20€ listing | Joyería, Personalizados | Alta (Nativa) |
| **Zalando Partner** | ~40€ | 5-25% | Moda, Calzado | Baja (Requiere integrador robusto) |
| **Wallapop PRO** | 39€ (Básico) | 0% (la protección la paga el comprador) | Recommerce, Liquidación | Nula/Manual |

### Análisis por canal (España)
- **Amazon.es:** Excelente para volumen en "Ecommerce Disruptivo" (Hogar Inteligente, Pet Tech). Exige guerra de precios. Las nuevas tarifas 2026 benefician productos por debajo de 20€.
- **Miravia:** La gran apuesta de Alibaba para Europa. Es ideal para la línea de **Cosmética K-Beauty**. A diferencia de Amazon, no tiene cuota fija y el tráfico para *beauty* y moda es muy alto, pero su integración requiere *middleware* (ej. Oceges o Channable).
- **TikTok Shop:** El canal revelación para **Moda y Creator Merch**. La comisión base subió al 9% en 2026, pero la fricción de compra es mínima (*Live Shopping*).
- **Zalando:** Altamente restrictivo. Exige envíos y devoluciones gratuitas (100 días) y GTINs válidos. Descartado para fase inicial.

### Canales secundarios evaluados y descartados (Fase inicial)

| Canal | Razón de descarte en Fase 1-2 |
|---|---|
| Pinterest Shopping | Gratuito pero tráfico de descubrimiento lento. Activar en Fase 3 para cosmética y moda sostenible como canal de SEO visual |
| Carrefour Marketplace | Acceso restrictivo para nuevos vendedores, proceso de alta lento. Fase 4 |
| El Corte Inglés Online | Solo acepta marcas establecidas con volumen. Fuera de alcance actual |
| Druni / Primor | No tienen marketplace abierto a terceros vendedores. Descartado |

## BLOQUE 2 — Mercado Venezuela B2C

| Canal | Cuota | Comisión | Tráfico Activo | Modelo de Cierre |
|---|---|---|---|---|
| **MercadoLibre VE** | 0€ | Variable + Cargo Fijo (Según categoría/Premium) | Muy Alto (Búsqueda por intención) | Plataforma / PagoMixto |
| **Instagram (IG Store)**| 0€ | 0% (Venta por DM) | Alto (Visual/Aspiracional) | DM a WhatsApp |
| **WhatsApp Business** | 0€ | 0% | Medio (Retención/Comunidad) | Chat (Venta Consultiva) |

### Análisis por canal (Venezuela)
- **MercadoLibre:** El algoritmo castiga a vendedores sin reputación. El coste operativo (Comisión + Cargo Fijo + Costo de Envío Gratis asumido por el vendedor) puede hundir el margen en productos baratos. Útil como escaparate de validación.
- **Instagram + WhatsApp:** La dupla dominante en LATAM. El consumidor venezolano requiere "venta consultiva" (preguntar disponibilidad, coordinar pagos en divisas/Zelle o PagoMóvil). Shopify actúa como un catálogo premium y gestor de inventario, pero el checkout suele derivarse a un operador humano (WhatsApp) para cerrar la venta debido a la fricción de las pasarelas de pago internacionales.

## BLOQUE 3 — Estrategia Multicanal e Integración con Shopify (El "Hub")

El enfoque técnico consiste en utilizar **Shopify** como el "Hub Central" (única fuente de verdad para inventario y pedidos) y los canales como "Spokes" (radios) de distribución.

1. **Ruta Cosmética K-Beauty (España):** 
   - *Estrategia:* Shopify + Miravia + TikTok Shop. 
   - *Por qué:* Miravia concentra a la audiencia compradora de cosmética en España.
2. **Ruta Moda / Joyería Private Label:** 
   - *Estrategia:* Shopify + TikTok Shop + Etsy.
   - *Por qué:* El descubrimiento visual en TikTok impulsa ventas por impulso de merch y joyería minimalista.
3. **Ruta Ecommerce Disruptivo (Gadgets/Arbitraje VE):**
   - *Estrategia:* Instagram Ads -> Shopify (catálogo) -> WhatsApp (cierre manual).
   - *Por qué:* Mitiga el riesgo de falsificaciones generando confianza uno a uno con el cliente venezolano.

**Conclusión del CTO:** 
Evitar Amazon FBA en la primera fase para las líneas de Moda y Cosmética para proteger el branding y el margen bruto. Iniciar la tracción apoyándonos en el algoritmo orgánico de TikTok Shop (Moda) y Miravia (Cosmética), centralizando todo el *stock* en Shopify mediante integradores como CedCommerce o la app nativa de TikTok.

### Top 3 canales por línea (resumen ejecutivo)

| Línea | Canal 1 (Hub) | Canal 2 (Captación) | Canal 3 (Escalado Fase 3) |
|---|---|---|---|
| Ecommerce Disruptivo | Shopify | Instagram Ads → WhatsApp (VE) | Amazon.es |
| Cosmética | Shopify | Miravia | Instagram + Telegram VE |
| Moda | Shopify | TikTok Shop | Etsy |

## Prompt usado
```text
TAREA 4.1 — Comparativa canales de venta (España + Venezuela 2026)

Comparativa de rentabilidad y esfuerzo para integrar distintos marketplaces
con Shopify.

BLOQUE 1 — ESPAÑA B2C
Analizar comisiones, cuota mensual, requisitos técnicos e integración Shopify de:
- Amazon.es Seller (plan Profesional)
- Miravia
- TikTok Shop España
- Instagram Shopping / Pinterest Shopping
- Etsy
- Marketplaces secundarios (Zalando Partner, Carrefour, El Corte Inglés, Druni/Primor, Wallapop PRO)
*Nota: Descartar explícitamente AliExpress*

BLOQUE 2 — VENEZUELA B2C
- Estructura de comisiones MercadoLibre Venezuela 2026 y cómo funciona el tráfico activo
- Venta consultiva por WhatsApp Business / Instagram DM vs Checkout automático

BLOQUE 3 — INTEGRACIÓN
- Matriz de qué canales se conectan de forma nativa a Shopify y cuáles requieren middleware (ej. Channable)
- Recomendación de 2 canales iniciales por categoría (gadgets, cosmética, moda)
```
