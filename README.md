# Nano Banana Pro API (nano-banana-pro / nanobananapro) — api guide with published pricing

<p align="center">
  <img src="hero.jpg" width="820" alt="Nano Banana Pro sample">
</p>

> **default $0.03; 4K $0.04** — flat per-unit billing through the OpenAI-compatible APIMart gateway, $1 minimum top-up.

**[Live pricing](https://apimart.ai/pricing)** · **[Get an API key](https://apimart.ai/keys)**

Everything here refers to **nano-banana-pro** — also written **nanobananapro** or **nano banana pro**.

## Pricing (observed, snapshot 2026-09-24)

| Tier | Price |
| --- | --- |
| `default` | $0.03 |
| `4K` | $0.04 |

## Cost at scale

| Volume | Cost |
| --- | --- |
| 100 | $3 |
| 1,000 | $30 |

## How to call it

```bash
curl --request POST --url https://api.apimart.ai/v1/images/generations \
  --header "Authorization: Bearer $APIMART_API_KEY" --header 'Content-Type: application/json' \
  --data '{"model":"gemini-3-pro-image-preview","prompt":"a modern cliffside villa at dusk","size":"16:9","n":1}'
```

Submit, keep the `task_id`, poll `GET /v1/tasks/{id}` until `completed`; the response carries the URL and the exact amount charged.

## Disclosure

Documents access through APIMart, a third-party API gateway; not affiliated with the model vendor.
