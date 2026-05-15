# Local Gateway

The local gateway for AI coding context.

Receives session logs from your editor, filters and sanitizes based on your config, extracts structured knowledge via LLM, and routes it to your chosen context engines.

## Architecture

- **MCP Server**: Both streamable-HTTP and stdio modes for editor integration.
- **Config Management**: Per-user routing rules, filtering, and sanitization.
- **Extraction Pipeline**: Converts raw session logs into structured episodes.
- **Auth & Routing**: Sends credentials to engines; routes episodes per user rules.
- **Web UI**: Static TypeScript SPA served by the gateway binary.

## Installation

```bash
go install github.com/MAnders333/local-gateway/cmd/local-gateway@latest
```

## License

MIT
