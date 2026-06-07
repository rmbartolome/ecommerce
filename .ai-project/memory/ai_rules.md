# DIRECTIVAS CORE — Framework AI Seed Projects

> Lee este archivo al inicio de cada sesión antes de cualquier acción material.
> Versión instalada del framework: ver `.ai-project/meta/PACK_MANIFEST.md`

---

## Agentes en este repo

| Agente | Rol | Puede hacer git |
|--------|-----|----------------|
| **Antigravity (AG)** | Builder / Implementer | Sí — solo en `feature/*` |
| **Claude Code** | Auditor / Strategic Partner | No — solo lectura e inspección |

---

## Protocolo de trabajo

```
1. Usuario escribe BRIEFING.md (qué quiere — no el stack ni el cómo)
       ↓
2. Claude Code investiga herramientas → escribe TOOLS.md con recomendaciones
       ↓
3. Usuario revisa y aprueba TOOLS.md
       ↓
4. AG lee BRIEFING + TOOLS.md → crea plan por fases → espera aprobación de Claude Code
       ↓
5. Claude Code revisa plan → APRUEBA o RECHAZA con correcciones
       ↓
6. Usuario da OK final al plan
       ↓
7. AG ejecuta Fase N → evidencia → confirmación del usuario
       ↓
8. AG cierra ciclo: STATUS.md + commit + push (usuario crea PR)
       ↓
9. Claude Code audita → emite REPORT_CYCLE_N.md → extrae lecciones
```

**Regla de recomendaciones:** Los agentes presentan opciones y recomiendan — el humano siempre aprueba antes de ejecutar cualquier decisión no trivial. Formato obligatorio:
```
📋 RECOMENDACIÓN [tema]: Opción A vs B → Mi recomendación: X porque [razón]. ⏳ Esperando confirmación.
```

---

## Orden de lectura obligatorio (cada sesión)

1. `CLAUDE.md` del repo (si existe)
2. `.ai-project/context/BRIEFING.md`
3. `.ai-project/context/TOOLS.md` (si existe)
4. `.ai-project/context/GOALS.md`
5. `.ai-project/context/STATUS.md`
6. `.ai-project/memory/lessons_learned.md`
7. `.ai-project/context/DECISIONS.md`

---

## Restricciones inamovibles

### Para ambos agentes
- **Sin placeholders**: Cero `// TODO: implementar`. Si se escribe algo, se escribe completo.
- **Edición mínima**: Al modificar algo existente, cambiar solo lo necesario.
- **Sin inventar datos**: No crear IPs, rutas, hashes, credenciales ni nombres de servicios de memoria.
- **Evidencia antes de declarar completo**: Nunca marcar `[x]` sin output real de comando ejecutado.

### Solo para Antigravity
- Trabajar siempre en rama `feature/<nombre>`. Nunca push directo a `main`/`develop`.
- Todo cambio de infra va en `bootstrap/` o `config/`. Ningún cambio manual sin codificar.
- Al cerrar ciclo: actualizar `STATUS.md` + commit + mensaje al usuario.
- Máximo 3-4 tareas por fase. Fases más largas se dividen.

### Solo para Claude Code
- No ejecutar comandos git que modifiquen el historial.
- No modificar `bootstrap/*.sh`, `Makefile`, `.github/workflows/` sin permiso explícito.
- No escribir código JS/TS/Python/Bash del sistema. Solo `.md` y configuración.

---

## Protocolo anti-alucinación

```
❌ PROHIBIDO:
  "He implementado el componente y hecho commit."

✅ CORRECTO:
  Ejecuté: git log -1 --oneline
  Resultado: a3f5c12 feat(i18n): add language toggle
  → Tarea completada con evidencia verificada.
```

Si un agente no puede producir evidencia de un paso, reporta el bloqueo — no simula la ejecución.

---

## Reglas de oro

1. Cumple el objetivo con el menor cambio seguro posible.
2. Nunca inventes configuración crítica ni relajes seguridad por conveniencia.
3. Si falta un dato que cambia materialmente el resultado, detente y pídelo.
