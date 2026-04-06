# [BUG] [v0.0.7] mcp get --json prints JSON and plain-text error output for missing servers

## Repro Steps
1. Run `cortex mcp get missing-server --json --color never`.
2. Compare with `cortex mcp get codex-temp-proof --json --color never`.

## Actual Result
The missing-server path prints a JSON error object and then also prints a plain-text `Error:` line.

## Expected Result
When `--json` is requested, the command should emit only JSON output.

## Evidence
- `01-help-proof.png`
- `02-mixed-error-output-proof.png`
- `03-control-json-proof.png`
