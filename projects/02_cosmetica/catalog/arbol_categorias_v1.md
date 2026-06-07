# Árbol de Categorías — Cosmética v1

## Criterios de diseño del catálogo cosmético
Este catálogo está enfocado en productos cosméticos de alta percepción de valor para el mercado de Venezuela (importación desde España) y validación en España. Incluye atributos críticos regulatorios (SACS para Venezuela, CPNP para UE), naming de origen (ej. K-Beauty) y separa claramente las variantes que generan stock de los metafields informativos de la formulación del producto.

## Estructura de 3 niveles

### NIVEL 1 — Categorías principales

#### Skincare y K-Beauty
**Código:** SKN
**Descripción:** Cuidado facial premium y cosmética coreana.
**Razón de inclusión:** Alta rentabilidad, bajo peso (ideal envío aéreo), alta demanda de ingredientes activos.
**Equivalencia Amazon (Fase 3):** Belleza > Cuidado de la piel > Rostro

**Subcategorías (Nivel 2):**
- Limpieza y Tonificación — SKN-LIM
  - Aceite Limpiador — SKU: SKN-ACELIM-VAR
  - Tónico Centella Asiática — SKU: SKN-TONCEN-VAR
- Tratamiento y Sérums — SKN-TRA
  - Sérum Niacinamida — SKU: SKN-SERNIA-VAR
  - Ampolla Snail Mucin — SKU: SKN-AMPSNA-VAR
- Hidratación y Protección — SKN-HID
  - Crema Hidratante Ligera — SKU: SKN-CREHID-VAR
  - Protector Solar SPF50 — SKU: SKN-PROSOL-VAR

#### Perfumería de Autor y Nicho
**Código:** PRF
**Descripción:** Fragancias de alta calidad, equivalencias premium o marcas nicho europeas.
**Razón de inclusión:** El perfume es el artículo de cuidado personal de mayor estatus en Venezuela.
**Equivalencia Amazon (Fase 3):** Belleza > Perfumes y fragancias

**Subcategorías (Nivel 2):**
- Perfumes Femeninos — PRF-FEM
  - Eau de Parfum Floral — SKU: PRF-EDPFEM-VAR
- Perfumes Masculinos — PRF-MAS
  - Eau de Parfum Amaderado — SKU: PRF-EDPMAS-VAR
- Unisex / Nicho — PRF-UNI
  - Extrait de Parfum Ámbar — SKU: PRF-EXTUNI-VAR

#### Body Care y Cuidado Personal
**Código:** BDY
**Descripción:** Cuidado corporal, exfoliantes y lociones de tratamiento.
**Razón de inclusión:** Complemento ideal para cross-selling con skincare.
**Equivalencia Amazon (Fase 3):** Belleza > Cuidado de la piel > Cuerpo

**Subcategorías (Nivel 2):**
- Hidratación Corporal — BDY-HID
  - Loción Reafirmante — SKU: BDY-LOCREA-VAR
- Tratamientos Específicos — BDY-TRA
  - Exfoliante Enzimático — SKU: BDY-EXFENZ-VAR

#### Cosmética Masculina
**Código:** MEN
**Descripción:** Cuidado facial y de barba para hombres.
**Razón de inclusión:** Nicho de mercado en expansión, menos saturado que el femenino.
**Equivalencia Amazon (Fase 3):** Belleza > Cuidado del hombre

**Subcategorías (Nivel 2):**
- Skincare Hombre — MEN-SKN
  - Limpiador Facial Hombre — SKU: MEN-LIMFAC-VAR
- Cuidado Barba y Cabello — MEN-BAR
  - Aceite para Barba — SKU: MEN-ACEBAR-VAR

#### Kits y Bundles de Regalo
**Código:** BUN
**Descripción:** Sets de productos curados presentados en empaque de alto valor.
**Razón de inclusión:** Incremento de AOV, formato regalo altamente demandado en temporadas (Navidad, Madres).
**Equivalencia Amazon (Fase 3):** Belleza > Estuches y sets de belleza

**Política de Stock Shopify para Bundles:**
Los sets de regalo **NO tendrán stock independiente** en la plataforma. Se gestionarán usando una **Bundle App** en Shopify, que vinculará el inventario disponible al stock de los SKUs individuales de cosmética, evitando que se vendan kits si un componente está agotado.

**Subcategorías (Nivel 2):**
- Rutinas Completas — BUN-RUT
  - Set Rutina K-Beauty — SKU: BUN-RUTKBE-VAR
- Sets de Descubrimiento — BUN-DES
  - Mini Tallas Perfumes — SKU: BUN-MINPRF-VAR

## Tabla de nomenclatura SKU

| Categoría N1 | Prefijo | Ejemplo SKU | Estructura |
|---|---|---|---|
| Skincare | SKN | SKN-SERNIA-50M | [PREFIJO]-[NOMBRE_CORTO]-[VARIANTE_VOLUMEN] |
| Perfumería | PRF | PRF-EDPFEM-100M | [PREFIJO]-[NOMBRE_CORTO]-[VARIANTE_VOLUMEN] |
| Body Care | BDY | BDY-LOCREA-250M | [PREFIJO]-[NOMBRE_CORTO]-[VARIANTE_VOLUMEN] |
| Cosmética Hombre | MEN | MEN-ACEBAR-30M | [PREFIJO]-[NOMBRE_CORTO]-[VARIANTE_VOLUMEN] |
| Bundles | BUN | BUN-RUTKBE-UNI | [PREFIJO]-[NOMBRE_CORTO]-[VARIANTE] |

## Atributos Shopify: Variantes vs Metafields

> **CRÍTICO:** Diferenciar entre variante (que dicta inventario por tamaño) y metafields (que detallan ingredientes y regulaciones).

| Categoría | Variantes (Generan Stock - máx 3) | Metafields (Informativos - No Stock) |
|---|---|---|
| Skincare | Volumen/Capacidad | Tipo de piel, Ingrediente activo, Origen, Certificación (K-Beauty/Vegano), Regulación SACS, CPNP |
| Perfumería | Volumen/Capacidad, Concentración (EDT/EDP/EXT) | Familia olfativa, Notas de salida/corazón/fondo, Regulación SACS |
| Body Care | Volumen/Capacidad | Tipo de piel, Aroma, Ingrediente principal, Regulación SACS |
| Cosmética Hombre | Volumen/Capacidad | Tipo de piel/barba, Ingrediente activo, Regulación SACS |
| Bundles | Tamaño kit | Componentes, Valor ahorrado, Temática |

## Tabla de Atributos Cosméticos (Metafields)

| Metafield | Valores posibles | Obligatorio |
|---|---|---|
| Tipo de piel | Seca / Grasa / Mixta / Sensible / Normal / Todo tipo | Sí |
| Ingrediente activo | Ácido Hialurónico / Centella Asiática / Niacinamida / Vitamina C... | Sí (máx 3) |
| Origen | Corea / Francia / España / Japón / Alemania / Otro | Sí |
| Certificación | K-Beauty / Vegano / COSMOS / Cruelty Free / Ninguna | No |
| Regulación SACS | Requerida / En trámite / Aprobada / No requerida | Sí (para Venezuela) |
| Regulación CPNP | Registrado / No registrado | Sí (para España/UE) |

## Reglas de nomenclatura SKU y Catálogo de Variantes
1. Todo mayúsculas, sin caracteres especiales, uso de guion medio ("-").
2. Nombre corto de producto: máximo 7 caracteres (ej: SERNIA = Sérum Niacinamida).

### Catálogo Estándar de Variantes (Volúmenes y Tamaños)
Para asegurar consistencia en cosmética:
- **Mini tallas / Muestras:** 05M (5ml), 10M (10ml), 15M (15ml)
- **Skincare / Sérums:** 30M (30ml), 50M (50ml)
- **Cremas / Limpiadores:** 100M (100ml), 150M (150ml)
- **Body Care / Perfumes:** 200M (200ml), 250M (250ml), 500M (500ml)
- **Concentración (Perfumería):** EDT (Eau de Toilette), EDP (Eau de Parfum), EXT (Extrait)
- **Sets:** UNI (Talla/Tamaño Único)

## Reglas de etiquetado bilingüe e internacional
- **Para España (UE):** Etiquetado CPNP obligatorio (lista INCI correcta, responsable europeo, caducidad PAO).
- **Para Venezuela:** Traducción al español obligatoria si el envase está en coreano/inglés. Debe incluir código de aprobación del SACS (Servicio Autónomo de Contraloría Sanitaria) una vez importado.
