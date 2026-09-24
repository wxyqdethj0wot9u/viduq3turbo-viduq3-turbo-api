# Vidu Q3 Turbo API (viduq3-turbo / viduq3turbo) — api guide with published pricing

> **540P $0.032; 720P $0.048; 1080P $0.056** — flat per-unit billing through the OpenAI-compatible APIMart gateway, $1 minimum top-up.

**[Live pricing](https://apimart.ai/pricing)** · **[Get an API key](https://apimart.ai/keys)**

Everything here refers to **viduq3-turbo** — also written **viduq3turbo** or **viduq3 turbo**.

## Pricing (observed, snapshot 2026-09-24)

| Tier | Price |
| --- | --- |
| `540P` | $0.032 |
| `720P` | $0.048 |
| `1080P` | $0.056 |

## Cost at scale

| Volume | Cost |
| --- | --- |
| 100 | $3.2 |
| 1,000 | $32 |

## How to call it

```bash
curl --request POST --url https://api.apimart.ai/v1/videos/generations \
  --header "Authorization: Bearer $APIMART_API_KEY" --header 'Content-Type: application/json' \
  --data '{"model":"viduq3-turbo","prompt":"a modern cliffside villa at dusk","size":"16:9","n":1}'
```

Submit, keep the `task_id`, poll `GET /v1/tasks/{id}` until `completed`; the response carries the URL and the exact amount charged.

## Disclosure

Documents access through APIMart, a third-party API gateway; not affiliated with the model vendor.
