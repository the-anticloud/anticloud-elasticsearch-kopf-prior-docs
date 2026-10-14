# Command Line Interface — ELASTICSEARCH_KOPF

**Upstream:** https://github.com/lmenezes/elasticsearch-kopf

## Anticloud CLI

```bash
# Install
pip install anticloud-elasticsearch-kopf

# Run offline with PAX inference
anticloud-elasticsearch-kopf --offline --pax-local

# Run with AIOSS logging
anticloud-elasticsearch-kopf --aioss-log ./ledger.jsonl

# Single binary (after build)
./elasticsearch_kopf --config config.yaml
```

## Options

| Flag | Description |
| --- | --- |
| `--offline` | Disable all network calls |
| `--pax-local` | Use local PAX inference at 127.0.0.1:11434 |
| `--aioss-log PATH` | Write AIOSS audit chain to PATH |
| `--encrypt` | Enable AES-256 at rest for output files |
| `--gpu` | Force GPU inference |
| `--cpu` | Force CPU inference |
| `--config PATH` | Load configuration from YAML file |
