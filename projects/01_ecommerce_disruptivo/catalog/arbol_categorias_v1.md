# Árbol de Categorías — Ecommerce Disruptivo v1

## Criterios de diseño del catálogo
Este catálogo prioriza productos funcionales y estéticos con alto valor percibido para el mercado español (2026). La estructura de 3 niveles está diseñada para permitir escalabilidad hasta 200+ SKUs en el modelo de dropshipping europeo (BigBuy/Spocket) sin tener que rediseñar la navegación principal. Siguiendo el ADR-008 (Multicanal), la estructura diferencia claramente entre variantes que generan inventario (Shopify) y metafields informativos, y prepara la equivalencia para la futura expansión a Amazon.

## Estructura de 3 niveles

### NIVEL 1 — Categorías principales

#### Hogar inteligente y confort
**Código:** HOG
**Descripción:** Soluciones de domótica y accesorios de bienestar para el día a día en casa.
**Razón de inclusión:** Tendencia en alza de "hogar como refugio", alta disposición a invertir en confort post-2020.
**Equivalencia Amazon (Fase 3):** Bricolaje y herramientas > Domótica / Hogar y cocina > Climatización

**Subcategorías (Nivel 2):**
- Confort y Climatización — HOG-CLI
  - Humidificador Aromaterapia — SKU: HOG-HUMAROM-VAR
  - Purificador de Aire Mini — SKU: HOG-PURMINI-VAR
- Gadgets Domésticos — HOG-GAD
  - Dispensador Automático Jabón — SKU: HOG-DISPJAB-VAR

#### Tecnología wearable
**Código:** TEC
**Descripción:** Dispositivos que se llevan puestos enfocados en salud, productividad y estilo.
**Razón de inclusión:** Alto valor percibido y bajo costo de envío.
**Equivalencia Amazon (Fase 3):** Electrónica > Dispositivos portátiles y smartwatches

**Subcategorías (Nivel 2):**
- Smartwatches y Bandas — TEC-SMW
  - Pulsera Actividad Básica — SKU: TEC-PULSBA-VAR
- Audio Inteligente — TEC-AUD
  - Auriculares TWS — SKU: TEC-AURTWS-VAR

#### Salud, bienestar y deporte
**Código:** SAL
**Descripción:** Equipamiento y tecnología para fitness en casa y cuidado personal.
**Razón de inclusión:** Crecimiento sostenido del fitness en casa.
**Equivalencia Amazon (Fase 3):** Deportes y aire libre / Salud y cuidado personal

**Subcategorías (Nivel 2):**
- Recuperación Muscular — SAL-REC
  - Pistola Masaje Portátil — SKU: SAL-PISMAS-VAR
- Equipamiento Funcional — SAL-EQU
  - Esterilla Yoga Antideslizante — SKU: SAL-ESTYOG-VAR

#### Pet Tech
**Código:** PET
**Descripción:** Tecnología y accesorios innovadores para mascotas.
**Razón de inclusión:** Humanización de mascotas y alto gasto en accesorios.
**Equivalencia Amazon (Fase 3):** Productos para mascotas

**Subcategorías (Nivel 2):**
- Alimentación y Agua — PET-ALI
  - Comedero Inteligente WiFi — SKU: PET-COMINT-VAR
  - Fuente de Agua Silenciosa — SKU: PET-FUEAGU-VAR
- Entretenimiento y Rastreo — PET-ENT
  - Rastreador GPS Collar — SKU: PET-GPSCOL-VAR

#### Sostenibilidad y economía circular
**Código:** ECO
**Descripción:** Productos reutilizables para reducir plásticos.
**Razón de inclusión:** Demanda de Gen Z y Millennials por opciones verdes.
**Equivalencia Amazon (Fase 3):** Depende del producto (Hogar y cocina, Salud y cuidado)

**Subcategorías (Nivel 2):**
- Hidratación y Térmicos — ECO-HID
  - Botella Acero Inoxidable — SKU: ECO-BOTACE-VAR
- Cuidado Personal Reutilizable — ECO-CUI
  - Discos Desmaquillantes Bambú — SKU: ECO-DISBAM-VAR

#### Kits y bundles curados
**Código:** BUN
**Descripción:** Conjuntos de productos de las demás categorías agrupados por necesidad.
**Razón de inclusión:** Aumenta el AOV y los márgenes de beneficio.
**Equivalencia Amazon (Fase 3):** Mapeado según el producto principal del kit.

**Política de Stock Shopify para Bundles:**
Los kits/bundles **NO tendrán stock independiente** configurado manualmente. Se utilizará una **Bundle App** en Shopify. El kit se mostrará como un solo producto de cara al cliente, pero su disponibilidad estará vinculada automáticamente al stock de los SKUs individuales que lo componen, garantizando la correcta sincronización con el proveedor de dropshipping.

**Subcategorías (Nivel 2):**
- Kits de Regalo — BUN-REG
  - Kit Relax (Humidificador + Antifaz) — SKU: BUN-KITREL-VAR
- Kits de Iniciación — BUN-INI
  - Kit Eco-Cocina — SKU: BUN-KITECO-VAR

## Tabla de nomenclatura SKU

| Categoría N1 | Prefijo | Ejemplo SKU | Estructura |
|---|---|---|---|
| Hogar inteligente | HOG | HOG-HUMAROM-BLA | [PREFIJO]-[NOMBRE_CORTO]-[VARIANTE] |
| Tecnología wearable | TEC | TEC-AURTWS-NEG | [PREFIJO]-[NOMBRE_CORTO]-[VARIANTE] |
| Salud y bienestar | SAL | SAL-PISMAS-GRS | [PREFIJO]-[NOMBRE_CORTO]-[VARIANTE] |
| Pet Tech | PET | PET-COMINT-BLA | [PREFIJO]-[NOMBRE_CORTO]-[VARIANTE] |
| Sostenibilidad | ECO | ECO-BOTACE-VER | [PREFIJO]-[NOMBRE_CORTO]-[VARIANTE] |
| Kits y bundles | BUN | BUN-KITREL-UNI | [PREFIJO]-[NOMBRE_CORTO]-[VARIANTE] |

## Atributos Shopify: Variantes vs Metafields

> **CRÍTICO:** Shopify maneja hasta 3 opciones de variante por producto que generan filas de stock. El resto de características deben ser Metafields (informativos).

| Categoría | Variantes (Generan Stock - máx 3) | Metafields (Informativos - No Stock) |
|---|---|---|
| Hogar inteligente | Color, Capacidad, Tipo enchufe | Material, Potencia/Alimentación, Conectividad (WiFi/Bluetooth), Dimensiones |
| Tecnología wearable | Color, Tamaño (Correa) | Autonomía batería, Compatibilidad (iOS/Android), Resistencia agua (IPXX), Peso |
| Salud y bienestar | Color, Resistencia (Lbs), Talla | Material, Modo de uso, Niveles de velocidad |
| Pet Tech | Color, Tamaño/Capacidad | Tipo de mascota compatible, Conectividad, App |
| Sostenibilidad | Color, Capacidad | Material principal, Vida útil estimada, Certificaciones Eco |
| Kits y bundles | Color dominante, Tamaño kit | Contenido del kit, Valor ahorrado, Packaging |

## Reglas de nomenclatura SKU
1. Todo el SKU debe escribirse en letras MAYÚSCULAS sin caracteres especiales (ñ, ç) ni espacios. Usar guion medio ("-").
2. El nombre corto del producto no debe superar los 7 caracteres.
3. La variante debe utilizar el **Catálogo Estándar de Variantes** de 3 o 4 caracteres.

### Catálogo Estándar de Variantes
Para asegurar consistencia al subir catálogos a Shopify, utilizar exclusivamente estos códigos:
- **Colores:** BLA (Blanco), NEG (Negro), GRS (Gris), AZL (Azul), ROJ (Rojo), VER (Verde), ROS (Rosa), AMA (Amarillo), MUL (Multicolor)
- **Tamaños (Ropa/Accesorios):** S (Small), M (Medium), L (Large), XL (Extra Large), UNI (Talla Única)
- **Capacidades:** 250M (250ml), 500M (500ml), 750M (750ml), 1LT (1 Litro), 2LT (2 Litros)
- **Pesos/Resistencias:** LIG (Ligero), MED (Medio), PES (Pesado)

## Productos excluidos de este catálogo
- **Electrónica compleja o baterías no certificadas:** Para evitar problemas aduaneros e incendios.
- **Ropa y calzado con tallajes complejos:** Derivados a la línea de Moda.
- **Productos líquidos o cosméticos:** Derivados a la línea de Cosmética.
- **Muebles de gran volumen o pesados:** Costes de dropshipping prohibitivos.
- **Alimentación (humana o animal):** Por regulaciones sanitarias.
