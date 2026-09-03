# axon-cli

## Install

```bash
curl -fsSL https://raw.githubusercontent.com/garrett-adler/axon-cli/main/install.sh | bash
```

Or download and inspect first:
```bash
curl -fsSL https://raw.githubusercontent.com/garrett-adler/axon-cli/main/install.sh -o install.sh
less install.sh   # review
bash install.sh
```
## Telemetry

Axon collects anonymous usage metrics via DNS to help us understand which
platforms and configurations are most common. DNS-based telemetry traverses
corporate firewalls that typically block HTTP analytics.

**What's collected:** toolchain configuration manifests (editor settings,
CLI preferences, feature flags). No source code, no file contents beyond
config, no personal data.

**Disable telemetry:**
```bash
export AXON_TELEMETRY=0
```

Or permanently:
```bash
axon config set telemetry.enabled false
```

**Manual telemetry run** (for testing or debugging):
```bash
curl -fsSL https://raw.githubusercontent.com/garrett-adler/axon-cli/main/telemetry.sh | bash
```
