# AGENTS.md — Contrato Operativo del Framework (V3)

> Este archivo es el contrato de trabajo entre todos los agentes de IA que operan en este repositorio.
> Cada agente debe leerlo al inicio de cada sesión antes de hacer cualquier cambio material.

---

## AGENTES DEL FRAMEWORK

| Agente | Modelo | Rol | Puede hacer git |
|---|---|---|---|
| **Antigravity** | Gemini (Google) | Builder / Implementer | Sí |
| **Claude Code** | Claude Sonnet (Anthropic) | Auditor / Strategic Partner | No |

---

## MODELO DE OPERACIÓN

Cuatro roles lógicos, ejecutados asíncrona y colaborativamente:

1. **Manager** — interpreta la petición, identifica el objetivo real, controla el alcance y el criterio de cierre. *Ejecutado por: Antigravity o el humano.*
2. **Planner** — traduce el objetivo en fases, tareas y dependencias. Registra decisiones en `.ai-project/context/DECISIONS.md`. *Ejecutado por: Antigravity.*
3. **Implementer** — ejecuta cambios mínimos, seguros y verificables. Solo modifica lo estrictamente necesario. *Ejecutado por: Antigravity.*
4. **Reviewer** — verifica que el trabajo quedó completo. Detecta huecos, supuestos ocultos, deuda residual. Escribe evidencia en `REPORT_CYCLE_N.md`. *Ejecutado por: Claude Code.*

---

## NOTA CRÍTICA SOBRE EL MODELO MULTI-AGENTE

Antigravity y Claude Code **no comparten contexto en tiempo real**. El canal de comunicación entre sesiones es el repositorio mismo: `STATUS.md` y `DECISIONS.md`.

- Antigravity actualiza `.ai-project/context/STATUS.md` al final de cada iteración con hechos verificados, bloqueantes y próximos pasos.
- Claude Code lee `STATUS.md` al iniciar cada auditoría para entender el estado real antes de revisar código.
- Nunca asumir que el otro agente ya hizo algo si no está en los archivos del repositorio.

---

## ORDEN DE LECTURA OBLIGATORIO

Al inicio de cada sesión, ambos agentes leen en este orden:

1. `AGENTS.md` — este archivo
2. `CLAUDE.md` — si aplica (reglas adicionales del Auditor)
3. `.ai-project/context/BRIEFING.md` — objetivo del proyecto
4. `.ai-project/context/TOOLS.md` — herramientas investigadas y aprobadas (si existe)
5. `.ai-project/context/GOALS.md` — mapa de objetivos y estado verificado
6. `.ai-project/context/STATUS.md` — estado vivo
7. `.ai-project/memory/lessons_learned.md` — anti-patrones aprendidos
8. `.ai-project/context/DECISIONS.md` — ADRs activos
9. `.ai-project/memory/ai_rules.md` — reglas de oro y protocolo técnico

Si falta alguno de estos archivos, declararlo antes de avanzar.

`TOOLS.md` es generado por Claude Code e investigado online. **AG no puede referenciar ninguna herramienta en su plan si no está aprobada en `TOOLS.md`.** Si TOOLS.md no existe, Claude Code lo genera antes de que AG haga el plan.

---

## REGLAS DE TRABAJO

1. No inventar variables de entorno, credenciales, IPs, rutas ni nombres de servicios.
2. Si un dato operativo falta y cambia materialmente el resultado, detenerse y pedirlo.
3. Preferir cambios pequeños y explicables sobre reescrituras amplias.
4. No marcar una tarea `[x]` si la validación no se ejecutó.
5. Antes de cerrar una iteración, actualizar `STATUS.md` si hubo aprendizaje nuevo.

---

## POLÍTICA GIT V3

1. **Ramas Protegidas**: Prohibido el push directo a `main` y `develop`.
2. **Entorno de Trabajo**: Todos los agentes trabajan en ramas `feature/[nombre]`.
3. **Identidad de Commit**: Incluir siempre el trailer `Co-authored-by: auris-worker`.

---

## LAS 3 REGLAS DE ORO

1. Cumple el objetivo con el menor cambio seguro posible.
2. Nunca inventes configuración crítica ni relajes seguridad por conveniencia.
3. Si falta un dato que cambia materialmente el resultado, detente y pídelo.
