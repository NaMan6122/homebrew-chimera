# homebrew-chimera

Homebrew tap for [Chimera](https://github.com/NaMan6122/ChimerA) — your chat
subscriptions as an OpenAI-compatible API.

```bash
brew tap NaMan6122/chimera
brew install chimera
```

Installs three binaries: `chimera` (gateway), `chimera-spin` (headless
harness), `chimera-chat` (TUI). First run needs a session export:

```bash
cd ~/chimera
chimera auth login chatgpt
TRANSPORT=webapi PROVIDER=chatgpt API_PORT=8000 API_TOKEN=chimera chimera
```

The formula is generated per release by
[`scripts/dist.sh`](https://github.com/NaMan6122/ChimerA/blob/main/scripts/dist.sh)
and pins the sha256 of every platform archive; update it with:

```bash
curl -fsSLo Formula/chimera.rb \
  https://github.com/NaMan6122/ChimerA/releases/download/<tag>/chimera.rb
```

See [docs/DISTRIBUTION.md](https://github.com/NaMan6122/ChimerA/blob/main/docs/DISTRIBUTION.md)
for the full release runbook.
