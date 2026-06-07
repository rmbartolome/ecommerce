# Prompts de Ejecución para AG

> Esta carpeta contiene los prompts listos para copiar y pegar en Gemini Pro (AG).
> Generados por Claude Code como auditor del proyecto.

---

## Prompts disponibles

| Archivo | Semana | Tareas | Prerequisito |
|---|---|---|---|
| `AG_SEMANA1_ARQUITECTURA.md` | Semana 1 | 0.1, 0.2, 0.3, 4.2 — Árboles de categorías + calculadora | CEO aprueba TOOLS.md |
| `AG_SEMANA2_RESEARCH.md` | Semana 2 | 1.1, 1.2, 2.1, 2.4, 3.1, 3.2 — Research de mercado | Semana 1 completada y aprobada |

---

## Cómo usar estos prompts

1. Verificar que el prerequisito está cumplido
2. Abrir Gemini Pro (Google AI Studio o Gemini Advanced)
3. Copiar la **Instrucción de apertura** del prompt como primer mensaje
4. Esperar confirmación de AG
5. Pegar cada tarea individual en orden
6. AG genera el contenido → tú lo guardas en el repo en la ruta indicada
7. Claude Code audita antes de hacer commit

## Flujo completo

```
CEO aprueba TOOLS.md
       ↓
AG ejecuta Semana 1 → CEO + Claude Code revisan → CEO aprueba
       ↓
AG ejecuta Semana 2 → CEO + Claude Code revisan → CEO aprueba
       ↓
Claude Project sintetiza matrices de decisión (Semana 4)
       ↓
CEO toma decisión de SKU inicial por línea
       ↓
Claude Cowork publica en Shopify
```
