# Árbol de Categorías — Moda v1

## Criterios de diseño del catálogo textil
Este catálogo soporta la línea de Moda, Diseño y Fabricación orientada al mercado español (y potencial LATAM). Inicia con un modelo Print-on-Demand (Printful/Gelato) evolucionando a marca propia. La arquitectura prioriza el manejo correcto de la complejidad de variantes talla/color nativa de Shopify, estructurando el catálogo para facilitar la gestión de inventario y la navegación del usuario.

## Política de variantes (CRÍTICO)

La correcta configuración de variantes en Shopify es esencial para la línea textil, ya que el límite es de 100 variantes por producto y 3 opciones (ej. Talla, Color, Material).

### Productos con variantes agrupadas (mismo SKU padre)
Se agrupan bajo un mismo listing de Shopify:
- **Tallas y colores básicos del mismo diseño:** Ejemplo, "Camiseta Logo Clásico" tendrá variantes de Talla (S, M, L, XL) y Color (NEG, BLA). Todos conviven en el mismo producto.
- **Accesorios con ligeras variaciones de tamaño:** Ejemplo, "Anillo Minimalista" con variantes de talla (US 6, 7, 8).

### Productos independientes (SKU diferente por color/diseño)
Se crean como productos separados en Shopify (no como variantes):
- **Diseños o estampados completamente diferentes:** "Sudadera Colección Invierno" y "Sudadera Colección Verano" son productos separados aunque la prenda base sea igual.
- **Colores muy especiales que requieran galería fotográfica propia extensa:** Si un color cambia drásticamente el material (ej. Bolso Negro Mate vs Bolso Plata Brillante).
- **Kits/Bundles:** No tienen stock propio, se configuran mediante Bundle App en Shopify enlazando los SKUs base.

## Estructura de 3 niveles

### NIVEL 1 — Categorías principales

#### Ropa Estética e Identity-Driven
**Código:** ROP
**Descripción:** Prendas principales con diseños propios y mensajes aspiracionales.
**Razón de inclusión:** Core del modelo Print-on-Demand. Alta rotación impulsada por comunidad.
**Equivalencia Amazon (Fase 3):** Ropa, zapatos y joyería > Ropa > Mujer / Hombre

**Subcategorías (Nivel 2):**
- Camisetas y Tops — ROP-CAM
  - Camiseta Oversize — SKU: ROP-CAMOVE-NEG-M
- Sudaderas y Hoodies — ROP-SUD
  - Sudadera con Capucha — SKU: ROP-SUDCAP-BLA-L

#### Accesorios Lifestyle
**Código:** ACC
**Descripción:** Accesorios cotidianos, mayormente sin talla.
**Razón de inclusión:** Bajo ratio de devoluciones y excelente up-sell.
**Equivalencia Amazon (Fase 3):** Ropa, zapatos y joyería > Accesorios

**Subcategorías (Nivel 2):**
- Bolsos y Tote Bags — ACC-BOL
  - Tote Bag Lona Ecológica — SKU: ACC-TOTLON-NAT-UNI
- Gorras y Sombreros — ACC-GOR
  - Gorra Deportiva — SKU: ACC-GORDEP-NEG-UNI

#### Joyería Private Label
**Código:** JOY
**Descripción:** Bisutería fina y accesorios de metal.
**Razón de inclusión:** Alto margen percibido y envío muy económico.
**Equivalencia Amazon (Fase 3):** Ropa, zapatos y joyería > Joyería

**Subcategorías (Nivel 2):**
- Anillos y Pulseras — JOY-ANI
  - Anillo Minimalista Plata — SKU: JOY-ANIPLA-PLT-S
- Collares y Pendientes — JOY-COL
  - Collar Minimalista Plata — SKU: JOY-COLPLA-PLT-UNI

#### Moda Sostenible
**Código:** SOS
**Descripción:** Ropa fabricada con materiales orgánicos (GOTS).
**Razón de inclusión:** Aumento de demanda por textiles ecológicos en Europa.
**Equivalencia Amazon (Fase 3):** Ropa, zapatos y joyería > Ropa (Asignado según la prenda base)

**Subcategorías (Nivel 2):**
- Prendas Ecológicas — SOS-PRE
  - Camiseta Algodón Orgánico — SKU: SOS-CAMORG-BLA-M

#### Creator Merch
**Código:** MER
**Descripción:** Línea de merchandising específica vinculada a la marca personal.
**Razón de inclusión:** Exclusividad para la comunidad fidelizada.
**Equivalencia Amazon (Fase 3):** Ropa, zapatos y joyería > Novedades

**Subcategorías (Nivel 2):**
- Ediciones Limitadas — MER-EDL
  - Camiseta "Frase Core" — SKU: MER-CAMFRA-NEG-UNI

## Tabla de nomenclatura SKU textil

| Categoría N1 | Prefijo | Ejemplo SKU | Estructura |
|---|---|---|---|
| Ropa Estética | ROP | ROP-CAMOVE-NEG-M | [PREFIJO]-[PRODUCTO]-[COLOR]-[TALLA] |
| Accesorios | ACC | ACC-TOTLON-NAT-UNI | [PREFIJO]-[PRODUCTO]-[COLOR]-[TALLA] |
| Joyería | JOY | JOY-ANIPLA-PLT-S | [PREFIJO]-[PRODUCTO]-[COLOR]-[TALLA] |
| Sostenible | SOS | SOS-CAMORG-BLA-M | [PREFIJO]-[PRODUCTO]-[COLOR]-[TALLA] |
| Creator Merch | MER | MER-CAMFRA-NEG-UNI | [PREFIJO]-[PRODUCTO]-[COLOR]-[TALLA] |

## Atributos Shopify: Variantes vs Metafields

> **CRÍTICO:** Las variantes de talla/color determinan la matriz de SKUs (máximo 100 por producto). Los materiales o certificaciones van como metafields informativos y no afectan el stock.

| Categoría | Variantes (Generan Stock - máx 3) | Metafields (Informativos - No Stock) |
|---|---|---|
| Ropa Estética | Talla, Color | Material (Algodón/Poliester), Técnica impresión, Instrucciones lavado |
| Accesorios | Color, Tamaño (si aplica) | Material, Dimensiones (cm), Capacidad |
| Joyería | Talla anillo, Color de acabado | Material base (Plata/Acero), Tipo de cierre |
| Moda Sostenible | Talla, Color | Material (Algodón Orgánico), Certificación (GOTS, OEKO-TEX) |
| Creator Merch | Talla, Color | Significado del diseño, Colección/Drop |

## Tabla de Atributos Textiles UE (Metafields)

| Metafield | Valores posibles | Obligatorio |
|---|---|---|
| Material | Algodón / Poliéster / Mezcla / Algodón Orgánico / Plata 925... | Sí |
| Técnica impresión | DTG / Sublimación / Bordado / Serigrafía | Sí (para POD) |
| Certificación | GOTS / OEKO-TEX / Ninguna | No |
| Instrucciones Cuidado | Lavar en frío / No planchar el diseño / Secado a máquina | Sí |

## Reglas de nomenclatura SKU y Catálogo Estándar de Variantes
1. El SKU no lleva caracteres especiales, ñ, o espacios. Se separa con guion medio ("-").
2. Usar un máximo de 4 segmentos: `[PREFIJO]-[PRODUCTO]-[COLOR]-[TALLA]`.

### Catálogo Estándar de Variantes
Para evitar duplicidades en Shopify, usar estos códigos:
- **Tallas (Ropa):** XS, S, M, L, XL, 2XL, 3XL, UNI (Talla Única)
- **Tallas (Joyería):** US6, US7, US8, UNI
- **Colores (Textil):** BLA (Blanco), NEG (Negro), GRS (Gris), AZL (Azul Marino), ROJ (Rojo), VER (Verde), NAT (Natural/Crudo)
- **Colores (Acabado Joyería):** ORO (Dorado), PLT (Plateado), ROS (Oro Rosa)

## Guía de sizing europeo (Equivalencias para reducir devoluciones)
Para el mercado español, las tallas POD (frecuentemente basadas en US) deben mapearse correctamente:
### Ropa Textil
- **XS (US):** 34 (ES/FR/DE)
- **S (US):** 36-38 (ES/FR/DE)
- **M (US):** 40-42 (ES/FR/DE)
- **L (US):** 44-46 (ES/FR/DE)
- **XL (US):** 48-50 (ES/FR/DE)

### Joyería (Anillos)
- **US 6:** 52 mm de circunferencia (Equivale a Talla 12 ES)
- **US 7:** 54.4 mm de circunferencia (Equivale a Talla 14 ES)
- **US 8:** 57 mm de circunferencia (Equivale a Talla 17 ES)

> *Nota: Se debe añadir siempre una tabla de medidas en centímetros (pecho, largo) en las imágenes o metafield del producto en Shopify, ya que la ropa POD no tiene devolución por error de talla del cliente.*
