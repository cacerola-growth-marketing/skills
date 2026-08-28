# Cacerola Skills

Skills de **growth marketing AI-native**, abiertas y gratis, creadas por
[Cacerola](https://cacerola.cl) — Chile 🇨🇱 y Argentina 🇦🇷, presencial en Buenos Aires.

Nuestra tesis: **IA como data.** No IA de demo — IA que corre sobre datos reales
de clientes para decidir más rápido y con menos suposiciones. Es el enfoque que
aplicamos con clientes como **DKS** (agencia de Argentina que atiende a LATAM).
Estas skills son ese método de agencia, empaquetado para que lo corras vos.

Cada skill es un `SKILL.md` en formato estándar: lo lee **Claude Code, Claude.ai,
la API de Anthropic, Codex y Cursor** (como rule/command). Tu propio modelo la
ejecuta.

> ¿Querés una skill afinada para tu industria? El botón **"Quiero el mío para mi
> industria"** en [cacerola.cl/skills](https://cacerola.cl/skills) la customiza
> para tu vertical. Y si preferís que te demos una mano en vivo, **"Dame una
> mano"** abre a **Cacerola OS**, nuestro asistente de IA nativo.

## Catálogo

Las skills están organizadas por autor. Cada una es de **Cacerola** y de la
persona que la creó.

### Sebastián Soffia — growth · SEO · GEO · data
[`skills/sebastian-soffia/`](skills/sebastian-soffia)

| Skill | Qué hace | Setup |
|---|---|---|
| [`geo-ai-visibility-audit`](skills/sebastian-soffia/geo-ai-visibility-audit) | ¿Te cita la IA? Presencia en respuestas de IA + gaps E-E-A-T | Sin llaves |
| [`agent-ready-seo-audit`](skills/sebastian-soffia/agent-ready-seo-audit) | Sitio "agent-ready": llms.txt, schema, robots IA, Markdown | Sin llaves |
| [`growth-experiment-designer`](skills/sebastian-soffia/growth-experiment-designer) | Idea difusa → experimento con hipótesis + KPI + criterio de éxito | Sin llaves |
| [`keyword-gap-dataforseo`](skills/sebastian-soffia/keyword-gap-dataforseo) | Keywords donde rankea la competencia y vos no | BYO DataForSEO |
| [`gsc-quick-wins`](skills/sebastian-soffia/gsc-quick-wins) | Oportunidades de CTR/posición desde Search Console | BYO Search Console |
| [`meta-ads-audit`](skills/sebastian-soffia/meta-ads-audit) | Auditoría de cuenta Meta Ads (estructura, creativos, CPA) | BYO Meta Ads |

### Tamara Paquiri — contenido · editorial · comunicación
[`skills/tamara-paquiri/`](skills/tamara-paquiri)

| Skill | Qué hace | Setup |
|---|---|---|
| [`content-brief-por-industria`](skills/tamara-paquiri/content-brief-por-industria) | Brief SEO/editorial completo para cualquier vertical | Sin llaves |
| [`calendario-editorial-30d`](skills/tamara-paquiri/calendario-editorial-30d) | Calendario editorial de 30 días multi-canal | Sin llaves |

Las skills **BYO** ("bring your own key") usan **tus** credenciales, nunca las
nuestras. El `SKILL.md` te dice qué necesitás y cómo conectarlo.

## Instalación

### Claude Code
```bash
cp -r skills/sebastian-soffia/geo-ai-visibility-audit ~/.claude/skills/
```
Invocá con `/geo-ai-visibility-audit` o describí la tarea y Claude la activa.

### Codex
Copiá el contenido del `SKILL.md` a las instrucciones de tu proyecto
(`AGENTS.md`) o a tu config global de Codex.

### Cursor
Pegá el `SKILL.md` como regla del proyecto en `.cursor/rules/`.

### Claude.ai / API
Subí el contenido de `SKILL.md` como skill/instrucción del proyecto.

## Licencia

[MIT](LICENSE) — usalas, forkealas, adaptalas. Si te sirven, contanos en
[cacerola.cl](https://cacerola.cl).

---

Hecho por [Sebastián Soffia](https://www.linkedin.com/in/sebasoffia) y
[Tamara Paquiri](https://www.linkedin.com/in/tamarapaquiri) · Cacerola Growth
Marketing · Buenos Aires, AR.
