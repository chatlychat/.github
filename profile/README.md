<h1 align="center">Chatly</h1>

<p align="center">
  Live chat, shared inbox and AI agents for small teams — self-hostable, API-first.
</p>

<p align="center">
  <a href="https://chatlychat.com/docs">Documentation</a> ·
  <a href="https://chatlychat.com/guides">Guides</a> ·
  <a href="https://chatlychat.com/docs/api-rest">REST API</a> ·
  <a href="https://api.chatlychat.com/docs">OpenAPI</a>
</p>

---

## Install

| Package | What it is |
| --- | --- |
| [`@chatlychat/sdk-js`](https://www.npmjs.com/package/@chatlychat/sdk-js) | Browser SDK — control the widget, identify visitors, or run a conversation headlessly with no UI of ours |
| [`@chatlychat/sdk-node`](https://www.npmjs.com/package/@chatlychat/sdk-node) | Server SDK — typed REST client, per-write idempotency, webhook signature verification |
| [`@chatlychat/widget-element`](https://www.npmjs.com/package/@chatlychat/widget-element) | `<chatly-widget>` custom element and the embed lifecycle. Zero dependencies |
| [`@chatlychat/widget-react`](https://www.npmjs.com/package/@chatlychat/widget-react) | `<ChatlyWidget />` for React. `react` is a peer dependency |
| [`@chatlychat/react-native`](https://www.npmjs.com/package/@chatlychat/react-native) | React Native / Expo client, including block and canvas renderers |

```bash
pnpm add @chatlychat/sdk-node
```

You do not need a package to embed the widget — one script tag works, and puts
the same control surface on `window.Chatly`. See
[the web channel guide](https://chatlychat.com/guides/channel-web).

## Build against it

- **[REST API](https://chatlychat.com/docs/api-rest)** — `/v1/*`, cursor-paginated, `Idempotency-Key` on every write. The spec at [`api.chatlychat.com/docs`](https://api.chatlychat.com/docs) is generated from the code, never hand-maintained.
- **[External agents](https://chatlychat.com/docs/api-external-agents)** — bring your own model. We POST each visitor turn to your HTTPS endpoint, signed; you reply with text, rich cards, an interactive step, or a token stream.
- **[Rich blocks](https://chatlychat.com/docs/api-blocks)** — one block vocabulary shared by cards, tool results, widget home screens, interactive steps and action results.
- **[Webhooks](https://chatlychat.com/docs/api-webhooks)** — 30 event types, HMAC-signed with a timestamp, replay-bounded.
- **[MCP](https://chatlychat.com/docs/api-mcp)** — drive a workspace from an AI agent.

## Self-hosting

Chatly runs on your own infrastructure: Postgres 16, Redis 7, S3-compatible
object storage, and Docker or Kubernetes. Start with
[Docker Compose](https://chatlychat.com/docs/selfhost-docker), or
[Helm](https://chatlychat.com/docs/selfhost-helm) for a cluster. Every
third-party service is optional — the product boots without an AI provider, a
voice gateway or a telemetry collector, and says so rather than failing.

## Security

Found something? Please **do not** open a public issue — see
[SECURITY.md](https://github.com/chatlychat/.github/blob/main/SECURITY.md).
