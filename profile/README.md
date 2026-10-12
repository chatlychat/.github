<h1 align="center">Chatly</h1>

<p align="center">
  Live chat, shared inbox and AI agents for small teams — API-first, with SDKs in eleven languages.
</p>

<p align="center">
  <a href="https://chatlychat.com/docs">Documentation</a> ·
  <a href="https://chatlychat.com/guides">Guides</a> ·
  <a href="https://chatlychat.com/docs/api-rest">REST API</a> ·
  <a href="https://api.chatlychat.com/docs">OpenAPI</a>
</p>

---

## Backend SDKs

Eight languages, one surface. All 55 methods, the same typed errors, the same
retry policy, the same per-write idempotency key, the same auto-pagination —
built from one shared manifest, and each one proves its coverage by calling
every method and committing what went over the wire. Zero runtime
dependencies, in all eight.

| Language          | Package                                                                      | Repository                                                       |
| ----------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| Node / TypeScript | [`@chatlychat/sdk-node`](https://www.npmjs.com/package/@chatlychat/sdk-node) | [chatly-sdk-node](https://github.com/chatlychat/chatly-sdk-node) |
| Python            | `chatly` · not on PyPI yet                                                   | [chatly-python](https://github.com/chatlychat/chatly-python)     |
| Go                | `github.com/chatlychat/chatly-go`                                            | [chatly-go](https://github.com/chatlychat/chatly-go)             |
| Ruby              | `chatly` · not on RubyGems yet                                               | [chatly-ruby](https://github.com/chatlychat/chatly-ruby)         |
| PHP               | `chatly/chatly-php` · not on Packagist yet                                   | [chatly-php](https://github.com/chatlychat/chatly-php)           |
| Java              | `com.chatlychat:chatly-java` · not on Maven Central yet                      | [chatly-java](https://github.com/chatlychat/chatly-java)         |
| .NET              | `Chatly` · not on NuGet yet                                                  | [chatly-dotnet](https://github.com/chatlychat/chatly-dotnet)     |
| Rust              | `chatly` · not on crates.io yet                                              | [chatly-rust](https://github.com/chatlychat/chatly-rust)         |

```bash
npm install @chatlychat/sdk-node
```

## In-page SDKs

These run where your customer is and authenticate with a channel public id,
which is not a secret.

| Platform         | Package                                                                                  | Repository                                                                   |
| ---------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| JavaScript       | [`@chatlychat/sdk-js`](https://www.npmjs.com/package/@chatlychat/sdk-js)                 | [chatly-sdk-js](https://github.com/chatlychat/chatly-sdk-js)                 |
| Custom element   | [`@chatlychat/widget-element`](https://www.npmjs.com/package/@chatlychat/widget-element) | [chatly-widget-element](https://github.com/chatlychat/chatly-widget-element) |
| React            | [`@chatlychat/widget-react`](https://www.npmjs.com/package/@chatlychat/widget-react)     | [chatly-widget-react](https://github.com/chatlychat/chatly-widget-react)     |
| React Native     | [`@chatlychat/react-native`](https://www.npmjs.com/package/@chatlychat/react-native)     | [chatly-react-native](https://github.com/chatlychat/chatly-react-native)     |
| Flutter          | `chatly` · not on pub.dev yet                                                            | [chatly-flutter](https://github.com/chatlychat/chatly-flutter)               |
| Swift            | SwiftPM · not tagged yet                                                                 | [chatly-swift](https://github.com/chatlychat/chatly-swift)                   |
| Kotlin / Android | `com.chatlychat:chatly-android` · not on Maven Central yet                               | [chatly-android](https://github.com/chatlychat/chatly-android)               |

You do not need a package to embed the widget — one script tag works, and puts
the same control surface on `window.Chatly`. See
[the web channel guide](https://chatlychat.com/guides/channel-web).

## Tooling

|                                                                    |                                                                                                                                                  |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| [`@chatlychat/cli`](https://www.npmjs.com/package/@chatlychat/cli) | `chatly` in your terminal: read a thread, send a reply, pull a report, or call any route. [chatly-cli](https://github.com/chatlychat/chatly-cli) |
| [`@chatlychat/mcp`](https://www.npmjs.com/package/@chatlychat/mcp) | 49 typed MCP tools over stdio or Streamable HTTP, for Claude, Cursor or any MCP client. [chatly-mcp](https://github.com/chatlychat/chatly-mcp)   |

## Build against it

- **[REST API](https://chatlychat.com/docs/api-rest)** — `/v1/*`, cursor-paginated, `Idempotency-Key` on every write. The spec at [`api.chatlychat.com/docs`](https://api.chatlychat.com/docs) is generated from the code, never hand-maintained.
- **[External agents](https://chatlychat.com/docs/api-external-agents)** — bring your own model. We POST each visitor turn to your HTTPS endpoint, signed; you reply with text, rich cards, an interactive step, or a token stream.
- **[Rich blocks](https://chatlychat.com/docs/api-blocks)** — one block vocabulary shared by cards, tool results, widget home screens, interactive steps and action results.
- **[Webhooks](https://chatlychat.com/docs/api-webhooks)** — 30 event types, HMAC-signed with a timestamp, replay-bounded.
- **[MCP](https://chatlychat.com/docs/api-mcp)** — drive a workspace from an AI agent.

## How it runs

Chatly is a managed service — we operate the infrastructure and you never run
a database, a queue or a TURN server. What stays yours is every third-party
account: your Stripe, your Twilio, your OpenAI or Anthropic key, your identity
provider. You paste a key, and you can revoke it without asking us.

## These repositories are mirrors

The platform is built in a private monorepo, so a pull request here cannot be
merged directly — but a patch is still the fastest way to get something fixed
and we will port it with attribution. Read the source, run the tests, open an
issue, or open a PR and we will treat the diff as the proposal.

## Security

Found something? Please **do not** open a public issue — see
[SECURITY.md](https://github.com/chatlychat/.github/blob/main/SECURITY.md).
