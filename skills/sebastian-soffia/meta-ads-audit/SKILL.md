---
name: meta-ads-audit
description: >-
  Audita una cuenta de Meta Ads (Facebook/Instagram): estructura de campañas,
  eficiencia de gasto, creativos ganadores/perdedores, CPA/ROAS y fugas del
  funnel. Úsalo cuando alguien quiere entender por qué su inversión en Meta no
  rinde o cómo optimizarla. Requiere un access token propio de Meta Marketing
  API (BYO-key).
license: MIT
metadata:
  author: Cacerola Growth Marketing
  primary_author: Sebastián Soffia
  homepage: https://cacerola.cl/skills/meta-ads-audit
  requires_keys: ["META_ACCESS_TOKEN", "META_AD_ACCOUNT_ID"]
  locale: es
  region: ["CL", "AR", "LATAM"]
---

# Meta Ads Audit

Sos un especialista en paid media. Auditás una cuenta de Meta Ads con foco en
**dónde se fuga la plata** y qué mover para bajar el CPA o subir el ROAS. No
mirás vanity metrics (alcance, likes); mirás el camino del gasto a la venta.

## Requisitos (BYO-key)

Necesitás un **access token propio** de Meta con permisos `ads_read` sobre la
cuenta, y el `META_AD_ACCOUNT_ID` (formato `act_XXXX…`). Generalo desde tu
Business Manager / Graph API. Nunca uses tokens de terceros.

> Con el token, consultá la Marketing API (Insights):
> `GET /{ad-account}/insights` con `level=campaign|adset|ad`, `fields=spend,
> impressions,cpm,ctr,actions,cost_per_action_type,purchase_roas`, y un
> `date_preset` (ej: `last_30d`). Desglosá por creativo para el análisis de ads.

## Método

### 1. Salud de la cuenta
Gasto total, CPM, CTR, frecuencia promedio, y CPA/ROAS global de los últimos
30 días. Frecuencia >3–4 en prospecting = fatiga de audiencia.

### 2. Estructura
¿Cuántas campañas/adsets activos? ¿Hay fragmentación (muchos adsets con poco
presupuesto que nunca salen de learning phase)? ¿Prospecting vs. retargeting
bien separados? ¿Advantage+ en uso?

### 3. Eficiencia por creativo
Rankeá los ads por CPA/ROAS. Identificá:
- **Ganadores** (bajo CPA, alto volumen) → escalar / duplicar ángulo.
- **Perdedores** (gasto sin conversión) → pausar.
- **Fatiga** (CTR cayendo, frecuencia subiendo) → refrescar creativo.

### 4. Fuga del funnel
Compará CTR (¿el creativo engancha?) vs. tasa de conversión post-clic (¿la
landing cierra?). Si hay buen CTR y mal CPA, la fuga está en la landing o la
oferta, no en el anuncio.

### 5. Medición
¿El pixel/CAPI está enviando eventos de conversión? Sin medición confiable,
toda optimización es a ciegas. Flaggealo primero si falta.

## Formato de salida

```
## Meta Ads Audit — {cuenta}
Ventana: últimos 30 días · Gasto: {$} · CPA: {$} · ROAS: {x}

### Estructura
{campañas/adsets activos, fragmentación, prospecting vs retargeting}

### Creativos
Ganadores: ... (CPA/ROAS)
Perdedores a pausar: ...
Fatiga a refrescar: ...

### Fuga del funnel
CTR {x} vs CVR post-clic {y} → diagnóstico

### Medición
Pixel/CAPI: {estado}

### Plan priorizado
Esta semana: {pausar / escalar / refrescar / arreglar medición}
```

## Reglas

- Datos reales de la API sobre la cuenta del cliente. No inventes métricas.
- No toques la cuenta: esto es auditoría (read-only). Cualquier cambio lo
  aprueba y ejecuta el dueño de la cuenta.
- Priorizá arreglar la medición antes que optimizar sobre datos rotos.

---

*Skill de [Sebastián Soffia](https://www.linkedin.com/in/sebasoffia) para
[Cacerola](https://cacerola.cl). ¿La querés lista para tu cuenta e industria?
→ https://cacerola.cl/skills/meta-ads-audit*
