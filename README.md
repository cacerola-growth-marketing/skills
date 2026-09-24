# Cacerola Skills

Skills de **growth marketing AI-native**, abiertas y gratis, creadas por
[Cacerola](https://cacerola.cl). Chile y Argentina, presencial en Buenos Aires.

Nuestra tesis es **IA como data**: no IA de demo, sino IA que corre sobre datos
reales para decidir más rápido y con menos suposiciones. Es el enfoque que
aplicamos con todos nuestros clientes y que aportamos a nuestros partners.
Estas skills son ese método de agencia, empaquetado para que lo uses tú.

Cada skill es un `SKILL.md` en formato estándar. Lo leen **Claude Code,
Claude.ai, la API de Anthropic, Codex y Cursor** (como regla o comando), y lo
ejecuta tu propio modelo.

> ¿Quieres una skill afinada para tu industria? El botón **"Quiero el mío para mi
> industria"** en [cacerola.cl/skills](https://cacerola.cl/skills) la adapta a tu
> vertical.

## Catálogo

Las skills están organizadas por autor. Cada una es de **Cacerola** y de la
persona que la creó.

### Sebastián Soffia. Growth, SEO, GEO y data.
[`skills/sebastian-soffia/`](skills/sebastian-soffia)

| Skill | Qué hace | Setup |
|---|---|---|
| [`geo-ai-visibility-audit`](skills/sebastian-soffia/geo-ai-visibility-audit) | ¿Te cita la IA? Presencia en respuestas de IA y gaps de E-E-A-T | Sin llaves |
| [`agent-ready-seo-audit`](skills/sebastian-soffia/agent-ready-seo-audit) | Sitio "agent-ready": llms.txt, schema, robots IA, Markdown | Sin llaves |
| [`growth-experiment-designer`](skills/sebastian-soffia/growth-experiment-designer) | Idea difusa a experimento con hipótesis, KPI y criterio de éxito | Sin llaves |
| [`keyword-gap-dataforseo`](skills/sebastian-soffia/keyword-gap-dataforseo) | Keywords donde rankea la competencia y tú no | Tu llave de DataForSEO |
| [`gsc-quick-wins`](skills/sebastian-soffia/gsc-quick-wins) | Oportunidades de CTR y posición desde Search Console | Tu llave de Search Console |
| [`meta-ads-audit`](skills/sebastian-soffia/meta-ads-audit) | Auditoría de cuenta Meta Ads (estructura, creativos, CPA) | Tu llave de Meta Ads |

### Tamara Paquiri. Contenido, editorial y comunicación.
[`skills/tamara-paquiri/`](skills/tamara-paquiri)

| Skill | Qué hace | Setup |
|---|---|---|
| [`content-brief-por-industria`](skills/tamara-paquiri/content-brief-por-industria) | Brief SEO y editorial completo para cualquier vertical | Sin llaves |
| [`calendario-editorial-30d`](skills/tamara-paquiri/calendario-editorial-30d) | Calendario editorial de 30 días multicanal | Sin llaves |

Las skills que usan una llave propia trabajan con **tus** credenciales, nunca con
las nuestras. El `SKILL.md` te dice qué necesitas y cómo conectarlo.

## Instalación

### Con `npx skills` (recomendado)
Usa el CLI abierto [`skills`](https://github.com/vercel-labs/skills) (requiere
Node 22 o superior). Detecta tus agentes (Claude Code, Codex, Cursor y otros) y
te deja elegir qué skills instalar:
```bash
npx skills add cacerola-growth-marketing/skills
```

Para instalar una sola skill, pasa su nombre con `--skill`:
```bash
npx skills add cacerola-growth-marketing/skills --skill geo-ai-visibility-audit
npx skills add cacerola-growth-marketing/skills --skill agent-ready-seo-audit
npx skills add cacerola-growth-marketing/skills --skill growth-experiment-designer
npx skills add cacerola-growth-marketing/skills --skill keyword-gap-dataforseo
npx skills add cacerola-growth-marketing/skills --skill gsc-quick-wins
npx skills add cacerola-growth-marketing/skills --skill meta-ads-audit
npx skills add cacerola-growth-marketing/skills --skill content-brief-por-industria
npx skills add cacerola-growth-marketing/skills --skill calendario-editorial-30d
```

Agrega `-g` para instalarla a nivel global (no solo en el proyecto actual) y
`-a claude-code` para elegir el agente sin preguntas. Para ver la lista sin
instalar nada: `npx skills add cacerola-growth-marketing/skills --list`.

### Claude Code (manual)
```bash
cp -r skills/sebastian-soffia/geo-ai-visibility-audit ~/.claude/skills/
```
Escribe `/geo-ai-visibility-audit`, o describe la tarea y Claude activa la skill.

### Codex
Pega el contenido del `SKILL.md` en las instrucciones de tu proyecto
(`AGENTS.md`) o en tu configuración global de Codex.

### Cursor
Pega el `SKILL.md` como regla del proyecto en `.cursor/rules/`.

### Claude.ai o API
Sube el contenido del `SKILL.md` como skill o instrucción del proyecto.

## Licencia

[MIT](LICENSE). Úsalas, forkéalas, adáptalas. Si te sirven, cuéntanos en
[cacerola.cl](https://cacerola.cl).

Hecho por [Sebastián Soffia](https://www.linkedin.com/in/sebasoffia) y
[Tamara Paquiri](https://www.linkedin.com/in/tamarapaquiri). Cacerola Growth
Marketing, Buenos Aires.
