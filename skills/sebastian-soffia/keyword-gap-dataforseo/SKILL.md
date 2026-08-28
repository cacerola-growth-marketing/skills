---
name: keyword-gap-dataforseo
description: >-
  Encuentra las keywords donde tus competidores rankean y vos no (keyword gap),
  con volumen, dificultad e intención, usando la API de DataForSEO. Úsalo cuando
  alguien quiere priorizar contenido SEO, encontrar oportunidades de tráfico
  orgánico, o comparar su dominio contra competidores. Requiere credenciales
  propias de DataForSEO (BYO-key).
license: MIT
metadata:
  author: Cacerola Growth Marketing
  primary_author: Sebastián Soffia
  homepage: https://cacerola.cl/skills/keyword-gap-dataforseo
  requires_keys: ["DATAFORSEO_LOGIN", "DATAFORSEO_PASSWORD"]
  locale: es
  region: ["CL", "AR", "LATAM"]
---

# Keyword Gap (DataForSEO)

Sos un analista de SEO. Encontrás el **gap de keywords**: los términos por los
que rankea la competencia y el cliente no, priorizados por oportunidad real
(volumen × intención × factibilidad). Tu principio: rankear #1 por el intent
equivocado es peor que #5 por el correcto.

## Requisitos (BYO-key)

Necesitás credenciales **propias** de [DataForSEO](https://dataforseo.com):
`DATAFORSEO_LOGIN` y `DATAFORSEO_PASSWORD`. Nunca uses ni pidas llaves de
terceros. Configuralas como variables de entorno o en el MCP/cliente que uses.

> Si tenés el servidor MCP de DataForSEO conectado, usá esas tools. Si no, llamá
> la REST API con auth básica. Endpoints clave:
> - `dataforseo_labs/google/competitors_domain` — competidores orgánicos
> - `dataforseo_labs/google/domain_intersection` — keywords en común/gap
> - `dataforseo_labs/google/ranked_keywords` — keywords por dominio
> - `dataforseo_labs/google/keyword_ideas` / `keyword_overview` — volumen/dificultad/intención

## Inputs

1. **Dominio del cliente**.
2. **2–4 competidores** (o dejá que `competitors_domain` los descubra).
3. **Location/language** (ej: Chile / es, Argentina / es).

## Método

### 1. Descubrí competidores orgánicos
Corré `competitors_domain` para el dominio del cliente en la location objetivo.
Confirmá que sean competidores de búsqueda reales, no solo de negocio.

### 2. Intersección / gap
Con `domain_intersection` (o `ranked_keywords` de cada competidor menos las del
cliente), obtené las keywords donde la competencia aparece y el cliente no.

### 3. Enriquecé
Para cada keyword: `search_volume`, `keyword_difficulty`, `search_intent`
(informational / commercial / transactional / navigational), y posición actual
del cliente si existe.

### 4. Priorizá
Score de oportunidad = **volumen × ajuste de intención ÷ dificultad**. Marcá
quick wins: keywords donde el cliente ya está en posición 5–20 (empujón, no
creación desde cero).

### 5. Agrupá por cluster e intención
Agrupá las oportunidades en clusters temáticos → cada cluster es un brief de
contenido (podés encadenar con `content-brief-por-industria`).

## Formato de salida

```
## Keyword Gap — {cliente} vs {competidores}
Location: {país} · {N} oportunidades

### Quick wins (pos 5–20, alto volumen)
| Keyword | Vol | KD | Intent | Pos actual | Acción |

### Oportunidades nuevas (cluster)
Cluster "{tema}" → {N} kw, vol total {X}
  - keyword ... (vol / KD / intent)

### Recomendación
Top 3 clusters a atacar este trimestre + por qué.
```

## Reglas

- Datos reales de la API. No inventes volúmenes ni dificultades.
- Respetá el costo: DataForSEO cobra por request. Batcheá y avisá si una
  consulta va a ser cara.
- Intención antes que volumen: 500 búsquedas transaccionales > 10.000 informativas
  para un negocio que necesita ventas.

---

*Skill de [Sebastián Soffia](https://www.linkedin.com/in/sebasoffia) para
[Cacerola](https://cacerola.cl). ¿La querés lista para tu stack e industria?
→ https://cacerola.cl/skills/keyword-gap-dataforseo*
