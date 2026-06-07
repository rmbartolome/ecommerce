# PROYECTO: Portafolio Familiar de Emprendimientos (Ecommerce)

> Este archivo fue completado por el agente a partir de los documentos semilla del ecosistema ecommerce (Ecommerce Disruptivo, Cosmética, Moda).

---

## Objetivo Core

Consolidar y gestionar el ecosistema ecommerce del Portafolio Familiar en un solo lugar estructurado. Sirve como sistema operativo para tres líneas de negocio:
1. **Ecommerce Disruptivo** (Línea madre - Laboratorio comercial)
2. **Cosmética, Perfumes y Marca Personal** (Importación y marca curada)
3. **Moda, Diseño y Fabricación** (POD y marca propia)
Todo el proceso desde research, selección de producto, diseño, hasta lanzamiento multicanal se gestiona aquí.

---

## Topología de Repositorios

- **Tipo:** [x] Single-repo  [ ] Multi-repo
- **Nota:** Estructura monorepo gestionada en GitHub (`ecommerce-portfolio`). Centraliza investigación, estrategia, activos de marketing y configuraciones de tiendas (Shopify/Amazon) para las tres líneas de negocio bajo el paraguas del portafolio.

---

## Área Tecnológica a Investigar

- **Dominio principal:** Comercio electrónico, automatización de tiendas, integraciones OMS (Order Management System), análisis de tendencias y catálogos.
- **Restricciones de herramientas:** Herramientas orientadas a validación rápida con bajo coste. Herramientas de IA para análisis de mercado (Minea, SellTheTrend) y generación de contenido/catálogo en batch.
- **Herramientas que ya usas o quieres mantener:**
  - Tienda: Shopify (como núcleo de lanzamiento y validación) y luego Amazon/Miravia.
  - IA: Stack de Claude (Project/Code/Cowork/Design), Gemini Pro, ChatGPT, NotebookLM.
  - Operaciones: Dropshipping (DSers, Spocket), POD (Printful, Printify, Gelato).

---

## Tech Stack (si ya lo tienes claro)

- **Plataforma Ecommerce:** Shopify (Base central) con expansión posterior a Amazon/Miravia vía OMS.
- **IA / Automatización:** Claude (Principal), Gemini Pro (Research), NotebookLM (Archivo vivo).
- **Control de versiones:** Git / GitHub para documentación y gestión de activos.
- **Formatos:** Markdown para trabajo vivo, DOCX para documentos ejecutivos finales.

---

## Restricciones Duras

- [x] NO hacer cambios destructivos en catálogos (`catalog/`), tiendas (`shopify/`) o scripts (`tools/`) sin aprobación explícita del CEO (Roberto).
- [x] NO comprometer capital (proveedores, inventario, campañas) sin validación y decisión explícita.
- [x] NO usar herramientas de IA descontinuadas en este ecosistema (OpenClaw, NemoClaw, Auris).
- [x] Los secretos y credenciales NUNCA van en el repositorio.
- [x] Arquitectura de catálogo: Definir siempre el árbol de categorías con visión de futuro ANTES de configurar Shopify.

---

## Agentes IA involucrados (si aplica)

| Agente | Rol en este proyecto |
|---|---|
| **Claude Project** | Cerebro estratégico, análisis, documentos ejecutivos, decisiones de arquitectura de catálogo. |
| **Claude Code** | Desarrollo técnico, scripts, automatizaciones, generación de fichas en batch. |
| **Claude Cowork** | Operaciones, gestión de tareas, flujos de trabajo, publicación en Shopify. |
| **Claude Design** | Activos visuales, mockups, contenido gráfico. |
| **Gemini Pro** | Research externo, datos de mercado, validación de tendencias. |

---

## Criterios de Exito

- [ ] Árboles de categorías completos y validados (3 niveles) para Ecommerce, Cosmética y Moda.
- [ ] Calculadora de Unit Economics universal funcional y testeada.
- [ ] Documentación de research de mercado y proveedores (España y Venezuela) completada y sintetizada.
- [ ] Catálogo inicial (3-5 SKUs) definido para el laboratorio de Ecommerce Disruptivo.
- [ ] Tienda Shopify base configurada y lanzada para la validación comercial.
- [ ] Primera expansión a marketplace (Amazon/Miravia) mediante OMS validada con stock sincronizado.

---

> **Briefing completo.** GOALS.md generado por Claude Code (2026-06-07). AG puede leer este briefing y proceder según el protocolo del framework.
